
PS TO SPOOL -SEQUENTIAL READ

IDENTIFICATION DIVISION.               
PROGRAM-ID. FILEH1.                    
ENVIRONMENT DIVISION.                  
INPUT-OUTPUT SECTION.                  
FILE-CONTROL.                          
     SELECT CUSTFILE ASSIGN TO VISHNU  
     ORGANIZATION IS SEQUENTIAL        
     ACCESS MODE IS SEQUENTIAL         
     FILE STATUS IS FS1.               
DATA DIVISION.                         
FILE SECTION.                          
FD CUSTFILE.                           
01 CUST-REC.                           
     05 CUST-ID PIC X(4).              
     05 CUST-NAME PIC X(10).           
     05 CUST-ADDRESS PIC X(10).        
     05 FILLER PIC X(56).              
WORKING-STORAGE SECTION.               
  01 WS-EOF PIC X(3) VALUE  'NO'.      
  01 FS1 PIC 9(2).                     
PROCEDURE DIVISION.                    
A001-CUST-PARA.                        
    PERFORM 0001-OPEN-PARA. 
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'. 
    PERFORM C001-CLOSE-PARA.                        
    STOP RUN.                                       
0001-OPEN-PARA.           
    OPEN INPUT CUSTFILE.  
P001-PROCESS-PARA.        
     READ CUSTFILE        
     AT END               
     MOVE 'YES' TO WS-EOF 
     NOT AT END           
     DISPLAY CUST-REC     
     END-READ.            
C001-CLOSE-PARA.          
     CLOSE CUSTFILE.      
OUT :
   A001RAKESHKUMAR 9987654329 ENGINEER     BANGALORE      
A002ANIL        9987652222 SR.ARCHITECT CHENNAI        
A003VIJAY       9287635439 ENGINEER     MYSORE         
A004RAMAY       9966777884 EMPLOYE      HYDERABED      
A005KRISHNA     9995556778 EMPLOYE      KARANATAKA     
A006VIKAS       9998876534 SHOPKEPPER   BHARE          
A007VARUN       5654345635 SHOPKEPPER   OSORE          
A008VISHNU      1234566434 ITEMPLOY     MYHYD          
A009RAMESH      9876431234 EMPLOYE      ANDRAPRADESHE  
4,0  11,6        10,18      12,29        13,42     
PS TO PS WRITE  SEQUENTIAL PGM:
IDENTIFICATION DIVISION.             
PROGRAM-ID. FILEH2.                  
ENVIRONMENT DIVISION.                
INPUT-OUTPUT SECTION.                
FILE-CONTROL.                        
     SELECT INFILE ASSIGN TO INDD    
     ORGANIZATION IS SEQUENTIAL      
     ACCESS MODE IS SEQUENTIAL       
     FILE STATUS IS FS1.             
     SELECT OUTFILE ASSIGN TO OUTDD  
     ORGANIZATION IS SEQUENTIAL      
     ACCESS MODE IS SEQUENTIAL       
     FILE STATUS IS FS2.             
DATA DIVISION.                       
FILE SECTION.                        
FD INFILE.                           
01 IN-REC.                           
     05 IN-EMP-ID PIC X(4).          
     05 IN-EMP-NAME PIC X(10).       
     05 IN-EMP-ADDRESS PIC X(10).    
     05 FILLER PIC X(61).            
FD OUTFILE.                          
01 OUT-REC.                          
     05 OUT-EMP-ID PIC X(10).    
     05 OUT-EMP-NAME PIC X(4).   
     05 OUT-EMP-ADDRESS PIC 9(5).
     05 FILLER PIC X(61).                            
WORKING-STORAGE SECTION.                             
  01 WS-EOF PIC X(3) VALUE  'NO'.                    
  01 FS1 PIC 9(2).                                   
  01 FS2 PIC 9(2).                                   
PROCEDURE DIVISION.                                  
A001-EMP-PARA.                                       
    PERFORM 0001-OPEN-PARA.                          
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'.  
    PERFORM C001-CLOSE-PARA.                         
    STOP RUN.                                        
0001-OPEN-PARA.                                      
    OPEN INPUT INFILE.                               
    OPEN OUTPUT OUTFILE.                             
P001-PROCESS-PARA.                                   
    READ INFILE                                      
        AT END                                       
        MOVE 'YES' TO WS-EOF                         
        NOT AT END                                   
        MOVE IN-REC TO OUT-REC                       
        WRITE OUT-REC                                
        END-READ.                                    
C001-CLOSE-PARA.                                     
        CLOSE INFILE.                                
        CLOSE OUTFILE.                               
OUT PUT : NOT GOT
            
ESDS TO SPOOL -SEQUENTIAL READ
IDENTIFICATION DIVISION.                  
PROGRAM-ID. FIHESDS1.                     
ENVIRONMENT DIVISION.                     
INPUT-OUTPUT SECTION.                     
FILE-CONTROL.                             
     SELECT CUSTFILE ASSIGN TO AS-VISHNU  
     ORGANIZATION IS SEQUENTIAL           
     ACCESS MODE IS SEQUENTIAL            
     FILE STATUS IS FS1.                  
DATA DIVISION.                            
FILE SECTION.                             
FD CUSTFILE.                              
01 CUST-REC.                              
     05 CUST-ID PIC X(4).                 
     05 CUST-NAME PIC X(10).              
     05 CUST-ADDRESS PIC X(10).           
     05 FILLER PIC X(56).                 
