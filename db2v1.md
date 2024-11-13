
SELECT * FROM SYSIBM.SYSTABLES; 
---------+---------+---------+--
NAME                            
---------+---------+---------+--
EMP                             
V1                              
V2                              
V3                              
V4                              
ADBCHG                          
ADBCHGSR                        
ADBCHGS    
ADBCID     
ADBCIGNORES
ADBCIGNORE 
ADBCMASKS  
ADBCMASK   
ADBCPREREQ
DSN_WQA_WL_REF   
DSN_WQA_SR_REF   
DSN_WQA_EXCEPTION
DSN_WQA_WARNING  
UTTRELS    
UTPROCEB   
UTPROCET   
UTPROCE    
NAME       
---------+-
UTPROC     
UTRESTART2 
UTRESTART  
UTTMPLDFLT 
UTTEMPLATE 
UTLISTE    
UTLIST     
SELECT * FROM SYSIBM.SYSROW WHERE TABLENAME='EMP1';                   
---------+---------+---------+---------+---------+---------+---------+
DSNT408I SQLCODE = -204, ERROR:  SYSIBM.SYSROW IS AN UNDEFINED NAME   
SELECT * FROM SYSIBM.SYSCOLUMN WHERE TABLENAME='EMP1';                  
---------+---------+---------+---------+---------+---------+---------+--
DSNT408I SQLCODE = -204, ERROR:  SYSIBM.SYSCOLUMN IS AN UNDEFINED NAME  
SELECT * FROM SYSIBM.SYSTABLES WHERE USERID='TECN93';                   00600
---------+---------+---------+---------+---------+---------+---------+-------
DSNT408I SQLCODE = -206, ERROR:  USERID IS NOT VALID IN THE CONTEXT WHERE IT 
         IS USED                                                          
   CREATE TABLE EMM1 LIKE EMP1;                                            0061004
---------+---------+---------+---------+---------+---------+---------+---------
DSNT408I SQLCODE = -551, ERROR:  TECN93 DOES NOT HAVE THE PRIVILEGE TO PERFORM 
         OPERATION CREATE TABLE ON OBJECT DSNDB04   
SELECT CURRENT DATE FROM SYSIBM.SYSDUMMY1;
---------+---------+---------+---------+--
                                          
---------+---------+---------+---------+--
2023-01-23                                
SELECT DAYS(CURRENT DATE) FROM SYSIBM.SYSDUMMY1;
738543 
SELECT DAYS(DATE(2017-03-16))-DAYS(DATE(2017-03-11))FROM 
SYSIBM.SYSDUMMY1;                                        
-5 
CREATE TABLE EMP6(EMID CHAR(4) NOT NULL,        
                  EMNM CHAR(10) NOT NULL,       
         EMSAL DEC(6,2),                          
         PRIMARY KEY(EMID))                       
         WITH RESTRICT ON DROP IN SHRDB4.SHRTS4;  
+---------+---------+---------+---------+---------
STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0  











COBOL DB2  PROGRAMS

