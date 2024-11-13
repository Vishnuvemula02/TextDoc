EDIT       TECN93.VISHNU.MAPPDS(CALC) - 01.10              Columns 00001 00072 
****** ***************************** Top of Data ******************************
000100 CALC     DFHMSD TYPE=&SYSPARM,MODE=INOUT,LANG=COBOL,STORAGE=AUTO,      X
000200                TIOPFX=YES,TERM=ALL,CTRL=(FREEKB,FRSET,PRINT),          X
000300                MAPATTS=(COLOR,HILIGHT),DSATTS=(COLOR,HILIGHT)           
000400 IBM      DFHMDI SIZE=(24,80),LINE=1,COLUMN=1,TIOAPFX=YES,              X
000500                JUSTIFYT=LEFT,CTRL=(FREEKB,PRINT,FRSET)                  
000600          DFHMDF POS=(04,27),LENGTH=30,INITIAL='WELCOME CALCULATOR',    X
000700                JUSTIFY=LEFT,ATTRB=(ASKIP,PROT,BRT,FSET),               X
000800                COLOR=RED,HILIGHT=(UNDERLINE,REVERSE)                    
000900          DFHMDF POS=(07,03),LENGTH=5,INITIAL='DATE',JUSTIFY=LEFT,      X
001000                ATTRB=(ASKIP,PROT,NORM,FSET)                             
001200 DATE     DFHMDF POS=(07,08),LENGTH=8,INITIAL='__/__/____',             X
001300                JUSTIFY=LEFT,ATTRB=(ASKIP,UNPROT,NORM,FSET)              
001400          DFHMDF POS=(07,65),LENGTH=5,INITIAL='TIME:',JUSTIFY=LEFT,     X
001500                ATTRB=(ASKIP,PROT,NORM,FSET)                             
001600 TIME     DFHMDF POS=(07,71),LENGTH=5,INITIAL='_____',                  X
001700                ATTRB=(ASKIP,UNPROT,NORM,FSET)                           
001800          DFHMDF POS=(09,32),LENGTH=7,INITIAL='VALUE1:',JUSTIFY=LEFT,   X
001900                ATTRB=(ASKIP,PORT,NORM,FEST),COLOR=YELLOW                
002000 VALUE1   DFHMDF POS=(09,40),LENGTH=5,INITIAL='_____',JUSTIFY=LEFT,     X
002100                ATTRB=(UNPROT,IC,FSET),COLOR=BLUE,                      X
002200                PICIN='9(5)'                                             
002300          DFHMDF POS=(09,46),LENGTH=1,ATTRB=ASKIP                        
002400          DFHMDF POS=(11,32),LENGTH=7,INITIAL='VALUE2:',JUSTIFY=LEFT,   X
002500                ATTRB=(ASKIP,PROT,NORM,FSET),COLOR=YELLOW                
002600 VALUE2   DFHMDF POS=(11,40),LENGTH=5,INITIAL='_____',JUSTIFY=LEFT,     X
002700                ATTRB=(UNPROT,IC,FSET),COLOR=BLUE,                      X
002800                PICIN='9(5)'                                             
002900          DFHMDF POS=(11,46),LENGTH=1,ATTRB=PROT                         
003000          DFHMDF POS=(13,32),LENGTH=7,INITIAL='RESULT:',JUSTIFY=LEFT,   X
003100                ATTRB=(ASKIP,PROT,NORM,FSET),COLOR=YELLOW                
003200 RESULT   DFHMDF POS=(13,40),LENGTH=7,INITIAL='_______',JUSTIFY=LEFT,   X
003300                ATTRB=(PROT,FSET),COLOR=BLUE,                           X
003400                PICOUT='9(7)'                                            
003500          DFHMDF POS=(17,22),LENGTH=43,                                 X
003600                INITIAL='F1:ADD F2:SUB F3:MUL F4:DIV F5:EXIT',          X
003700                ATTRB=(PROT,FSET)                                        
003800          DFHMSD TYPE=FINAL END                                          
    TECN93.VISHNU.MAPPDS(MAPCOMP) - 01.67           Columns 00001 00072 