WORKING-STORAGE SECTION.                  
  01 WS-EOF PIC X(3) VALUE  'NO'.         
  01 FS1 PIC 9(2).                        
PROCEDURE DIVISION.                       
A001-CUST-PARA.                           
    PERFORM 0001-OPEN-PARA.               
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'.
    PERFORM C001-CLOSE-PARA.                       
    STOP RUN.                                      
0001-OPEN-PARA.          
    OPEN INPUT CUSTFILE. 
P001-PROCESS-PARA.       
    READ CUSTFILE        
    AT END               
    MOVE 'YES' TO WS-EOF 
    NOT AT END           
    DISPLAY CUST-REC     
    END-READ.            
C001-CLOSE-PARA.         
    CLOSE CUSTFILE.  
RUN:
//RUN      EXEC PGM=FIHESDS1    MEMBER NAME       
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR
//SYSPRINT DD   SYSOUT=*                          
//VISHNU   DD   DSN=TECN93.COBOL.ESDSA,DISP=SHR   
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR     
//SYSOUT   DD   SYSOUT=*                          
//SYSIN    DD   DUMMY                                 
OUT PUT:
A001 RAKESHKUMAR 9987654329 ENGINEER     BANGALORE     
A002 ANIL        9987652222 SR.ARCHITECT CHENNAI       
A003 VIJAY       9287635439 ENGINEER     MYSORE        
A004 RAMAY       9966777884 EMPLOYE      HYDERABED     
A005 KRISHNA     9995556778 EMPLOYE      KARANATAKA    
A006 VIKAS       9998876534 SHOPKEPPER   BHARE         
A007 VARUN       5654345635 SHOPKEPPER   OSORE         
A008 VISHNU      1234566434 ITEMPLOY     MYHYD         
A009 RAMESH      9876431234 EMPLOYE      ANDRAPRADESHE 
4,0  11,6        10,18      12,29        13,42         
KSDS TO SPOOL -SEQUENTLAL READ
IDENTIFICATION DIVISION.              
PROGRAM-ID. FIHKSDS1.                 
ENVIRONMENT DIVISION.                 
INPUT-OUTPUT SECTION.                 
FILE-CONTROL.                         
     SELECT CUSTFILE ASSIGN TO VISHNU 
     ORGANIZATION IS INDEXED          
     ACCESS MODE IS SEQUENTIAL        
     RECORD KEY IS CUST-ID            
     FILE STATUS IS FS1.              
DATA DIVISION.                        
FILE SECTION.                         
FD CUSTFILE.                          
01 CUST-REC.                          
     05 CUST-ID PIC X(4).             
     05 CUST-NAME PIC X(10).          
     05 CUST-ADDRESS PIC X(10).       
     05 FILLER PIC X(56).             
WORKING-STORAGE SECTION.              
  01 WS-EOF PIC X(3) VALUE  'NO'.     
  01 FS1 PIC 9(2).                    
PROCEDURE DIVISION.                   
A001-CUST-PARA.      
    PERFORM 0001-OPEN-PARA.                         
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'. 
    PERFORM C001-CLOSE-PARA.                        
    STOP RUN.             
0001-OPEN-PARA.           
    OPEN INPUT CUSTFILE.  
P001-PROCESS-PARA.        
     READ CUSTFILE        
     AT END               
     MOVE 'YES' TO WS-EOF 
     NOT AT END           
     DISPLAY CUST-REC     
     END-READ.            
C001-CLOSE-PARA.          
     CLOSE CUSTFILE. 
RUN PGM
//RUN      EXEC PGM=FIHKSDS1            MEMBER NAME 
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR -
//SYSPRINT DD   SYSOUT=*                            
//VISHNU   DD   DSN=TECN93.COBOL.KSDSA,DISP=SHR     
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR       
//SYSOUT   DD   SYSOUT=*                            
//SYSIN    DD   DUMMY                               
OUT PUT:
A001 RAKESHKUMAR 9987654329 ENGINEER     BANGALORE     
A002 ANIL        9987652222 SR.ARCHITECT CHENNAI       
A003 VIJAY       9287635439 ENGINEER     MYSORE        
A004 RAMAY       9966777884 EMPLOYE      HYDERABED     
A005 KRISHNA     9995556778 EMPLOYE      KARANATAKA    
A006 VIKAS       9998876534 SHOPKEPPER   BHARE         
A007 VARUN       5654345635 SHOPKEPPER   OSORE         
A008 VISHNU      1234566434 ITEMPLOY     MYHYD         
A009 RAMESH      9876431234 EMPLOYE      ANDRAPRADESHE 
4,0  11,6        10,18      12,29        13,42                               
RRDS TO SPOOL-SEQUENTIAL READ
IDENTIFICATION DIVISION.              
PROGRAM-ID. FIHRRDS1.                 
ENVIRONMENT DIVISION.                 
INPUT-OUTPUT SECTION.                 
FILE-CONTROL.                         
     SELECT CUSTFILE ASSIGN TO VISHNU 
     ORGANIZATION IS RELATIVE         
     ACCESS MODE IS SEQUENTIAL        
     RELATIVE KEY IS RRN1             
     FILE STATUS IS FS1.              
DATA DIVISION.                        
FILE SECTION.                         
FD CUSTFILE.                          
01 CUST-REC.                          
     05 CUST-ID PIC X(4).             
     05 CUST-NAME PIC X(10).          
     05 CUST-ADDRESS PIC X(10).       
     05 FILLER PIC X(56).             
