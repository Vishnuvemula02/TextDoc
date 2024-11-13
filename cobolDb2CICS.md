    TECN93.VISHNU.DB2PDS1(TECN8) - 01.06            Colum
***************************** Top of Data ***************
--CREATE TABLE TECN8(XID CHAR(4) NOT NULL PRIMARY KEY,   
--                   XNAME CHAR(10) NOT NULL,            
--                   XSAL CHAR (05) NOT NULL)            
--                   IN SHRDB4.SHRTS4;                   
--CREATE INDEX AN9 ON TECN8(XID);                        
--CREATE UNIQUE INDEX AN5 ON TECN8(XID);                 
--INSERT INTO TECN8 VALUES ('V001','VISHNU','65432');    
--INSERT INTO TECN8 VALUES ('V002','RAJKUMAR','55432');  
--INSERT INTO TECN8 VALUES ('V003','VISHAL','75432');    
--INSERT INTO TECN8 VALUES ('V004','VARUN','85432');     
--INSERT INTO TECN8 VALUES ('V005','SAI','95432');       
--INSERT INTO TECN8 VALUES ('V006','VKASE','45432');     
SELECT * FROM TECN8;
















EDIT       TECN93.VISHNU.MAPPDS(DB2MAPA) - 01.01           Columns 00001 00072 
****** ***************************** Top of Data ******************************
000100 DB2MAPA  DFHMSD TYPE=&&SYSPARM,MODE=INOUT,LANG=COBOL,                  X
000200                TIOAPFX=YES,CTRL=(FRSET,FREEKB),STORAGE=AUTO,TERM=ALL    
000300 VVMAP1   DFHMDI SIZE=(24,80),LINE=1,COLUMN=1,JUSTIFY=LEFT,TIOAPFX=YES   
000400          DFHMDF POS=(04,28),LENGTH=16,INITIAL='EMPLOYEE DETAILS:',     X
000500                ATTRB=(PORT,FSET)                                        
000600          DFHMDF POS=(06,30),LENGTH=8,INITIAL='EMPID :',                X
000700                ATTRB=(PROT,FSET)                                        
000800 EMPID    DFHMDF POS=(06,39),LENGTH=4,INITIAL='____',                   X
000900                ATTRB=(UNPORT,FSET,IC)                                   
001000          DFHMDF POS=(06,44),LENGTH=1,ATTRB=ASKIP                        
001100          DFHMDF POS=(08,30),LENGTH=10,INITIAL='EMPNAME :',             X
001200                ATTRB=(PROT,FSET)                                        
001300 EMPNAME  DFHMDF POS=(08,39),LENGTH=10,INITAL='__________',             X
001400                ATTRB=(UNPORT,FSET,IC)                                   
001500          DFHMDF POS=(08,50),LENGTH=1,ATTRB=ASKIP                        
001600          DFHMDF POS=(10,30),LENGTH=8,INITIAL='EMPSAL :',               X
001700                ATTRB=(PORT,FSET)                                        
001800 EMPSAL   DFHMDF POS=(10,39),LENGTH=5,INITIAL='_____',                  X
001900                ATTRB=(UNPROT,FSET,IC)                                   
002000          DFHMDF POS=(10,45),LENGTH=1,ATTRB=ASKIP                        
002100          DFHMDF POS=(13,28),LENGTH=22,ATTRB=(PORT,FSET),               X
002200                 INITIAL='F1:SELECT F2:UPDATE'                           
002300          DFHMDF POS=(15,28),LENGTH=22,ATTRB=(PORT,FSET),               X
002400                 INITIAL='F3:INSERT F5:DELETE'                           
002500          DFHMDF POS=(17,33),LENGTH=8,SATTRB=(PORT,FSET),               X
002600                INITAL='F6:EXEIT'                                        
002700          DFHMDF POS=(20,27),LENGTH=4,INITIAL='MSG:'                    X
002800                ATTRB=(PROT,FSET)                                        
002900 MSG      DFHMDF POS=(20,32),LENGTH=20,INITIAL='____________________',  X
003000                ATTRB=(UNPORT,FSET,IC)                                   
003100          DFHMDF POS=(20,53),LENGTH=1,ATTRB=PORT                         
003200          DFHMSD TYPE=FINAL                                              
003300                  END                                                    
****** **************************** Bottom of Data ****************************
EDIT       TECN93.VISHNU.MAPPDS(MAPCOMP) - 01.65           Columns 00001 00072 
****** ***************************** Top of Data ******************************
000001 //TECN93VV JOB ,,CLASS=A,                                               
000002 //         MSGCLASS=H,MSGLEVEL=(1,1),                                   
000003 //         NOTIFY=&SYSUID                                               
000004 //JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                                    
000005 //CICSMAP  EXEC CICSMAP1,                                               
000006 //         OUTC=*,                                                      
000007 //         COPYLIB=TECN93.VISHNU.COPYLIB,                               
000008 //         LOADLIB=CICS.APPLI.LOADLIB,               ** DONT CHANGE **  
000009 //         MAPNAME=DB2MAPA                        -->  MEMBER NAME      
000010 //COPY.SYSUT1  DD  DSN=TECN93.VISHNU.MAPPDS(&MAPNAME),                  
000011 //         DISP=SHR                                                     
000012 /*                                                                      
****** **************************** Bottom of Data ****************************











TECN93.VISHNU.MAPPDS(DB2PGM1) - 01.08         
************************* Top of Data ********
   IDENTIFICATION DIVISION.                   
   PROGRAM-ID. DB2PGM1.                       
   ENVIRONMENT DIVISION.                      
   DATA DIVISION.                             
   WORKING-STORAGE SECTION.                   
       EXEC SQL                               
          INCLUDE TECN8                       
       END-EXEC.                              
       EXEC SQL                               
          INCLUDE SQLCA                       
       END-EXEC.                              
       COPY DB2MAPA.                          
       COPY DFHBMSCA.                         
       COPY DFHAID.                           
   77 CID PIC X(4).                           
   77 CNAME PIC X(10).                        
   77 CSAL PIC X(5).                          
   77 COMM PIC X(4).                          
   LINKAGE SECTION.                           
   01 DFHCOMMAREA PIC X(4).                   
   PROCEDURE DIVISION.                        
   BEGIN.                                     
       MOVE LOW-VALUES TO VVMAP1O.            
       IF EIBCALEN = 0                        
       PERFORM SEND-PARA                      
       ELSE                                     
       PERFORM EVALUATE-PARA                    
       END-IF.                                  
  ********CICS DECLERATION*********             
   TRANS-PARA.                                  
       EXEC CICS RETURN                         
         TRANSID('1212')                        
         COMMAREA(COMM)                         
       END-EXEC.                                
   RECEIVE-PARA.                                
       EXEC CICS RECEIVE                        
         MAP('VVMAP1')                          
         MAPSET('DB2MAPA')                      
       END-EXEC.                                
  ********SENDING******************             
   SEND-PARA.                                   
       EXEC CICS SEND                           
         MAP('VVMAP1')                          
         MAPSET('DB2MAPA')                      
       FREEKB                                   
       ERASE                                    
       END-EXEC.                                
       PERFORM TRANS-PARA.                      
   EVALUATE-PARA.                               
       EVALUATE TRUE                            
       WHEN EIBAID = DFHPF1 PERFORM SELECT-PARA
    WHEN EIBAID = DFHPF2 PERFORM UPDATE-PARA          
    WHEN EIBAID = DFHPF3 PERFORM INSERT-PARA          
    WHEN EIBAID = DFHPF4 PERFORM DELETE-PARA          
    WHEN EIBAID = DFHPF5 PERFORM EXIT-PARA            
    WHEN OTHER MOVE 'INVALID FUNCTION KEY' TO MSGO    
    END-EVALUATE.                                     
SELECT-PARA.                                          
    PERFORM RECEIVE-PARA.                             
    MOVE EMPIDI TO CID.                               
    MOVE CID TO XID.                                  
    EXEC SQL                                          
    SELECT XID,XNAME,XSAL INTO :XID, :XNAME, :XSAL    
    FROM TECN8                                        
    WHERE EMPID = :XID                                
    END-EXEC.                                         
    IF SQLCODE = 0                                    
    MOVE XID TO EMPIDO                                
    MOVE XNAME TO EMPNAMEO                            
    MOVE XSAL TO EMPSALO                              
    MOVE 'SELECT SUCCESSFULL' TO MSGO                 
    PERFORM SEND-PARA                                 
    ELSE                                              
    MOVE SQLCODE TO MSGO                              
    PERFORM SEND-PARA                                 
    END-IF.                                           
INSERT-PARA.                                          
     PERFORM RECEIVE-PARA.                          
     MOVE EMPIDI TO CID.                            
     MOVE EMPNAMEI TO CNAME.                        
     MOVE EMPSALI TO CSAL.                          
     MOVE CID TO XID.                               
     MOVE CNAME TO XNAME.                           
     MOVE CSAL TO XSAL.                             
     EXEC SQL                                       
     INSERT INTO TECN8 VALUES( :XID, :XNAME, :XSAL) 
     END-EXEC.                                      
     IF SQLCODE = 0                                 
     MOVE 'INSERT SUCCESSFULL' TO MSGO              
     PERFORM SEND-PARA                              
     ELSE                                           
     MOVE SQLCODE TO MSGO                           
     PERFORM SEND-PARA                              
     END-IF.                                        
 UPDATE-PARA.                                       
     PERFORM RECEIVE-PARA.                          
     MOVE EMPIDI TO CID.                            
     MOVE EMPNAMEI TO CNAME.                        
     MOVE EMPSALI TO CSAL.                          
     MOVE CID TO XID.                               
     MOVE CNAME TO XNAME.                           
     MOVE CSAL TO XSAL.                             
     EXEC SQL                                       
     UPDATE TECN8 SET XNAME = :XNAME,XSAL = :XSAL   
     WHERE XID = :XID                               
     END-EXEC.                                      
     IF SQLCODE = 0                                 
     MOVE 'UPDATE SUCCESSFULL' TO MSGO              
     PERFORM SEND-PARA                              
     ELSE                                           
     MOVE SQLCODE TO MSGO                           
     PERFORM SEND-PARA                              
     END-IF.                                        
 DELETE-PARA.                                       
     PERFORM RECEIVE-PARA.                          
     MOVE EMPIDI TO CID.                            
     MOVE CID TO XID.                               
     EXEC SQL                                       
     DELETE FROM TECN8                              
     WHERE XID = :XID                               
     END-EXEC.                                      
     IF SQLCODE = 0                                 
     MOVE 'DELETE SUCCESSFULL' TO MSGO              
     PERFORM SEND-PARA                              
     ELSE                                           
     MOVE SQLCODE TO MSGO                           
     PERFORM SEND-PARA                              
     END-IF.                                        
 EXIT-PARA.                                         
EXEC CICS 
RETURN    
END-EXEC.
-------------------------------------------------------------------------------
EDIT       TECN93.VISHNU.MAPPDS(COBDB2C) - 01.20           Columns 00001 00072 
****** ***************************** Top of Data ******************************
000001 //TECN93VV JOB ,,NOTIFY=&SYSUID,CLASS=A,MSGLEVEL=(1,1),MSGCLASS=H,      
000002 //           LINES=999999                                               
000003 //DD1 SET SRCLIB=TECN93.VISHNU.MAPPDS      --> SOURCE LIBRARY           
000004 //DD2 SET DBRMLIB=TECN93.VISHNU.DBRM       --> DBRM LIBRARY             
000005 //DD3 SET MEM=DB2PGM1                    -->MEMBER NAME                 
000006 //DD4 SET DCLLIB=TECN93.VISHNU.DCLGEN      --> DCLGEN LIBRARY           
000007 //DD5 SET COPYLIB=TECN93.VISHNU.COPYLIB     -->SYMBOLIC MAP             
000008 //DD6 SET LOADLIB=CICS.APPLI.LOADLIB         ** DO NOT CHANGE           
000009 //DD7 SET BMSLIB=TECN93.VISHNU.MAPPDS(DB2MAPA)   ---> BMS MAP LIB       
000010 //DD8 SET WSPC=500                                                      
000011 //DD9 SET REG=4096K                                                     
000012 //DDA SET LNKPARM='XREF'                                                
000013 //DDB SET WORK=ZAPRD6                                                   
000014 //********************************************************************  
000015 //*   1.PRECOMPILER                                                     
000016 //*******************************************************************   
000017 //PRECOMP  EXEC PGM=DSNHPC,                                             
000018 //         PARM='HOST(IBMCOB),APOST,SOURCE,LEVEL(GLM)',                 
000019 //         REGION=4096K                                                 
000020 //STEPLIB  DD   DISP=SHR,DSN=DSN810.SDSNEXIT                            
000021 //         DD   DISP=SHR,DSN=DSN810.SDSNLOAD                            
000022 //DBRMLIB  DD   DISP=SHR,DSN=&DBRMLIB(&MEM)                             
000023 //SYSCIN   DD   DSN=&&DSNHOUT,DISP=(MOD,PASS),UNIT=SYSDA,               
000024 //             SPACE=(800,(&WSPC,&WSPC))                                
000025 //SYSLIB   DD   DSN=&DCLLIB,DISP=SHR                                    
000026 //         DD   DSN=&COPYLIB,DISP=SHR                                   
000027 //SYSTERM  DD   SYSOUT=*                                                
000028 //SYSDUMP  DD   SYSOUT=*                                                
000029 //SYSPRINT DD   SYSOUT=*                                                
000030 //SYSIN    DD   DSN=&SRCLIB(&MEM),DISP=SHR                              
000031 //SYSUT1   DD   SPACE=(800,(&WSPC,&WSPC),,,ROUND),UNIT=SYSDA,           
000032 //         VOL=SER=&WORK                                                
000033 //SYSUT2   DD   SPACE=(800,(&WSPC,&WSPC),,,ROUND),UNIT=SYSDA,           
000034 //         VOL=SER=&WORK                                                
000035 //********************************************************************  
000036 //* 2. CICS TRANSALATION                                                
000037 //*******************************************************************   
000038 //TRANSL   EXEC PGM=DFHECP1$,REGION=&REG,PARM='COBOL2',                 
000039 //         COND=(5,LT)                                                  
000040 //STEPLIB  DD   DSN=DFH320.CICS.SDFHLOAD,DISP=SHR                       
000041 //SYSPRINT DD   SYSOUT=*                                                
000042 //SYSIN    DD   DSN=&&DSNHOUT,DISP=(MOD,PASS),UNIT=SYSDA                
000043 //SYSPUNCH DD   DSN=&&SYSCIN,                                           
000044 //         DISP=(,PASS),UNIT=SYSDA,                                     
000045 //         DCB=BLKSIZE=400,                                             
000046 //         SPACE=(400,(400,100))                                        
000047 //********************************************************************  
000048 //* 3. COMPILATION                                                      
000049 //********************************************************************  
000050 //COBOL    EXEC PGM=IGYCRCTL,REGION=&REG,                               
000051 //     PARM='NODYNAM,LIB,OBJECT,RENT,APOST',COND=(5,LT)                 
000052 //STEPLIB  DD   DSN=IGY410.SIGYCOMP,DISP=SHR                            
000053 //SYSLIB   DD   DSN=DFH320.CICS.SDFHCOB,DISP=SHR                        
000054 //         DD   DSN=&COPYLIB,DISP=SHR                                   
000055 //         DD   DSN=&BMSLIB,DISP=SHR                                    
000056 //SYSPRINT DD   SYSOUT=*                                                
000057 //SYSIN    DD   DSN=&&SYSCIN,DISP=(OLD,DELETE)                          
000058 //SYSLIN   DD   DSN=&&LOADSET,DISP=(MOD,PASS),                          
000059 //         UNIT=SYSDA,SPACE=(80,(250,100))                              
000060 //SYSUT1   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000061 //SYSUT2   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000062 //SYSUT3   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000063 //SYSUT4   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000064 //SYSUT5   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000065 //SYSUT6   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000066 //SYSUT7   DD   UNIT=SYSDA,SPACE=(460,(350,100)),VOL=SER=&WORK          
000067 //********************************************************************  
000068 //* 4. BIND & RUN PROGRAMS                                              
000069 //*****************************************************************     
000070 //BIND     EXEC PGM=IKJEFT01,DYNAMNBR=20                                
000071 //STEPLIB  DD   DISP=SHR,DSN=DSN910.DB9G.SDSNEXIT                       
000072 //         DD   DISP=SHR,DSN=DSN910.SDSNLOAD                            
000073 //DBRMLIB  DD   DISP=SHR,DSN=TECN93.VISHNU.DBRM       --->DBRM LIB      
000074 //SYSTSPRT DD   SYSOUT=*                                                
000075 //SYSPRINT DD   SYSOUT=*                                                
000076 //SYSUDUMP DD   SYSOUT=*                                                
000077 //SYSOUT   DD   SYSOUT=*                                                
000078 //REPORT   DD   SYSOUT=*                                               
000079 //SYSTSIN  DD   *                                                      
000080       DSN SYSTEM(DB9G)                                                 
000081       BIND PLAN(TECN93)-                                               
000082       MEMBER(DB2PGM1)-                                                 
000083       ISOLATION(CS)-                                                   
000084       ENCODING(EBCDIC)-                                                
000085       ACT(REP)                                                         
000086 /*                                                                     
000087 //*********************************************************************
000088 //* 5. LINK EDIT                                                       
000089 //*********************************************************************
000090 //LKED     EXEC PGM=IEWL,REGION=&REG,COND=(5,LT,COBOL),                
000091 //         PARM=&LNKPARM                                               
000092 //SYSLIB   DD   DSN=DFH320.CICS.SDFHLOAD,DISP=SHR                      
000093 //         DD   DSN=DFH320.CICS.SDFHCOB,DISP=SHR                       
000094 //         DD   DSN=CEE.SCEELKED,DISP=SHR                              
000095 //         DD   DSN=CEE.SCEERUN,DISP=SHR                               
000096 //         DD   DSN=DSN910.SDSNLOAD,DISP=SHR                           
000097 //DB2LOAD  DD   DSN=DSN910.SDSNLOAD,DISP=SHR                           
000098 //SYSLMOD  DD   DSN=&LOADLIB(&MEM),DISP=SHR                            
000099 //SYSUT1   DD   UNIT=SYSDA,DCB=BLKSIZE=1024,VOL=SER=&WORK,             
000100 //         SPACE=(1024,(200,20))                                       
000101 //SYSPRINT DD   SYSOUT=*                                               
000102 //SYSLIN   DD   DSN=DFH320.CICS.SDFHCOB(DFHEILIC),DISP=SHR             
000103 //         DD   DSN=&&LOADSET,DISP=(OLD,DELETE)                        
000104 //SYSIN    DD   DUMMY               
000105 /*                                  






CEDA DEF PROG(DB2PGM1) G(VISHNU)
  DEF PROG(DB2PGM1) G(VISHNU)                                                   
  OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
   CEDA  DEFine PROGram( DB2PGM1  )                                             
    PROGram        : DB2PGM1                                                    
    Group          : VISHNU                                                     
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
 +  DYnamic      ==> No                 No | Yes                                
                                                                                
                                                      SYSID=CICS APPLID=CICS    
   DEFINE SUCCESSFUL                            TIME:  14.38.30  DATE: 23.049   
 PF 1 HELP 2 COM 3 END             6 CRSR 7 SBH 8 SFH 9 MSG 10 SB 11 SF 12 CNCL
DEF MAP(VVMAP1) G(VISHNU)                                                     
OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
 CEDA  DEFine Mapset( VVMAP1   )                                              
  Mapset         : VVMAP1                                                     
  Group          : VISHNU                                                     
  Description  ==>                                                            
  REsident     ==> No                 No | Yes                                
  USAge        ==> Normal             Normal | Transient                      
  USElpacopy   ==> No                 No | Yes                                
  Status       ==> Enabled            Enabled | Disabled                      
  RSl            : 00                 0-24 | Public         
                  
DEF MAPSET(DB2MAPA) G(VISHNU)                                                 
OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
 CEDA  DEFine Mapset( DB2MAPA  )                                              
  Mapset         : DB2MAPA                                                    
  Group          : VISHNU                                                     
  Description  ==>                                                            
  REsident     ==> No                 No | Yes                                
  USAge        ==> Normal             Normal | Transient                      
  USElpacopy   ==> No                 No | Yes                                
  Status       ==> Enabled            Enabled | Disabled                      
  RSl            : 00                 0-24 | Public                           
CEDA DEF TRANS(1212) PROG(DB2PGM1) G(VISHNU)
OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
 CEDA  DEFine TRANSaction( 1212 )                                             
  TRANSaction    : 1212                                                       
  Group          : VISHNU                                                     
  DEscription  ==>                                                            
  PROGram      ==> DB2PGM1                                                    
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
 REMOTE ATTRIBUTES                                                            
                                                                              
                                                    SYSID=CICS APPLID=CICS    
 DEFINE SUCCESSFUL                            TIME:  14.53.45  DATE: 23.049   
F 1 HELP 2 COM 3 END             6 CRSR 7 SBH 8 SFH 9 MSG 10 SB 11 SF 12 CNCL
CEDA DEF DB2E(SE) G(VISHNU)
DEF DB2E(SE) G(VISHNU)                                                        
OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
 CEDA  DEFine DB2Entry( SE       )                                            
  DB2Entry       : SE                                                         
  Group          : VISHNU                                                     
  DEscription  ==>                                                            
 THREAD SELECTION ATTRIBUTES                                                  
  TRansid      ==>                                                            
 THREAD OPERATION ATTRIBUTES                                                  
  ACcountrec   ==> None               None | TXid | TAsk | Uow                
  AUTHId       ==>                                                            
  AUTHType     ==> Userid             Userid | Opid | Group | Sign | TErm     
                                      | TX                                    
  DRollback    ==> Yes                Yes | No                                
  PLAN         ==>                                                            
  PLANExitname ==> DSNCUEXT                                                   
  PRIority     ==> High               High | Equal | Low                      
  PROtectnum   ==> 0000               0-2000                                  
  THREADLimit  ==> 0000               0-2000                                  
  THREADWait   ==> Pool               Pool | Yes | No                         
+  AUTHType     ==> Userid             Userid | Opid | Group | Sign | TErm 
                                       | TX                                
   DRollback    ==> Yes                Yes | No                            
   PLAN         ==> TECN93                                                 
   PLANExitname ==>                                                        
   PRIority     ==> High               High | Equal | Low                  
   PROtectnum   ==> 0000               0-2000                              
   THREADLimit  ==> 0000               0-2000                              
   THREADWait   ==> Pool               Pool | Yes | No                     
THREAD SELECTION ATTRIBUTES                                               
 TRansid      ==> 1212                                                    
THREAD OPERATION ATTRIBUTES                                               
 ACcountrec   ==> None               None | TXid | TAsk | Uow             
 AUTHId       ==>                                                         
 AUTHType     ==> Userid             Userid | Opid | Group | Sign | TErm  
                                     | TX                                 
 DRollback    ==> Yes                Yes | No                             
 PLAN         ==> TECN93                                                  

DEF DB2T(TC) G(VISHNU)              
OVERTYPE TO MODIFY                  
 CEDA  DEFine DB2Tran( TC       )   
  DB2Tran      ==> TC               
  Group        ==> VISHNU           
  Description  ==>                  
  Entry        ==>                  
  Transid      ==>     



             
DEF DB2T(TC) G(VISHNU)               
OVERTYPE TO MODIFY                   
 CEDA  DEFine DB2Tran( TC       )    
  DB2Tran      ==> TC                
  Group        ==> VISHNU            
  Description  ==>                   
  Entry        ==>  SE               
  Transid      ==>  TC       
                                                     SYSID=CICS APPLID=CICS    
  DEFINE SUCCESSFUL                            TIME:  15.05.18  DATE: 23.049   
PF 1 HELP 2 COM 3 END             6 CRSR 7 SBH 8 SFH 9 MSG 10 SB 11 SF 12 CNCL 
CEDA DIS G(VISHNU)    
DB2MAPA  MAPSET       VISHNU     I
VVMAP1   MAPSET       VISHNU   I          
DB2PGM1  PROGRAM      VISHNU   I                 
1212     TRANSACTION  VISHNU   I                              23.049 14.53.44
SE       DB2ENTRY     VISHNU   I                              23.049 15.01.24
TC       DB2TRAN      VISHNU    I                             23.049 15.05.18        
ENTER COMMANDS                                                                
 NAME     TYPE         GROUP                                   DATE   TIME    
 DB2MAPA  MAPSET       VISHNU   *                           INSTALL SUCCESSFUL
VVMAP1   MAPSET       VISHNU   *                           INSTALL SUCCESSFUL
DB2PGM1  PROGRAM      VISHNU   *                           INSTALL SUCCESSFUL
1212     TRANSACTION  VISHNU   *                           INSTALL SUCCESSFUL
SE       DB2ENTRY     VISHNU   ?                           USE PF9 FOR S MSGS
TC       DB2TRAN      VISHNU   *                           INSTALL SUCCESSFUL
CEDA INS DB2E(SE) G(VISHNU)
CEDA INS DB2E(SE) G(VISHNU)   
OVERTYPE TO MODIFY            
 CEDA  Install                
  CONnection   ==>            
  CORbaserver  ==>            
  DB2Conn      ==>            
  DB2Entry     ==> SE         
  DB2Tran      ==>            
  DJar         ==>            
  DOctemplate  ==>            
  Enqmodel     ==>            
  File         ==>            
  Ipconn       ==>            
  Journalmodel ==>            
  LIBrary      ==>            
  LSrpool      ==>            
  Mapset       ==> VVMAP1     
  PARTItionset ==>            
  PARTNer      ==>            
  PIpeline     ==>            
   PROCesstype  ==>                         
   PROFile      ==>                         
   PROGram      ==> DB2PGMA                 
   Requestmodel ==>                         
   Sessions     ==>                         
   TCpipservice ==>                         
   TDqueue      ==>                         
+  TErminal     ==>      
CEDA  INS DB2T(TC) G(VISHNU)
OVERTYPE TO MODIFY              
 CEDA  Install                  
  File         ==>              
  Ipconn       ==>              
  Journalmodel ==>              
  LIBrary      ==>              
  LSrpool      ==>              
  Mapset       ==>              
  PARTItionset ==>              
  PARTNer      ==>              
  PIpeline     ==>              
  PROCesstype  ==>              
  PROFile      ==>              
  PROGram      ==> DB2PGM1      
  Requestmodel ==>              
  Sessions     ==>              
  TCpipservice ==>              
  TDqueue      ==>              
  TErminal     ==>              
                                
                                
 INSTALL SUCCESSFUL             
1212         
                                
     EMPLOYEE DETAILS           
                                
       EMPID :  ____            
                                
       EMPNAME                  
                                
       EMPSAL : _____           
                                
                                
                                
                                
                                
                                
                                
                                
                                
    MSG: ____________________   
                                                   







                                      