***************************** Top of Data ******************************
//TECN93VV JOB ,,CLASS=A,                                               
//         MSGCLASS=H,MSGLEVEL=(1,1),                                   
//         NOTIFY=&SYSUID                                               
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                                    
//CICSMAP  EXEC CICSMAP1,                                               
//         OUTC=*,                                                      
//         COPYLIB=TECN93.VISHNU.COPYLIB,                               
//         LOADLIB=CICS.APPLI.LOADLIB,               ** DONT CHANGE **  
//         MAPNAME=CALC                        -->  MEMBER NAME         
//COPY.SYSUT1  DD  DSN=TECN93.VISHNU.MAPPDS(&MAPNAME),                  
//         DISP=SHR                                                     
/*                                                                      
    TECN93.VISHNU.MAPPDS(CALCPGM) - 01.19           Columns 00001 00072 
***************************** Top of Data ******************************
       IDENTIFICATION DIVISION.                                         
       PROGRAM-ID. CALCPGM.                                             
       ENVIRONMENT DIVISION.                                            
       DATA DIVISION.                                                   
       WORKING-STORAGE SECTION.                                         
       77 TSTAMP PIC S9(5) COMP-3.                                      
       77 OUTDATE PIC X(10).                                            
       77 OUTTIME PIC X(10).                                            
       77 A PIC 9(5).                                                   
       77 B PIC 9(5).                                                   
       77 C PIC 9(7).                                                   
       77 WS-COMMAREA PIC X(11).                                        
            COPY CALC.                                                  
            COPY DFHBMSCA.                                              
            COPY DFHAID.                                                
       PROCEDURE DIVISION.                                              
           EXEC CICS                                                    
                 ASKTIME                                                
                 ABSTIME(TSTAMP)                                        
           END-EXEC.                                                    
           EXEC CICS                                                    
               FORMATTIME                                               
               ABSTIME(TSTAMP)                                          
               DATESEP('/')                                             
               DDMMYYYY(OUTDATE)                                        
           END-EXEC.                                                    
           EXEC CICS FORMATTIME                                         
               ABSTIME(TSTAMP)                                          
               TIMESEP(':')                                             
               TIME(OUTTIME)                                            
           END-EXEC.                                                    
        MAIN-PARA.                                                      
            MOVE LOW-VALUES TO IBMO.                                    
            MOVE OUTTIME TO TIMEO.                                      
            MOVE OUTDATE TO DATEO.                                      
            IF   EIBCALEN = 0 THEN                                      
            PERFORM SEND-PARA                                           
            ELSE                                                        
            EVALUATE EIBAID                                             
                 WHEN DFHPF1 PERFORM ADD-PARA                           
                 WHEN DFHPF2 PERFORM SUB-PARA                           
                 WHEN DFHPF3 PERFORM MUL-PARA                           
                 WHEN DFHPF4 PERFORM DIV-PARA                           
            END-EVALUATE                                                
            END-IF.                                                     
        TRANS-PARA.                                                     
                EXEC CICS RETURN                                        
                     TRANSID('1234')                                    
                     COMMAREA(WS-COMMAREA)                              
                     END-EXEC.                                          
        SEND-PARA.                                                      
           EXEC CICS SEND                        
                MAP('IBM')                       
                MAPSET('CALC')                   
                FREEKB                           
                ERASE                            
             END-EXEC.                           
           MOVE OUTTIME TO TIMEO.                
           MOVE OUTDATE TO DATEO.                
       RECEIVE-PARA.                             
           EXEC CICS RECEIVE                     
                MAP('IBM')                       
                MAPSET('CALC')                   
           END-EXEC.                             
           MOVE OUTTIME TO TIMEO.                
           MOVE OUTTIME TO DATEO.                
       ADD-PARA.                                 
           PERFORM RECEIVE-PARA.                 
           MOVE VALUE1I TO A.                    
           MOVE VALUE2I TO B.                    
                ADD A TO B GIVING C.             
           MOVE A TO VALUE1O.                    
           MOVE B TO VALUE2O.                    
           MOVE C TO RESULTO.                    
           PERFORM SEND-PARA.                    
           PERFORM TRANS-PARA.                   
       SUB-PARA.                                 
        PERFORM RECEIVE-PARA.                   
        MOVE VALUE1I TO A.                      
        MOVE VALUE2I TO B.                      
             SUBTRACT A FROM B GIVING C.        
        MOVE A TO VALUE1O.                      
        MOVE B TO VALUE2O.                      
        MOVE C TO RESULTO.                      
        PERFORM SEND-PARA.                      
        PERFORM TRANS-PARA.                     
    MUL-PARA.                                   
        PERFORM RECEIVE-PARA.                   
        MOVE VALUE1I TO A.                      
        MOVE VALUE2I TO B.                      
             MULTIPLY  A BY B GIVING C.         
        MOVE A TO VALUE1O.                      
        MOVE B TO VALUE2O.                      
        MOVE C TO RESULTO.                      
        PERFORM SEND-PARA.                      
        PERFORM TRANS-PARA.                     
    DIV-PARA.                                   
        PERFORM RECEIVE-PARA.                   
        MOVE VALUE1I TO A.                      
        MOVE VALUE2I TO B.                      
             DIVIDE A INTO  B GIVING C.         
        MOVE A TO VALUE1O.                      
        MOVE B TO VALUE2O.                      
        MOVE C TO RESULTO.   
        PERFORM SEND-PARA.   
        PERFORM TRANS-PARA.  
    EXIT-PARA.               
        EXEC CICS            
             RETURN          
        END-EXEC.            
//TECN93VV JOB ,,NOTIFY=&SYSUID                                         
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                                    
//CICSCOB  EXEC CICSCOB1,                                               
//         SRCLIB=TECN93.VISHNU.MAPPDS,         --> SOURCE PDS LIBRARY  
//         MEM=CALCPGM,               --> PROGRAM NAME                  
//         COPYLIB=TECN93.VISHNU.COPYLIB,        --> COPYBOOK PDS LIB   
//         BMSLIB=TECN93.VISHNU.MAPPDS,           --> BMS MAP LIB       
//         LOADLIB=CICS.APPLI.LOADLIB             **  DO NOT CHANGE  ** 
/*                                                                      
CICS PART
CEDA DEF MAP(IBM) G(A1)
OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
 CEDA  DEFine Mapset( IBM      )                                              
  Mapset         : IBM                                                        
  Group          : A1                                                         
  Description  ==>                                                            
  REsident     ==> No                 No | Yes                                
  USAge        ==> Normal             Normal | Transient                      
  USElpacopy   ==> No                 No | Yes                                
  Status       ==> Enabled            Enabled | Disabled                      
  RSl            : 00                 0-24 | Public                           
CEDA DEF MAPSET(CALC) G(A1)
OVERTYPE TO MODIFY                                        
 CEDA  DEFine Mapset( CALC     )                          
  Mapset         : CALC                                   
  Group          : A1                                     
  Description  ==>                                        
  REsident     ==> No                 No | Yes            
  USAge        ==> Normal             Normal | Transient  
  USElpacopy   ==> No                 No | Yes            
  Status       ==> Enabled            Enabled | Disabled  
  RSl            : 00                 0-24 | Public       
DEF PROG(CALCPGM) G(A1)                                                       
OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
 CEDA  DEFine PROGram( CALCPGM  )                                             
  PROGram        : CALCPGM                                                    
  Group          : A1                                                         
  DEscription  ==>                                                            
  Language     ==>                    CObol | Assembler | Le370 | C | Pli     
  RELoad       ==> No                 No | Yes                                
  RESident     ==> No                 No | Yes                                
  USAge        ==> Normal             Normal | Transient                      
  USElpacopy   ==> No                 No | Yes                                
  Status       ==> Enabled            Enabled | Disabled                      
  RSl            : 00                 0-24 | Public                           
  CEdf         ==> Yes                Yes | No                                
  DAtalocation ==> Below              Below | Any                             
  EXECKey      ==> User               User | Cics                             
  COncurrency  ==> Quasirent          Quasirent | Threadsafe                  
  Api          ==> Cicsapi            Cicsapi | Openapi                       
 REMOTE ATTRIBUTES                                                            
  DYnamic      ==> No                 No | Yes                                
DEF TRANS(1441) PROG(CALCPGM) G(A1)                            
OVERTYPE TO MODIFY                                        CICS 
 CEDA  DEFine TRANSaction( 1441 )                              
  TRANSaction    : 1441                                        
  Group          : A1                                          
  DEscription  ==>                                             
  PROGram      ==> CALCPGM                                     
  TWasize      ==> 00000              0-32767                  
  PROFile      ==> DFHCICST                                    
  PArtitionset ==>                                             
  STAtus       ==> Enabled            Enabled | Disabled       
  PRIMedsize     : 00000              0-65520                  
  TASKDATALoc  ==> Below              Below | Any              
  TASKDATAKey  ==> User               User | Cics              
  STOrageclear ==> No                 No | Yes                 
  RUnaway      ==> System             System | 0 | 500-2700000 
  SHutdown     ==> Disabled           Disabled | Enabled       
  ISolate      ==> Yes                Yes | No                 
  Brexit       ==>                                             

DIS G(A1)                                                                     
ENTER COMMANDS                                                                
 NAME     TYPE         GROUP                                   DATE   TIME    
 CALC     MAPSET       A1                                      21.216 17.43.09
 IBM      MAPSET       A1                                      21.216 17.42.26
 CALCPGM  PROGRAM      A1                                      23.049 16.48.47
 HCICS    PROGRAM      A1                                      21.211 17.12.32
 SUBLINK  PROGRAM      A1                                      23.045 15.12.35

CALC     MAPSET       A1         I                            21.216 17.43.09
IBM      MAPSET       A1          I                           21.216 17.42.26
CALCPGM  PROGRAM      A1           I                          23.049 16.48.47

CALC     MAPSET       A1       *                           INSTALL SUCCESSFUL
IBM      MAPSET       A1       *                           INSTALL SUCCESSFUL
CALCPGM  PROGRAM      A1       *                           INSTALL SUCCESSFUL
TRANSACTION ID 
1441
                         WELCOME CALCULATOR                                  
                                                                             
                                                                             
 DATE 18/02/20                                                 TIME: 17:07   
                                                                             
                              VALUE1: _____                                  
                                                                             
                              VALUE2: _____                                  
                                                                             
                              RESULT: _______                                
                                                                             
                                                                             
                                                                             
                    F1:ADD F2:SUB F3:MUL F4:DIV F5:EXIT                      
                                                                             
 








   TECN93.VISHNU.MAPPDS(VSAMKSDS) - 01.01        
***************************** Top of Data ********
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP02     
//STEP01   EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
      DEFINE CLUSTER(NAME(TECN93.VISHNU.KSDS)-    
      TRK(1,1)-                                   
      VOL(ZAPRD6)-                                
      RECORDSIZE(80,80)-                          
      CISZ(4096)-                                 
      KEYS(4,0)-                                  
      INDEXED)                                    
/*                            
    TECN93.VISHNU.PS 
*********************
E001 VISHNU 59000    
E002 RAMESH 67990    
E003 SURESH 78900    
E004 RAJKUM 66667    
E005 VIKAS  66789    
E006 VARUN  77777    
E007 SAI    34567    
E008 ANIL   12344    
E009 VENKET 13334    
E010 RANIE  12334                        
                                                  
//STEP02   EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//DD1      DD   DSN=TECN93.VISHNU.PS,DISP=SHR     
//DD2      DD   DSN=TECN93.VISHNU.KSDS,DISP=SHR   
//SYSIN    DD   *                                 
     REPRO-                                       
     INFILE(DD1),OUTFILE(DD2)                     
/*                                                
TECN93.VISHNU.KSDS       
TECN93.VISHNU.KSDS.DATA  
TECN93.VISHNU.KSDS.INDEX
IKJ56712I INVALID KEYWORD, SHNU.KSDS 
IKJ56703A REENTER THIS OPERAND -     
    TECN93.VISHNU.MAPPDS(VSAMMAP) - 01.03           Columns 00001 00072 
***************************** Top of Data ******************************
VSAMMAP  DFHMSD TYPE=&&SYSPARM,MODE=INOUT,LANG=COBOL,                  X
               TIOAPFX=YES,CTRL=(FRSET,FREEKB),STORAGE=AUTO,TERM=ALL    
MAPA     DFHMDI SIZE=(24,80),LINE=1,COLUMN=1,JUSTIFY=LEFT,TIOAPFX=YES   
         DFHMDF POS=(04,28),LENGTH=16,INITIAL='EMPLOYEE DETAILS',      X
               ATTRB=(PROT,FSET)                                        
         DFHMDF POS=(06,30),LENGTH=10,INITIAL='EMPID    :',            X
               ATTRB=(PROT,FSET)                                        
EMPID    DFHMDF POS=(06,39),LENGTH=4,INITIAL='____',                   X
               ATTRB=(UNPROT,FSET,IC)                                   
         DFHMDF POS=(06,44),LENGTH=1,ATTRB=ASKIP                        
         DFHMDF POS=(08,30),LENGTH=10,INITIAL='EMPNAME  :',            X
               ATTRB=(PROT,FSET)                                        
EMPNAME  DFHMDF POS=(08,39),LENGTH=10,INITIAL='__________',            X
               ATTRB=(UNPROT,FSET,IC)                                   
         DFHMDF POS=(08,50),LENGTH=1,ATTRB=ASKIP                        
         DFHMDF POS=(10,30),LENGTH=10,INITIAL='EMPSAL   :',            X
               ATTRB=(PROT,FSET)                                        
EMPSAL   DFHMDF POS=(10,39),LENGTH=5,INITIAL='_____',                  X
               ATTRB=(UNPROT,FSET,IC)                                   
         DFHMDF POS=(10,45),LENGTH=1,ATTRB=ASKIP                        
         DFHMDF POS=(13,28),LENGTH=22,ATTRB=(PROT,FSET),               X
               INITIAL='F1:READ  F2:UPDATE'                             
         DFHMDF POS=(15,28),LENGTH=22,ATTRB=(PROT,FSET),               X
               INITIAL='F3:INSERT F4:DELETE'                            
         DFHMDF POS=(17,33),LENGTH=5,INITIAL='MSG1:',                  X
                ATTRB=(PROT,FSET)                                        
 MSG1     DFHMDF POS=(20,32),LENGTH=20,INITAL=20,INITIAL='____________',X
                ATTRB=(UNPROT,FSET,IC)                                   
          DFHMDF POS=(20,53),LENGTH=1,ATTRB=PROT                         
          DFHMSD TYPE=FINAL                                              
               END                                                       
//TECN93VV JOB ,,CLASS=A,                                              
//         MSGCLASS=H,MSGLEVEL=(1,1),                                  
//         NOTIFY=&SYSUID                                              
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                                   
//CICSMAP  EXEC CICSMAP1,                                              
//         OUTC=*,                                                     
//         COPYLIB=TECN93.VISHNU.COPYLIB,                              
//         LOADLIB=CICS.APPLI.LOADLIB,               ** DONT CHANGE ** 
//         MAPNAME=VSAMMAP                     -->  MEMBER NAME        
//COPY.SYSUT1  DD  DSN=TECN93.VISHNU.MAPPDS(&MAPNAME),                 
//         DISP=SHR                                                    
/*                                                                     
IDENTIFICATION DIVISION.         
PROGRAM-ID. VSAMPRO.             
ENVIRONMENT DIVISION.            
DATA DIVISION.                   
WORKING-STORAGE SECTION.         
*******MAP SET**************     
    COPY VSAMMAP.                
****************************     
    COPY DFHBMSCA.               
    COPY DFHAID.                 
01 EMP-RECORD.                   
  05 EMPID PIC X(4).             
  05 FILLER PIC X.               
  05 EMPNAME PIC X(10).          
  05 FILLER PIC X.               
  05 EMPSAL PIC X(5).            
  05 FILLER PIC X(61).           
77 LENGTH1 PIC S9(4) COMP.       
77 RESP    PIC S9(8) COMP.       
77 TEXT1   PIC X(80).            
77 MSG1    PIC X(30).            
77 WS-COMMAREA PIC X(4).         
PROCEDURE DIVISION.              
MAIN-PARA.                       
    IF EIBCALEN = 0 THEN         
       MOVE LOW-VALUES TO MAPAO                         
    PERFORM SEND-PARA                                   
     ELSE                                               
    EVALUATE EIBAID                                     
       WHEN  DFHPF1 PERFORM READ-PARA                   
       WHEN  DFHPF2 PERFORM UPDATE-PARA                 
       WHEN  DFHPF3 PERFORM INSERT-PARA                 
       WHEN  DFHPF4 PERFORM DELETE-PARA                 
       WHEN  DFHPF5 PERFORM EXIT-PARA                   
       WHEN OTHER MOVE 'INVALID FUNCTION KEY' TO MSG1   
    PERFORM MSG-PARA                                    
    END-EVALUATE                                        
    END-IF.                                             
    EXEC CICS                                           
      RETURN                                            
      TRANSID('1432')                                   
      COMMAREA(WS-COMMAREA)                             
    END-EXEC.                                           
RECEIVE-PARA.                                           
    EXEC CICS RECEIVE                                   
      MAP('MAPA')                                       
      MAPSET('VSAMMAP')                                 
    END-EXEC.                                           
      MOVE EMPIDI TO EMPID.                             
      MOVE EMPNAMEI TO EMPNAME.                         
      MOVE EMPSALI TO EMPSAL.                           
      MOVE 58 TO LENGTH1.             
SEND-PARA.                            
    IF RESP = DFHRESP(NORMAL)         
      MOVE EMPID TO EMPIDO            
      MOVE EMPNAME TO EMPNAMEO        
      MOVE EMPSAL  TO EMPSALO         
    END-IF.                           
    EXEC CICS SEND                    
      MAP('MAPA')                     
      MAPSET('VSAMMAP')               
      FREEKB                          
      ERASE                           
    END-EXEC.                         
READ-PARA.                            
    PERFORM RECEIVE-PARA.             
    EXEC CICS READ                    
      DATASET('VISHNU1')              
      INTO(EMP-RECORD)                
      LENGTH(LENGTH1)                 
      RIDFLD(EMPID)                   
      RESP(RESP)                      
    END-EXEC.                         
    PERFORM SEND-PARA.                
      MOVE 'READ SUCCESSFUL' TO MSG1. 
    PERFORM MSG-PARA.                 
INSERT-PARA.                          
    PERFORM RECEIVE-PARA.                 
    EXEC CICS WRITE                       
      DATASET('VISHNU1')                  
      FROM(EMP-RECORD)                    
      LENGTH(LENGTH1)                     
      RIDFLD(EMPID)                       
      RESP(RESP)                          
    END-EXEC.                             
      MOVE 'INSERT SUCCESSFUL' TO MSG1.   
    PERFORM MSG-PARA.                     
UPDATE-PARA.                              
    PERFORM RECEIVE-PARA.                 
    EXEC CICS READ                        
      DATASET('VISHNU1')                  
      INTO(EMP-RECORD)                    
      LENGTH(LENGTH1)                     
      RIDFLD(EMPID)                       
      RESP(RESP)                          
      KEYLENGTH(EMPID)                    
      UPDATE                              
    END-EXEC.                             
    EXEC CICS REWRITE                     
      FILE('VISHNU1')                     
      FROM(EMP-RECORD)                    
      LENGTH(LENGTH1)                     
    END-EXEC.                             
    EXEC CICS                                 
      UNLOCK                                  
      FILE('VISHNU1')                         
    END-EXEC.                                 
      MOVE 'UPDATE SUCCESSFUL' TO MSG1.       
    PERFORM MSG-PARA.                         
DELETE-PARA.                                  
    PERFORM RECEIVE-PARA.                     
    EXEC CICS DELETE                          
      DATASET('VISHNU1')                      
      RIDFLD(EMPID)                           
      RESP(RESP)                              
    END-EXEC.                                 
      MOVE 'DELETE SUCCESSFUL' TO MSG1.       
    PERFORM MSG-PARA.                         
EXIT-PARA.                                    
      MOVE 'THANKS' TO MSG1.                  
    PERFORM MSG-PARA.                         
MSG-PARA.                                     
      MOVE MSG1 TO MSG1O.                     
      PERFORM SEND-PARA.                      
    EXEC CICS                                 
      RETURN                                  
    END-EXEC.    




                             
//TECN93VV JOB ,,NOTIFY=&SYSUID                                         
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                                    
//CICSCOB  EXEC CICSCOB1,                                               
//         SRCLIB=TECN93.VISHNU.MAPPDS,         --> SOURCE PDS LIBRARY  
//         MEM=VSAMPRO,               --> PROGRAM NAME                  
//         COPYLIB=TECN93.VISHNU.COPYLIB,        --> COPYBOOK PDS LIB   
//         BMSLIB=TECN93.VISHNU.MAPPDS,           --> BMS MAP LIB       
//         LOADLIB=CICS.APPLI.LOADLIB             **  DO NOT CHANGE  ** 
/*                                 
DEF PROG(VSAMPRO) G(VV1)            
OVERTYPE TO MODIFY                  
 CEDA  DEFine PROGram( VSAMPRO  )   
  PROGram        : VSAMPRO          
  Group          : VV1              
  DEscription  ==>                  
  Language     ==>                  
  RELoad       ==> No               
  RESident     ==> No               
  USAge        ==> Normal           
  USElpacopy   ==> No               
  Status       ==> Enabled          
  RSl            : 00               
  CEdf         ==> Yes              
  DAtalocation ==> Below            
  EXECKey      ==> User             
  COncurrency  ==> Quasirent        
  Api          ==> Cicsapi  



        
DEF MAP(MAPA) G(VV1)               
OVERTYPE TO MODIFY                 
 CEDA  DEFine Mapset( MAPA     )   
  Mapset         : MAPA            
  Group          : VV1             
  Description  ==>                 
  REsident     ==> No              
  USAge        ==> Normal          
  USElpacopy   ==> No              
  Status       ==> Enabled         
  RSl            : 00           
      
DEF MAPSET(VSAMMAP) G(VV1)        
OVERTYPE TO MODIFY                
 CEDA  DEFine Mapset( VSAMMAP  )  
  Mapset         : VSAMMAP        
  Group          : VV1            
  Description  ==>                
  REsident     ==> No             
  USAge        ==> Normal         
  USElpacopy   ==> No             
  Status       ==> Enabled        
  RSl            : 00             
DEF TRANS(1432) PROG(VSAMPRO) G(VV1)                           
OVERTYPE TO MODIFY                                        CICS 
 CEDA  DEFine TRANSaction( 1432 )                              
  TRANSaction    : 1432                                        
  Group          : VV1                                         
  DEscription  ==>                                             
  PROGram      ==> VSAMPRO                                     
  TWasize      ==> 00000              0-32767                  
  PROFile      ==> DFHCICST                                    
  PArtitionset ==>                                             
  STAtus       ==> Enabled            Enabled | Disabled       
  PRIMedsize     : 00000              0-65520                  
  TASKDATALoc  ==> Below              Below | Any              
  TASKDATAKey  ==> User               User | Cics              
  STOrageclear ==> No                 No | Yes                 
  RUnaway      ==> System             System | 0 | 500-2700000 
  SHutdown     ==> Disabled           Disabled | Enabled       
  ISolate      ==> Yes                Yes | No                 
  Brexit       ==>              
CEDA DEF FILE(VISHNU1)PROG(VSAMPRO) G(VV1) 
CEDA  DEFine File( VISHNU1  )                                              
 File         ==> VISHNU1                                                  
 Group        ==> VV1                                                      
 DEScription  ==>                                                          
VSAM PARAMETERS                                                            
 DSNAme       ==> TECN93.VISHNU.KSDS                                       
 Password     ==>                    PASSWORD NOT SPECIFIED                
 RLsaccess    ==> No                 Yes | No                              
 LSrpoolid    ==> 1                  1-8 | None                            
 READInteg    ==> Uncommitted        Uncommitted | Consistent | Repeatable 
 DSNSharing   ==> Allreqs            Allreqs | Modifyreqs                  
 STRings      ==> 001                1-255                                 
 Nsrgroup     ==>                                                          
REMOTE ATTRIBUTES                                                          
 REMOTESystem ==>                                                          
 REMOTEName   ==>                                                          
REMOTE AND CFDATATABLE PARAMETERS                                          
F8 3 TIMES AND ALL YES
CEDA  DEFine File( VISHNU1  )                                 
DATATABLE PARAMETERS                                          
 TABLE        ==> No                 No | CIcs | User | CF    
 Maxnumrecs   ==> Nolimit            Nolimit | 1-99999999     
CFDATATABLE PARAMETERS                                        
 Cfdtpool     ==>                                             
 TABLEName    ==>                                             
 UPDATEModel  ==> Locking            Contention | Locking     
 LOad         ==> No                 No | Yes                 
DATA FORMAT                                                   
 RECORDFormat ==> V                  V | F                    
OPERATIONS                                                    
 Add          ==> Yes                No | Yes                 
 BRowse       ==> Yes                No | Yes                 
 DELete       ==> Yes                No | Yes                 
 READ         ==> Yes                Yes | No                 
 UPDATE       ==> Yes                No | Yes                 
AUTO JOURNALLING                                              
CEDA DIS  G(VV1)                                                              
 ENTER COMMANDS                                                                
  NAME     TYPE         GROUP                                   DATE   TIME    
  VISHNU1  FILE         VV1      ?                           USE PF9 FOR S MSGS
  MAPA     MAPSET       VV1      *                           INSTALL SUCCESSFUL
  VSAMMAP  MAPSET       VV1      *                           INSTALL SUCCESSFUL
  VSAMPRO  PROGRAM      VV1      *                           INSTALL SUCCESSFUL
  1432     TRANSACTION  VV1      *                           INSTALL SUCCESSFUL
  2222     TRANSACTION  VV1                                     23.049 17.35.13

INQ FILE(VISHNU1) PROG(VSANPRO) G(VV1)                        
 STATUS:  RESULTS - OVERTYPE TO MODIFY                         
  Fil(VISHNU1 ) Vsa Ope Ena Rea Upd Add Bro Del     Sha        
         Dsn( TECN93.VISHNU.KSDS                           )   
  IF NOT CLOSED
IKJ56712I INVALID KEYWORD, SHNU.KSDS 
IKJ56703A REENTER THIS OPERAND -     

OUT PUT
                                                                        
                                                                        
                          EMPLOYEE DETAILS                              
                                                                        
                            EMPID                                       
                                                                        
                            EMPNAME                                     
                                                                        
                            EMPSAL                                      
                                                                        
                                                                        
                          F1:READ  F2:UPDATE                            
                                                                        
                          F3:INSERT F4:DELETE                           
                                                                        
                               MSG1:                                    
                                                                        
                                                                        
                              ____________                              
                                                                        
                                                                        
                                                                        
                                                                        
                                                             


EMPLOYEE DETAILS    
                    
  EMPID    E001     
                    
  EMPNAME  VISHNU   
                    
  EMPSAL   59000    
                    
                    
F1:READ  F2:UPDATE  
                    
F3:INSERT F4:DELETE 
                    
     MSG1:          
                    
                    
    READ SUCCESSFUL 
EMPLOYEE DETAILS         
                         
  EMPID    E008          
                         
  EMPNAME  VVVV          
                         
  EMPSAL   04567         
                         
                         
F1:READ  F2:UPDATE       
                         
F3:INSERT F4:DELETE      
                         
     MSG1:               
                         
                         
    READ SUCCESSFUL      
                               