WORKING-STORAGE SECTION.              
  01 WS-EOF PIC X(3) VALUE  'NO'.     
  01 FS1 PIC 9(2).                    
  01 RRN1 PIC 9(2).                   
PROCEDURE DIVISION.             
A001-CUST-PARA.                                    
    PERFORM 0001-OPEN-PARA.                        
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'.
    PERFORM C001-CLOSE-PARA.   
    STOP RUN.                  
0001-OPEN-PARA.                
    OPEN INPUT CUSTFILE.       
P001-PROCESS-PARA.             
    READ CUSTFILE              
    AT END                     
    MOVE 'YES' TO WS-EOF       
    NOT AT END                 
    DISPLAY CUST-REC           
    END-READ.                  
C001-CLOSE-PARA.               
    CLOSE CUSTFILE.            
RUN PGM :
//RUN      EXEC PGM=FIHRRDS1                    
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SH
//SYSPRINT DD   SYSOUT=*                         
//VISHNU   DD   DSN=TECN93.COBOL.RRDSA,DISP=SHR  
OUT PUT:
 A001 RAKESHKUMAR 9987654329 ENGINEER     BANGALORE    
A002 ANIL        9987652222 SR.ARCHITECT CHENNAI      
A003 VIJAY       9287635439 ENGINEER     MYSORE       
A004 RAMAY       9966777884 EMPLOYE      HYDERABED    
A005 KRISHNA     9995556778 EMPLOYE      KARANATAKA   
A006 VIKAS       9998876534 SHOPKEPPER   BHARE        
A007 VARUN       5654345635 SHOPKEPPER   OSORE        
A008 VISHNU      1234566434 ITEMPLOY     MYHYD        
A009 RAMESH      9876431234 EMPLOYE      ANDRAPRADESHE
4,0  11,6        10,18      12,29        13,42        
     
PS TO SPOOL RANDOM READ ESDS
IDENTIFICATION DIVISION.              
PROGRAM-ID. PSREADES.                 
ENVIRONMENT DIVISION.                 
INPUT-OUTPUT SECTION.                 
FILE-CONTROL.                         
     SELECT INFILE ASSIGN TO AS-DD1   
     ORGANIZATION IS SEQUENTIAL       
     ACCESS MODE IS RANDOM            
     RECORD KEY IS ADDRESS            
     FILE STATUS IS FS.               
DATA DIVISION.                        
FILE SECTION.                         
FD INFILE.                            
01 INREC.                             
    05 FS-ID PIC X(4).                
    05 FILLER PIC X(3).               
    05 FS-NAME PIC A(10).             
    05 FILLER PIC X(68).              
WORKING-STORAGE SECTION.              
01 FS PIC 9(2).                       
01 WS-EOF PIC X(3) VALUE 'NO'.        
01 RBA PIC 9(2).                      
PROCEDURE DIVISION.            
     PERFORM OPEN-PARA.        
     PERFORM READ-PARA.        
     PERFORM CLOSE-PARA.       
     STOP RUN.                 
OPEN-PARA.                     
     OPEN INPUT INFILE.        
READ-PARA.                     
     MOVE '80' TO FS-ID.       
     READ INFILE               
     INVALID KEY               
     DISPLAY 'RECORD NOT FOUND'
     NOT INVALID KEY           
     DISPLAY INREC             
     END-READ.                 
CLOSE-PARA.                    
     CLOSE INFILE.             
OUT PUT:       
PS TO SPOOL -RANDOM READ KSDS.
IDENTIFICATION DIVISION.          
PROGRAM-ID. PSREADKS.             
ENVIRONMENT DIVISION.             
INPUT-OUTPUT SECTION.             
FILE-CONTROL.                     
     SELECT INFILE ASSIGN TO DD1  
     ORGANIZATION IS INDEXED      
     ACCESS MODE IS RANDOM        
     RECORD KEY IS FS-ID          
     FILE STATUS IS FS.           
DATA DIVISION.                    
FILE SECTION.                     
FD INFILE.                        
01 INREC.                         
  05 FS-ID PIC X(4).              
  05 FILLER PIC X.                
  05 FS-NAME PIC X(7).            
  05 FILLER PIC X(68).            
WORKING-STORAGE SECTION.          
01 FS PIC 9(2).                   
01 WS-EOF PIC X(3) VALUE 'NO'.    
PROCEDURE DIVISION.               
       PERFORM OPEN-PARA.  
      PERFORM READ-PARA.                                                                        PERFORM CLOSE-PARA.                                                                        PERFORM OPEN-PARA.
   STOP RUN.                                                                                                                                   //TECN93VV  JOB NOTIFY=&SYSUID                              
//*       CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),                
//JOBPROC   JCLLIB ORDER=IBMUSER.ALL1                       
//COBCL     EXEC IGYWCL,                                    
//          PGMLIB=TECN93.COBOL.LOADLIB2,   -->LOADLIB NAME 
//*         COPYLIB=IBMUSER.COPY.LIB,          -->COPYLIB NA
//          GOPGM=PSREADKS                                  
//COBOL.SYSIN DD  DSN=TECN93.COBOL.VISHNU3(&GOPGM),DISP=SHR 
//*KED.SYSLIB DD  DSN=TECN93.COBOL.LOADLIB1(CSPGM),DISP=SHR 
//
//RUN      EXEC PGM=PSREADKS                      
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR
//SYSPRINT DD   SYSOUT=*                          
//DD1      DD   DSN=TECN93.COBOL.KSDSA,DISP=SHR   
 ********************************* TOP OF DATA **********************************