//TECN93VV JOB ,,NOTIFY=&SYSUID                                  
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                             
//DB2COB   EXEC DB2JCL,                                          
//   SRCLIB=TECN93.COBOL.DB2,                 --> SOURCE LIB     
//   DBRMLIB=TECN93.COBOL.DBRM,                   --> DBRM LIB   
//   MEM=COBDB2I,                               --> MEMBER NAME  
//   INCLIB=TECN93.COBOL.DCLGEN,                 --> DCLGEN LIB  
//   COPYLIB=TECN93.COBOL.COPYLIB,                --> COPY LIB   
//   LOADLIB=TECN93.COBOL.LOADLIB4                --> LOAD LIB   
/*                                                               
//                                                               
//TECN93VJ JOB ,,NOTIFY=&SYSUID                                     
//JOBLIB   DD  DISP=SHR,                                            
//            DSN=DSN910.DB9G.SDSNEXIT                              
//         DD DISP=SHR,                                             
//            DSN=DSN910.SDSNLOAD                                   
//BIND     EXEC PGM=IKJEFT01,DYNAMNBR=20                            
//DBRMLIB  DD DISP=SHR,                                             
//         DSN=TECN93.COBOL.DBRM     --> DBRM LIBRARY               
//SYSTSPRT DD SYSOUT=*                                              
//SYSPRINT DD SYSOUT=*                                              
//SYSUMUMP DD SYSOUT=*                                              
//SYSOUT   DD SYSOUT=*                                              
//REPORT   DD SYSOUT=*                                              
//SYSTSIN  DD *                                                     
  DSN SYSTEM(DB9G)                                                  
  BIND PLAN(TECN93) MEMBER(COBDB2I) ISOLATION(CS) ACTION(REP) -     
  ENCODING(EBCDIC)                                                  
/*                                                                  
//TECN93VR JOB ,,NOTIFY=&SYSUID                                   
//JOBLIB   DD   DISP=SHR,                                         
// DSN=DSN910.DB9G.SDSNEXIT                                       
//         DD DISP=SHR,                                           
// DSN=DSN910.SDSNLOAD                                            
//         DD DISP=SHR,                                           
// DSN=CEE.SCEERUN                                                
//PH02CS04 EXEC PGM=IKJEFT01,DYNAMNBR=20,COND=(4,LT)              
//SYSTSPRT DD SYSOUT=*                                            
//SYSPRINT DD SYSOUT=*                                            
//SYSOUT   DD SYSOUT=*                                            
//SYSIN    DD DUMMY                                               
//SYSTSIN  DD *                                                   
  DSN SYSTEM(DB9G)                                                
  RUN PROGRAM(COBDB2I) PLAN(TECN93) LIB('TECN93.COBOL.LOADLIB4')  
  END                                                             
/*     
SELECT PROGRAM 
FIRST  CREATE  TABLE IN DB2 
Enter the input data set name:        (Can be sequential or partitioned)       
 1  DATA SET NAME ... ===> 'TECN93.VISHNU.DB2PDS1(TAB)'                        
 2  VOLUME SERIAL ... ===>            (Enter if not cataloged)                 
 3  DATA SET PASSWORD ===>            (Enter if password protected)            
                                                                               
Enter the output data set name:       (Must be a sequential data set)          
 4  DATA SET NAME ... ===> 'TECN93.VISHNU.PSDB2'                               
                                                                               
Specify processing options:                                                    
 5  CHANGE DEFAULTS   ===> YES        (Y/N - Display SPUFI defaults panel?)    
 6  EDIT INPUT ...... ===> YES        (Y/N - Enter SQL statements?)            
 7  EXECUTE ......... ===> YES        (Y/N - Execute SQL statements?)          
 8  AUTOCOMMIT ...... ===> YES        (Y/N - Commit after successful run?)     
 9  BROWSE OUTPUT ... ===> YES        (Y/N - Browse output data set?)          
                                                                               
For remote SQL processing:                                                     
10  CONNECT LOCATION  ===>                                                     
                                                                               
                                                                               
PRESS:  ENTER to process    END to exit              HELP for more information 
                                                                               
EDIT       TECN93.VISHNU.DB2PDS1(TAB) - 01.05              Columns 00001 00072 
****** ***************************** Top of Data ******************************
000100 --TABLE CONNECTIN DB2 AND COBOL PGM                                     
000200 --CREATE TABLE TAB(EMPID CHAR (4) NOT NULL PRIMARY KEY,                 
000300 --                     EMPNAME CHAR(15),                                
000400 --                     EMPSAL DEC(10,2))                                
000500 --                     IN SHRDB4.SHRTS4;                                
000600 --CREATE INDEX VID ON TAB(EMPID);                                       
000700 --CREATE UNIQUE INDEX VIS ON TAB(EMPID);                                
000800 --INSERT INTO TAB VALUES ('V001','RAJ',12345678.20);                    
000900 --INSERT INTO TAB VALUES ('V002','CHADAN',52462528.20);                 
001000 --INSERT INTO TAB VALUES ('V003','ABHILASH',86248528.20);               
001100 --INSERT INTO TAB VALUES ('V004','AJIT',45214563.20);                   
001200 --INSERT INTO TAB VALUES ('V005','PRAVEEN',86256328.20);                
001300 SELECT * FROM TAB;                                                      
****** **************************** Bottom of Data ****************************
SELECT * FROM TAB;                      
---------+---------+---------+---------+
EMPID  EMPNAME                EMPSAL    
---------+---------+---------+---------+
V001   RAJ               12345678.20    
V002   CHADAN            52462528.20    
V003   ABHILASH          86248528.20    
V004   AJIT              45214563.20    
V005   PRAVEEN           86256328.20    
V006   VAMES             23456778.00    
V007   HJGGS               526557.88    
V009   VARUN               126557.88    
THEN WRITE PROGRAM IN COBOL 
1 SELECT                                                            
IDENTIFICATION DIVISION.                                
PROGRAM-ID. COBDB2.                                     
ENVIRONMENT DIVISION.                                   
INPUT-OUTPUT SECTION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
    EXEC SQL                                            
    INCLUDE TAB                                         
    END-EXEC.                                           
    EXEC SQL                                            
    INCLUDE SQLCA                                       
    END-EXEC.                                           
PROCEDURE DIVISION.                                     
MAIN-PARA.                                              
    PERFORM PARA1 THRU PARA2.                           
    STOP RUN.                                           
PARA1.                                                  
    EXEC SQL                                            
    SELECT EMPID,EMPNAME INTO :EMPID, :EMPNAME FROM TAB 
    WHERE EMPID='V002'                                  
    END-EXEC.                                           
    IF SQLCODE = 0                                      
    DISPLAY EMPID                                       
    DISPLAY EMPNAME             
    ELSE                        
    DISPLAY 'ROW NOT FOUND'     
    END-IF.                     
    STOP RUN.                   
 PARA2.                         
    EXIT.    
  1  DB2COB
//TECN93VV JOB ,,NOTIFY=&SYSUID                                  
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                             
//DB2COB   EXEC DB2JCL,                                          
//   SRCLIB=TECN93.COBOL.DB2,                           --> SOURCE LIB     
//   DBRMLIB=TECN93.COBOL.DBRM,                   --> DBRM LIB   
//   MEM=COBDB2I,                                                 --> MEMBER NAME  
//   INCLIB=TECN93.COBOL.DCLGEN,                    --> DCLGEN LIB  
//   COPYLIB=TECN93.COBOL.COPYLIB,               --> COPY LIB   
//   LOADLIB=TECN93.COBOL.LOADLIB4               --> LOAD LIB   
/*                                                               
//    
2   DB2BIND                                                           
//TECN93VJ JOB ,,NOTIFY=&SYSUID                                     
//JOBLIB   DD  DISP=SHR,                                            
//            DSN=DSN910.DB9G.SDSNEXIT                              
//         DD DISP=SHR,                                             
//            DSN=DSN910.SDSNLOAD                                   
//BIND     EXEC PGM=IKJEFT01,DYNAMNBR=20                            
//DBRMLIB  DD DISP=SHR,                                             
//         DSN=TECN93.COBOL.DBRM     --> DBRM LIBRARY               
//SYSTSPRT DD SYSOUT=*                                              
//SYSPRINT DD SYSOUT=*                                              
//SYSUMUMP DD SYSOUT=*                                              
//SYSOUT   DD SYSOUT=*                                              
//REPORT   DD SYSOUT=*                                              
//SYSTSIN  DD *                                                     
  DSN SYSTEM(DB9G)                                                  
  BIND PLAN(TECN93) MEMBER(COBDB2I) ISOLATION(CS) ACTION(REP) -     
  ENCODING(EBCDIC)                                                  
/* 
3   DB2RUN                                                                 
//TECN93VR JOB ,,NOTIFY=&SYSUID                                   
//JOBLIB   DD   DISP=SHR,                                         
// DSN=DSN910.DB9G.SDSNEXIT                                       
//         DD DISP=SHR,                                           
// DSN=DSN910.SDSNLOAD                                            
//         DD DISP=SHR,                                           
// DSN=CEE.SCEERUN                                                
//PH02CS04 EXEC PGM=IKJEFT01,DYNAMNBR=20,COND=(4,LT)              
//SYSTSPRT DD SYSOUT=*                                            
//SYSPRINT DD SYSOUT=*                                            
//SYSOUT   DD SYSOUT=*                                            
//SYSIN    DD DUMMY                                               
//SYSTSIN  DD *                                                   
  DSN SYSTEM(DB9G)                                                
  RUN PROGRAM(COBDB2I) PLAN(TECN93) LIB('TECN93.COBOL.LOADLIB4')  
  END                                                             
/*     
OIUT PUT 
******
V007  
HJGGS
EMPID  EMPNAME                EMPSAL  
---------+---------+---------+--------
V001   RAJ               12345678.20  
V002   CHADAN            52462528.20  
V003   ABHILASH          86248528.20  
V004   AJIT              45214563.20  
V005   PRAVEEN           86256328.20  
V006   VAMES             23456778.00  
V007   HJGGS               526557.88  
V009   VARUN               126557.88  
//TECN93A1 JOB ,,NOTIFY=&SYSUID                                 
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                            
//DB2COB   EXEC DB2JCL,                                         
//   SRCLIB=TECN93.COBOL.DB2,                 --> SOURCE LIB    
//   DBRMLIB=TECN93.COBOL.DBRM,                   --> DBRM LIB  
//   MEM=COBDB2I,                               --> MEMBER NAME 
//   INCLIB=TECN93.COBOL.DCLGEN,                 --> DCLGEN LIB 
//   COPYLIB=TECN93.COBOL.COPYLIB,                --> COPY LIB  
//   LOADLIB=TECN93.COBOL.LOADLIB4                --> LOAD LIB  
/*                                                              
//             
Command ===> TSO SDSF ST  
COMMAND INPUT ===>                                            SCROLL ===> PAGE 
NP   JOBNAME  JobID    Owner    Prty Queue      C  Pos  SAff  ASys Status      
     TECN93   TSU02120 TECN93     15 EXECUTION          SYS1  SYS1             
     TECN93VV JOB02050 TECN93      1 PRINT      A                              
     TECN93VV JOB02051 TECN93      1 PRINT      A                              
     TECN93VJ JOB02055 TECN93      1 PRINT      A                              
     TECN93VR JOB02056 TECN93      1 PRINT      A                              
     TECN93A1 JOB02137 TECN93      1 PRINT      A                              
COMMAND INPUT ===>                                            SCROLL ===> PAGE 
NP   DDNAME   StepName ProcStep DSID Owner    C Dest               Rec-Cnt Page
     JESMSGLG JES2                 2 TECN93   H LOCAL                   17     
     JESJCL   JES2                 3 TECN93   H LOCAL                   90     
     JESYSMSG JES2                 4 TECN93   H LOCAL                  110     
     SYSPRINT DB2COB   PC        101 TECN93   H LOCAL                   89     
     SYSTERM  DB2COB   PC        102 TECN93   H LOCAL                   12     
     SYSPRINT DB2COB   COB       104 TECN93   H LOCAL                  360     
     SYSPRINT DB2COB   LKED      105 TECN93   H LOCAL                  185                                                     
17.01.27 JOB02137 $HASP165 TECN93A1 ENDED AT N1  MAXCC=4 CN(INTERNAL)
 2      INSERT
  IDENTIFICATION DIVISION.                                  
PROGRAM-ID. COBDB2I.                                      
ENVIRONMENT DIVISION.                                     
INPUT-OUTPUT SECTION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
    EXEC SQL                                              
    INCLUDE TAB                                           
    END-EXEC.                                             
    EXEC SQL                                              
    INCLUDE SQLCA                                         
    END-EXEC.                                             
PROCEDURE DIVISION.                                       
MAIN-PARA.                                                
     PERFORM 200-PROCESS-PARA THRU 200-PROCESS-EXIT.      
     STOP RUN.                                            
200-PROCESS-PARA.                                         
     MOVE 'V009'TO EMPID.                                 
     MOVE 'VARUN' TO EMPNAME.                             
     MOVE 126557.88 TO EMPSAL.                            
     EXEC SQL                                             
     INSERT INTO TAB VALUES(:EMPID, :EMPNAME, :EMPSAL )   
     END-EXEC.                                            
     IF SQLCODE = 0                         
    DISPLAY 'RECORD INSERTED SUCCESSFULLY'  
    ELSE                                    
    DISPLAY 'RECORD NOT INSERTED'           
    END-IF.                                 
200-PROCESS-EXIT.                           
    EXIT.   
OUT PUT :
                                
********************************* TOP OF DATA **********************************
RECORD INSERTED SUCCESSFULLY                                                    
******************************** BOTTOM OF DATA ********************************
SELECT * FROM TAB;                      
---------+---------+---------+---------+
EMPID  EMPNAME                EMPSAL    
---------+---------+---------+---------+
V001   RAJ               12345678.20    
V002   CHADAN            52462528.20    
V003   ABHILASH          86248528.20    
V004   AJIT              45214563.20    
V005   PRAVEEN           86256328.20    
V006   VAMES             23456778.00    
V007   HJGGS               526557.88    
V009   VARUN               126557.88    
V008   MANES               926557.88   
DSNE610I NUMBER OF ROWS DISPLAYED IS 9
3  UPDATE
IDENTIFICATION DIVISION.                             
PROGRAM-ID. COBDB2U.                                 
ENVIRONMENT DIVISION.                                
INPUT-OUTPUT SECTION.                                
DATA DIVISION.                                       
WORKING-STORAGE SECTION.                             
    EXEC SQL                                         
    INCLUDE TAB                                      
    END-EXEC.                                        
    EXEC SQL                                         
    INCLUDE SQLCA                                    
    END-EXEC.                                        
PROCEDURE DIVISION.                                  
MAIN-PARA.                                           
     PERFORM 200-PROCESS-PARA THRU 200-PROCESS-EXIT. 
     STOP RUN.                                       
200-PROCESS-PARA.                                    
     MOVE 'V005'TO EMPID.                            
     MOVE 'PRAVEEN' TO EMPNAME.                      
     MOVE 86256328.20 TO EMPSAL.                     
     EXEC SQL                                        
     UPDATE  TAB SET :EMPID, :EMPNAME, :EMPSAL       
           WHERE EMPID= :EMPID                       
     END-EXEC.                                       
     IF SQLCODE = 0   
    DISPLAY 'RECORD UPDATED SUCCESSFULLY'   
    ELSE                                    
    DISPLAY 'RECORD NOT UPDATED'            
    END-IF.                                 
200-PROCESS-EXIT.                           
    EXIT.                                   
OUT PUT 

 4 DELETE
IDENTIFICATION DIVISION.                              
PROGRAM-ID. COBDB2D.                                  
ENVIRONMENT DIVISION.                                 
INPUT-OUTPUT SECTION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
    EXEC SQL                                          
    INCLUDE TAB                                       
    END-EXEC.                                         
    EXEC SQL                                          
    INCLUDE SQLCA                                     
    END-EXEC.                                         
PROCEDURE DIVISION.                                   
MAIN-PARA.                                            
     PERFORM 200-PROCESS-PARA THRU 200-PROCESS-EXIT.  
     STOP RUN.                                        
200-PROCESS-PARA.                                     
     EXEC SQL                                         
     DELETE FROM TAB WHERE EMPID='A009'               
     END-EXEC.                                        
     IF SQLCODE = 0                                   
    DISPLAY 'RECORD DELETED SUCCESSFULLY'             
    ELSE                                              
    DISPLAY 'RECORD NOT DELETED'                      
    END-IF.                                           
200-PROCESS-EXIT. 
    EXIT.  
OUT PUT 

****************************
RECORD DELETED SUCCESSFULLY 
****************************


SELECT * FROM TAB2;              
---------+---------+---------+---
EMPID  EMPNAME          EMPSAL   
---------+---------+---------+---
V001   RAJ              123478   
V002   CHADAN           562528   
V003   ABHILASH         848528   
V004   AJIT             45214563

CURSORS
IDENTIFICATION DIVISION.                      
PROGRAM-ID. CURSOR1.                          
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
    EXEC SQL                                  
    INCLUDE TAB2                              
    END-EXEC.                                 
    EXEC SQL                                  
    INCLUDE SQLCA                             
    END-EXEC.                                 
PROCEDURE DIVISION.                           
    EXEC SQL                                  
    DECLARE SS1 CURSOR FOR SELECT * FROM TAB2 
    END-EXEC.                                 
    EXEC SQL                                  
    OPEN SS1                                  
    END-EXEC.                                 
    PERFORM FETCH-PARA UNTIL SQLCODE = 100.   
FETCH-PARA.                                   
     EXEC SQL                                 
     FETCH SS1 INTO :EMPID, :EMPNAME          
    END-EXEC.        
IF             
SQLCODE = 100  
DISPLAY EMPNAME
DISPLAY EMPID  
END-IF.        
 EXEC SQL      
  CLOSE SS1    
 END-EXEC      
STOP RUN.    
OUT PUT :
  
IDENTIFICATION DIVISION.                         
PROGRAM-ID. CURSOR2.                             
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
    EXEC SQL                                     
      INCLUDE TAB2                               
    END-EXEC.                                    
    EXEC SQL                                     
      INCLUDE SQLCA                              
    END-EXEC.                                    
    EXEC SQL                                     
       DECLARE SS1 CURSOR FOR SELECT * FROM TAB2 
    END-EXEC.                                    
    EXEC SQL                                     
       OPEN SS1                                  
    END-EXEC.                                    
PROCEDURE DIVISION.                              
    PERFORM FETCH-PARA UNTIL SQLCODE = 100.      
FETCH-PARA.                                      
     EXEC SQL                                    
       FETCH SS1 INTO :EMPID, :EMPNAME           
    END-EXEC.                                    
IF             
SQLCODE = 100  
DISPLAY EMPNAME
DISPLAY EMPID  
END-IF.        
 EXEC SQL      
    CLOSE SS1  
 END-EXEC      
STOP RUN. 
IDENTIFICATION DIVISION.                             
PROGRAM-ID. CURSOR3.                                 
ENVIRONMENT DIVISION.                                
DATA DIVISION.                                       
WORKING-STORAGE SECTION.                             
    EXEC SQL                                         
      INCLUDE TAB2                                   
    END-EXEC.                                        
    EXEC SQL                                         
      INCLUDE SQLCA                                  
    END-EXEC.                                        
    EXEC SQL                                         
      DECLARE VH1 CURSOR FOR SELECT * FROM TAB2      
        WHERE EMPSAL < 100000 FOR UPDATE OF EMPSAL   
    END-EXEC.                                        
PROCEDURE DIVISION.                                  
MAIN-PARA.                                           
    PERFORM OPEN-PARA.                               
    PERFORM PROCESS-PARA UNTIL SQLCODE =100.         
    PERFORM CLOSE-PARA.                              
    STOP RUN.                                        
OPEN-PARA.                                           
    EXEC SQL                                         
      OPEN VH1                                 
    END-EXEC.                                  
PROCESS-PARA.                                  
    EXEC SQL                                   
      FETCH VH1 INTO :EMPID, :EMPNAME, :EMPSAL 
    END-EXEC.                                  
    MOVE 170000 TO EMPSAL.                     
    EXEC SQL                                   
      UPDATE TAB2                              
      SET EMPSAL = :EMPSAL                     
      WHERE CURRENT OF VH1                     
    END-EXEC.                                  
CLOSE-PARA.                                    
    EXEC SQL                                   
      CLOSE VH1                                
    END-EXEC.                                  
CDENTIFICATION DIVISION.                                  
PROGRAM-ID. CURSOR4.                                      
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
    EXEC SQL                                              
      INCLUDE TAB2                                        
    END-EXEC.                                             
    EXEC SQL                                              
      INCLUDE SQLCA                                       
    END-EXEC.                                             
    EXEC SQL                                              
      DECLARE VB1 CURSOR WITH HOLD FOR SELECT * FROM TAB2 
        WHERE EMPSAL < 200000 FOR UPDATE OF EMPSAL        
    END-EXEC.                                             
PROCEDURE DIVISION.                                       
MAIN-PARA.                                                
    PERFORM OPEN-PARA.                                    
    PERFORM PROCESS-PARA UNTIL SQLCODE =100.              
    PERFORM CLOSE-PARA.                                   
    STOP RUN.                                             
OPEN-PARA.                                                
    EXEC SQL                                              
      OPEN VB1                                 
    END-EXEC.                                  
PROCESS-PARA.                                  
    EXEC SQL                                   
      FETCH VB1 INTO :EMPID, :EMPNAME, :EMPSAL 
    END-EXEC.                                  
    MOVE 250000 TO EMPSAL.                     
    EXEC SQL                                   
      UPDATE TAB2                              
      SET EMPSAL = :EMPSAL                     
      WHERE CURRENT OF VB1                     
    END-EXEC.                                  
    EXEC SQL                                   
      COMMIT                                   
    END-EXEC.                                  
CLOSE-PARA.                                    
    EXEC SQL                                   
      CLOSE VB1                                
    END-EXEC.                                  
OUT PUT =

DYNSQL 

IDENTIFICATION DIVISION.                                     
PROGRAM-ID. DYNSQL1.                                         
ENVIRONMENT DIVISION.                                        
DATA DIVISION.                                               
WORKING-STORAGE SECTION.                                     
    EXEC SQL                                                 
      INCLUDE TAB2                                           
    END-EXEC.                                                
    EXEC SQL                                                 
      INCLUDE SQLCA                                          
    END-EXEC.                                                
01 WS.                                                       
   49 WS-LENGTH PIC S9(4) COMP.                              
   49 WS-TEXT PIC X(80).                                     
PROCEDURE DIVISION.                                          
MAIN-PARA.                                                   
    MOVE 50 TO WS-LENGTH.                                    
    MOVE "DELETE FROM TAB2 WHERE EMPID = 'V001'" TO WS-TEXT. 
    EXEC SQL                                                 
      EXECUTE IMMEDIATE:WS                                   
    END-EXEC.                                                
    IF SQLCODE = 0                                           
    DISPLAY 'RECORD DELETED SUCCESSFULLY'                    
ELSE                            
DISPLAY 'RECORDS NOT DELETED'   
END-IF.                         
STOP RUN.                       
OUT PUT =
                              
       
  IDENTIFICATION DIVISION.                                    
PROGRAM-ID. DYNSQL2.                                        
ENVIRONMENT DIVISION.                                       
DATA DIVISION.                                              
WORKING-STORAGE SECTION.                                    
    EXEC SQL                                                
      INCLUDE TAB2                                          
    END-EXEC.                                               
    EXEC SQL                                                
      INCLUDE SQLCA                                         
    END-EXEC.                                               
01 WS.                                                      
    49 WS-LENGTH PIC S9(4) COMP.                            
    49 WS-TEXT PIC X(80).                                   
PROCEDURE DIVISION.                                         
MAIN-PARA.                                                  
    MOVE 50 TO WS-LENGTH.                                   
    MOVE "DELETE FROM TAB2 WHERE EMPID = 'V001'" TO WS-TEXT.
    EXEC SQL                                                
      PREPARE RAJ FROM :WS                                  
    END-EXEC.                                               
    IF                                                      
    SQLCODE = 0                                             
DISPLAY 'RECORD DELETED SUCCESSFULLY' 
ELSE                                  
DISPLAY SQLCODE                       
END-IF.                               
STOP RUN.                             
IDENTIFICATION DIVISION.                               
PROGRAM-ID. DYNSQL3.                                   
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
    EXEC SQL                                           
      INCLUDE TAB2                                     
    END-EXEC.                                          
    EXEC SQL                                           
      INCLUDE SQLCA                                    
    END-EXEC.                                          
01 WS.                                                 
    49 WS-LENGTH PIC S9(4) COMP.                       
    49 WS-TEXT PIC X(80).                              
    01 AS                                              
       10 E1 PIC X(4).                                 
PROCEDURE DIVISION.                                    
MAIN-PARA.                                             
    MOVE 50 TO WS-LENGTH.                              
    MOVE "DELETE FROM TAB2 WHERE EMPID = ?" TO WS-TEXT.
    EXEC SQL                                           
      PREPARE RAJ FROM :WS                             
    END-EXEC.                                          
ACCEPT E1.                           
EXEC SQL                             
  EXECUTE RAJ USING :E1              
END-EXEC.                            
IF                                   
SQLCODE = 0                          
DISPLAY 'RECORD DELETED SUCCESSFULLY'
ELSE                                 
DISPLAY SQLCODE                      
END-IF.                              
STOP RUN.                            
IDENTIFICATION DIVISION.                             
PROGRAM-ID. DYNSQL4.                                 
ENVIRONMENT DIVISION.                                
DATA DIVISION.                                       
WORKING-STORAGE SECTION.                             
    EXEC SQL                                         
      INCLUDE TAB2                                   
    END-EXEC.                                        
    EXEC SQL                                         
      INCLUDE SQLCA                                  
    END-EXEC.                                        
01 WS.                                               
   49 WS-LENGTH PIC S9(4) COMP.                      
   49 WS-TEXT PIC X(80).                             
PROCEDURE DIVISION.                                  
MAIN-PARA.                                           
    MOVE 50 TO WS-LENGTH.                            
    MOVE "SELECT EMPID,EMPNAME FROM TAB2" TO WS-TEXT.
    EXEC SQL                                         
      PREPARE RAJ FROM :WS                           
    END-EXEC.                                        
    EXEC SQL                                         
      DECLARE CURS CURSOR FOR RAJ                    
    END-EXEC                                
    EXEC SQL                                
      OPEN CURS                             
    END-EXEC.                               
    PERFORM FETCH-PARA UNTIL SQLCODE = 100. 
    EXEC SQL                                
        CLOSE CURS                          
    END-EXEC                                
    STOP RUN.                               
FETCH-PARA.                                 
    EXEC SQL                                
     FETCH CURS INTO :EMPID, :EMPNAME       
    END-EXEC.                               
    DISPLAY EMPID.                          
    DISPLAY EMPNAME.                        
                             


 