A002 ANIL        9987652222 SR.ARCHITECT CHENNAI                        00000200  SPACE                                                                                                                            PS TO SPOOL RANDOM READ RRDS
IDENTIFICATION DIVISION.
PROGRAM-ID. RRAND.                 
ENVIRONMENT DIVISION.              
INPUT-OUTPUT SECTION.              
FILE-CONTROL.                      
     SELECT INFILE ASSIGN TO DD1   
     ORGANIZATION IS RELATIVE      
     ACCESS MODE IS RANDOM         
     RELATIVE KEY IS RRN1          
     FILE STATUS IS FS.            
DATA DIVISION.                     
FILE SECTION.                      
FD INFILE.                         
01 INREC.                          
  05 FS-ID PIC X(4).               
  05 FILLER PIC X.                 
  05 FS-NAME PIC A(7).             
  05 FILLER PIC X(68).             
WORKING-STORAGE SECTION.           
01 FS PIC 9(2).                    
01 WS-EOF PIC X(3) VALUE 'NO'.     
01 RRN1 PIC 9.                     
PROCEDURE DIVISION.                
   PERFORM OPEN-PARA. 
   PERFORM READ-PARA. 
   PERFORM CLOSE-PARA.
    STOP RUN.                 
OPEN-PARA.                    
    OPEN INPUT INFILE.        
READ-PARA.                    
    MOVE '3' TO RRN1.         
    READ INFILE               
    INVALID KEY               
    DISPLAY 'RECORD NOT FOUND'
    NOT INVALID KEY           
    DISPLAY INREC             
    END-READ.                 
CLOSE-PARA.                   
    CLOSE INFILE.             
//TECN93VV  JOB NOTIFY=&SYSUID                                        
//*       CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),                          
//JOBPROC   JCLLIB ORDER=IBMUSER.ALL1                                 
//COBCL     EXEC IGYWCL,                                              
//          PGMLIB=TECN93.COBOL.LOADLIB2,   -->LOADLIB NAME           
//*         COPYLIB=IBMUSER.COPY.LIB,          -->COPYLIB NAME        
//          GOPGM=PSREADRR                                   MBER NAME
//COBOL.SYSIN DD  DSN=TECN93.COBOL.VISHNU3(&GOPGM),DISP=SHR  -->SRC   
//*KED.SYSLIB DD  DSN=TECN93.COBOL.LOADLIB1(CSPGM),DISP=SHR -->CALL   
//                                                                    
//TECN93VV JOB  NOTIFY=&SYSUID                                
//*        CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),LINES=(1,CANCEL),
//RUN      EXEC PGM=PSREADRR                            MEMBER
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR --> LOADLIB
//SYSPRINT DD   SYSOUT=*                                      
//DD1      DD   DSN=TECN93.COBOL.RRDSA,DISP=SHR               
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR                 
//SYSOUT   DD   SYSOUT=*                                      
//SYSIN    DD   DUMMY                                         
/*                                                            
********************************* TOP OF DATA *
A003 VIJAY       9287635439 ENGINEER     MYSORE
******************************** BOTTOM OF DATA
PS TO PS -WRITE SEQUENTIAL
IDENTIFICATION DIVISION.              
PROGRAM-ID. FILEH2.                   
ENVIRONMENT DIVISION.                 
INPUT-OUTPUT SECTION.                 
FILE-CONTROL.                         
     SELECT INFILE ASSIGN TO INDD     
     ORGANIZATION IS SEQUENTIAL       
     ACCESS MODE IS SEQUENTIAL        
     FILE STATUS IS FS1.              
     SELECT OUTFILE ASSIGN TO OUTDD   
     ORGANIZATION IS SEQUENTIAL       
     ACCESS MODE IS SEQUENTIAL        
     FILE STATUS IS FS2.              
DATA DIVISION.                        
FILE SECTION.                         
FD INFILE.                            
01 IN-REC.                            
     05 IN-EMP-NAME PIC X(10).        
     05 IN-EMP-ID PIC X(4).           
     05 IN-EMP-SAL PIC 9(5).          
     05 FILLER PIC X(61).             
FD OUTFILE.                           
01 OUT-REC.  
      05 OUT-EMP-NAME PIC X(10). 
      05 OUT-EMP-ID PIC X(4).    
      05 OUT-EMP-SAL PIC 9(5).   
      05 FILLER PIC X(61).
WORKING-STORAGE SECTION.                              
  01 WS-EOF PIC X(3) VALUE  'NO'.                     
  01 FS1 PIC 9(2).                                    
  01 FS2 PIC 9(2).                                    
PROCEDURE DIVISION.                                   
A001-EMP-PARA.                                        
    PERFORM 0001-OPEN-PARA.                           
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'.   
    PERFORM C001-CLOSE-PARA.                          
    STOP RUN.                                         
0001-OPEN-PARA.                                       
    OPEN INPUT INFILE.                                
    OPEN OUTPUT OUTFILE.                              
P001-PROCESS-PARA.                                    
    READ INFILE                                       
        AT END                                        
        MOVE 'YES' TO WS-EOF                          
        NOT AT END                                    
        MOVE IN-REC TO OUT-REC                        
        WRITE OUT-REC                                 
        END-READ.    
C001-CLOSE-PARA.     
       CLOSE INFILE. 
       CLOSE OUTFILE.
RUN PGM=
 //RUN      EXEC PGM=PSWRKSDS                   MEM
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR
//SYSPRINT DD   SYSOUT=*                          
//INDD     DD   DSN=TECN93.COBOL.PS2,DISP=SHR     
//OUTDD    DD   DSN=TECN93.COBOL.PS3SC,DISP=SHR   
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR     
//SYSOUT   DD   SYSOUT=*                          
//SYSIN    DD   DUMMY                             
OUT PUT:
A001 RAKESHKUM 20000 
A002 ANIL      10000 
A003 VIJAY     15000 
A004 RAMAY     16000 
A005 KRISHNA   18000 
A006 VIKAS     19000 
A007 VARUN     20000 
A008 VISHNU    23000 
A009 RAMESH    23456 
4,0  9,5       11,5  
IDENTIFICATION DIVISION.              
PROGRAM-ID. PSWRKSDS.                   
ENVIRONMENT DIVISION.                 
INPUT-OUTPUT SECTION.                 
FILE-CONTROL.                         
     SELECT INFILE ASSIGN TO INDD     
     ORGANIZATION IS SEQUENTIAL       
     ACCESS MODE IS SEQUENTIAL        
     FILE STATUS IS FS1.              
     SELECT OUTFILE ASSIGN TO OUTDD   
     ORGANIZATION IS SEQUENTIAL       
     ACCESS MODE IS SEQUENTIAL        
     FILE STATUS IS FS2.              
DATA DIVISION.                        
FILE SECTION.                         
FD INFILE.                            
01 IN-REC.                            
     05 IN-EMP-NAME PIC X(10).        
     05 IN-EMP-ID PIC X(4).           
     05 IN-EMP-SAL PIC 9(5).          
     05 FILLER PIC X(61).             
FD OUTFILE.                           
01 OUT-REC.  
      05 OUT-EMP-NAME PIC X(10). 
      05 OUT-EMP-ID PIC X(4).    
      05 OUT-EMP-SAL PIC 9(5).   
      05 FILLER PIC X(61).
WORKING-STORAGE SECTION.                              
  01 WS-EOF PIC X(3) VALUE  'NO'.                     
  01 FS1 PIC 9(2).                                    
  01 FS2 PIC 9(2).                                    
PROCEDURE DIVISION.                                   
A001-EMP-PARA.                                        
    PERFORM 0001-OPEN-PARA.                           
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'.   
    PERFORM C001-CLOSE-PARA.                          
    STOP RUN.                                         
0001-OPEN-PARA.                                       
    OPEN INPUT INFILE.                                
    OPEN OUTPUT OUTFILE.                              
P001-PROCESS-PARA.                                    
    READ INFILE                                       
        AT END                                        
        MOVE 'YES' TO WS-EOF                          
        NOT AT END                                    
        MOVE IN-REC TO OUT-REC                        
        WRITE OUT-REC                                 
        END-READ.    
C001-CLOSE-PARA.     
       CLOSE INFILE. 
       CLOSE OUTFILE.
//RUN      EXEC PGM=PSWRKSDS                   MEM
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR
//SYSPRINT DD   SYSOUT=*                          
//INDD     DD   DSN=TECN93.COBOL.PS3,DISP=SHR     
//OUTDD    DD   DSN=TECN93.COBOL.KSDSC,DISP=SHR   
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR     
//SYSOUT   DD   SYSOUT=*                          
//SYSIN    DD   DUMMY                             
OUT PUT:
NOT GOT
PS TO ESDS -WRITE SEQUENTIAL
IDENTIFICATION DIVISION.                  
PROGRAM-ID. PSWRESDS                      
ENVIRONMENT DIVISION.                     
INPUT-OUTPUT SECTION.                     
FILE-CONTROL.                             
     SELECT INFILE ASSIGN TO INDD         
     ORGANIZATION IS SEQUENTIAL           
     ACCESS MODE IS SEQUENTIAL            
     FILE STATUS IS FS1.                  
     SELECT OUTFILE ASSIGN TO AS-OUTDD    
     ORGANIZATION IS INDEXED              
     ACCESS MODE IS SEQUENTIAL            
     FILE STATUS IS FS2.                  
DATA DIVISION.                            
FILE SECTION.                             
FD INFILE.                                
01 IN-REC.                                
     05 IN-EMP-ID PIC X(4).               
     05 IN-EMP-NAME PIC X(10).            
     05 IN-EMP-SAL PIC 9(5).              
     05 FILLER PIC X(61).                 
FD OUTFILE.                               
01 OUT-REC.                               
01 OUT-REC.                    
     05 OUT-EMP-ID PIC X(4).   
     05 OUT-EMP-NAME PIC X(10).
     05 OUT-EMP-SAL PIC 9(5).  
     05 FILLER PIC X(61).                            
WORKING-STORAGE SECTION.                             
  01 WS-EOF PIC X(3) VALUE  'NO'.                    
  01 FS1 PIC 9(2).                                   
  01 FS2 PIC 9(2).                                   
PROCEDURE DIVISION.                                  
A001-EMP-PARA.                                       
    PERFORM 0001-OPEN-PARA.                          
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'.  
    PERFORM C001-CLOSE-PARA.                         
    STOP RUN.                                        
0001-OPEN-PARA.                                      
    OPEN INPUT INFILE.                               
    OPEN OUTPUT OUTFILE.                             
P001-PROCESS-PARA.                                   
        READ INFILE                                  
        AT END                                       
        MOVE 'YES' TO WS-EOF                         
        NOT AT END                                   
        MOVE IN-REC TO OUT-REC                       
        WRITE OUT-REC                                
        END-READ.                                    
           C001-CLOSE-PARA.       
         CLOSE INFILE.  
         CLOSE OUTFILE.
OUT NOT GOT:
PS TO RRDS WRITE SEQUENTIAL
IDENTIFICATION DIVISION.                
PROGRAM-ID. PSWRRRDS                    
ENVIRONMENT DIVISION.                   
INPUT-OUTPUT SECTION.                   
FILE-CONTROL.                           
     SELECT INFILE ASSIGN TO INDD       
     ORGANIZATION IS SEQUENTIAL         
     ACCESS MODE IS SEQUENTIAL          
     FILE STATUS IS FS1.                
     SELECT OUTFILE ASSIGN TO OUTDD     
     ORGANIZATION IS RELATIVE           
     ACCESS MODE IS SEQUENTIAL          
     RELATIVE KEY IS RRN1               
     FILE STATUS IS FS2.                
DATA DIVISION.                          
FILE SECTION.                           
FD INFILE.                              
01 IN-REC.                              
     05 IN-EMP-ID PIC X(4).             
     05 IN-EMP-NAME PIC X(10).          
     05 IN-EMP-SAL PIC 9(5).            
     05 FILLER PIC X(61).               
FD OUTFILE.                             
01 OUT-REC.                     
     05 OUT-EMP-ID PIC X(4).    
     05 OUT-EMP-NAME PIC X(10).
     05 OUT-EMP-SAL PIC 9(5).                     
     05 FILLER PIC X(61).                         
WORKING-STORAGE SECTION.                          
  01 WS-EOF PIC X(3) VALUE  'NO'.                 
  01 FS1 PIC 9(2).                                
  01 FS2 PIC 9(2).                                
  01 RRN1 PIC 9(2).                               
PROCEDURE DIVISION.                               
A001-EMP-PARA.                                    
    PERFORM 0001-OPEN-PARA.                       
    PERFORM P001-PROCESS-PARA UNTIL WS-EOF = 'YES'
    PERFORM C001-CLOSE-PARA.                      
    STOP RUN.                                     
0001-OPEN-PARA.                                   
    OPEN INPUT INFILE.                            
    OPEN OUTPUT OUTFILE.                          
P001-PROCESS-PARA.                                
        READ INFILE                               
        AT END                                    
        MOVE 'YES' TO WS-EOF                      
        NOT AT END                                
        MOVE IN-REC TO OUT-REC                    
        WRITE OUT-REC                             
        END-READ.      
C001-CLOSE-PARA.       
        CLOSE INFILE.  
        CLOSE OUTFILE.
RUN PGM=
//RUN      EXEC PGM=PSWRRRDS                MEMBER
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR
//SYSPRINT DD   SYSOUT=*                          
//INDD     DD   DSN=TECN93.COBOL.PS2,DISP=SHR     
//OUTDD    DD   DSN=TECN93.COBOL.RRDSB,DISP=SHR   
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR     
//SYSOUT   DD   SYSOUT=*                          
//SYSIN    DD   DUMMY                             
OUT PUT=
RELATIVE RECORD NUMBER - 1 
 A001 RAKESHKUM 20000       
0                        
RELATIVE RECORD NUMBER - 2                 
 A002 ANIL      10000                       
0                                           
 RELATIVE RECORD NUMBER - 3                 
 A003 VIJAY     15000                       
0                                           
 RELATIVE RECORD NUMBER - 4                 
 A004 RAMAY     16000                       
0                                           
 RELATIVE RECORD NUMBER - 5                 
 A005 KRISHNA   18000                       
0                                           
 RELATIVE RECORD NUMBER - 6                 
 A006 VIKAS     19000                       
0                                           
 RELATIVE RECORD NUMBER - 7                 
 A007 VARUN     20000                       
0                                           
 RELATIVE RECORD NUMBER - 8                 
 A008 VISHNU    23000                       
0                                           
 RELATIVE RECORD NUMBER - 9                 
 A009 RAMESH    23456                       
0                                           
 RELATIVE RECORD NUMBER - 10                
 4,0  9,5       11,5                        
0                                           
 IDC0005I NUMBER OF RECORDS PROCESSED WAS 10
 ***
DELETE :
IDENTIFICATION DIVISION.               
PROGRAM-ID. DELTE.                     
ENVIRONMENT DIVISION.                  
INPUT-OUTPUT SECTION.                  
FILE-CONTROL.                          
     SELECT INFILE ASSIGN TO INDD      
     ORGANIZATION IS INDEXED           
     ACCESS MODE IS RANDOM             
     RECORD KEY IS EMP-ID              
     FILE STATUS IS FS.                
DATA DIVISION.                         
FILE SECTION.                          
FD INFILE.                             
01 INREC.                              
  05 EMP-ID PIC X(4).                  
  05 EMP-NM PIC X(10).                 
  05 FS-SAL PIC X(5).                  
  05 FILLER PIC X(6).                  
WORKING-STORAGE SECTION.               
01 FS PIC 9(2).                        
01 EOF PIC X VALUE 'Y'.                
PROCEDURE DIVISION.                    
    OPEN I-O INFILE.                   
    MOVE 'A006' TO EMP-ID.
    PERFORM DELETE-PARA.  
    CLOSE INFILE.         
    STOP RUN.                                  
DELETE-PARA.                                   
    READ INFILE KEY IS EMP-ID                  
    INVALID KEY DISPLAY 'INVALID KEY'          
    NOT INVALID KEY DISPLAY 'KEY MATCHED'      
    DELETE INFILE RECORD                       
    INVALID KEY DISPLAY 'RECORED NOT DELETED'  
    NOT INVALID KEY DISPLAY 'RECORD DELETED'   
    END-DELETE                                 
    END-READ.                                  
OUT PUT OF RUN KSDS FILE

KEY OF RECORD - A001   
 A001 RAKESHKUM 20000   
0                       
 ***                    
KEY OF RECORD - A002   
 A002 ANIL      10000   
0                       
 KEY OF RECORD - A003   
 A003 VIJAY     15000   
0                       
 KEY OF RECORD - A004   
 A004 RAMAY     16000   
0                       
 KEY OF RECORD - A005   
 A005 KRISHNA   18000   
0                       
 KEY OF RECORD - A006   
 A006 VIKAS     19000   
0                       
 KEY OF RECORD - A007   
 A007 VARUN     20000   
0                       
 KEY OF RECORD - A008   
 A008 VISHNU    23000   
0                       
 KEY OF RECORD - A009   
 A009 RAMESH    23456   
0                       
 KEY OF RECORD - 4,0    
 4,0  9,5       11,5    
0                       
RE WRIT:KSDS FILE
IDENTIFICATION DIVISION.            
PROGRAM-ID. REWRIT.                 
ENVIRONMENT DIVISION.               
INPUT-OUTPUT SECTION.               
FILE-CONTROL.                       
     SELECT INFILE ASSIGN TO INDD   
     ORGANIZATION IS INDEXED        
     ACCESS MODE IS RANDOM          
     RECORD KEY IS EMP-ID           
     FILE STATUS IS FS.             
DATA DIVISION.                      
FILE SECTION.                       
FD INFILE.                          
01 IN-REC.                          
  05 EMP-ID PIC X(4).               
  05 EMP-NM PIC A(10).              
  05 EMP-SAL PIC X(5).              
  05 FILLER PIC X(6).               
WORKING-STORAGE SECTION.            
01 FS PIC X(2).                     
01 EOF PIC X VALUE 'Y'.             
PROCEDURE DIVISION.                 
    OPEN I-O INFILE.                
    MOVE 'A006' TO EMP-ID.  
    MOVE 'FAIZAL' TO EMP-NM.
    MOVE '20000' TO EMP-SAL.
REWRITE IN-REC INVALID KEY DISPLAY 'NOT DONE'.  
CLOSE INFILE.                                   
STOP RUN.                                       
OUT PUT
KEY OF RECORD - A001  
 A001 RAKESHKUM 20000  
0                      
 ***                   
KEY OF RECORD - A002                       
 A002 ANIL      10000                       
0                                           
 KEY OF RECORD - A003                       
 A003 VIJAY     15000                       
0                                           
 KEY OF RECORD - A004                       
 A004 RAMAY     16000                       
0                                           
 KEY OF RECORD - A005                       
 A005 KRISHNA   18000                       
0                                           
 KEY OF RECORD - A006                       
 A006FAIZAL    20000......                  
 KEY OF RECORD - A007                       
 A007 VARUN     20000                       
0                                           
 KEY OF RECORD - A008                       
 A008 VISHNU    23000                       
0                                           
 KEY OF RECORD - A009                       
 A009 RAMESH    23456                       
0                                           
 KEY OF RECORD - 4,0                        
 4,0  9,5       11,5                        
0                                           
 IDC0005I NUMBER OF RECORDS PROCESSED WAS 10
 *** 
ODD OR EVEN
IDENTIFICATION DIVISION.                   
PROGRAM-ID. EVEN.                          
ENVIRONMENT DIVISION.                      
INPUT-OUTPUT SECTION.                      
FILE-CONTROL.                              
     SELECT INFILE ASSIGN TO DD1           
     ORGANIZATION IS SEQUENTIAL            
     ACCESS MODE IS SEQUENTIAL             
     FILE STATUS IS FS1.                   
DATA DIVISION.                             
FILE SECTION.                              
FD INFILE.                                 
01 IN-REC.                                 
   05 SANJU PIC 9(2).                      
   05 FILLER PIC X(78).                    
WORKING-STORAGE SECTION.                   
01 FS1 PIC 9(2).                           
01 QUO PIC 9(2).                           
01 REM PIC 9(2).                           
01 WS-EOF PIC X(3) VALUE 'NO'.             
PROCEDURE DIVISION.                        
    PERFORM OPEN-PARA.                     
    PERFORM READ-PARA UNTIL WS-EOF = 'YES'.
    PERFORM CLOSE-PARA.  
    STOP RUN.            
OPEN-PARA.               
    OPEN INPUT INFILE.                         
READ-PARA.                                     
    READ INFILE                                
    AT END                                     
    MOVE 'YES' TO WS-EOF                       
    NOT AT END                                 
    DIVIDE SANJU BY 2 GIVING QUO REMAINDER REM 
    IF REM EQUAL TO 0                          
    DISPLAY 'SANJU' SANJU                      
    ELSE                                       
    DISPLAY 'ODD'                              
    END-IF.                                    
CLOSE-PARA.                                    
    CLOSE INFILE.                              
OUT PUT 
ODD
ODD
ODD
ODD
ODD
IDENTIFICATION DIVISION.                    
PROGRAM-ID. EVEN.                           
ENVIRONMENT DIVISION.                       
INPUT-OUTPUT SECTION.                       
FILE-CONTROL.                               
     SELECT INFILE ASSIGN TO DD1            
     ORGANIZATION IS SEQUENTIAL             
     ACCESS MODE IS SEQUENTIAL              
     FILE STATUS IS FS1.                    
DATA DIVISION.                              
FILE SECTION.                               
FD INFILE.                                  
01 IN-REC.                                  
   05 SANJU PIC 9(2).                       
   05 FILLER PIC X(64).                     
WORKING-STORAGE SECTION.                    
01 FS1 PIC 9(2).                            
01 QUO PIC 9(2).                            
01 REM PIC 9(2).                            
01 WS-EOF PIC X(3) VALUE 'NO'.              
PROCEDURE DIVISION.                         
    PERFORM OPEN-PARA.                      
    PERFORM READ-PARA UNTIL WS-EOF = 'YES'.
    PERFORM CLOSE-PARA. 
    STOP RUN.           
OPEN-PARA.              
    OPEN INPUT INFILE.                           
READ-PARA.                                       
    READ INFILE                                  
    AT END                                       
    MOVE 'YES' TO WS-EOF                         
    NOT AT END                                   
    DIVIDE SANJU BY 2 GIVING QUO REMAINDER REM   
    IF REM EQUAL TO 0                            
    DISPLAY 'SANJU' SANJU                        
    ELSE                                         
    DISPLAY 'ODD'                                
    END-IF.                                      
CLOSE-PARA.                                      
    CLOSE INFILE.                                
OUT PUT NOT DEFINE

IDENTIFICATION DIVISION.               
PROGRAM-ID. SORT1.                     
ENVIRONMENT DIVISION.                  
INPUT-OUTPUT SECTION.                  
FILE-CONTROL.                          
     SELECT INFILE ASSIGN TO SORTIN    
     ORGANIZATION IS SEQUENTIAL        
     ACCESS IS SEQUENTIAL              
     FILE STATUS IS FS1.               
     SELECT OUTFILE ASSIGN TO SORTOUT  
     ORGANIZATION IS SEQUENTIAL        
     ACCESS IS SEQUENTIAL              
     FILE STATUS IS FS2.               
     SELECT WKFILE ASSIGN TO DD.       
DATA DIVISION.                         
FILE SECTION.                          
FD INFILE.                             
01 INREC.                              
  05 INEMP-ID PIC 9(4).                
  05 FILLER PIC X(2).                  
  05 INEMP-NM PIC X(10).               
  05 FILLER PIC X(2).                  
  05 INEMP-SAL PIC X(5).               
  05 FILLER PIC X(57).                      
FD OUTFILE.                                 
01 OUTREC.                                  
   05 OUT-EMPID PIC 9(4).                   
   05 FILLER PIC X(2).                      
   05 OUT-EMPNM PIC X(10).                  
   05 FILLER PIC X(2).                      
   05 OUT-SAL PIC 9(5).                     
   05 FILLER PIC X(57).                     
SD WKFILE.                                  
01 WK-REC.                                  
   05 WK-EMPID PIC 9(4).                    
   05 FILLER PIC X(2).                      
   05 WK-EMPNM PIC X(10).                   
   05 FILLER PIC X(2).                      
   05 WK-SAL PIC 9(5).                      
   05 FILLER PIC X(57).                     
WORKING-STORAGE SECTION.                    
01 FS1 PIC X(2).                            
01 FS2 PIC X(2).                            
PROCEDURE DIVISION.                         
    SORT WKFILE ON ASCENDING KEY WK-EMPID   
      USING INFILE GIVING OUTFILE.          
    STOP RUN.                               
RUN PGM:
//TECN93VV JOB  NOTIFY=&SYSUID                                        
//*        CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),LINES=(1,CANCEL),        
//RUN      EXEC PGM=SORT1                MEMBER NAME                  
//STEPLIB  DD   DSN=TECN93.COBOL.LOADLIB2,DISP=SHR --> LOADLIB NAME   
//SYSPRINT DD   SYSOUT=*                                              
//SORTIN   DD   DSN=TECN93.COBOL.PS6,DISP=SHR                         
//DD       DD   DSN=&&TEMP                                            
//SORTOUT  DD   DSN=TECN93.COBOL.PS7,DISP=SHR                         
//*UTDD    DD   DSN=TECN54.COBOL.PS1,DISP=SHR                         
//SYSOUT   DD   SYSOUT=*                                              
//SYSIN    DD   *                                                     
     SORT FILEDS=(1,4,CH,A)                                           
/*                                                                    
INPUT FILE PS7
1004 RAMRAJ 50000 
1002 SURESH 10000 
1001 IMRAN  25000 
1003 KHOLI  90000
OUT PUT:
1001 IMRAN  25000
1002 SURESH 10000
1003 KHOLI  90000
1004 RAMRAJ 50000

                                                                                                                                        
