
EDIT       TECN93.COBOL.VISHNPDS(HELLO) - 01.02            Columns 00001 00072 
=COLS> ----+----1----+----2----+----3----+----4----+----5----+----6----+----7--
****** ***************************** Top of Data ******************************
000100 000100 IDENTIFICATION DIVISION.                                         
000200 000200 PROGRAM-ID. HELLO.                                               
000300 000300 DATA DIVISION.                                                   
000400 000400 PROCEDURE DIVISION.                                              
000500 000500      DISPLAY "*************************************".            
000600 000600      DISPLAY "***COMMON BUSINESS ORIENTED LANGUAGE*".            
000700 000700      DISPLAY "*********WELCOMES YOU****************".            
000800 000800      DISPLAY "*********CREATED BY VISHNU VARDHAN***".            
000900 000900      DISPLAY "*************************************".            
001000 001000      DISPLAY "*************************************".            
001100 001100      DISPLAY "*************************************".            
001200             STOP RUN.                                                   
****** **************************** Bottom of Data ****************************
COMPLING PGM=
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV  JOB NOTIFY=&SYSUID                                          
000200 //*       CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),                            
000300 //JOBPROC   JCLLIB ORDER=IBMUSER.ALL1                                   
000400 //COBCL     EXEC IGYWCL,                                                
000500 //          PGMLIB=TECN93.VISHNU.LOADLIB1,   -->LOADLIB NAME            
000600 //*         COPYLIB=IBMUSER.COPY.LIB,          -->COPYLIB NAME          
000700 //          GOPGM=HELLO          -->MEMBER NAME                         
000800 //COBOL.SYSIN DD  DSN=TECN93.COBOL.VISHNPDS(&GOPGM),DISP=SHR  -->SRC    
000900 //*KED.SYSLIB DD  DSN=TECN54.RAHUL.LOADLIB7(CSUBPGM),DISP=SHR -->CALL   
001000 //                                                                      
****** **************************** Bottom of Data ****************************
RUN PGM:
EDIT       TECN93.COBOL.VISHNPDS(COBRUN) - 01.99           Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //*        CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),LINES=(1,CANCEL),          
000400 //RUN      EXEC PGM=DIVI     -> MEMBER NAME                             
000500 //STEPLIB  DD    DSN=TECN93.VISHNU.LOADLIB1,DISP=SHR --> LOADLIB NAME   
000600 //SYSPRINT DD    SYSOUT=*                                               
000800 //*NDD     DD   DSN=TECN54.RAHUL.INPS,DISP=SHR                          
000900 //*UTDD    DD   DSN=TECN54.RAHUL.OUTPS,DISP=SHR                         
000910 //*YSOUT   DD   SYSOUT=*                                                
001000 //SYSIN    DD   DUMMY                                                   
001300 /*                                                                      
****** **************************** Bottom of Data ****************************
OUT PUT:
 SDSF OUTPUT DISPLAY TECN93VV JOB04557  DSID   102 LINE 0       COLUMNS 02- 81  
 COMMAND INPUT ===>                                            SCROLL ===> PAGE 
********************************* TOP OF DATA **********************************
*************************************                                           
***COMMON BUSINESS ORIENTED LANGUAGE*                                           
*********WELCOMES YOU****************                                           
*********CREATED BY VISHNU VARDHAN***                                           
*************************************                                           
*************************************                                           
*************************************                                           
******************************** BOTTOM OF DATA ********************************

LOADLIB OUT PUT:
 -------------------------------------------------------------------------------
 BROWSE    TECN93.VISHNU.LOADLIB1(HELLO)                     Browse substituted 
********************************* Top of Data **********************************
.Ø.....0HELLO   ........IGZCBSO .......ØCEESTART...Ç...^CEEBETBL... ....CEESG005
.Ø.....0CEEROOTD......  IGZEOPT ......  IGZETUN ......  CEEINT  ...&....CEEARLU 
.Ø.....^CEESG006......  CEESG007......  CEESG008......  CEESG009......  CEESG010
Ø³..............................................................................
Ø..5695PMB01 .......è|                                                          
ØÌ.Ø..5655S7100  ......Ø..569623400 ....€PL/X-390  ....€........Ø..569623400 ...
Ø.h....€.RSI80792818....€.RSI80792684                                           
............ .......                                                            
å00..CEE...^....å00.qóÐ....¶............°Ö}. .0.qÕ0<...................Þ........
.......è....................... ...à...ç...<...è...F...­...O...................ú
............ .......                                                            
.<K....ìP..d.d&°.*.Jì{°Y..&}}ììµ{.°Ö}.K.}hµ. .J.&.}ðŸ.jÇì^{.åØ^[ì.°*ì0.4 .~?.Õ!.
....................................                                            
...........  ..Y...Y                                                            
.V...........................................Y.Ú.Ú.............Ú................
...........................â...ã...¢...¦                                        
............ ..0...........^                                                    
S005...............................ç...Y....... .......}........å...å...°Ö}...å0
.......È............æ..à.......ç.......<....æ..&.......è.......*....æ..-.......Ø
............ .......                                                            
å00..CEE........å00...................N..Ÿ. N.}.©ÖåØ^%N.}.©4åØ^«N.}.©0åØ^uN.}.©Y
.......................-...@...Ð....                                            
............ ..-...-                                                            
ì0}4nO0.åØ·ã °..K.}8©Q \..&°}u&\}Ð(\©.oØ}0 °}©..& °.o.°.oØ°.&&°.ì\©Ü&\°.ì\©8&\°.
.......................^.......À.......-....................æ.......æ...        


ADD1
       IDENTIFICATION DIVISION.                                     
       PROGRAM-ID ADD1.                                             
       ENVIRONMENT DIVISION.                                        
       DATA DIVISION.                                               
       WORKING-STORAGE SECTION.                                     
       01 WS-A PIC 9(2) VALUE 30.                                   
       01 WS-B PIC 9(2) VALUE 40.                                   
       01 WS-C PIC 9(2).                                            
       PROCEDURE DIVISION.                                          
            COMPUTE WS-C = WS-A + WS-B.                             
            DISPLAY "**************************************".       
            DISPLAY '**ADDITON OF A AND B IS:' WS-C.                
            DISPLAY "************************************".         
            STOP RUN.                                               

OUT PUT********************************* TOP OF DATA **************
**************************************                      
**ADDITON OF A AND B IS:70                                  
************************************                        
******************************** BOTTOM OF DATA ************
SUB1:
        IDENTIFICATION DIVISION.                          
        PROGRAM-ID. SUB1.                                 
        ENVIRONMENT DIVISION.                             
        DATA DIVISION.                                    
        WORKING-STORAGE SECTION.                          
        01 WS-A PIC 9(2) VALUE 30.                        
        01 WS-B PIC 9(2) VALUE 40.                        
        01 WS-C PIC 9(2).                                 
        PROCEDURE DIVISION.                               
             COMPUTE WS-C = WS-B - WS-A.                  
             DISPLAY "*****************************".     
             DISPLAY 'SUBTRACTION OF A AND B IS:' WS-C.   
             DISPLAY "*****************************".     
             STOP RUN.                                    
OUT PUT:
********************************* TOP OF DATA ***********
*****************************                            
SUBTRACTION OF A AND B IS:10                             
*****************************                            
******************************** BOTTOM OF DATA *********

MULT 
        IDENTIFICATION DIVISION.                               
        PROGRAM-ID. MULT                                       
        ENVIRONMENT DIVISION.                                  
        DATA DIVISION.                                         
        WORKING-STORAGE SECTION.                               
        01 WS-A PIC 9(2) VALUE 30.                             
        01 WS-B PIC 9(2) VALUE 40.                             
        01 WS-C PIC 9(4).                                      
        PROCEDURE DIVISION.                                    
             COMPUTE WS-C = WS-A * WS-B.                       
             DISPLAY "*****************************".          
             DISPLAY 'MULTIPLICATION OF A AND B IS:' WS-C.     
             DISPLAY "*****************************".          
             STOP RUN.                                         
OUT PUT:
********************************* TOP OF DATA ****
*****************************                     
MULTIPLICATION OF A AND B IS:1200                 
*****************************                     
******************************** BOTTOM OF DATA **

DIVI
        IDENTIFICATION DIVISION.                          
        PROGRAM-ID. DIVI.                                 
        ENVIRONMENT DIVISION.                             
        DATA DIVISION.                                    
        WORKING-STORAGE SECTION.                          
        01 WS-A PIC 9(2) VALUE 30.                        
        01 WS-B PIC 9(2) VALUE 10.                        
        01 WS-C PIC 9(2).                                 
        PROCEDURE DIVISION.                               
             COMPUTE WS-C = WS-A / WS-B.                  
             DISPLAY "*****************************".     
             DISPLAY 'DIVISION OF A AND B IS:' WS-C.      
             DISPLAY "*****************************".     
             STOP RUN.                                    
OUT PUT:
********************************* TOP OF DATA ****
*****************************                     
DIVISION OF A AND B IS:03                         
*****************************                     
******************************** BOTTOM OF DATA **


IDENTIFICATION DIVISION.                                
PROGRAM-ID. ADD2.                                       
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 A PIC S9(3) VALUE 100.                               
PROCEDURE DIVISION.                                     
     ADD 27 TO A.                                       
     DISPLAY "***************************************". 
     DISPLAY A.                                         
     DISPLAY "****************************".            
     STOP RUN.                                          

OUT PUT:
********************************* TOP OF DATA ****
***************************************           
127                                               
****************************                      
******************************** BOTTOM OF DATA **

IDENTIFICATION DIVISION.                                
PROGRAM-ID. ADD2.                                       
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 A PIC 9(2) VALUE 23.                                 
01 B PIC 9(2) VALUE 34.                                 
PROCEDURE DIVISION.                                     
     ADD  A TO B.                                       
     DISPLAY "***************************************". 
     DISPLAY B.                                         
     DISPLAY "****************************".            
     STOP RUN.                                          
OUT PUT:
****************************
****************************
57                          
****************************
****************************

IDENTIFICATION  DIVISION.                              
PROGRAM-ID. ADD4.                                      
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 A PIC 9(2) VALUE 23.                                
01 B PIC 9(2) VALUE 34.                                
01 C PIC 9(2).                                         
PROCEDURE DIVISION.                                    
    ADD  A TO B GIVING C.                              
    DISPLAY "***************************************". 
    DISPLAY C.                                         
    DISPLAY "****************************".            
    STOP RUN.                                          
OUT PUT:
*****************
*****************
57               
*****************
*****************

IDENTIFICATION  DIVISION.                                     
PROGRAM-ID. ADD5.                                             
ENVIRONMENT DIVISION.                                         
DATA DIVISION.                                                
WORKING-STORAGE SECTION.                                      
01 A PIC 9(2) VALUE 23.                                       
01 B PIC 9(2) VALUE 34.                                       
01 C PIC 9(2).                                                
PROCEDURE DIVISION.                                           
    ADD A , B , 6 TO C.                                       
    DISPLAY "***************************************".        
    DISPLAY C.                                                
    DISPLAY "****************************".                   
    STOP RUN.                                                 
OUT PUT:
************
************
63          
************
************

IDENTIFICATION  DIVISION.                         
PROGRAM-ID. ADD5.                                 
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 A PIC 9(2) VALUE 23.                           
01 B PIC 9(2) VALUE 34.                           
01 C PIC 9(2).                                    
01 D PIC 9(2).                                    
PROCEDURE DIVISION.                               
    ADD A , B , 6 TO C GIVING D.                  
    DISPLAY "*************************************
    DISPLAY D.                                    
    DISPLAY "****************************".       
    STOP RUN.                                     
OUT PUT:
*******************
*******************
63                 
*******************
*******************

IDENTIFICATION  DIVISION.                              
PROGRAM-ID. ADD7.                                      
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 A PIC 9(2) VALUE 23.                                
01 B PIC 9(2) VALUE 34.                                
01 C PIC 9(2) VALUE 50.                                
01 D PIC 9(4) VALUE 50.                                
PROCEDURE DIVISION.                                    
    ADD A , B , TO C , D.                              
    DISPLAY "***************************************". 
    DISPLAY D.                                         
    DISPLAY "****************************".            
    STOP RUN.                                          
OUTPUT:
*****************
*****************
0107             
*****************
*****************

IDENTIFICATION  DIVISION.                             
PROGRAM-ID. ADD7.                                     
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 A PIC 9(2) VALUE 23.                               
01 B PIC 9(2) VALUE 34.                               
01 C PIC 9(2) VALUE 50.                               
01 D PIC 9(4) VALUE 50.                               
01 E PIC 9(4).                                        
PROCEDURE DIVISION.                                   
    ADD A , B , TO C , D GIVING E.                    
    DISPLAY "***************************************".
    DISPLAY E.                                        
    DISPLAY "****************************".           
    STOP RUN.                                         

OUT PUT:
MAX=12
?
IDENTIFICATION DIVISION.                      
PROGRAM-ID. SUB2.                             
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 A PIC 9(2) VALUE 30.                       
PROCEDURE DIVISION.                           
     SUBTRACT 10 FROM A.                      
     DISPLAY "*****************************". 
     DISPLAY 'SUBTRACTION OF A AND B IS:' A.  
     DISPLAY "*****************************". 
     STOP RUN.                                

OUT PUT:
*******************************
*****************************  
SUBTRACTION OF A AND B IS:20   
*****************************  
*******************************
IDENTIFICATION DIVISION.                         
PROGRAM-ID. SUB1.                                
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 A PIC 9(2) VALUE 30.                          
01 B PIC 9(2) VALUE 40.                          
PROCEDURE DIVISION.                              
     SUBTRACT A FROM B.                          
     DISPLAY "*****************************".    
     DISPLAY 'SUBTRACTION OF A AND B IS:' B.     
     DISPLAY "*****************************".    
     STOP RUN.                                   
 
OUTPUT:
*****************************
*****************************
SUBTRACTION OF A AND B IS:10 
*****************************
*****************************  

IDENTIFICATION DIVISION.                     
PROGRAM-ID. SUB4.                            
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 A PIC 9(2) VALUE 30.                      
01 B PIC 9(2) VALUE 40.                      
01 C PIC 9(2).                               
PROCEDURE DIVISION.                          
     SUBTRACT A FROM B GIVING C.             
     DISPLAY "*****************************".
     DISPLAY 'SUBTRACTION OF A AND B IS:' C. 
     DISPLAY "*****************************".
     STOP RUN.    
OUT PUT:
******************************
***************************** 
SUBTRACTION OF A AND B IS:10  
***************************** 
****************************

IDENTIFICATION DIVISION.                          
PROGRAM-ID. SUB4.                                 
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 A PIC 9(2) VALUE 30.                           
01 B PIC 9(2) VALUE 40.                           
01 C PIC 9(2) VALUE 90.                           
PROCEDURE DIVISION.                               
     SUBTRACT A , B , 6 , FROM C.                 
     DISPLAY "*****************************".     
     DISPLAY 'SUBTRACTION OF A AND B IS:' C.      
     DISPLAY "*****************************".     
     STOP RUN.                                    
OUTPUT:
******************************
***************************** 
SUBTRACTION OF A AND B IS:14  
***************************** 
******************************
IDENTIFICATION DIVISION.                       
PROGRAM-ID. SUB6.                              
ENVIRONMENT DIVISION.                          
DATA DIVISION.                                 
WORKING-STORAGE SECTION.                       
01 A PIC 9(2) VALUE 30.                        
01 B PIC 9(2) VALUE 40.                        
01 C PIC 9(2) VALUE 90.                        
01 D PIC 9(2).                                 
PROCEDURE DIVISION.                            
     SUBTRACT A , B , 6 , FROM C GIVING D.     
     DISPLAY "*****************************".  
     DISPLAY 'SUBTRACTION OF A AND B IS:' C.   
     DISPLAY "*****************************".  
     STOP RUN.                                 
OUTPUT:
*******************************
*****************************  
SUBTRACTION OF A AND B IS:90   
*****************************  
*******************************
IDENTIFICATION DIVISION.                        
PROGRAM-ID. SUB7.                               
ENVIRONMENT DIVISION.                           
DATA DIVISION.                                  
WORKING-STORAGE SECTION.                        
01 A PIC 9(2) VALUE 30.                         
01 B PIC 9(2) VALUE 40.                         
01 C PIC 9(2) VALUE 90.                         
01 D PIC 9(2) VALUE 80.                         
PROCEDURE DIVISION.                             
     SUBTRACT A , B FROM C , D.                 
     DISPLAY "*****************************".   
     DISPLAY 'SUBTRACTION OF A AND B IS:' D.    
     DISPLAY "*****************************".   
     STOP RUN.                                  
OUTPUT :
******************************
***************************** 
SUBTRACTION OF A AND B IS:10  
***************************** 
******************************
IDENTIFICATION DIVISION.                          
PROGRAM-ID. SUB7.                                 
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 A PIC 9(2) VALUE 30.                           
01 B PIC 9(2) VALUE 40.                           
01 C PIC 9(2) VALUE 90.                           
01 D PIC 9(2) VALUE 80.                           
01 E PIC 9(3).                                    
PROCEDURE DIVISION.                               
     SUBTRACT A , B FROM C , D GIVING E.          
     DISPLAY "*****************************".     
     DISPLAY 'SUBTRACTION OF A AND B IS:' E.      
     DISPLAY "*****************************".     
     STOP RUN.                                   
OUT PUT :
MAX=12
IDENTIFICATION DIVISION.                        
PROGRAM-ID. MULT1.                              
ENVIRONMENT DIVISION.                           
DATA DIVISION.                                  
WORKING-STORAGE SECTION.                        
01 A PIC 9(2) VALUE 5.                          
PROCEDURE DIVISION.                             
     MULTIPLY 10 BY A.                          
     DISPLAY "*****************************".   
     DISPLAY 'MULTIPLICATION OF A AND B IS:' A. 
     DISPLAY "*****************************".   
     STOP RUN.                                  
OUTPUT:
*********************************
*****************************    
MULTIPLICATION OF A AND B IS:50  
*****************************    
********************************  
IDENTIFICATION DIVISION.                        
PROGRAM-ID. MULT1.                              
ENVIRONMENT DIVISION.                           
DATA DIVISION.                                  
WORKING-STORAGE SECTION.                        
01 A PIC 9(2) VALUE 5.                          
01 B PIC 9(2).                                  
PROCEDURE DIVISION.                             
     MULTIPLY 10 BY A GIVING B.                 
     DISPLAY "*****************************".   
     DISPLAY 'MULTIPLICATION OF A AND B IS:' B. 
     DISPLAY "*****************************".   
     STOP RUN.                                  
OUT PUT:
      ********************************* 
*****************************     
MULTIPLICATION OF A AND B IS:50   
*****************************     
******************************** B
IDENTIFICATION DIVISION.                           
PROGRAM-ID. MULT3.                                 
ENVIRONMENT DIVISION.                              
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 A PIC 9(2) VALUE 5.                             
01 B PIC 9(2) VALUE 10.                            
01 C PIC 9(3).                                     
PROCEDURE DIVISION.                                
     MULTIPLY A BY B GIVING C.                     
     DISPLAY "*****************************".      
     DISPLAY 'MULTIPLICATION OF A AND B IS:' C.    
     DISPLAY "*****************************".      
     STOP RUN.
OUT PUT:
********************************* 
*****************************     
MULTIPLICATION OF A AND B IS:050  
*****************************     
******************************** B                                              
IDENTIFICATION DIVISION.                             
PROGRAM-ID. MULT4.                                   
ENVIRONMENT DIVISION.                                
DATA DIVISION.                                       
WORKING-STORAGE SECTION.                             
01 A PIC 9(2) VALUE 5.                               
01 B PIC 9(2) VALUE 10.                              
01 C PIC 9(3) VALUE 25.                              
PROCEDURE DIVISION.                                  
     MULTIPLY A BY B , C.                            
     DISPLAY "*****************************".        
     DISPLAY 'MULTIPLICATION OF A AND B IS:' B.      
     DISPLAY "MULTIPLICATION OF A AND C IS:" C.      
     DISPLAY "*****************************".        
     STOP RUN.                                                                            
OUTPUT:
********************************* TO
*****************************       
MULTIPLICATION OF A AND B IS:50     
MULTIPLICATION OF A AND C IS:125    
***************************** 
IDENTIFICATION DIVISION.                                  
PROGRAM-ID. MULT5.                                        
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 A PIC 9(2) VALUE 5.                                    
01 B PIC 9(2) VALUE 10.                                   
01 C PIC 9(2).                                            
01 D PIC 9(4) VALUE 50.                                   
PROCEDURE DIVISION.                                       
     MULTIPLY A BY B , GIVING C , D.                      
     DISPLAY "*****************************".             
     DISPLAY 'MULTIPLICATION OF A AND B IS:' B.           
     DISPLAY "MULTIPLICATION OF A AND C IS:" C.           
     DISPLAY "MULTIPLICATION OF B AND D IS:" D.           
     DISPLAY "*****************************".             
     STOP RUN.                                                  

OUT PUT:
********************************* TO
*****************************       
MULTIPLICATION OF A AND B IS:10     
MULTIPLICATION OF A AND C IS:50     
MULTIPLICATION OF B AND D IS:0050   
*****************************       
******************************** BOT      
IDENTIFICATION DIVISION.                         
PROGRAM-ID. MULT6.                               
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 A PIC 9(2) VALUE 5.                           
01 B PIC 9(2) VALUE 10.                          
01 C PIC 9(2).                                   
01 D PIC 9(4) VALUE 50.                          
PROCEDURE DIVISION.                              
     MULTIPLY A BY B ,C GIVING D.                
     DISPLAY "*****************************".    
     DISPLAY 'MULTIPLICATION OF A AND B IS:' B.  
     DISPLAY "MULTIPLICATION OF A AND C IS:" C.  
     DISPLAY "MULTIPLICATION OF B AND D IS:" D.  
     DISPLAY "*****************************".    
     STOP RUN.                                   
OUT PUT :
MAX=12.
IDENTIFICATION DIVISION.                         
PROGRAM-ID. DIVI1.                               
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 A PIC 9(2) VALUE 6.                           
01 B PIC 9(2) VALUE 30.                          
PROCEDURE DIVISION.                              
     DIVIDE  B INTO A.                           
     DISPLAY "*****************************".    
     DISPLAY 'DIVISION OF A AND B IS:' B.        
     DISPLAY "*****************************".    
     STOP RUN.                                   
OUT PUT:
 *******************************
*****************************  
DIVISION OF A AND B IS:05n     
*****************************  
*******************************
IDENTIFICATION DIVISION.                      
PROGRAM-ID. DIVI2.                            
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 A PIC 9(2) VALUE 6.                        
PROCEDURE DIVISION.                           
     DIVIDE  3 INTO A.                        
     DISPLAY "*****************************". 
     DISPLAY 'DIVISION OF A AND B IS:' A.     
     DISPLAY "*****************************". 
     STOP RUN.                                
OUT PUT:
****************************
****************************
DIVISION OF A AND B IS:02   
****************************
IDENTIFICATION DIVISION.                      
PROGRAM-ID. DIVI3.                            
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 A PIC 9(2) VALUE 30.                       
01 B PIC 9(2) VALUE 6.                        
01 C PIC 9(2).                                
PROCEDURE DIVISION.                           
     DIVIDE  B INTO A GIVING C.               
     DISPLAY "*****************************". 
     DISPLAY 'DIVISION OF A AND B IS:' C.     
     DISPLAY "*****************************". 
     STOP RUN.                                
OUT PUT:
*****************************
*****************************
DIVISION OF A AND B IS:05    
*****************************
*****************************
IDENTIFICATION DIVISION.                        
PROGRAM-ID. DIVI4.                              
ENVIRONMENT DIVISION.                           
DATA DIVISION.                                  
WORKING-STORAGE SECTION.                        
01 A PIC 9(2) VALUE 30.                         
01 B PIC 9(2) VALUE 4.                          
01 C PIC 9(2).                                  
01 D PIC 9(2).                                  
PROCEDURE DIVISION.                             
     DIVIDE  A BY B  GIVING C REMAINDER D.      
     DISPLAY "*****************************".   
     DISPLAY 'DIVISION OF A AND B IS:' C.       
     DISPLAY "DIVISION OF REMAINDER VALUE:" D.  
     DISPLAY "*****************************".   
     STOP RUN.                                  
OUT PUT:
********************************
*****************************   
DIVISION OF A AND B IS:07       
DIVISION OF REMAINDER VALUE:02  
*****************************   
********************************
IDENTIFICATION DIVISION.                            
PROGRAM-ID. DIVI5.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 A PIC 9(2) VALUE 30.                             
01 B PIC 9(2) VALUE 4.                              
01 C PIC 9(2).                                      
01 D PIC 9(2).                                      
PROCEDURE DIVISION.                                 
     DIVIDE  B INTO A GIVING C REMAINDER D.         
     DISPLAY "*****************************".       
     DISPLAY 'DIVISION OF A AND B IS:' C.           
     DISPLAY "DIVISION OF REMAINDER VALUE:" D.      
     DISPLAY "*****************************".       
     STOP RUN.                                      
                                  
OUT PUT:
*********************************
*****************************    
DIVISION OF A AND B IS:07        
DIVISION OF REMAINDER VALUE:02   
*****************************    
******************************** 
IDENTIFICATION DIVISION.                       
PROGRAM-ID. DIVI6.                             
ENVIRONMENT DIVISION.                          
DATA DIVISION.                                 
WORKING-STORAGE SECTION.                       
01 A PIC 9(2) VALUE 30.                        
01 B PIC 9(2) VALUE 4.                         
01 C PIC 9(2) VALUE 5.                         
PROCEDURE DIVISION.                            
     DIVIDE  B INTO A , C.                     
     DISPLAY "*****************************".  
     DISPLAY 'DIVISION OF A AND B IS:' A.      
     DISPLAY "DIVISION OF REMAINDER VALUE:" C. 
     DISPLAY "*****************************".  
     STOP RUN.                                 
OUT PUT:
*******************************
*****************************  
DIVISION OF A AND B IS:07      
DIVISION OF REMAINDER VALUE:01 
*****************************  
IDENTIFICATION DIVISION.                       
PROGRAM-ID. DIVI7.                             
ENVIRONMENT DIVISION.                          
DATA DIVISION.                                 
WORKING-STORAGE SECTION.                       
01 A PIC 9(2) VALUE 30.                        
01 B PIC 9(2) VALUE 4.                         
01 C PIC 9(2).                                 
PROCEDURE DIVISION.                            
     DIVIDE  A BY B ,C GIVING D                
     DISPLAY "*****************************".  
     DISPLAY 'DIVISION OF A AND B IS:' C.      
     DISPLAY "DIVISION OF REMAINDER VALUE:" D. 
     DISPLAY "*****************************".  
     STOP RUN.                                 
OUT PUT:MAX=12
 IDENTIFICATION DIVISION.                        
 PROGRAM-ID. DIVI8.                              
 ENVIRONMENT DIVISION.                           
 DATA DIVISION.                                  
 WORKING-STORAGE SECTION.                        
 01 A PIC 9(2) VALUE 30.                         
 01 B PIC 9(2) VALUE 4.                          
 01 C PIC 9(2) VALUE 5.                          
 PROCEDURE DIVISION.                             
      DIVIDE  B INTO A , C GIVING D.             
      DISPLAY "*****************************".   
      DISPLAY 'DIVISION OF A AND B IS:' A.       
      DISPLAY "DIVISION OF REMAINDER VALUE:" C.  
      DISPLAY "*****************************".   
      STOP RUN.                                  
OUT PUT:
MAX=12
    your edit profile using the command RECOVERY ON.       
 IDENTIFICATION DIVISION.                                  
 PROGRAM-ID. MOVE1.                                        
 ENVIRONMENT DIVISION.                                     
 DATA DIVISION.                                            
 WORKING-STORAGE SECTION.                                  
 01 A PIC 9(5) VALUE 11112.                                
 01 B PIC 9(6) VALUE 155112.                               
 PROCEDURE DIVISION.                                       
      MOVE    A TO B.                                      
      DISPLAY "***************************************".   
      DISPLAY "SF IS LESS &RF IS MORE:" B.                 
      DISPLAY "****************************".              
      STOP RUN.                                            
OUT PUT MOVE A TO B
*******************************
*******************************
SF IS LESS &RF IS MORE:011112  
****************************   
*******************************
IDENTIFICATION DIVISION.                                    
PROGRAM-ID. ACPT1.                                          
ENVIRONMENT DIVISION.                                       
DATA DIVISION.                                              
WORKING-STORAGE SECTION.                                    
01 WS-A PIC 9(3).                                           
01 WS-B PIC 9(3).                                           
01 WS-C PIC 9(3).                                           
PROCEDURE DIVISION.                                         
    ACCEPT WS-A.                                            
    ACCEPT WS-B.                                            
    DISPLAY WS-A.                                           
    DISPLAY WS-B.                                           
    COMPUTE WS-C = WS-A + WS-B.                             
    DISPLAY "***************************************".      
    DISPLAY "SF IS LESS &RF IS MORE:" WS-C.                 
    DISPLAY "****************************".                 
    STOP RUN.                                               

//TECN93VV  JOB NOTIFY=&SYSUID                                          
//*       CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),                            
//JOBPROC   JCLLIB ORDER=IBMUSER.ALL1                                   
//COBCL     EXEC IGYWCL,                                                
//          PGMLIB=TECN93.VISHNU.LOADLIB1,   -->LOADLIB NAME            
//*         COPYLIB=IBMUSER.COPY.LIB,          -->COPYLIB NAME          
//          GOPGM=ACPT1                  -->MEMBER NAME                 
//COBOL.SYSIN DD  DSN=TECN93.COBOL.VISHNPDS(&GOPGM),DISP=SHR  -->SRC    
//*KED.SYSLIB DD  DSN=TECN54.RAHUL.LOADLIB7(CSUBPGM),DISP=SHR -->CALL   
//                                                                      
//TECN93VV JOB  NOTIFY=&SYSUID                                        
//*        CLASS=A,MSGCLASS=H,MSGLEVEL=(1,1),LINES=(1,CANCEL),        
//RUN      EXEC  PGM=ACPT1                 -> MEMBER NAME             
//STEPLIB  DD    DSN=TECN93.VISHNU.LOADLIB1,DISP=SHR --> LOADLIB NAME 
//SYSPRINT DD    SYSOUT=*                                             
//*NDD     DD   DSN=TECN54.RAHUL.INPS,DISP=SHR                        
//*UTDD    DD   DSN=TECN54.RAHUL.OUTPS,DISP=SHR                       
//*YSOUT   DD   SYSOUT=*                                              
//SYSIN    DD   *                                                     
150                                                                   
150                                                                   
/*                                                                    
OUT PUT:
********************************
150                             
150                             
********************************
SF IS LESS &RF IS MORE:300      
****************************    
********************************
COBOL 2

IDENTIFICATION DIVISION.                                   
PROGRAM-ID. N2.                                            
ENVIRONMENT DIVISION.                                      
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 VISHNU PIC 9(5) VALUE ZEROS.                            
PROCEDURE DIVISION.                                        
     MOVE    ZEROS TO VISHNU.                              
     DISPLAY "**************************************".     
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.               
     DISPLAY "************************************".       
     STOP RUN.                                             
********************************
********************************
**NUMERIC MOVE 54321:00000      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N1.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    54321 TO VISHNU.                           
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
out put:
********************************* TOP OF DATA ***
**************************************           
**NUMERIC MOVE 54321:54321                       
************************************             
******************************** BOTTOM OF DATA *
IDENTIFICATION DIVISION.                              
PROGRAM-ID. N3.                                       
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(5).                                   
PROCEDURE DIVISION.                                   
     MOVE    543 TO VISHNU.                           
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.          
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************
********************************
**NUMERIC MOVE 54321:00543      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N4.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    543210 TO VISHNU.                          
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT:
*****************************
*****************************
**NUMERIC MOVE 54321:43210   
*****************************
*****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM1.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(5)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    ZEROS TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000000   
*********************************
******************************** 
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM2.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC 9(7)V999.                        
PROCEDURE DIVISION.                           
     MOVE    123.456 TO VISHNU.               
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.
     DISPLAY "********************************
     STOP RUN.                                
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000123456 
*********************************
******************************** 
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM2.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 VISHNU PIC 9(7)V99.                           
PROCEDURE DIVISION.                              
     MOVE    32124.45 TO VISHNU.                 
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.   
     DISPLAY "***********************************
     STOP RUN.                                   
OUTPUT :
*********************************
*********************************
**NUMERIC MOVE BLOCKS :003212445 
*********************************
******************************** 
IDENTIFICATION DIVISION.                              
PROGRAM-ID. NM2.                                      
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(4)V99.                                
PROCEDURE DIVISION.                                   
     MOVE    32124.45 TO VISHNU.                      
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.        
     DISPLAY "************************************".  
     STOP RUN.                                        
OUTPUT:
*******************************
*******************************
**NUMERIC MOVE BLOCKS :212445  
*******************************
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    124.4 TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :012440   
********************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    12345.757 TO VISHNU.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
******************************
******************************
**NUMERIC MOVE BLOCKS :234575 
******************************
IDENTIFICATION DIVISION.                                  
PROGRAM-ID. NM2.                                          
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 VISHNU PIC 9(5).                                       
01 VISHNU1 PIC 9(4).                                      
01 VISHNU2 PIC 9(6).                                      
01 VISHNU3 PIC 9(3)V99.                                   
01 VISHNU4 PIC 9V99.                                      
01 VISHNU5 PIC 9(3)V99.                                   
PROCEDURE DIVISION.                                       
     MOVE    12345 TO VISHNU.                             
     MOVE    12345 TO VISHNU1.                            
     MOVE    123456 TO VISHNU2.                           
     MOVE    123457 TO VISHNU3.                           
     MOVE    12345 TO VISHNU4.                            
     MOVE    123 TO VISHNU5.                              
     DISPLAY "**************************************".    
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.            
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU1.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU2.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU3.           
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU4.     
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU5.     
    DISPLAY "************************************".
    STOP RUN.                                      
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :12345    
**NUMERIC MOVE BLOCKS :2345     
**NUMERIC MOVE BLOCKS :123456   
**NUMERIC MOVE BLOCKS :45700    
**NUMERIC MOVE BLOCKS :500      
**NUMERIC MOVE BLOCKS :12300    
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. NM1.                                        
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 COUNTRY-POP PIC 999.                                 
01 PRICE-RS PIC 999V99.                                 
01 AMOUNT PIC 99V9.                                     
01 PRICE1-RS1 PIC 999V99.                               
PROCEDURE DIVISION.                                     
     MOVE    43.25 TO AMOUNT.                           
     MOVE    1234 TO COUNTRY-POP.                       
     MOVE    154 TO PRICE-RS.                           
     MOVE    3552.75 TO PRICE1-RS1.                     
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE BLOCKS :' AMOUNT.          
     DISPLAY '**NUMERIC MOVE BLOCKS :' COUNTRY-POP.     
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE-RS.        
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE1-RS1.      
     DISPLAY "************************************".    
     STOP RUN.                                          
*********************************
*********************************
**NUMERIC MOVE BLOCKS :432       
**NUMERIC MOVE BLOCKS :234       
**NUMERIC MOVE BLOCKS :15400     
**NUMERIC MOVE BLOCKS :55275     
*********************************
******************************** 
ALPHABETIC MOVE
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM7.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC X(6).                           
PROCEDURE DIVISION.                           
     MOVE    "ABCDEF" TO VISHNU.              
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.  
     DISPLAY "********************************
     STOP RUN.                                
******************************
******************************
**NUMERIC MOVE 54321:ABCDEF   
******************************
******************************
******************************
******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM7.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC X(6).                                    
01 VISHNU1 PIC X(5).                                   
01 VISHNU2 PIC X(5).                                   
01 VISHNU3 PIC X(5).                                   
PROCEDURE DIVISION.                                    
     MOVE    "ABCDEF" TO VISHNU.                       
     MOVE    "RANII" TO VISHNU1.                       
     MOVE    "RAJE" TO VISHNU2.                        
     MOVE    "KIRANI" TO VISHNU3.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.           
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU3.          
     DISPLAY "************************************".   
     STOP RUN.                                         
**NUMERIC MOVE 54321:ABCDEF   
**NUMERIC MOVE 54321:RANII    
**NUMERIC MOVE 54321:RAJE     
**NUMERIC MOVE 54321:KIRAN    
******************************
******************************

ALPHANUMERIC MOVE
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM6.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 NAME PIC X(6).                                
01 EMP-ID PIC X(4).                              
01 VISHNU PIC X(4).                              
01 RAM PIC X(4).                                 
PROCEDURE DIVISION.                              
     MOVE    "SPACES" TO NAME.                   
     MOVE    "TOO1" TO EMP-ID.                   
     MOVE    "TO1" TO VISHNU.                    
     MOVE    "TTOO1" TO RAM.                     
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' NAME.     
     DISPLAY "**NUMERIC MOVE BLOCKS :" EMP-ID.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" VISHNU.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" RAM.      
     DISPLAY "***********************************
     STOP RUN.                                   
******************************
******************************
**NUMERIC MOVE BLOCKS :SPACES 
**NUMERIC MOVE BLOCKS :TOO1   
**NUMERIC MOVE BLOCKS :TO1    
**NUMERIC MOVE BLOCKS :TTOO   
******************************
******************************
****************************
IDENTIFICATION DIVISION.                     
PROGRAM-ID. NM8.                             
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 VISHNU PIC X(5).                          
01 VISHNU1 PIC X(4).                         
01 VISHNU2 PIC X(6).                         
PROCEDURE DIVISION.                          
     MOVE    "ABCDE" TO VISHNU.              
     MOVE    "RANII" TO VISHNU1.             
     MOVE    "KIRAN" TO VISHNU2.             
     DISPLAY "*******************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU. 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.
     DISPLAY "*******************************
     STOP RUN.                               
****************************
**NUMERIC MOVE 54321:ABCDE  
**NUMERIC MOVE 54321:RANI   
**NUMERIC MOVE 54321:KIRAN  
****************************
****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR1.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(2) VALUE 30.                             
01 WS-B PIC 9(2) VALUE 40.                             
01 WS-C PIC 9(3).                                      
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :
*******************************
*******************************
SENDING AND RESIVING SAME:30   
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC 9(6) VALUE 000000.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*******************************
********************************* TO
************************************
*SENDING AND RESIVING SAME:030000   
************************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC A(6) VALUE.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :WE CAN NOT DO NUM TO ALP

ALPHANUMERIC TO NUMERIC

IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC X(5) VALUE 12345.                          
01 WS-B PIC 9(6) VALUE 00000.                          
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT WHEN WE GIVEN 12345
A "VALUE" clause literal was not compatible with the da
subject data item.  The "VALUE" claus was discarded.
SAME NM TO SAME NM  
IDENTIFICATION DIVISION.                                
PROGRAM-ID NMCOR2.                                      
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 WS-A PIC 9(5) VALUE 12345.                           
01 WS-B PIC 9(6) VALUE 00000.                           
PROCEDURE DIVISION.                                     
     MOVE WS-B TO WS-A.                                 
     DISPLAY "**************************************".  
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.        
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT :
********************************* TOP O
************************************** 
*SENDING AND RESIVING SAME:00000       
************************************  
IDENTIFICATION DIVISION.                          
PROGRAM-ID NMCOR2.                                
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 WS-A PIC 9(5)V99 VALUE 12345.33                
01 WS-B PIC A(6) VALUE ABCDEF.                    
PROCEDURE DIVISION.                               
     MOVE WS-B TO WS-A.                           
     DISPLAY "************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.  
     DISPLAY "************************************
     STOP RUN.                                    
OUT PUT :IN VILED
NM TO ALPN
IDENTIFICATION DIVISION.                              
PROGRAM-ID NMCOR2.                                    
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 WS-A PIC 9(5)V99 VALUE 12345.33.                   
01 WS-B PIC X(6) VALUE "ABC22F".                      
PROCEDURE DIVISION.                                   
     MOVE WS-B TO WS-A.                               
     DISPLAY "**************************************".
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.      
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************* 
**********************************
*SENDING AND RESIVING SAME:BC22600
********************************** 
NME TO NM
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6) VALUE 123456.                      
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

OUT PUT:
********************************* T
***********************************
*SENDING AND RESIVING SAME:2345600 
NME TO NME WE CAN DO
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6)V99 VALUE 1234.56.                  
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

IDENTIFICATION DIVISION.                                 
PROGRAM-ID. NMQ.                                         
ENVIRONMENT DIVISION.                                    
DATA DIVISION.                                           
WORKING-STORAGE SECTION.                                 
01 PART-RECORD.                                          
   02 NUMBR PIC X(5) VALUE "PE002".                      
01 DETAIL-LINE.                                          
   02 NUMBR PIC X(5) VALUE "DE008".                      
PROCEDURE DIVISION.                                      
     DISPLAY DETAIL-LINE.                                
     MOVE NUMBR OF PART-RECORD TO NUMBR OF DETAIL-LINE.. 
     DISPLAY PART-RECORD.                                
     DISPLAY DETAIL-LINE.                                
     STOP RUN.                                           
out put:
********
DE008   
PE002   
PE002   
********
REFERENCE MODIFICCATION

IDENTIFICATION DIVISION.                      
PROGRAM-ID. NMR.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 DATA-ITEM-1 PIC A(11) VALUE "HELLO WORLD". 
01 DATA-ITEM-2 PIC A(6) VALUE "SPACES".       
PROCEDURE DIVISION.                           
     MOVE DATA-ITEM-1(6:5) TO DATA-ITEM-2.    
     DISPLAY DATA-ITEM-2.                     
     STOP RUN.                                
*********
 WORL    
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR.                
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "*******". 
01 B2 PIC X(7) VALUE SPACES . 
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  

OUT PUT:
       *
      **
     ***
    ****
   *****
  ******
 *******
*SENDING AND RESIVING SAME:0123456 
OUT PUT:
SPACES *  
SPACES**  
SPACE***  
SPAC****  
SPA*****  
SP******  
S*******
IDENTIFICATION DIVISION.          
PROGRAM-ID. NMR1.                 
ENVIRONMENT DIVISION.             
DATA DIVISION.                    
WORKING-STORAGE SECTION.          
01 A1 PIC X(7) VALUE "*******".   
01 B2 PIC X(7) VALUE "0000000".     
PROCEDURE DIVISION.               
MAIN-PARA.                        
     DISPLAY B2(1:7) A1(7:01).    
     DISPLAY B2(1:6) A1(6:02).    
     DISPLAY B2(1:5) A1(5:03).    
     DISPLAY B2(1:4) A1(4:04).    
     DISPLAY B2(1:3) A1(3:05).    
     DISPLAY B2(1:2) A1(2:06).    
     DISPLAY B2(1:1) A1(1:07).    
     STOP RUN.                      
OUT PUT:
0000000*
000000**
00000***
0000****
000*****
00******
0******* 
IDENTIFICATION DIVISION.           
PROGRAM-ID. NMR2.                  
ENVIRONMENT DIVISION.              
DATA DIVISION.                     
WORKING-STORAGE SECTION.           
01 A1 PIC X(7) VALUE "*******".    
01 B2 PIC X(7) VALUE SPACES.    
PROCEDURE DIVISION.                
MAIN-PARA.                         
     DISPLAY B2(1:7) A1(7:01).     
     DISPLAY B2(1:6) A1(6:02).     
     DISPLAY B2(1:5) A1(5:03).     
     DISPLAY B2(1:4) A1(4:04).     
     DISPLAY B2(1:3) A1(3:05).     
     DISPLAY B2(1:2) A1(2:06).     
     DISPLAY B2(1:1) A1(1:07).     
     STOP RUN.                     
OUT PUT:
*********
       * 
      ** 
     *** 
    **** 
   ***** 
  ****** 
 ******* 
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR3.               
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "123457".  
01 B2 PIC X(7) VALUE "ZEROS".   
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  
OUT PUT:
ZEROS  
ZEROS 7
ZEROS57
ZERO457
ZER3457
ZE23457
Z123457
IDENTIFICATION DIVISION.            
PROGRAM-ID. NMR3.                   
ENVIRONMENT DIVISION.               
DATA DIVISION.                      
WORKING-STORAGE SECTION.            
01 A1 PIC X(7) VALUE "123457".      
01 B2 PIC X(7).                     
PROCEDURE DIVISION.                 
MAIN-PARA.                          
     DISPLAY B2(1:7) A1(7:01).      
     DISPLAY B2(1:6) A1(6:02).      
     DISPLAY B2(1:5) A1(5:03).      
     DISPLAY B2(1:4) A1(4:04).      
     DISPLAY B2(1:3) A1(3:05).      
     DISPLAY B2(1:2) A1(2:06).      
     DISPLAY B2(1:1) A1(1:07).      
     STOP RUN.                      
OUT PUT:
*******
       
      7
     57
    457
   3457
  23457
 123457
OUT PUT:
IF C AND D ARE EMPTY
+++++++++ 
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
OUT PUT :
+++++++++S        
++++++++S         
++++++++SS        
++++++++SES       
++++++++SCES      
++++++++SACES     
++++++++SPACES    
++++++++SSPACES     
 
COBOL3 
IDENTIFICATION DIVISION.                                   
PROGRAM-ID. N2.                                            
ENVIRONMENT DIVISION.                                      
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 VISHNU PIC 9(5) VALUE ZEROS.                            
PROCEDURE DIVISION.                                        
     MOVE    ZEROS TO VISHNU.                              
     DISPLAY "**************************************".     
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.               
     DISPLAY "************************************".       
     STOP RUN.                                             
********************************
********************************
**NUMERIC MOVE 54321:00000      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N1.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    54321 TO VISHNU.                           
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
out put:
********************************* TOP OF DATA ***
**************************************           
**NUMERIC MOVE 54321:54321                       
************************************             
******************************** BOTTOM OF DATA *
IDENTIFICATION DIVISION.                              
PROGRAM-ID. N3.                                       
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(5).                                   
PROCEDURE DIVISION.                                   
     MOVE    543 TO VISHNU.                           
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.          
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************
********************************
**NUMERIC MOVE 54321:00543      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N4.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    543210 TO VISHNU.                          
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT:
*****************************
*****************************
**NUMERIC MOVE 54321:43210   
*****************************
*****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM1.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(5)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    ZEROS TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000000   
*********************************
******************************** 
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM2.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC 9(7)V999.                        
PROCEDURE DIVISION.                           
     MOVE    123.456 TO VISHNU.               
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.
     DISPLAY "********************************
     STOP RUN.                                
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000123456 
*********************************
******************************** 
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM2.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 VISHNU PIC 9(7)V99.                           
PROCEDURE DIVISION.                              
     MOVE    32124.45 TO VISHNU.                 
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.   
     DISPLAY "***********************************
     STOP RUN.                                   
OUTPUT :
*********************************
*********************************
**NUMERIC MOVE BLOCKS :003212445 
*********************************
******************************** 
IDENTIFICATION DIVISION.                              
PROGRAM-ID. NM2.                                      
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(4)V99.                                
PROCEDURE DIVISION.                                   
     MOVE    32124.45 TO VISHNU.                      
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.        
     DISPLAY "************************************".  
     STOP RUN.                                        
OUTPUT:
*******************************
*******************************
**NUMERIC MOVE BLOCKS :212445  
*******************************
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    124.4 TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :012440   
********************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    12345.757 TO VISHNU.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
******************************
******************************
**NUMERIC MOVE BLOCKS :234575 
******************************
IDENTIFICATION DIVISION.                                  
PROGRAM-ID. NM2.                                          
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 VISHNU PIC 9(5).                                       
01 VISHNU1 PIC 9(4).                                      
01 VISHNU2 PIC 9(6).                                      
01 VISHNU3 PIC 9(3)V99.                                   
01 VISHNU4 PIC 9V99.                                      
01 VISHNU5 PIC 9(3)V99.                                   
PROCEDURE DIVISION.                                       
     MOVE    12345 TO VISHNU.                             
     MOVE    12345 TO VISHNU1.                            
     MOVE    123456 TO VISHNU2.                           
     MOVE    123457 TO VISHNU3.                           
     MOVE    12345 TO VISHNU4.                            
     MOVE    123 TO VISHNU5.                              
     DISPLAY "**************************************".    
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.            
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU1.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU2.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU3.           
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU4.     
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU5.     
    DISPLAY "************************************".
    STOP RUN.                                      
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :12345    
**NUMERIC MOVE BLOCKS :2345     
**NUMERIC MOVE BLOCKS :123456   
**NUMERIC MOVE BLOCKS :45700    
**NUMERIC MOVE BLOCKS :500      
**NUMERIC MOVE BLOCKS :12300    
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. NM1.                                        
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 COUNTRY-POP PIC 999.                                 
01 PRICE-RS PIC 999V99.                                 
01 AMOUNT PIC 99V9.                                     
01 PRICE1-RS1 PIC 999V99.                               
PROCEDURE DIVISION.                                     
     MOVE    43.25 TO AMOUNT.                           
     MOVE    1234 TO COUNTRY-POP.                       
     MOVE    154 TO PRICE-RS.                           
     MOVE    3552.75 TO PRICE1-RS1.                     
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE BLOCKS :' AMOUNT.          
     DISPLAY '**NUMERIC MOVE BLOCKS :' COUNTRY-POP.     
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE-RS.        
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE1-RS1.      
     DISPLAY "************************************".    
     STOP RUN.                                          
*********************************
*********************************
**NUMERIC MOVE BLOCKS :432       
**NUMERIC MOVE BLOCKS :234       
**NUMERIC MOVE BLOCKS :15400     
**NUMERIC MOVE BLOCKS :55275     
*********************************
******************************** 
ALPHABETIC MOVE
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM7.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC X(6).                           
PROCEDURE DIVISION.                           
     MOVE    "ABCDEF" TO VISHNU.              
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.  
     DISPLAY "********************************
     STOP RUN.                                
******************************
******************************
**NUMERIC MOVE 54321:ABCDEF   
******************************
******************************
******************************
******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM7.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC X(6).                                    
01 VISHNU1 PIC X(5).                                   
01 VISHNU2 PIC X(5).                                   
01 VISHNU3 PIC X(5).                                   
PROCEDURE DIVISION.                                    
     MOVE    "ABCDEF" TO VISHNU.                       
     MOVE    "RANII" TO VISHNU1.                       
     MOVE    "RAJE" TO VISHNU2.                        
     MOVE    "KIRANI" TO VISHNU3.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.           
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU3.          
     DISPLAY "************************************".   
     STOP RUN.                                         
**NUMERIC MOVE 54321:ABCDEF   
**NUMERIC MOVE 54321:RANII    
**NUMERIC MOVE 54321:RAJE     
**NUMERIC MOVE 54321:KIRAN    
******************************
******************************

ALPHANUMERIC MOVE
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM6.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 NAME PIC X(6).                                
01 EMP-ID PIC X(4).                              
01 VISHNU PIC X(4).                              
01 RAM PIC X(4).                                 
PROCEDURE DIVISION.                              
     MOVE    "SPACES" TO NAME.                   
     MOVE    "TOO1" TO EMP-ID.                   
     MOVE    "TO1" TO VISHNU.                    
     MOVE    "TTOO1" TO RAM.                     
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' NAME.     
     DISPLAY "**NUMERIC MOVE BLOCKS :" EMP-ID.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" VISHNU.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" RAM.      
     DISPLAY "***********************************
     STOP RUN.                                   
******************************
******************************
**NUMERIC MOVE BLOCKS :SPACES 
**NUMERIC MOVE BLOCKS :TOO1   
**NUMERIC MOVE BLOCKS :TO1    
**NUMERIC MOVE BLOCKS :TTOO   
******************************
******************************
****************************
IDENTIFICATION DIVISION.                     
PROGRAM-ID. NM8.                             
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 VISHNU PIC X(5).                          
01 VISHNU1 PIC X(4).                         
01 VISHNU2 PIC X(6).                         
PROCEDURE DIVISION.                          
     MOVE    "ABCDE" TO VISHNU.              
     MOVE    "RANII" TO VISHNU1.             
     MOVE    "KIRAN" TO VISHNU2.             
     DISPLAY "*******************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU. 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.
     DISPLAY "*******************************
     STOP RUN.                               
****************************
**NUMERIC MOVE 54321:ABCDE  
**NUMERIC MOVE 54321:RANI   
**NUMERIC MOVE 54321:KIRAN  
****************************
****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR1.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(2) VALUE 30.                             
01 WS-B PIC 9(2) VALUE 40.                             
01 WS-C PIC 9(3).                                      
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :
*******************************
*******************************
SENDING AND RESIVING SAME:30   
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC 9(6) VALUE 000000.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*******************************
********************************* TO
************************************
*SENDING AND RESIVING SAME:030000   
************************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC A(6) VALUE.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :WE CAN NOT DO NUM TO ALP

ALPHANUMERIC TO NUMERIC

IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC X(5) VALUE 12345.                          
01 WS-B PIC 9(6) VALUE 00000.                          
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT WHEN WE GIVEN 12345
A "VALUE" clause literal was not compatible with the da
subject data item.  The "VALUE" claus was discarded.
SAME NM TO SAME NM  
IDENTIFICATION DIVISION.                                
PROGRAM-ID NMCOR2.                                      
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 WS-A PIC 9(5) VALUE 12345.                           
01 WS-B PIC 9(6) VALUE 00000.                           
PROCEDURE DIVISION.                                     
     MOVE WS-B TO WS-A.                                 
     DISPLAY "**************************************".  
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.        
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT :
********************************* TOP O
************************************** 
*SENDING AND RESIVING SAME:00000       
************************************  
IDENTIFICATION DIVISION.                          
PROGRAM-ID NMCOR2.                                
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 WS-A PIC 9(5)V99 VALUE 12345.33                
01 WS-B PIC A(6) VALUE ABCDEF.                    
PROCEDURE DIVISION.                               
     MOVE WS-B TO WS-A.                           
     DISPLAY "************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.  
     DISPLAY "************************************
     STOP RUN.                                    
OUT PUT :IN VILED
NM TO ALPN
IDENTIFICATION DIVISION.                              
PROGRAM-ID NMCOR2.                                    
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 WS-A PIC 9(5)V99 VALUE 12345.33.                   
01 WS-B PIC X(6) VALUE "ABC22F".                      
PROCEDURE DIVISION.                                   
     MOVE WS-B TO WS-A.                               
     DISPLAY "**************************************".
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.      
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************* 
**********************************
*SENDING AND RESIVING SAME:BC22600
********************************** 
NME TO NM
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6) VALUE 123456.                      
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

OUT PUT:
********************************* T
***********************************
*SENDING AND RESIVING SAME:2345600 
NME TO NME WE CAN DO
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6)V99 VALUE 1234.56.                  
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

IDENTIFICATION DIVISION.                                 
PROGRAM-ID. NMQ.                                         
ENVIRONMENT DIVISION.                                    
DATA DIVISION.                                           
WORKING-STORAGE SECTION.                                 
01 PART-RECORD.                                          
   02 NUMBR PIC X(5) VALUE "PE002".                      
01 DETAIL-LINE.                                          
   02 NUMBR PIC X(5) VALUE "DE008".                      
PROCEDURE DIVISION.                                      
     DISPLAY DETAIL-LINE.                                
     MOVE NUMBR OF PART-RECORD TO NUMBR OF DETAIL-LINE.. 
     DISPLAY PART-RECORD.                                
     DISPLAY DETAIL-LINE.                                
     STOP RUN.                                           
out put:
********
DE008   
PE002   
PE002   
********
REFERENCE MODIFICCATION

IDENTIFICATION DIVISION.                      
PROGRAM-ID. NMR.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 DATA-ITEM-1 PIC A(11) VALUE "HELLO WORLD". 
01 DATA-ITEM-2 PIC A(6) VALUE "SPACES".       
PROCEDURE DIVISION.                           
     MOVE DATA-ITEM-1(6:5) TO DATA-ITEM-2.    
     DISPLAY DATA-ITEM-2.                     
     STOP RUN.                                
*********
 WORL    
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR.                
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "*******". 
01 B2 PIC X(7) VALUE SPACES . 
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  

OUT PUT:
       *
      **
     ***
    ****
   *****
  ******
 *******
*SENDING AND RESIVING SAME:0123456 
OUT PUT:
SPACES *  
SPACES**  
SPACE***  
SPAC****  
SPA*****  
SP******  
S*******
IDENTIFICATION DIVISION.          
PROGRAM-ID. NMR1.                 
ENVIRONMENT DIVISION.             
DATA DIVISION.                    
WORKING-STORAGE SECTION.          
01 A1 PIC X(7) VALUE "*******".   
01 B2 PIC X(7) VALUE "0000000".     
PROCEDURE DIVISION.               
MAIN-PARA.                        
     DISPLAY B2(1:7) A1(7:01).    
     DISPLAY B2(1:6) A1(6:02).    
     DISPLAY B2(1:5) A1(5:03).    
     DISPLAY B2(1:4) A1(4:04).    
     DISPLAY B2(1:3) A1(3:05).    
     DISPLAY B2(1:2) A1(2:06).    
     DISPLAY B2(1:1) A1(1:07).    
     STOP RUN.                      
OUT PUT:
0000000*
000000**
00000***
0000****
000*****
00******
0******* 
IDENTIFICATION DIVISION.           
PROGRAM-ID. NMR2.                  
ENVIRONMENT DIVISION.              
DATA DIVISION.                     
WORKING-STORAGE SECTION.           
01 A1 PIC X(7) VALUE "*******".    
01 B2 PIC X(7) VALUE SPACES.    
PROCEDURE DIVISION.                
MAIN-PARA.                         
     DISPLAY B2(1:7) A1(7:01).     
     DISPLAY B2(1:6) A1(6:02).     
     DISPLAY B2(1:5) A1(5:03).     
     DISPLAY B2(1:4) A1(4:04).     
     DISPLAY B2(1:3) A1(3:05).     
     DISPLAY B2(1:2) A1(2:06).     
     DISPLAY B2(1:1) A1(1:07).     
     STOP RUN.                     
OUT PUT:
*********
       * 
      ** 
     *** 
    **** 
   ***** 
  ****** 
 ******* 
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR3.               
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "123457".  
01 B2 PIC X(7) VALUE "ZEROS".   
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  
OUT PUT:
ZEROS  
ZEROS 7
ZEROS57
ZERO457
ZER3457
ZE23457
Z123457
IDENTIFICATION DIVISION.            
PROGRAM-ID. NMR3.                   
ENVIRONMENT DIVISION.               
DATA DIVISION.                      
WORKING-STORAGE SECTION.            
01 A1 PIC X(7) VALUE "123457".      
01 B2 PIC X(7).                     
PROCEDURE DIVISION.                 
MAIN-PARA.                          
     DISPLAY B2(1:7) A1(7:01).      
     DISPLAY B2(1:6) A1(6:02).      
     DISPLAY B2(1:5) A1(5:03).      
     DISPLAY B2(1:4) A1(4:04).      
     DISPLAY B2(1:3) A1(3:05).      
     DISPLAY B2(1:2) A1(2:06).      
     DISPLAY B2(1:1) A1(1:07).      
     STOP RUN.                      
OUT PUT:
*******
       
      7
     57
    457
   3457
  23457
 123457
OUT PUT:
IF C AND D ARE EMPTY
+++++++++ 
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
OUT PUT :
+++++++++S        
++++++++S         
++++++++SS        
++++++++SES       
++++++++SCES      
++++++++SACES     
++++++++SPACES    
++++++++SSPACES     
COBOL STRINGS
IDENTIFICATION DIVISION.                                   
PROGRAM-ID. N2.                                            
ENVIRONMENT DIVISION.                                      
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 VISHNU PIC 9(5) VALUE ZEROS.                            
PROCEDURE DIVISION.                                        
     MOVE    ZEROS TO VISHNU.                              
     DISPLAY "**************************************".     
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.               
     DISPLAY "************************************".       
     STOP RUN.                                             
********************************
********************************
**NUMERIC MOVE 54321:00000      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N1.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    54321 TO VISHNU.                           
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
out put:
********************************* TOP OF DATA ***
**************************************           
**NUMERIC MOVE 54321:54321                       
************************************             
******************************** BOTTOM OF DATA *
IDENTIFICATION DIVISION.                              
PROGRAM-ID. N3.                                       
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(5).                                   
PROCEDURE DIVISION.                                   
     MOVE    543 TO VISHNU.                           
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.          
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************
********************************
**NUMERIC MOVE 54321:00543      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N4.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    543210 TO VISHNU.                          
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT:
*****************************
*****************************
**NUMERIC MOVE 54321:43210   
*****************************
*****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM1.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(5)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    ZEROS TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000000   
*********************************
******************************** 
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM2.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC 9(7)V999.                        
PROCEDURE DIVISION.                           
     MOVE    123.456 TO VISHNU.               
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.
     DISPLAY "********************************
     STOP RUN.                                
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000123456 
*********************************
******************************** 
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM2.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 VISHNU PIC 9(7)V99.                           
PROCEDURE DIVISION.                              
     MOVE    32124.45 TO VISHNU.                 
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.   
     DISPLAY "***********************************
     STOP RUN.                                   
OUTPUT :
*********************************
*********************************
**NUMERIC MOVE BLOCKS :003212445 
*********************************
******************************** 
IDENTIFICATION DIVISION.                              
PROGRAM-ID. NM2.                                      
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(4)V99.                                
PROCEDURE DIVISION.                                   
     MOVE    32124.45 TO VISHNU.                      
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.        
     DISPLAY "************************************".  
     STOP RUN.                                        
OUTPUT:
*******************************
*******************************
**NUMERIC MOVE BLOCKS :212445  
*******************************
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    124.4 TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :012440   
********************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    12345.757 TO VISHNU.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
******************************
******************************
**NUMERIC MOVE BLOCKS :234575 
******************************
IDENTIFICATION DIVISION.                                  
PROGRAM-ID. NM2.                                          
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 VISHNU PIC 9(5).                                       
01 VISHNU1 PIC 9(4).                                      
01 VISHNU2 PIC 9(6).                                      
01 VISHNU3 PIC 9(3)V99.                                   
01 VISHNU4 PIC 9V99.                                      
01 VISHNU5 PIC 9(3)V99.                                   
PROCEDURE DIVISION.                                       
     MOVE    12345 TO VISHNU.                             
     MOVE    12345 TO VISHNU1.                            
     MOVE    123456 TO VISHNU2.                           
     MOVE    123457 TO VISHNU3.                           
     MOVE    12345 TO VISHNU4.                            
     MOVE    123 TO VISHNU5.                              
     DISPLAY "**************************************".    
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.            
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU1.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU2.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU3.           
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU4.     
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU5.     
    DISPLAY "************************************".
    STOP RUN.                                      
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :12345    
**NUMERIC MOVE BLOCKS :2345     
**NUMERIC MOVE BLOCKS :123456   
**NUMERIC MOVE BLOCKS :45700    
**NUMERIC MOVE BLOCKS :500      
**NUMERIC MOVE BLOCKS :12300    
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. NM1.                                        
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 COUNTRY-POP PIC 999.                                 
01 PRICE-RS PIC 999V99.                                 
01 AMOUNT PIC 99V9.                                     
01 PRICE1-RS1 PIC 999V99.                               
PROCEDURE DIVISION.                                     
     MOVE    43.25 TO AMOUNT.                           
     MOVE    1234 TO COUNTRY-POP.                       
     MOVE    154 TO PRICE-RS.                           
     MOVE    3552.75 TO PRICE1-RS1.                     
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE BLOCKS :' AMOUNT.          
     DISPLAY '**NUMERIC MOVE BLOCKS :' COUNTRY-POP.     
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE-RS.        
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE1-RS1.      
     DISPLAY "************************************".    
     STOP RUN.                                          
*********************************
*********************************
**NUMERIC MOVE BLOCKS :432       
**NUMERIC MOVE BLOCKS :234       
**NUMERIC MOVE BLOCKS :15400     
**NUMERIC MOVE BLOCKS :55275     
*********************************
******************************** 
ALPHABETIC MOVE
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM7.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC X(6).                           
PROCEDURE DIVISION.                           
     MOVE    "ABCDEF" TO VISHNU.              
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.  
     DISPLAY "********************************
     STOP RUN.                                
******************************
******************************
**NUMERIC MOVE 54321:ABCDEF   
******************************
******************************
******************************
******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM7.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC X(6).                                    
01 VISHNU1 PIC X(5).                                   
01 VISHNU2 PIC X(5).                                   
01 VISHNU3 PIC X(5).                                   
PROCEDURE DIVISION.                                    
     MOVE    "ABCDEF" TO VISHNU.                       
     MOVE    "RANII" TO VISHNU1.                       
     MOVE    "RAJE" TO VISHNU2.                        
     MOVE    "KIRANI" TO VISHNU3.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.           
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU3.          
     DISPLAY "************************************".   
     STOP RUN.                                         
**NUMERIC MOVE 54321:ABCDEF   
**NUMERIC MOVE 54321:RANII    
**NUMERIC MOVE 54321:RAJE     
**NUMERIC MOVE 54321:KIRAN    
******************************
******************************

ALPHANUMERIC MOVE
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM6.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 NAME PIC X(6).                                
01 EMP-ID PIC X(4).                              
01 VISHNU PIC X(4).                              
01 RAM PIC X(4).                                 
PROCEDURE DIVISION.                              
     MOVE    "SPACES" TO NAME.                   
     MOVE    "TOO1" TO EMP-ID.                   
     MOVE    "TO1" TO VISHNU.                    
     MOVE    "TTOO1" TO RAM.                     
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' NAME.     
     DISPLAY "**NUMERIC MOVE BLOCKS :" EMP-ID.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" VISHNU.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" RAM.      
     DISPLAY "***********************************
     STOP RUN.                                   
******************************
******************************
**NUMERIC MOVE BLOCKS :SPACES 
**NUMERIC MOVE BLOCKS :TOO1   
**NUMERIC MOVE BLOCKS :TO1    
**NUMERIC MOVE BLOCKS :TTOO   
******************************
******************************
****************************
IDENTIFICATION DIVISION.                     
PROGRAM-ID. NM8.                             
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 VISHNU PIC X(5).                          
01 VISHNU1 PIC X(4).                         
01 VISHNU2 PIC X(6).                         
PROCEDURE DIVISION.                          
     MOVE    "ABCDE" TO VISHNU.              
     MOVE    "RANII" TO VISHNU1.             
     MOVE    "KIRAN" TO VISHNU2.             
     DISPLAY "*******************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU. 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.
     DISPLAY "*******************************
     STOP RUN.                               
****************************
**NUMERIC MOVE 54321:ABCDE  
**NUMERIC MOVE 54321:RANI   
**NUMERIC MOVE 54321:KIRAN  
****************************
****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR1.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(2) VALUE 30.                             
01 WS-B PIC 9(2) VALUE 40.                             
01 WS-C PIC 9(3).                                      
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :
*******************************
*******************************
SENDING AND RESIVING SAME:30   
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC 9(6) VALUE 000000.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*******************************
********************************* TO
************************************
*SENDING AND RESIVING SAME:030000   
************************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC A(6) VALUE.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :WE CAN NOT DO NUM TO ALP

ALPHANUMERIC TO NUMERIC

IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC X(5) VALUE 12345.                          
01 WS-B PIC 9(6) VALUE 00000.                          
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT WHEN WE GIVEN 12345
A "VALUE" clause literal was not compatible with the da
subject data item.  The "VALUE" claus was discarded.
SAME NM TO SAME NM  
IDENTIFICATION DIVISION.                                
PROGRAM-ID NMCOR2.                                      
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 WS-A PIC 9(5) VALUE 12345.                           
01 WS-B PIC 9(6) VALUE 00000.                           
PROCEDURE DIVISION.                                     
     MOVE WS-B TO WS-A.                                 
     DISPLAY "**************************************".  
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.        
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT :
********************************* TOP O
************************************** 
*SENDING AND RESIVING SAME:00000       
************************************  
IDENTIFICATION DIVISION.                          
PROGRAM-ID NMCOR2.                                
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 WS-A PIC 9(5)V99 VALUE 12345.33                
01 WS-B PIC A(6) VALUE ABCDEF.                    
PROCEDURE DIVISION.                               
     MOVE WS-B TO WS-A.                           
     DISPLAY "************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.  
     DISPLAY "************************************
     STOP RUN.                                    
OUT PUT :IN VILED
NM TO ALPN
IDENTIFICATION DIVISION.                              
PROGRAM-ID NMCOR2.                                    
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 WS-A PIC 9(5)V99 VALUE 12345.33.                   
01 WS-B PIC X(6) VALUE "ABC22F".                      
PROCEDURE DIVISION.                                   
     MOVE WS-B TO WS-A.                               
     DISPLAY "**************************************".
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.      
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************* 
**********************************
*SENDING AND RESIVING SAME:BC22600
********************************** 
NME TO NM
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6) VALUE 123456.                      
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

OUT PUT:
********************************* T
***********************************
*SENDING AND RESIVING SAME:2345600 
NME TO NME WE CAN DO
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6)V99 VALUE 1234.56.                  
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

IDENTIFICATION DIVISION.                                 
PROGRAM-ID. NMQ.                                         
ENVIRONMENT DIVISION.                                    
DATA DIVISION.                                           
WORKING-STORAGE SECTION.                                 
01 PART-RECORD.                                          
   02 NUMBR PIC X(5) VALUE "PE002".                      
01 DETAIL-LINE.                                          
   02 NUMBR PIC X(5) VALUE "DE008".                      
PROCEDURE DIVISION.                                      
     DISPLAY DETAIL-LINE.                                
     MOVE NUMBR OF PART-RECORD TO NUMBR OF DETAIL-LINE.. 
     DISPLAY PART-RECORD.                                
     DISPLAY DETAIL-LINE.                                
     STOP RUN.                                           
out put:
********
DE008   
PE002   
PE002   
********
REFERENCE MODIFICCATION

IDENTIFICATION DIVISION.                      
PROGRAM-ID. NMR.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 DATA-ITEM-1 PIC A(11) VALUE "HELLO WORLD". 
01 DATA-ITEM-2 PIC A(6) VALUE "SPACES".       
PROCEDURE DIVISION.                           
     MOVE DATA-ITEM-1(6:5) TO DATA-ITEM-2.    
     DISPLAY DATA-ITEM-2.                     
     STOP RUN.                                
*********
 WORL    
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR.                
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "*******". 
01 B2 PIC X(7) VALUE SPACES . 
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  

OUT PUT:
       *
      **
     ***
    ****
   *****
  ******
 *******
*SENDING AND RESIVING SAME:0123456 
OUT PUT:
SPACES *  
SPACES**  
SPACE***  
SPAC****  
SPA*****  
SP******  
S*******
IDENTIFICATION DIVISION.          
PROGRAM-ID. NMR1.                 
ENVIRONMENT DIVISION.             
DATA DIVISION.                    
WORKING-STORAGE SECTION.          
01 A1 PIC X(7) VALUE "*******".   
01 B2 PIC X(7) VALUE "0000000".     
PROCEDURE DIVISION.               
MAIN-PARA.                        
     DISPLAY B2(1:7) A1(7:01).    
     DISPLAY B2(1:6) A1(6:02).    
     DISPLAY B2(1:5) A1(5:03).    
     DISPLAY B2(1:4) A1(4:04).    
     DISPLAY B2(1:3) A1(3:05).    
     DISPLAY B2(1:2) A1(2:06).    
     DISPLAY B2(1:1) A1(1:07).    
     STOP RUN.                      
OUT PUT:
0000000*
000000**
00000***
0000****
000*****
00******
0******* 
IDENTIFICATION DIVISION.           
PROGRAM-ID. NMR2.                  
ENVIRONMENT DIVISION.              
DATA DIVISION.                     
WORKING-STORAGE SECTION.           
01 A1 PIC X(7) VALUE "*******".    
01 B2 PIC X(7) VALUE SPACES.    
PROCEDURE DIVISION.                
MAIN-PARA.                         
     DISPLAY B2(1:7) A1(7:01).     
     DISPLAY B2(1:6) A1(6:02).     
     DISPLAY B2(1:5) A1(5:03).     
     DISPLAY B2(1:4) A1(4:04).     
     DISPLAY B2(1:3) A1(3:05).     
     DISPLAY B2(1:2) A1(2:06).     
     DISPLAY B2(1:1) A1(1:07).     
     STOP RUN.                     
OUT PUT:
*********
       * 
      ** 
     *** 
    **** 
   ***** 
  ****** 
 ******* 
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR3.               
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "123457".  
01 B2 PIC X(7) VALUE "ZEROS".   
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  
OUT PUT:
ZEROS  
ZEROS 7
ZEROS57
ZERO457
ZER3457
ZE23457
Z123457
IDENTIFICATION DIVISION.            
PROGRAM-ID. NMR3.                   
ENVIRONMENT DIVISION.               
DATA DIVISION.                      
WORKING-STORAGE SECTION.            
01 A1 PIC X(7) VALUE "123457".      
01 B2 PIC X(7).                     
PROCEDURE DIVISION.                 
MAIN-PARA.                          
     DISPLAY B2(1:7) A1(7:01).      
     DISPLAY B2(1:6) A1(6:02).      
     DISPLAY B2(1:5) A1(5:03).      
     DISPLAY B2(1:4) A1(4:04).      
     DISPLAY B2(1:3) A1(3:05).      
     DISPLAY B2(1:2) A1(2:06).      
     DISPLAY B2(1:1) A1(1:07).      
     STOP RUN.                      
OUT PUT:
*******
       
      7
     57
    457
   3457
  23457
 123457
OUT PUT:
IF C AND D ARE EMPTY
+++++++++ 
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
OUT PUT :
+++++++++S        
++++++++S         
++++++++SS        
++++++++SES       
++++++++SCES      
++++++++SACES     
++++++++SPACES    
++++++++SSPACES     
CONCONDITION
IDENTIFICATION DIVISION.                                   
PROGRAM-ID. N2.                                            
ENVIRONMENT DIVISION.                                      
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 VISHNU PIC 9(5) VALUE ZEROS.                            
PROCEDURE DIVISION.                                        
     MOVE    ZEROS TO VISHNU.                              
     DISPLAY "**************************************".     
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.               
     DISPLAY "************************************".       
     STOP RUN.                                             
********************************
********************************
**NUMERIC MOVE 54321:00000      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N1.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    54321 TO VISHNU.                           
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
out put:
********************************* TOP OF DATA ***
**************************************           
**NUMERIC MOVE 54321:54321                       
************************************             
******************************** BOTTOM OF DATA *
IDENTIFICATION DIVISION.                              
PROGRAM-ID. N3.                                       
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(5).                                   
PROCEDURE DIVISION.                                   
     MOVE    543 TO VISHNU.                           
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.          
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************
********************************
**NUMERIC MOVE 54321:00543      
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. N4.                                         
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 VISHNU PIC 9(5).                                     
PROCEDURE DIVISION.                                     
     MOVE    543210 TO VISHNU.                          
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.            
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT:
*****************************
*****************************
**NUMERIC MOVE 54321:43210   
*****************************
*****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM1.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(5)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    ZEROS TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000000   
*********************************
******************************** 
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM2.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC 9(7)V999.                        
PROCEDURE DIVISION.                           
     MOVE    123.456 TO VISHNU.               
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.
     DISPLAY "********************************
     STOP RUN.                                
OUT PUT:
*********************************
*********************************
**NUMERIC MOVE BLOCKS :0000123456 
*********************************
******************************** 
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM2.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 VISHNU PIC 9(7)V99.                           
PROCEDURE DIVISION.                              
     MOVE    32124.45 TO VISHNU.                 
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.   
     DISPLAY "***********************************
     STOP RUN.                                   
OUTPUT :
*********************************
*********************************
**NUMERIC MOVE BLOCKS :003212445 
*********************************
******************************** 
IDENTIFICATION DIVISION.                              
PROGRAM-ID. NM2.                                      
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 VISHNU PIC 9(4)V99.                                
PROCEDURE DIVISION.                                   
     MOVE    32124.45 TO VISHNU.                      
     DISPLAY "**************************************".
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.        
     DISPLAY "************************************".  
     STOP RUN.                                        
OUTPUT:
*******************************
*******************************
**NUMERIC MOVE BLOCKS :212445  
*******************************
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    124.4 TO VISHNU.                          
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :012440   
********************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM2.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC 9(4)V99.                                 
PROCEDURE DIVISION.                                    
     MOVE    12345.757 TO VISHNU.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.         
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
******************************
******************************
**NUMERIC MOVE BLOCKS :234575 
******************************
IDENTIFICATION DIVISION.                                  
PROGRAM-ID. NM2.                                          
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 VISHNU PIC 9(5).                                       
01 VISHNU1 PIC 9(4).                                      
01 VISHNU2 PIC 9(6).                                      
01 VISHNU3 PIC 9(3)V99.                                   
01 VISHNU4 PIC 9V99.                                      
01 VISHNU5 PIC 9(3)V99.                                   
PROCEDURE DIVISION.                                       
     MOVE    12345 TO VISHNU.                             
     MOVE    12345 TO VISHNU1.                            
     MOVE    123456 TO VISHNU2.                           
     MOVE    123457 TO VISHNU3.                           
     MOVE    12345 TO VISHNU4.                            
     MOVE    123 TO VISHNU5.                              
     DISPLAY "**************************************".    
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU.            
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU1.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU2.           
     DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU3.           
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU4.     
    DISPLAY '**NUMERIC MOVE BLOCKS :' VISHNU5.     
    DISPLAY "************************************".
    STOP RUN.                                      
OUTPUT:
********************************
********************************
**NUMERIC MOVE BLOCKS :12345    
**NUMERIC MOVE BLOCKS :2345     
**NUMERIC MOVE BLOCKS :123456   
**NUMERIC MOVE BLOCKS :45700    
**NUMERIC MOVE BLOCKS :500      
**NUMERIC MOVE BLOCKS :12300    
********************************
********************************
IDENTIFICATION DIVISION.                                
PROGRAM-ID. NM1.                                        
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 COUNTRY-POP PIC 999.                                 
01 PRICE-RS PIC 999V99.                                 
01 AMOUNT PIC 99V9.                                     
01 PRICE1-RS1 PIC 999V99.                               
PROCEDURE DIVISION.                                     
     MOVE    43.25 TO AMOUNT.                           
     MOVE    1234 TO COUNTRY-POP.                       
     MOVE    154 TO PRICE-RS.                           
     MOVE    3552.75 TO PRICE1-RS1.                     
     DISPLAY "**************************************".  
     DISPLAY '**NUMERIC MOVE BLOCKS :' AMOUNT.          
     DISPLAY '**NUMERIC MOVE BLOCKS :' COUNTRY-POP.     
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE-RS.        
     DISPLAY '**NUMERIC MOVE BLOCKS :' PRICE1-RS1.      
     DISPLAY "************************************".    
     STOP RUN.                                          
*********************************
*********************************
**NUMERIC MOVE BLOCKS :432       
**NUMERIC MOVE BLOCKS :234       
**NUMERIC MOVE BLOCKS :15400     
**NUMERIC MOVE BLOCKS :55275     
*********************************
******************************** 
ALPHABETIC MOVE
IDENTIFICATION DIVISION.                      
PROGRAM-ID. NM7.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 VISHNU PIC X(6).                           
PROCEDURE DIVISION.                           
     MOVE    "ABCDEF" TO VISHNU.              
     DISPLAY "********************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.  
     DISPLAY "********************************
     STOP RUN.                                
******************************
******************************
**NUMERIC MOVE 54321:ABCDEF   
******************************
******************************
******************************
******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID. NM7.                                       
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 VISHNU PIC X(6).                                    
01 VISHNU1 PIC X(5).                                   
01 VISHNU2 PIC X(5).                                   
01 VISHNU3 PIC X(5).                                   
PROCEDURE DIVISION.                                    
     MOVE    "ABCDEF" TO VISHNU.                       
     MOVE    "RANII" TO VISHNU1.                       
     MOVE    "RAJE" TO VISHNU2.                        
     MOVE    "KIRANI" TO VISHNU3.                      
     DISPLAY "**************************************". 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU.           
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.          
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU3.          
     DISPLAY "************************************".   
     STOP RUN.                                         
**NUMERIC MOVE 54321:ABCDEF   
**NUMERIC MOVE 54321:RANII    
**NUMERIC MOVE 54321:RAJE     
**NUMERIC MOVE 54321:KIRAN    
******************************
******************************

ALPHANUMERIC MOVE
IDENTIFICATION DIVISION.                         
PROGRAM-ID. NM6.                                 
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 NAME PIC X(6).                                
01 EMP-ID PIC X(4).                              
01 VISHNU PIC X(4).                              
01 RAM PIC X(4).                                 
PROCEDURE DIVISION.                              
     MOVE    "SPACES" TO NAME.                   
     MOVE    "TOO1" TO EMP-ID.                   
     MOVE    "TO1" TO VISHNU.                    
     MOVE    "TTOO1" TO RAM.                     
     DISPLAY "***********************************
     DISPLAY '**NUMERIC MOVE BLOCKS :' NAME.     
     DISPLAY "**NUMERIC MOVE BLOCKS :" EMP-ID.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" VISHNU.   
     DISPLAY "**NUMERIC MOVE BLOCKS :" RAM.      
     DISPLAY "***********************************
     STOP RUN.                                   
******************************
******************************
**NUMERIC MOVE BLOCKS :SPACES 
**NUMERIC MOVE BLOCKS :TOO1   
**NUMERIC MOVE BLOCKS :TO1    
**NUMERIC MOVE BLOCKS :TTOO   
******************************
******************************
****************************
IDENTIFICATION DIVISION.                     
PROGRAM-ID. NM8.                             
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 VISHNU PIC X(5).                          
01 VISHNU1 PIC X(4).                         
01 VISHNU2 PIC X(6).                         
PROCEDURE DIVISION.                          
     MOVE    "ABCDE" TO VISHNU.              
     MOVE    "RANII" TO VISHNU1.             
     MOVE    "KIRAN" TO VISHNU2.             
     DISPLAY "*******************************
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU. 
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU1.
     DISPLAY '**NUMERIC MOVE 54321:' VISHNU2.
     DISPLAY "*******************************
     STOP RUN.                               
****************************
**NUMERIC MOVE 54321:ABCDE  
**NUMERIC MOVE 54321:RANI   
**NUMERIC MOVE 54321:KIRAN  
****************************
****************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR1.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(2) VALUE 30.                             
01 WS-B PIC 9(2) VALUE 40.                             
01 WS-C PIC 9(3).                                      
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :
*******************************
*******************************
SENDING AND RESIVING SAME:30   
*******************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC 9(6) VALUE 000000.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT:
*******************************
********************************* TO
************************************
*SENDING AND RESIVING SAME:030000   
************************************
IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC 9(5) VALUE 30000.                          
01 WS-B PIC A(6) VALUE.                                
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT :WE CAN NOT DO NUM TO ALP

ALPHANUMERIC TO NUMERIC

IDENTIFICATION DIVISION.                               
PROGRAM-ID NMCOR2.                                     
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-A PIC X(5) VALUE 12345.                          
01 WS-B PIC 9(6) VALUE 00000.                          
PROCEDURE DIVISION.                                    
     MOVE WS-A TO WS-B.                                
     DISPLAY "**************************************". 
     DISPLAY "*SENDING AND RESIVING SAME:" WS-B.       
     DISPLAY "************************************".   
     STOP RUN.                                         
OUT PUT WHEN WE GIVEN 12345
A "VALUE" clause literal was not compatible with the da
subject data item.  The "VALUE" claus was discarded.
SAME NM TO SAME NM  
IDENTIFICATION DIVISION.                                
PROGRAM-ID NMCOR2.                                      
ENVIRONMENT DIVISION.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 WS-A PIC 9(5) VALUE 12345.                           
01 WS-B PIC 9(6) VALUE 00000.                           
PROCEDURE DIVISION.                                     
     MOVE WS-B TO WS-A.                                 
     DISPLAY "**************************************".  
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.        
     DISPLAY "************************************".    
     STOP RUN.                                          
OUT PUT :
********************************* TOP O
************************************** 
*SENDING AND RESIVING SAME:00000       
************************************  
IDENTIFICATION DIVISION.                          
PROGRAM-ID NMCOR2.                                
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 WS-A PIC 9(5)V99 VALUE 12345.33                
01 WS-B PIC A(6) VALUE ABCDEF.                    
PROCEDURE DIVISION.                               
     MOVE WS-B TO WS-A.                           
     DISPLAY "************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.  
     DISPLAY "************************************
     STOP RUN.                                    
OUT PUT :IN VILED
NM TO ALPN
IDENTIFICATION DIVISION.                              
PROGRAM-ID NMCOR2.                                    
ENVIRONMENT DIVISION.                                 
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 WS-A PIC 9(5)V99 VALUE 12345.33.                   
01 WS-B PIC X(6) VALUE "ABC22F".                      
PROCEDURE DIVISION.                                   
     MOVE WS-B TO WS-A.                               
     DISPLAY "**************************************".
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.      
     DISPLAY "************************************".  
     STOP RUN.                                        
OUT PUT:
********************************* 
**********************************
*SENDING AND RESIVING SAME:BC22600
********************************** 
NME TO NM
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6) VALUE 123456.                      
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

OUT PUT:
********************************* T
***********************************
*SENDING AND RESIVING SAME:2345600 
NME TO NME WE CAN DO
IDENTIFICATION DIVISION.                            
PROGRAM-ID NMCOR2.                                  
ENVIRONMENT DIVISION.                               
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 WS-A PIC 9(5)V99 VALUE 12345.33.                 
01 WS-B PIC 9(6)V99 VALUE 1234.56.                  
PROCEDURE DIVISION.                                 
     MOVE WS-B TO WS-A.                             
     DISPLAY "**************************************
     DISPLAY "*SENDING AND RESIVING SAME:" WS-A.    
     DISPLAY "************************************".
     STOP RUN.                                      

IDENTIFICATION DIVISION.                                 
PROGRAM-ID. NMQ.                                         
ENVIRONMENT DIVISION.                                    
DATA DIVISION.                                           
WORKING-STORAGE SECTION.                                 
01 PART-RECORD.                                          
   02 NUMBR PIC X(5) VALUE "PE002".                      
01 DETAIL-LINE.                                          
   02 NUMBR PIC X(5) VALUE "DE008".                      
PROCEDURE DIVISION.                                      
     DISPLAY DETAIL-LINE.                                
     MOVE NUMBR OF PART-RECORD TO NUMBR OF DETAIL-LINE.. 
     DISPLAY PART-RECORD.                                
     DISPLAY DETAIL-LINE.                                
     STOP RUN.                                           
out put:
********
DE008   
PE002   
PE002   
********
REFERENCE MODIFICCATION

IDENTIFICATION DIVISION.                      
PROGRAM-ID. NMR.                              
ENVIRONMENT DIVISION.                         
DATA DIVISION.                                
WORKING-STORAGE SECTION.                      
01 DATA-ITEM-1 PIC A(11) VALUE "HELLO WORLD". 
01 DATA-ITEM-2 PIC A(6) VALUE "SPACES".       
PROCEDURE DIVISION.                           
     MOVE DATA-ITEM-1(6:5) TO DATA-ITEM-2.    
     DISPLAY DATA-ITEM-2.                     
     STOP RUN.                                
*********
 WORL    
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR.                
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "*******". 
01 B2 PIC X(7) VALUE SPACES . 
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  

OUT PUT:
       *
      **
     ***
    ****
   *****
  ******
 *******
*SENDING AND RESIVING SAME:0123456 
OUT PUT:
SPACES *  
SPACES**  
SPACE***  
SPAC****  
SPA*****  
SP******  
S*******
IDENTIFICATION DIVISION.          
PROGRAM-ID. NMR1.                 
ENVIRONMENT DIVISION.             
DATA DIVISION.                    
WORKING-STORAGE SECTION.          
01 A1 PIC X(7) VALUE "*******".   
01 B2 PIC X(7) VALUE "0000000".     
PROCEDURE DIVISION.               
MAIN-PARA.                        
     DISPLAY B2(1:7) A1(7:01).    
     DISPLAY B2(1:6) A1(6:02).    
     DISPLAY B2(1:5) A1(5:03).    
     DISPLAY B2(1:4) A1(4:04).    
     DISPLAY B2(1:3) A1(3:05).    
     DISPLAY B2(1:2) A1(2:06).    
     DISPLAY B2(1:1) A1(1:07).    
     STOP RUN.                      
OUT PUT:
0000000*
000000**
00000***
0000****
000*****
00******
0******* 
IDENTIFICATION DIVISION.           
PROGRAM-ID. NMR2.                  
ENVIRONMENT DIVISION.              
DATA DIVISION.                     
WORKING-STORAGE SECTION.           
01 A1 PIC X(7) VALUE "*******".    
01 B2 PIC X(7) VALUE SPACES.    
PROCEDURE DIVISION.                
MAIN-PARA.                         
     DISPLAY B2(1:7) A1(7:01).     
     DISPLAY B2(1:6) A1(6:02).     
     DISPLAY B2(1:5) A1(5:03).     
     DISPLAY B2(1:4) A1(4:04).     
     DISPLAY B2(1:3) A1(3:05).     
     DISPLAY B2(1:2) A1(2:06).     
     DISPLAY B2(1:1) A1(1:07).     
     STOP RUN.                     
OUT PUT:
*********
       * 
      ** 
     *** 
    **** 
   ***** 
  ****** 
 ******* 
*********
IDENTIFICATION DIVISION.        
PROGRAM-ID. NMR3.               
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A1 PIC X(7) VALUE "123457".  
01 B2 PIC X(7) VALUE "ZEROS".   
PROCEDURE DIVISION.             
MAIN-PARA.                      
     DISPLAY B2(1:7) A1(7:01).  
     DISPLAY B2(1:6) A1(6:02).  
     DISPLAY B2(1:5) A1(5:03).  
     DISPLAY B2(1:4) A1(4:04).  
     DISPLAY B2(1:3) A1(3:05).  
     DISPLAY B2(1:2) A1(2:06).  
     DISPLAY B2(1:1) A1(1:07).  
     STOP RUN.                  
OUT PUT:
ZEROS  
ZEROS 7
ZEROS57
ZERO457
ZER3457
ZE23457
Z123457
IDENTIFICATION DIVISION.            
PROGRAM-ID. NMR3.                   
ENVIRONMENT DIVISION.               
DATA DIVISION.                      
WORKING-STORAGE SECTION.            
01 A1 PIC X(7) VALUE "123457".      
01 B2 PIC X(7).                     
PROCEDURE DIVISION.                 
MAIN-PARA.                          
     DISPLAY B2(1:7) A1(7:01).      
     DISPLAY B2(1:6) A1(6:02).      
     DISPLAY B2(1:5) A1(5:03).      
     DISPLAY B2(1:4) A1(4:04).      
     DISPLAY B2(1:3) A1(3:05).      
     DISPLAY B2(1:2) A1(2:06).      
     DISPLAY B2(1:1) A1(1:07).      
     STOP RUN.                      
OUT PUT:
*******
       
      7
     57
    457
   3457
  23457
 123457
OUT PUT:
IF C AND D ARE EMPTY
+++++++++ 
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
++++++++  
OUT PUT :
+++++++++S        
++++++++S         
++++++++SS        
++++++++SES       
++++++++SCES      
++++++++SACES     
++++++++SPACES    
++++++++SSPACES   

COBOL PERFOROM

1)IDENTIFICATION DIVISION.                   
PROGRAM-ID. PERFOM.                        
ENVIRONMENT DIVISION.                      
DATA DIVISION.                             
WORKING-STORAGE SECTION.                   
PROCEDURE DIVISION.                        
    DISPLAY "HI VISHNU".                   
    PERFORM DISP-HELLO-PAPA.               
    PERFORM DISP-HIHI.                     
    PERFORM DISP-HAHA.                     
    PERFORM DISP-INDIA.                    
    DISPLAY "GOOD BYE PAPA".               
    DISPLAY "END OF THE PGM".              
    STOP RUN.                              
DISP-HELLO-PAPA.                           
    DISPLAY "HELLO HOW ARE YOU".           
DISP-HIHI.                                 
    DISPLAY "HI THIS IS VISHNU VARDHAN".   
DISP-INDIA.                                
    DISPLAY "I LOVE INDIA".                
DISP-HAHA.                                 
    DISPLAY "TECSACON TECSACON TECSACON".  
OUT PUT:
****************************
HI VISHNU                   
HELLO HOW ARE YOU           
HI THIS IS VISHNU VARDHAN   
TECSACON TECSACON TECSACON  
I LOVE INDIA                
GOOD BYE PAPA               
END OF THE PGM              
****************************
2)IDENTIFICATION DIVISION.                  
PROGRAM-ID. GOTO.                         
ENVIRONMENT DIVISION.                     
DATA DIVISION.                            
WORKING-STORAGE SECTION.                  
PROCEDURE DIVISION.                       
    DISPLAY "HI VISHNU".                  
    GO TO DISP-HELLO-PAPA.                
    DISPLAY "HI HI HI HI".                
DISP-HELLO-PAPA.                          
    DISPLAY "I AM GOOD BOY IN THE CLASS". 
    STOP RUN.                             
OUT PUT:
HI VISHNU                  
I AM GOOD BOY IN THE CLASS 
OUT PUT:2
HI VISHNU                       
I AM GOOD BOY IN THE CLASS      
VISHNU IS GOOD BOY IN THE CLASS
 IDENTIFICATION DIVISION.         
 PROGRAM-ID. PERFOMA.             
 ENVIRONMENT DIVISION.            
 DATA DIVISION.                   
 WORKING-STORAGE SECTION.         
 PROCEDURE DIVISION.              
     DISPLAY "HI VISHNU".         
     PERFORM PARA-1.              
     PERFORM PARA-2.              
     PERFORM PARA-3.              
     DISPLAY "PARA-1 EXECUTED".   
     DISPLAY "PARA-2 EXECUTED".   
     DISPLAY "PARA-3 EXECUTED".   
     STOP RUN.                    
 PARA-1.                          
     DISPLAY "I BELONG TO HYD".   
     DISPLAY "I AM FROM INDIA".   
     DISPLAY "I LOVE FOOD".       
     DISPLAY "I AM A GOOD BOY".   
 PARA-2.                          
     DISPLAY "I BELONG TO HYD".   
     DISPLAY "I AM FROM INDIA".   
     DISPLAY "I LOVE FOOD".        
OUT PUT:
HI VISHNU       
I BELONG TO HYD 
I AM FROM INDIA 
I LOVE FOOD     
I AM A GOOD BOY 
I BELONG TO HYD 
I AM FROM INDIA 
I LOVE FOOD     

I AM A GOOD BOY 
I BELONG TO HYD 
I AM FROM INDIA 
I LOVE FOOD     
I AM A GOOD BOY 
PARA-1 EXECUTED 
PARA-2 EXECUTED 
PARA-3 EXECUTED 
IDENTIFICATION DIVISION.                                     
PROGRAM-ID. PERFOMA.                                         
ENVIRONMENT DIVISION.                                        
DATA DIVISION.                                               
WORKING-STORAGE SECTION.                                     
01 WS-AMT-IN-RS PIC 9(8)V9(2).                               
01 WS-AMT-IN-DOLLAR PIC 9(5)V9(2).                           
01 WS-CONV-RATE PIC 9(2)V99 VALUE 45.50.                     
PROCEDURE DIVISION.                                          
A0000-FIRST-PARA.                                            
    PERFORM B0000-GET-VALUE.                                 
    PERFORM C0000-CONVERT-DOLLAR.                            
    PERFORM D0000-DISP-RESULT.                               
    STOP RUN.                                                
B0000-GET-VALUE.                                             
    DISPLAY "ENTER AMOUNT IN DOLLARS".                       
    ACCEPT WS-AMT-IN-DOLLAR.                                 
C0000-CONVERT-DOLLAR.                                        
    COMPUTE WS-AMT-IN-RS = WS-AMT-IN-DOLLAR * WS-CONV-RATE.  
D0000-DISP-RESULT.                                           
    DISPLAY "AMOUNT IN RUPEES: RS" WS-AMT-IN-RS.             
OUT PUT:
ENTER AMOUNT IN DOLLARS       
AMOUNT IN RUPEES: RS0159250000

IDENTIFICATION DIVISION.     
PROGRAM-ID. INLINE.          
ENVIRONMENT DIVISION.        
DATA DIVISION.               
WORKING-STORAGE SECTION.     
01 A PIC 9(4) VALUE 4500.    
01 B PIC 9(4) VALUE 200.     
01 C PIC 9(4) VALUE 10.      
PROCEDURE DIVISION.          
    PERFORM                  
    ADD A TO B               
    DISPLAY B                
    ADD B TO C               
    DISPLAY C                
    MULTIPLY C BY A          
    DISPLAY A                
    DISPLAY C                
    END-PERFORM.             
    STOP RUN. 
OUT PUT:
4700 
4710 
5000 
4710 
IDENTIFICATION DIVISION.                                   
PROGRAM-ID. INLINE.                                        
ENVIRONMENT DIVISION.                                      
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 A PIC 9(2) VALUE 24.                                    
PROCEDURE DIVISION.                                        
    PERFORM 5 TIMES                                        
    DISPLAY "HI HI HARISH IS VERY INTELEGENT IN THE CALLS" 
    PERFORM PARA-1                                         
    PERFORM PARA-2                                         
    END-PERFORM.                                           
    STOP RUN.                                              
PARA-1.                                                    
    DISPLAY "HARISH IS TOPER OF TECSOCON ".                
    DISPLAY "HARISH IS VERY GOOD BOY".                     
PARA-2.                                                    
    DISPLAY "APPLE".                                       
    DISPLAY "DOG IS GOOD FRIEND OF ".                      
OUT PUT:
HI HI HARISH IS VERY INTELEGENT IN THE CALLS  
HARISH IS TOPER OF TECSOCON                   
HARISH IS VERY GOOD BOY                       
APPLE                                         
DOG IS GOOD FRIEND OF                         
HI HI HARISH IS VERY INTELEGENT IN THE CALLS 

IDENTIFICATION DIVISION.             
PROGRAM-ID. INLINE.                  
ENVIRONMENT DIVISION.                
DATA DIVISION.                       
WORKING-STORAGE SECTION.             
01 NUM-1 PIC 9(3) VALUE 345.         
01 NUM-2 PIC 9(3) VALUE 456.         
01 MAX PIC 9(3).                     
PROCEDURE DIVISION.                  
    PERFORM                          
    MOVE NUM-1 TO MAX                
    IF NUM-2 > MAX THEN MOVE         
    NUM-2 TO MAX                     
    DISPLAY "MAXIMUM IS :" MAX       
    END-IF                           
    END-PERFORM.                     
    STOP RUN.                                       
OUT PUT:
*****************
MAXIMUM IS :456  
*****************
IDENTIFICATION DIVISION.                           
PROGRAM-ID. NESTED1                                
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
PROCEDURE DIVISION.                                
TOPLEVE1.                                          
    DISPLAY "IN TOPLEVEL.STARTING TO RUN PROGRAM". 
    PERFORM ONELEVELDOWN.                          
    DISPLAY "BACK IN TOPLEVEL".                    
    STOP RUN.                                      
TWOLEVELSDOWN.                                     
    DISPLAY ">>>>>>>>>>>>NOW IN TWOLEVELSDOWN.".   
ONELEVELDOWN.                                      
    DISPLAY ">>>>>>>> NOW IN ONELEVELDOWN"         
    PERFORM TWOLEVELSDOWN                          
    DISPLAY ">>>>>BACK IN ONELEVELDOWN".           
OUT PUT:
IN TOPLEVEL.STARTING TO RUN PROGRAM
>>>>>>>> NOW IN ONELEVELDOWN       
>>>>>>>>>>>>NOW IN TWOLEVELSDOWN.  
>>>>>BACK IN ONELEVELDOWN          
BACK IN TOPLEVEL                   
 IDENTIFICATION DIVISION.                              
PROGRAM-ID. NESTED1                                   
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 NUMOFTIMES PIC 9 VALUE 5.                          
PROCEDURE DIVISION.                                   
BEGIN.                                                
    DISPLAY "STARTING TO RUN PROGRAM"                 
    PERFORM 3 TIMES                                   
    DISPLAY ">>>>>>>>THIS IS AN IN LINE PERFORM"      
    END-PERFORM                                       
    DISPLAY "FINISHED IN LINE PERFORM"                
    PERFORM OUTOFLINEG 6 TIMES                        
    DISPLAY "BACK IN BEGIN. ABOUT TO STOP".           
    GOBACK.                                           
OUTOFLINEG.                                           
    DISPLAY ">>>>>>>. THES IS AN OUT OF LINE PERFORM".
OUT PUT:
STARTING TO RUN PROGRAM                
>>>>>>>>THIS IS AN IN LINE PERFORM     
>>>>>>>>THIS IS AN IN LINE PERFORM     
>>>>>>>>THIS IS AN IN LINE PERFORM     
FINISHED IN LINE PERFORM               
>>>>>>>. THES IS AN OUT OF LINE PERFORM
>>>>>>>. THES IS AN OUT OF LINE PERFORM
>>>>>>>. THES IS AN OUT OF LINE PERFORM
>>>>>>>. THES IS AN OUT OF LINE PERFORM
>>>>>>>. THES IS AN OUT OF LINE PERFORM
>>>>>>>. THES IS AN OUT OF LINE PERFORM
BACK IN BEGIN. ABOUT TO STOP    
  IDENTIFICATION DIVISION.                  
PROGRAM-ID. PERFOM.                       
ENVIRONMENT DIVISION.                     
DATA DIVISION.                            
WORKING-STORAGE SECTION.                  
01 NUM PIC 9(2).                          
01 N   PIC 9(2).                          
01 R   PIC 9(2).                          
PROCEDURE DIVISION.                       
    ACCEPT NUM.                           
    PERFORM P1.                           
    STOP RUN.                             
P1.                                       
    DIVIDE 2 INTO NUM GIVING N REMAINDER R
    IF R = 0                              
    DISPLAY NUM "IS EVE"                  
    ELSE                                  
    DISPLAY NUM "IS ODD"                  
    END-IF.                            
OUT PUT:
    4
IDENTIFICATION DIVISION.                
PROGRAM-ID. PERFOM.                     
ENVIRONMENT DIVISION.                   
DATA DIVISION.                          
WORKING-STORAGE SECTION.                
PROCEDURE DIVISION.                     
MAIN-PARA.                              
    DISPLAY "START OF PGM".             
    PERFORM A-LOVE THRU F-LOVE 2 TIMES  
    DISPLAY "END OF PGM".               
    STOP RUN.                           
A-LOVE.                                 
    DISPLAY "I LOVE YOU".               
B-LOVE.                                 
    DISPLAY "I LOVE INDIA".             
C-LOVE.                                 
    DISPLAY "1234567890".               
D-LOVE.                                 
    DISPLAY "APPLE".                    
E-LOVE.                                 
    DISPLAY "BAT".                      
F-LOVE.                                 
    DISPLAY "MALE".                     
                                        
OUT PUT:
START OF PGM  
I LOVE YOU    
I LOVE INDIA  
1234567890    
APPLE         
BAT           
MALE          
I LOVE YOU    
I LOVE INDIA  
1234567890    
APPLE         
BAT           
MALE          
END OF PGM
IDENTIFICATION DIVISION.         
PROGRAM-ID. PERFOM.              
ENVIRONMENT DIVISION.            
DATA DIVISION.                   
WORKING-STORAGE SECTION.         
01 WS-1 PIC 9 VALUE 0.           
PROCEDURE DIVISION.              
    PERFORM PARA-A UNTIL WS-1 = 4
    STOP RUN.                    
PARA-A.                          
    DISPLAY "TECSACON TECSACON". 
    ADD 1 TO WS-1.                
OUT PUT:
TECSACON TECSACON
TECSACON TECSACON
TECSACON TECSACON
TECSACON TECSACON
IDENTIFICATION DIVISION.                          
PROGRAM-ID. PERFOM.                               
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 CT PIC X(20) VALUE "CALIFORNIA CITY".          
01 CA PIC X(15).                                  
01 I  PIC 99.                                     
PROCEDURE DIVISION.                               
MP.                                               
    PERFORM PT VARYING I FROM 1 BY 1 UNTIL I > 15.
    STOP RUN.                                     
PT.                                               
    MOVE CT(I:) TO CA.                            
    DISPLAY CA.                                   
OUT PUT:
CALIFORNIA CITY
ALIFORNIA CITY 
LIFORNIA CITY  
IFORNIA CITY   
FORNIA CITY    
ORNIA CITY     
RNIA CITY      
NIA CITY       
IA CITY        
A CITY         
 CITY          
CITY           
ITY            
TY             
Y   
IDENTIFICATION DIVISION.                 
PROGRAM-ID. PERFOM.                      
ENVIRONMENT DIVISION.                    
DATA DIVISION.                           
WORKING-STORAGE SECTION.                 
01 WS-COUNT PIC 9(2) VALUE 0.            
PROCEDURE DIVISION.                      
0000-MAINLINE.                           
    DISPLAY "PROGRAM STARTING".          
    PERFORM 2100-DISPLAY WITH TEST BEFORE
    VARYING WS-COUNT FROM 1 BY 1 UNTIL   
    WS-COUNT > 3                         
    STOP RUN.                            
2100-DISPLAY.                            
    DISPLAY "THE COUNT NOW: " WS-COUNT.  
OUT PUT:
PROGRAM STARTING  
THE COUNT NOW: 01 
THE COUNT NOW: 02 
THE COUNT NOW: 03    
IDENTIFICATION DIVISION.                   
PROGRAM-ID. PERFOM.                        
ENVIRONMENT DIVISION.                      
DATA DIVISION.                             
WORKING-STORAGE SECTION.                   
01 WS-COUNT PIC 9(2) VALUE 0.              
PROCEDURE DIVISION.                        
0000-MAINLINE.                             
    DISPLAY "PROGRAM STARTING".            
    PERFORM 2100-DISPLAY WITH TEST AFTER   
    VARYING WS-COUNT FROM 1 BY 1 UNTIL     
    WS-COUNT > 3                           
    STOP RUN.                              
2100-DISPLAY.                              
    DISPLAY "THE COUNT NOW: " WS-COUNT.  
  
OUT PUT:
PROGRAM STARTING  
THE COUNT NOW: 01 
THE COUNT NOW: 02 
THE COUNT NOW: 03 
THE COUNT NOW: 04  
IDENTIFICATION DIVISION.                                         
PROGRAM-ID. PERFOM.                                              
ENVIRONMENT DIVISION.                                            
DATA DIVISION.                                                   
WORKING-STORAGE SECTION.                                         
01 WS-AMT-IN-RS PIC Z(8).9(2).                                   
01 WS-AMT-IN-DOLLAR PIC 9(5)V9(2).                               
01 WS-CONVERSION-RATE PIC 9(2)V99 VALUE 45.50.                   
PROCEDURE DIVISION.                                              
A0000-FIRST-PARA.                                                
    PERFORM B0000-GET-VALUE.                                     
    PERFORM C0000-CONVERT-DOLL.                                  
    PERFORM D0000-DISP-RESULT.                                   
    STOP RUN.                                                    
B0000-GET-VALUE.                                                 
    DISPLAY "ENTER AMOUNT IN DOLLARS".                           
    ACCEPT WS-AMT-IN-DOLLAR.                                     
C0000-CONVERT-DOLL.                                              
    COMPUTE WS-AMT-IN-RS = WS-AMT-IN-DOLLAR * WS-CONVERSION-RATE.
D0000-DISP-RESULT.                                               
    DISPLAY "AMOUNT IN RUPEES:" WS-AMT-IN-RS.                    
OUT PUT:
ENTER AMOUNT IN DOLLARS      
AMOUNT IN RUPEES: 1161828.85 
          
EVALUAE  

IDENTIFICATION DIVISION.                 
PROGRAM-ID. EVALUAE                      
ENVIRONMENT DIVISION.                    
DATA DIVISION.                           
WORKING-STORAGE SECTION.                 
01 TRANSACTION-CODE PIC X VALUE SPACES.  
PROCEDURE DIVISION.                      
    ACCEPT TRANSACTION-CODE.             
    EVALUATE TRANSACTION-CODE            
    WHEN 'A'                             
    DISPLAY "SB A / C "                  
    WHEN 'B'                             
    DISPLAY "RD A / C "                  
    WHEN 'C'                             
    DISPLAY "CURRENT A / C "             
    WHEN OTHER                           
    DISPLAY "UNDEFINED CHARACTER"        
    END-EVALUATE.                        
    STOP RUN.                            
OUT PUT:
*********
SB A / C

 IDENTIFICATION DIVISION.          
 PROGRAM-ID. DAE.                  
 ENVIRONMENT DIVISION.             
 DATA DIVISION.                    
 WORKING-STORAGE SECTION.          
 01 WEEK-DAY PIC 9.                
 PROCEDURE DIVISION.               
     ACCEPT WEEK-DAY.              
     EVALUATE WEEK-DAY             
     WHEN 1 DISPLAY "MONDAY"       
     WHEN 2 DISPLAY "TUESDAY"      
     WHEN 3 DISPLAY "WEDNESDAY"    
     WHEN 4 DISPLAY "THURSDAY"     
     WHEN 5 DISPLAY "FRIDAY"       
     WHEN 6 DISPLAY "SATURDAY"     
     WHEN 7 DISPLAY "SUNDAY"       
     WHEN OTHER DISPLAY "INVALID"  
     END-EVALUATE.                 
     STOP RUN.                      

OUT PUT :
MONDAY
IDENTIFICATION DIVISION.     
PROGRAM-ID. PLANET.          
ENVIRONMENT DIVISION.        
DATA DIVISION.               
WORKING-STORAGE SECTION.     
01 PLANT PIC X VALUE SPACE.  
   88 A VALUE '1'.           
   88 B VALUE '2'.           
   88 C VALUE '3'.           
   88 D VALUE '4'.           
   88 E VALUE '5'.           
   88 F VALUE '6'.           
   88 G VALUE '7'.           
   88 H VALUE '8'.           
   88 I VALUE '9'.           
PROCEDURE DIVISION.          
BEGIN.                       
    ACCEPT PLANT.            
    EVALUATE TRUE            
    WHEN A                   
    DISPLAY "MERCURY"        
    WHEN B                   
    DISPLAY "VENUS"          
    WHENC
     DISPLAY "EARTH"
D ISPLAY "MARS"      
WHEN E              
DISPLAY "JUPITER"   
WHEN F              
DISPLAY "SATURN"    
WHEN G              
DISPLAY "URANUS"    
WHEN H              
DISPLAY "NEPTUNE"   
WHEN I              
DISPLAY "A"         
WHEN G              
DISPLAY "NOT FOUND" 
END-EVALUATE.       
STOP RUN.           
OUT PUT:
MERCURY

IDENTIFICATION DIVISION.                               
PROGRAM-ID. COND.                                      
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 MARKS PIC 9(3) VALUE 0.                             
PROCEDURE DIVISION.                                    
    ACCEPT MARKS.                                      
    EVALUATE (MARKS > 400)                             
    WHEN TRUE DISPLAY "STUDENT SECORED 80% AND ABOVE"  
    WHEN TRUE DISPLAY "STUDENT SECORED LESS THAN 80%"  
    END-EVALUATE.                                      
    STOP RUN.                                          
OUT PUT:
STUDENT SECORED 80% AND ABOVE

IDENTIFICATION DIVISION.                                  
PROGRAM-ID. COND1.                                        
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 WS00-MARKS PIC 9(3) VALUE 081.                         
PROCEDURE DIVISION.                                       
A0000-MAIN-PARA.                                          
    EVALUATE TRUE                                         
    WHEN WS00-MARKS > 78                                  
    DISPLAY "YOU HAVE CLEARED EXAM WITH A GRADE"          
    WHEN ((WS00-MARKS > 64 ) AND (WS00-MARKS <= 79))      
    DISPLAY "YOU HAVE CLEARED THE EXAM WITH B GRADE"      
    WHEN OTHER                                            
    DISPLAY "SORRY YOU HAVE NOT CLEARED THE EXAM "        
    END-EVALUATE                                          
    DISPLAY "*******************************************" 
    STOP RUN.                                              
OUT PUT:
YOU HAVE CLEARED EXAM WITH A GRADE          
******************************************* 
OUT PUT < 79 099:
SORRY YOU HAVE NOT CLEARED THE EXAM 

IDENTIFICATION DIVISION.                   
PROGRAM-ID. COND2.                         
ENVIRONMENT DIVISION.                      
DATA DIVISION.                             
WORKING-STORAGE SECTION.                   
01 WS-N1 PIC 9(2)V9 VALUE 12.6.            
01 WS-N2 PIC 9(2)V9 VALUE 12.6.            
01 WS-N3 PIC 9(1)V9 VALUE 6.6.             
PROCEDURE DIVISION.                        
    EVALUATE (WS-N1 * WS-N2 ) / WS-N3      
    WHEN 24.0                              
    DISPLAY "VALUE IS :24.0545"            
    WHEN 27.2                              
    DISPLAY "VALUE IS :27.2"               
    WHEN 27.4                              
    DISPLAY "VALUE IS :27.4"               
    WHEN OTHER                             
    DISPLAY "VALUE IS UNKNOWN"             
    END-EVALUATE.                          
    STOP RUN.
 OUT PUT :
VALUE IS :24.0545
   
IDENTIFICATION DIVISION.                     
PROGRAM-ID. ARITHMATICALEX.                  
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 MARK PIC 9(3) VALUE 400.                  
01 TOTAL PIC 9(3) VALUE 500.                 
PROCEDURE DIVISION.                          
    EVALUATE (MARK / TOTAL) * 100            
    WHEN 100                                 
    DISPLAY "100 % MARKS SECURED BY STUDENT" 
    WHEN OTHER                               
    DISPLAY "STUDENT SCORED BELOW 100%"      
    END-EVALUATE.                            
    STOP RUN.                                                          
OUT PUT:
STUDENT SCORED BELOW 100%  
OUT PUT :
100 % MARKS SECURED BY STUDENT

IDENTIFICATION DIVISION.                    
PROGRAM-ID. ARITHMATICALEX.                 
ENVIRONMENT DIVISION.                       
DATA DIVISION.                              
WORKING-STORAGE SECTION.                    
01 MARK PIC 9(3) VALUE 470.                 
PROCEDURE DIVISION.                         
    EVALUATE (MARK > 400)                   
    WHEN TRUE                               
    DISPLAY "STUDENT SCORED 80% AND ABOVE"  
    WHEN FALSE                              
    DISPLAY "STUDENT SCORED LESS THEN 80%"  
    END-EVALUATE.                           
    STOP RUN.                               
OUT PUT:
STUDENT SCORED 80% AND ABOVE
IDENTIFICATION DIVISION.                          
PROGRAM-ID. EVAL.                                 
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 STUDENT1 PIC 9(3) VALUE 100.                   
01 STUDENT2 PIC 9(3) VALUE 50.                    
PROCEDURE DIVISION.                               
    EVALUATE 50                                   
    WHEN STUDENT1                                 
    DISPLAY "STUDENT SCORED 50% MARK IN SUBJECT1" 
    WHEN STUDENT2                                 
    DISPLAY "STUDENT SCORED 50% MARK IN SUBJECT2" 
    END-EVALUATE.                                 
    STOP RUN.                                      
OUT PUT:
STUDENT SCORED 50% MARK IN SUBJECT2
IDENTIFICATION DIVISION.                           
PROGRAM-ID. EVAL.                                  
ENVIRONMENT DIVISION.                              
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 TODAY PIC X(2).                                 
01 MONTH PIC 9(2).                                 
   88 WINTER-M VALUE 12,1,2.                       
   88 SPRING-M VALUE 3 THRU 5.                     
   88 SUMMER-M VALUE 6 THRU 8.                     
   88 AUTUMN-M VALUE 9 THRU 11.                    
PROCEDURE DIVISION.                                
    ACCEPT MONTH                                   
    EVALUATE TRUE                                  
    WHEN SPRING-M                                  
    DISPLAY "IT IS SPRING LET'S GO HIKING!!"       
    WHEN SUMMER-M                                  
    DISPLAY "IT IS SUMMRE LET'S GO FOR SWIMMING!!" 
    WHEN AUTUMN-M                                  
    DISPLAY "IT IS AUTUMN LET'S PLAY TENNIS!!"     
    WHEN WINTER-M                                  
    DISPLAY "IT WINTER LET'S GO SKIING!!"          
    END-EVALUATE.                                   

OUT PUT:
IT IS AUTUMN LET'S PLAY TENNIS!!

IDENTIFICATION DIVISION.                 
PROGRAM-ID. EVALUAE                      
ENVIRONMENT DIVISION.                    
DATA DIVISION.                           
WORKING-STORAGE SECTION.                 
01 TRANSACTION-CODE PIC X VALUE SPACES.  
PROCEDURE DIVISION.                      
    ACCEPT TRANSACTION-CODE.             
    EVALUATE TRANSACTION-CODE            
    WHEN 'A'                             
    DISPLAY "SB A / C "                  
    WHEN 'B'                             
    DISPLAY "RD A / C "                  
    WHEN 'C'                             
    DISPLAY "CURRENT A / C "             
    WHEN OTHER                           
    DISPLAY "UNDEFINED CHARACTER"        
    END-EVALUATE.                        
    STOP RUN.                            
OUT PUT:
*********
SB A / C

 IDENTIFICATION DIVISION.          
 PROGRAM-ID. DAE.                  
 ENVIRONMENT DIVISION.             
 DATA DIVISION.                    
 WORKING-STORAGE SECTION.          
 01 WEEK-DAY PIC 9.                
 PROCEDURE DIVISION.               
     ACCEPT WEEK-DAY.              
     EVALUATE WEEK-DAY             
     WHEN 1 DISPLAY "MONDAY"       
     WHEN 2 DISPLAY "TUESDAY"      
     WHEN 3 DISPLAY "WEDNESDAY"    
     WHEN 4 DISPLAY "THURSDAY"     
     WHEN 5 DISPLAY "FRIDAY"       
     WHEN 6 DISPLAY "SATURDAY"     
     WHEN 7 DISPLAY "SUNDAY"       
     WHEN OTHER DISPLAY "INVALID"  
     END-EVALUATE.                 
     STOP RUN.                      

OUT PUT :
MONDAY
IDENTIFICATION DIVISION.     
PROGRAM-ID. PLANET.          
ENVIRONMENT DIVISION.        
DATA DIVISION.               
WORKING-STORAGE SECTION.     
01 PLANT PIC X VALUE SPACE.  
   88 A VALUE '1'.           
   88 B VALUE '2'.           
   88 C VALUE '3'.           
   88 D VALUE '4'.           
   88 E VALUE '5'.           
   88 F VALUE '6'.           
   88 G VALUE '7'.           
   88 H VALUE '8'.           
   88 I VALUE '9'.           
PROCEDURE DIVISION.          
BEGIN.                       
    ACCEPT PLANT.            
    EVALUATE TRUE            
    WHEN A                   
    DISPLAY "MERCURY"        
    WHEN B                   
    DISPLAY "VENUS"          
    WHENC
     DISPLAY "EARTH"
D ISPLAY "MARS"      
WHEN E              
DISPLAY "JUPITER"   
WHEN F              
DISPLAY "SATURN"    
WHEN G              
DISPLAY "URANUS"    
WHEN H              
DISPLAY "NEPTUNE"   
WHEN I              
DISPLAY "A"         
WHEN G              
DISPLAY "NOT FOUND" 
END-EVALUATE.       
STOP RUN.           
OUT PUT:
MERCURY

IDENTIFICATION DIVISION.                               
PROGRAM-ID. COND.                                      
ENVIRONMENT DIVISION.                                  
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 MARKS PIC 9(3) VALUE 0.                             
PROCEDURE DIVISION.                                    
    ACCEPT MARKS.                                      
    EVALUATE (MARKS > 400)                             
    WHEN TRUE DISPLAY "STUDENT SECORED 80% AND ABOVE"  
    WHEN TRUE DISPLAY "STUDENT SECORED LESS THAN 80%"  
    END-EVALUATE.                                      
    STOP RUN.                                          
OUT PUT:
STUDENT SECORED 80% AND ABOVE

IDENTIFICATION DIVISION.                                  
PROGRAM-ID. COND1.                                        
ENVIRONMENT DIVISION.                                     
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 WS00-MARKS PIC 9(3) VALUE 081.                         
PROCEDURE DIVISION.                                       
A0000-MAIN-PARA.                                          
    EVALUATE TRUE                                         
    WHEN WS00-MARKS > 78                                  
    DISPLAY "YOU HAVE CLEARED EXAM WITH A GRADE"          
    WHEN ((WS00-MARKS > 64 ) AND (WS00-MARKS <= 79))      
    DISPLAY "YOU HAVE CLEARED THE EXAM WITH B GRADE"      
    WHEN OTHER                                            
    DISPLAY "SORRY YOU HAVE NOT CLEARED THE EXAM "        
    END-EVALUATE                                          
    DISPLAY "*******************************************" 
    STOP RUN.                                              
OUT PUT:
YOU HAVE CLEARED EXAM WITH A GRADE          
******************************************* 
OUT PUT < 79 099:
SORRY YOU HAVE NOT CLEARED THE EXAM 

IDENTIFICATION DIVISION.                   
PROGRAM-ID. COND2.                         
ENVIRONMENT DIVISION.                      
DATA DIVISION.                             
WORKING-STORAGE SECTION.                   
01 WS-N1 PIC 9(2)V9 VALUE 12.6.            
01 WS-N2 PIC 9(2)V9 VALUE 12.6.            
01 WS-N3 PIC 9(1)V9 VALUE 6.6.             
PROCEDURE DIVISION.                        
    EVALUATE (WS-N1 * WS-N2 ) / WS-N3      
    WHEN 24.0                              
    DISPLAY "VALUE IS :24.0545"            
    WHEN 27.2                              
    DISPLAY "VALUE IS :27.2"               
    WHEN 27.4                              
    DISPLAY "VALUE IS :27.4"               
    WHEN OTHER                             
    DISPLAY "VALUE IS UNKNOWN"             
    END-EVALUATE.                          
    STOP RUN.
 OUT PUT :
VALUE IS :24.0545
   
IDENTIFICATION DIVISION.                     
PROGRAM-ID. ARITHMATICALEX.                  
ENVIRONMENT DIVISION.                        
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 MARK PIC 9(3) VALUE 400.                  
01 TOTAL PIC 9(3) VALUE 500.                 
PROCEDURE DIVISION.                          
    EVALUATE (MARK / TOTAL) * 100            
    WHEN 100                                 
    DISPLAY "100 % MARKS SECURED BY STUDENT" 
    WHEN OTHER                               
    DISPLAY "STUDENT SCORED BELOW 100%"      
    END-EVALUATE.                            
    STOP RUN.                                                          
OUT PUT:
STUDENT SCORED BELOW 100%  
OUT PUT :
100 % MARKS SECURED BY STUDENT

IDENTIFICATION DIVISION.                    
PROGRAM-ID. ARITHMATICALEX.                 
ENVIRONMENT DIVISION.                       
DATA DIVISION.                              
WORKING-STORAGE SECTION.                    
01 MARK PIC 9(3) VALUE 470.                 
PROCEDURE DIVISION.                         
    EVALUATE (MARK > 400)                   
    WHEN TRUE                               
    DISPLAY "STUDENT SCORED 80% AND ABOVE"  
    WHEN FALSE                              
    DISPLAY "STUDENT SCORED LESS THEN 80%"  
    END-EVALUATE.                           
    STOP RUN.                               
OUT PUT:
STUDENT SCORED 80% AND ABOVE
IDENTIFICATION DIVISION.                          
PROGRAM-ID. EVAL.                                 
ENVIRONMENT DIVISION.                             
DATA DIVISION.                                    
WORKING-STORAGE SECTION.                          
01 STUDENT1 PIC 9(3) VALUE 100.                   
01 STUDENT2 PIC 9(3) VALUE 50.                    
PROCEDURE DIVISION.                               
    EVALUATE 50                                   
    WHEN STUDENT1                                 
    DISPLAY "STUDENT SCORED 50% MARK IN SUBJECT1" 
    WHEN STUDENT2                                 
    DISPLAY "STUDENT SCORED 50% MARK IN SUBJECT2" 
    END-EVALUATE.                                 
    STOP RUN.                                      
OUT PUT:
STUDENT SCORED 50% MARK IN SUBJECT2
IDENTIFICATION DIVISION.                           
PROGRAM-ID. EVAL.                                  
ENVIRONMENT DIVISION.                              
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 TODAY PIC X(2).                                 
01 MONTH PIC 9(2).                                 
   88 WINTER-M VALUE 12,1,2.                       
   88 SPRING-M VALUE 3 THRU 5.                     
   88 SUMMER-M VALUE 6 THRU 8.                     
   88 AUTUMN-M VALUE 9 THRU 11.                    
PROCEDURE DIVISION.                                
    ACCEPT MONTH                                   
    EVALUATE TRUE                                  
    WHEN SPRING-M                                  
    DISPLAY "IT IS SPRING LET'S GO HIKING!!"       
    WHEN SUMMER-M                                  
    DISPLAY "IT IS SUMMRE LET'S GO FOR SWIMMING!!" 
    WHEN AUTUMN-M                                  
    DISPLAY "IT IS AUTUMN LET'S PLAY TENNIS!!"     
    WHEN WINTER-M                                  
    DISPLAY "IT WINTER LET'S GO SKIING!!"          
    END-EVALUATE.                                   

OUT PUT:
IT IS AUTUMN LET'S PLAY TENNIS!!
SUB PGM:
IDENTIFICATION DIVISION.                
PROGRAM-ID. CSUBPGM.                    
ENVIRONMENT DIVISION.                   
DATA DIVISION.                          
PROCEDURE DIVISION.                     
      DISPLAY 'THIS IS SUB PROGRAM'.    
      DISPLAY "THIS IS CSUBPGM OF CALL".
      DISPLAY "VISHNU VARDHAN".         
      DISPLAY "INDIAN".                 
      GOBACK.
MAIN PGM:
IDENTIFICATION DIVISION.                                     
PROGRAM-ID. CMAINPGM.                                        
ENVIRONMENT DIVISION.                                        
DATA DIVISION.                                               
PROCEDURE DIVISION.                                          
      DISPLAY '********************************************'.
      DISPLAY 'THIS IS MAIN PROGRAM'.                        
      CALL 'CSUBPGM'.                                        
      DISPLAY 'BACK TO MAIN PROGRAM'.                        
      DISPLAY '********************************************'.
      STOP RUN.                                                                         
OUT PUT:
THIS IS MAIN PROGRAM     
THIS IS SUB PROGRAM      
THIS IS CSUBPGM OF CALL  
VISHNU VARDHAN           
INDIAN                   
BACK TO MAIN PROGRAM    
SUBPGM
IDENTIFICATION DIVISION.                   
PROGRAM-ID. CALLSUB.                       
ENVIRONMENT DIVISION.                      
DATA DIVISION.                             
PROCEDURE DIVISION.                        
      DISPLAY 'THIS IS SUB PROGRAM'.       
      DISPLAY "THIS IS SECON PGM OF CALL". 
      DISPLAY "THIS IS CSUBPGM OF CALL".   
      DISPLAY "VISHNU VARDHAN".            
      DISPLAY "INDIAN".                    
      GOBACK.                              
MAIN PGM:
IDENTIFICATION DIVISION.             
PROGRAM-ID. CLLMAIN.                 
ENVIRONMENT DIVISION.                
DATA DIVISION.                       
PROCEDURE DIVISION.                  
      DISPLAY '**********************
      DISPLAY 'THIS IS MAIN PROGRAM'.
      CALL 'CALLSUB'.                
      DISPLAY 'BACK TO MAIN PROGRAM'.
      DISPLAY "121211212".           
      STOP RUN.                      
OUT PUT:
**************************
THIS IS MAIN PROGRAM      
THIS IS SUB PROGRAM       
THIS IS SECON PGM OF CALL 
THIS IS CSUBPGM OF CALL   
VISHNU VARDHAN            
INDIAN                    
BACK TO MAIN PROGRAM      
121211212 

IDENTIFICATION DIVISION.             
PROGRAM-ID. CLLDM.                   
ENVIRONMENT DIVISION.                
DATA DIVISION.                       
WORKING-STORAGE SECTION.             
01 A PIC X(4).                       
PROCEDURE DIVISION.                  
    MOVE 'DEPT' TO A.                
    DISPLAY A.                       
    CALL 'CALLED' USING BY CONTENT A.
    DISPLAY A.                       
    STOP RUN.                     
IDENTIFICATION DIVISION.             
PROGRAM-ID. CALLED.                  
DATA DIVISION.                       
LINKAGE SECTION.                     
01 A PIC X(4).                       
PROCEDURE DIVISION USING A.          
    DISPLAY A.                       
    MOVE '1234' TO A.                
    DISPLAY A.                       
END PROGRAM CALLED.                  
END PROGRAM CLLDM.                                   
OUT PUT:
DEPT 
DEPT 
1234 
DEPT 
IDENTIFICATION DIVISION.                 
PROGRAM-ID. CLLDM1.                      
ENVIRONMENT DIVISION.                    
DATA DIVISION.                           
WORKING-STORAGE SECTION.                 
01 A PIC X(4).                           
PROCEDURE DIVISION.                      
    MOVE 'DEPT' TO A.                    
    DISPLAY A.                           
    CALL 'CALLED' USING BY REFERENCE A.  
    DISPLAY A.                           
    STOP RUN.                            
IDENTIFICATION DIVISION.                 
PROGRAM-ID. CALLED.                      
DATA DIVISION.                           
LINKAGE SECTION.                         
01 A PIC X(4).                           
PROCEDURE DIVISION USING A.              
    DISPLAY A.                           
    MOVE '1234' TO A.                    
    DISPLAY A.                           
END PROGRAM CALLED.                      
END PROGRAM CLLDM1.                      
SUB PGM:
IDENTIFICATION DIVISION.                       
PROGRAM-ID. CALLED.                            
ENVIRONMENT DIVISION.                          
DATA DIVISION.                                 
WORKING-STORAGE SECTION.                       
01 LI00-NAME PIC X(20) VALUE SPACES.           
01 LI00-AGE PIC 9(3) VALUE ZEROES.             
PROCEDURE DIVISION.                            
A000-MAIN-PARA.                                
    DISPLAY "*******************************". 
    DISPLAY "HI. YOUR NAME IS : . LI00-NAME".  
    DISPLAY "AND YOUR AGE IS :  . LI00-AGE".   
    DISPLAY "*******************************". 
IDENTIFICATION DIVISION.                 
PROGRAM-ID. CALLER.                      
ENVIRONMENT DIVISION.                    
DATA DIVISION.                           
WORKING-STORAGE SECTION.                 
01 ELEMENTS-TO-CALLED-PROG.              
   06 WS00-NAME PIC X(15).               
   06 WS00-AGE PIC X(3).                 
PROCEDURE DIVISION.                      
A000-MAIN-PARA.                          
    MOVE "VISHNU VARDHSN" TO WS00-NAME   
    MOVE "22"   TO WS00-AGE              
    CALL "CALLED"                        
    USING WS00-NAME , WS00-AGE.          
    STOP RUN.                            
OUT PUT:
******************************* 
HI. YOUR NAME IS : . LI00-NAME  
AND YOUR AGE IS :  . LI00-AGE   
******************************* 
IDENTIFICATION DIVISION.       
PROGRAM-ID. SUBPGM.            
ENVIRONMENT DIVISION.          
DATA DIVISION.                 
WORKING-STORAGE SECTION.       
LINKAGE SECTION.               
01 INREC.                      
   02 A PIC 99.                
   02 B PIC 99.                
   02 C PIC 999.               
PROCEDURE DIVISION USING INREC.
MAIN.                          
    COMPUTE C = A * B.         
    DISPLAY C.                 
    GOBACK.                    
IDENTIFICATION DIVISION.      
PROGRAM-ID. CALLM.            
ENVIRONMENT DIVISION.         
DATA DIVISION.                
WORKING-STORAGE SECTION.      
01 INREC.                     
   02 A PIC 99.               
   02 B PIC 99.               
   02 C PIC 999.              
PROCEDURE DIVISION.           
MAIN.                         
    ACCEPT A.                 
    ACCEPT B.                 
    CALL 'SUBPGM' USING INREC.
    STOP RUN.                 
OUT PUT:
748

FUNCATION.

IDENTIFICATION DIVISION.                           
PROGRAM-ID. FUNC.                                  
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 CSTRING PIC X(22) VALUE 'THIS IS COBOL STRING'. 
01 VAR1 PIC 9(2).                                  
PROCEDURE DIVISION.                                
    COMPUTE VAR1 = FUNCTION LENGTH(CSTRING).       
    DISPLAY VAR1.                                  
    STOP RUN.                                      
OUT PUT:
22
IDENTIFICATION DIVISION.                    
PROGRAM-ID. FUNC.                           
DATA DIVISION.                              
WORKING-STORAGE SECTION.                    
01 CSTRING PIC 9(4)V99 VALUE 56.87.         
01 VAR1 PIC 9(2).                           
PROCEDURE DIVISION.                         
    COMPUTE VAR1 = FUNCTION LENGTH(CSTRING).l
    DISPLAY VAR1.                           
    STOP RUN.                               
OUT PUT:
06
IDENTIFICATION DIVISION.                           
PROGRAM-ID. FUNC3.                                 
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 CSTRING PIC X(24) VALUE 'THIS IS COBOL STRING'. 
PROCEDURE DIVISION.                                
    DISPLAY FUNCTION UPPER-CASE(CSTRING).          
    DISPLAY FUNCTION LOWER-CASE(CSTRING).          
    STOP RUN.                                      
OUT 

PUT:
THIS IS COBOL STRING 
this is cobol string 

IDENTIFICATION DIVISION.                            
PROGRAM-ID. FUNC.                                   
DATA DIVISION.                                      
WORKING-STORAGE SECTION.                            
01 CSTRING PIC X(24) VALUE 'THIS IS COBOL STRING'.  
PROCEDURE DIVISION.                                 
    DISPLAY FUNCTION REVERSE(CSTRING).              
    STOP RUN.                                       
OUT PUT:
GNIRTS LOBOC SI SIHT  

OUT PUT:
GNIRTS 

IDENTIFICATION DIVISION.                     
PROGRAM-ID. FUNC4.                           
DATA DIVISION.                               
WORKING-STORAGE SECTION.                     
01 WS-D PIC 9(2) VALUE 10.                   
01 WS-X PIC 9(9).                            
PROCEDURE DIVISION.                          
    COMPUTE WS-X = FUNCTION FACTORIAL(WS-D). 
    DISPLAY 'FACTORIAL IS :' WS-X.           
    STOP RUN.                                
OUT PUT:
FACTORIAL IS :003628800 

IDENTIFICATION DIVISION.                              
PROGRAM-ID. FUNC5.                                    
DATA DIVISION.                                        
WORKING-STORAGE SECTION.                              
01 A PIC 9(2) VALUE 6.                                
01 B PIC 9(2) VALUE 5.                                
01 C PIC 9(2) VALUE 4.                                
01 D PIC 9(2) VALUE 5.                                
01 E PIC 9(2) VALUE 10.                               
01 WS-X PIC 9(2).                                     
PROCEDURE DIVISION.                                   
    COMPUTE WS-X = FUNCTION MEAN ( A , B  , C , D  E).
    DISPLAY "MEAN IS :" WS-X.                         
    STOP RUN.                                         
OUT PUT:
MEAN IS :06
IDENTIFICATION DIVISION.                                         
PROGRAM-ID. FUNC5.                                               
DATA DIVISION.                                                   
WORKING-STORAGE SECTION.                                         
01 WS-INTEGER1 PIC S9(2) VALUE -1.                               
01 WS-INTEGER2 PIC S9(2) VALUE -10.                              
01 WS-RESULT PIC 9(2).                                           
PROCEDURE DIVISION.                                              
    COMPUTE WS-RESULT = FUNCTION REM ( WS-INTEGER1, WS-INTEGER2).
    DISPLAY 'REM IS :' WS-RESULT.                                
    STOP RUN.  
IDENTIFICATION DIVISION.                                        
PROGRAM-ID. FUNC5.                                              
DATA DIVISION.                                                  
WORKING-STORAGE SECTION.                                        
01 WS-INTEGER1 PIC 9(2) VALUE 25.                               
01 WS-INTEGER2 PIC 9(2) VALUE 10.                               
01 WS-RESULT PIC 9(2).                                          
PROCEDURE DIVISION.                                             
    COMPUTE WS-RESULT = FUNCTION MOD( WS-INTEGER1, WS-INTEGER2).
    DISPLAY 'MOD IS :' WS-RESULT.                               
    STOP RUN.                                                                                                     
OUT PUT :
MOD IS :05  

OUT PUT:
REM IS :01

IDENTIFICATION DIVISION.                               
PROGRAM-ID. FUNC5.                                     
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 IRESULT PIC 9(5).                                   
01 INTEARRAY VALUE '1223037865'.                       
   02 IELEMENT OCCURS 5 TIMES PIC 99.                  
PROCEDURE DIVISION.                                    
    COMPUTE IRESULT = FUNCTION SUM(IELEMENT (ALL) ).   
    DISPLAY 'SUM VALUE IS ' IRESULT.                   
    STOP RUN.                                          
OUT PUT:
SUM VALUE IS 00181
 IDENTIFICATION DIVISION.                             
PROGRAM-ID. FUNC5.                                   
DATA DIVISION.                                       
WORKING-STORAGE SECTION.                             
01 IRESULT PIC 9(2).                                 
01 INTEARRAY VALUE '122303017865'.                   
   02 IELEMENT OCCURS 6 TIMES PIC 99.                
PROCEDURE DIVISION.                                  
    COMPUTE IRESULT = FUNCTION MIN(IELEMENT (ALL) ). 
    DISPLAY 'MIN VALUE IS ' IRESULT.                 
    STOP RUN.                                        
OUT PUT:
MIN VALUE IS 01
IDENTIFICATION DIVISION.                           
PROGRAM-ID. FUNC5.                                 
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 IRESULT PIC 9(3).                               
01 INTEARRAY   VALUE '1223037865'.                 
   02 IELEMENT OCCURS 5 TIMES PIC 99.              
PROCEDURE DIVISION.                                
    COMPUTE IRESULT = FUNCTION MAX(IELEMENT(ALL)). 
    DISPLAY 'MAX VALUE IS:' IRESULT.               
    STOP RUN.                                       
OUT PUT:
MAX VALUE IS:078

IDENTIFICATION DIVISION.                                       
PROGRAM-ID. FUNC5.                                             
DATA DIVISION.                                                 
WORKING-STORAGE SECTION.                                       
01 DATEANDTIMEC.                                               
  02 DATE1.                                                    
    05 YEARC PIC 9(4).                                         
    05 MONTHC PIC 99.                                          
    05 DATEC PIC 99.                                           
  02 TIME1.                                                    
    05 HOURC PIC 99.                                           
    05 MINUTEC PIC 99.                                         
    05 SECONDC PIC 99.                                         
PROCEDURE DIVISION.                                            
    MOVE FUNCTION CURRENT-DATE TO DATEANDTIMEC.                
    DISPLAY 'CURRENT-DATE IS :' YEARC '/' MONTHC '/' DATEC.    
    DISPLAY 'CURRENT-TIME IS :' HOURC '/' MINUTEC '/' SECONDC. 
    STOP RUN.                                                  
OUT PUT:
CURRENT-DATE IS :2022/12/15 
CURRENT-TIME IS :20/02/33
IDENTIFICATION DIVISION.                                         
PROGRAM-ID. FUNC5.                                               
DATA DIVISION.                                                   
WORKING-STORAGE SECTION.                                         
01 BIRTHDAY.                                                     
   02 YYYY PIC 9(4).                                             
   02 MMDD PIC 9(4).                                             
01 TODAY.                                                        
   02 YYYY PIC 9(4).                                             
   02 MMDD PIC 9(4).                                             
01 AGE PIC ZZ9.                                                  
PROCEDURE DIVISION.                                              
    DISPLAY "WHEN IS YOUR BIRTHDAY ".                            
    ACCEPT BIRTHDAY .                                            
    MOVE FUNCTION CURRENT-DATE TO TODAY.                         
    IF MMDD OF BIRTHDAY <= MMDD OF TODAY THEN COMPUTE AGE = YYYY 
    OF TODAY - YYYY OF BIRTHDAY                                  
    ELSE                                                         
    COMPUTE AGE = YYYY OF TODAY - YYYY OF BIRTHDAY               
    END-IF.                                                      
    DISPLAY "YOU ARE " AGE " YEARS OLD".                         
    STOP RUN.                                                        
OUT PUT:
WHEN IS YOUR BIRTHDAY 
YOU ARE  22 YEARS OLD 
IDENTIFICATION DIVISION.        
PROGRAM-ID. FUNC5.              
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 EDITING-DISPLAY.             
   02 PIC X(6) VALUE  "YEAR".   
   02 PIC 9(4).                 
   02 PIC X(7) VALUE "MONTH".   
   02 MONTH PIC 9(2).           
   02 PIC X(5) VALUE "DAY".     
   02 MONTH-DAY PIC 9(2).       
   02 PIC X(6) VALUE "HOUR".    
   02 HOUR PIC 9(2).            
   02 PIC X(8) VALUE "MINUTE".  
   02 MINUTE PIC 9(2).          
   02 PIC X(8) VALUE "SECOND".  
   02 SECOND PIC 9(2).          
01 CURRENT-DATE-AND-TIME.       
     02 YEAR PIC 9(4).          
     02 MONTH PIC 9(2).         
     02 MONTH-DAY PIC 9(2).     
     02 HOUR PIC 9(2).          
     02 MINUTE PIC 9(2).
     02 SECOND PIC 9(2).                                
PROCEDURE DIVISION.                                     
    MOVE FUNCTION CURRENT-DATE TO CURRENT-DATE-AND-TIME.
MOVE CORRESPONDING CURRENT-DATE-AND-TIME TO EDITING-DISPLAY. 
DISPLAY "THE CURRENT DATE AND TIME ARE".                     
DISPLAY EDITING-DISPLAY ".".                                 
DISPLAY FUNCTION CURRENT-DATE.                               
STOP RUN.                                                            
OUT PUT:
THE CURRENT DATE AND TIME ARE                           
YEAR      MONTH  12DAY  16HOUR  10MINUTE  38SECOND  24. 
2022121610382501-0600    
IDENTIFICATION DIVISION.                                   
PROGRAM-ID. FUNC5.                                         
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 WS-DATE PIC 9(8) VALUE 20221216.                        
01 WS-INTEGER-DATE PIC 9(8).                               
PROCEDURE DIVISION.                                        
    COMPUTE                                                
    WS-INTEGER-DATE = FUNCTION INTEGER-OF-DATE(WS-DATE)    
    DISPLAY "GREGORIAN TO INTEGER" WS-INTEGER-DATE.        
    STOP RUN.                                              
OUT PUT:
GREGORIAN TO INTEGER00154117 
IDENTIFICATION DIVISION.                               
PROGRAM-ID. FUNC5.                                     
DATA DIVISION.                                         
WORKING-STORAGE SECTION.                               
01 WS-INTEGER-DATE PIC 9(8) VALUE 00154117.            
01 WS-DATE PIC 9(8).                                   
PROCEDURE DIVISION.                                    
    COMPUTE                                            
    WS-DATE = FUNCTION DATE-OF-INTEGER(WS-INTEGER-DATE)
    DISPLAY " INTEGER TO GREGORIAN" WS-DATE.           
    STOP RUN.                                           
OUT PUT:
INTEGER TO GREGORIAN20221216    
IDENTIFICATION DIVISION.                                  
PROGRAM-ID. FUNC5.                                        
DATA DIVISION.                                            
WORKING-STORAGE SECTION.                                  
01 WS-JULDATE PIC 9(8) VALUE 02022350.                    
01 WS-INTEGER-DATE PIC 9(8).                              
PROCEDURE DIVISION.                                       
    COMPUTE                                               
    WS-INTEGER-DATE = FUNCTION INTEGER-OF-DAY(WS-JULDATE) 
    DISPLAY "JULIAN TO INTEGER" WS-INTEGER-DATE.          
    STOP RUN.                                             
OUT PUT:
JULIAN TO INTEGER00154117  
IDENTIFICATION DIVISION.                                 
PROGRAM-ID. FUNC5.                                       
DATA DIVISION.                                           
WORKING-STORAGE SECTION.                                 
01 WS-INTEGER-DATE PIC 9(8) VALUE 00154117.              
01 WS-JULDATE PIC 9(8) .                                 
PROCEDURE DIVISION.                                      
    COMPUTE                                              
    WS-JULDATE = FUNCTION DAY-OF-INTEGER(WS-INTEGER-DATE)
    DISPLAY "INTEGER TO JULIAN" WS-JULDATE.              
    STOP RUN.                                            
OUT PUT:   
INTEGER TO JULIAN02022350 
IDENTIFICATION DIVISION.                                       
PROGRAM-ID. EVBILL.                                            
DATA DIVISION.                                                 
WORKING-STORAGE SECTION.                                       
01 ACCOUNT-DETAILS.                                            
   02 AR-NO PIC 9(8) VALUE 6560524.                            
   02 ACC-ID PIC 9(10) VALUE 2479665356.                       
   02 MR-COD PIC 9(8) VALUE 14012846.                          
01 PARSONAL-DETAILS.                                           
   02 NAME PIC A(15) VALUE 'VISHNU VARDHAN'.                   
   02 ADDRSS PIC X(34) VALUE "#11C 100FT RINGROAD BTM2NSTAGE". 
01 CONNECTION-DETAILS.                                         
   02 TARIFF PIC X(6) VALUE "1LT3IN".                          
   02 LOAD  PIC X(3) VALUE "3KW".                              
01 BILLING-DETAILS.                                            
   02 BILL-PERIOD PIC 9(2)/9(2)/9(4).                          
   02 BILL-RDNG-DATE PIC 9(2)/9(2)/9(4).                       
   02 BILL-NUMBER PIC 9(16) VALUE 113813228090160.             
01 CONSUMPTION-DETAILS.                                        
   02 PRES-RDG PIC 9(4) VALUE 3943.                            
   02 PREV-RDG PIC 9(4) VALUE 3760.                            
   02 CONSTANT PIC 9 VALUE 1.                                  
   02 CONSUMPTION-UNITS PIC X(6) VALUE "1.71KW".               
01 ENERGY-CHARGAS PIC 9(4)V99 VALUE 1062.20.                    
01 FACCHARGES PIC 9(3)V99 VALUE 120.63.                         
01 ADDITIONALCHARGES.                                           
   02 REBATE PIC 9V99 VALUE 0.00.                               
   02 PF-PANAITY PIC 9V99 VALUE 0.00.                           
   02 LOAD-PENAITLY PIC 9V99 VALUE 0.00.                        
   02 INTEREST PIC 9V99 VALUE 3.89.                             
   02 OTHERS PIC 9V99 VALUE 0.00.                               
   02 TAX PIC 9(3)V99 VALUE 133.40.                             
   02 BILL-AMT PIC 9999V99 VALUE 2115.08.                       
   02 ARREARS PIC 9V99 VALUE 0.00.                              
   02 CREDITS PIC 9V99 VALUE 0.00.                              
   02 GOK-ADJUSTMENT PIC 9V99 VALUE 0.00.                       
   02 SUBSIDY PIC 9V99 VALUE 0.00.                              
01 NET-AMT-DUE PIC 9(4)V99 VALUE 2315.00.                       
01 DUEDATE  PIC 9(2)/9(2)/9(4).                                 
PROCEDURE DIVISION.                                             
    MOVE 09122022 TO BILL-PERIOD.                               
    MOVE 09122022 TO BILL-RDNG-DATE.                            
    MOVE 25122022 TO DUEDATE.                                   
    DISPLAY "!**********ELECTRICTYBILL***********************!".
    DISPLAY "!ACCOUNTS DT-".                                    
    DISPLAY "!AREA-NUM***-"AR-NO.                               
    DISPLAY "!ACC-ID******-" ACC-ID.                            
    DISPLAY "!MR-COD******-" MR-COD.                            
    DISPLAY "!PARSONAL****-".                                   
DISPLAY "!NAME********-" NAME.             
DISPLAY "!ADDRSS******-" ADDRSS.           
DISPLAY "!CONNECTION*-" CONNECTION-DETAILS.
DISPLAY "!TARIFF*****-" TARIFF.            
DISPLAY "!LOAD*******-" LOAD.              
DISPLAY "!BILLING****-".                   
DISPLAY "!BILL-PERIOD-" BILL-PERIOD.       
DISPLAY "!BILL-RDNG**-" BILL-RDNG-DATE.    
DISPLAY "!BILL-NUMBER-" BILL-NUMBER.       
DISPLAY "!CONSUMPTION-".                   
DISPLAY "!PRES-RDG***-".                   
DISPLAY "!PRES-RDG***-" PRES-RDG.          
DISPLAY "!PREV-RDG***-" PREV-RDG.          
DISPLAY "!CONSTANT***-" CONSTANT.          
DISPLAY "!CONSUMPTION-" CONSUMPTION-UNITS. 
DISPLAY "!POWER-FACTO-" POWER-FACTOR.      
DISPLAY "!CONNECTED**-" CONNECTED-LOAD.    
DISPLAY "!FIXED******-" FIXED-CHARGES.     
DISPLAY "!FACCHARGES*-" FACCHARGES.        
DISPLAY "!ADDITIONAL*-".                   
DISPLAY "!TAX********-" TAX.               
DISPLAY "!BILL-AMT***-" BILL-AMT.          
DISPLAY "!INTEREST***-" INTEREST.          
DISPLAY "!AMT********-" BILL-AMT.          
DISPLAY "!NET-AMT****-" NET-AMT-DUE.       
DISPLAY "!DUEDATE****-" DUEDATE.           
DISPLAY "!***************************************
STOP RUN.                                        
OUT PUT:
!**********ELECTRICTYBILL***********************!   
!ACCOUNTS DT-                                       
!AREA-NUM***-06560524                               
!ACC-ID******-2479665356                            
!MR-COD******-14012846                              
!PARSONAL****-                                      
!NAME********-VISHNU VARDHAN                        
!ADDRSS******-#11C 100FT RINGROAD BTM2NSTAGE        
!CONNECTION*-1LT3IN3KW                              
!TARIFF*****-1LT3IN                                 
!LOAD*******-3KW                                    
!BILLING****-                                       
!BILL-PERIOD-09/12/2022                             
!BILL-RDNG**-09/12/2022                             
!BILL-NUMBER-0113813228090160                       
!CONSUMPTION-                                       
!PRES-RDG***-                                       
!PRES-RDG***-3943                                   
!PREV-RDG***-3760                                   
!CONSTANT***-1                                      
!CONSUMPTION-1.71KW                                 
!POWER-FACTO-1.0                                    
!CONNECTED**-0.0KW                                  
!FIXED******-37500                                  
!FACCHARGES*-12063                                  
!ADDITIONAL*-                                       
!TAX********-13340                                  
!BILL-AMT***-211508                                 
!INTEREST***-389                                    
!AMT********-211508                                
!NET-AMT****-231500                                
!DUEDATE****-25/12/2022                            
!************************************************!                        
PIC   EDITING


IDENTIFICATION DIVISION.                        
PROGRAM-ID. NAME.                               
ENVIRONMENT DIVISION.                           
DATA DIVISION.                                  
WORKING-STORAGE SECTION.                        
01 A-NAME PIC A(20) VALUE 'VEMULAVISHNUVARDHAN'.
01 B-NAME PIC A(6)BA(6)BA(5) VALUE SPACES.      
PROCEDURE DIVISION.                             
    MOVE A-NAME TO B-NAME.                      
    DISPLAY B-NAME.                             
    STOP RUN.
IDENTIFICATION DIVISION.        
PROGRAM-ID. NAME.               
ENVIRONMENT DIVISION.           
DATA DIVISION.                  
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(5) VALUE 00077. 
01 B-NAME PIC ZZ999.            
PROCEDURE DIVISION.             
    MOVE A-NAME TO B-NAME.      
    DISPLAY B-NAME.             
    DISPLAY LENGTH OF A-NAME.   
    DISPLAY LENGTH OF B-NAME.   
    STOP RUN.                   
OUTPUT:
VEMULA VISHNU VARDHAN
OUT PUT:
  077    
000000005
000000005
IDENTIFICATION DIVISION.     
PROGRAM-ID. NAME.            
ENVIRONMENT DIVISION.        
DATA DIVISION.               
WORKING-STORAGE SECTION.     
01 A-NAME PIC 9(2) VALUE 20. 
01 B-NAME PIC ***99.         
PROCEDURE DIVISION.          
    MOVE A-NAME TO B-NAME.   
    DISPLAY B-NAME.          
    DISPLAY LENGTH OF A-NAME.
    DISPLAY LENGTH OF B-NAME.
    STOP RUN.                
OUT PUT:
***20     
000000002 
000000005 
WORKING-STORAGE SECTION.     
01 A-NAME PIC 9(3) VALUE 124.
01 B-NAME PIC $9(4).         
OUT PUT:
$0124     
000000003 
000000005
WORKING-STORAGE SECTION.         
01 A-NAME PIC S9(4) VALUE -4256. 
01 B-NAME PIC -9999.             
OUT PUT:
-4256    
000000004
000000005 
WORKING-STORAGE SECTION.        
01 A-NAME PIC S9(4) VALUE -1256.
01 B-NAME PIC +9999.            
OUT PUT:
-1256 
WORKING-STORAGE SECTION.      
01 A-NAME PIC S9(2) VALUE -12.
01 B-NAME PIC 999CR.           
OP
012CR
WORKING-STORAGE SECTION.      
01 A-NAME PIC S9(2) VALUE 24. 
01 B-NAME PIC 999CR.          
OP
024  
WORKING-STORAGE SECTION.            
01 A-NAME PIC 9(2)V9(2) VALUE 12.34.
01 B-NAME PIC 9(3).9.               
OP
012.3
WORKING-STORAGE SECTION.      
01 A-NAME PIC 9(4) VALUE 3456.
01 B-NAME PIC 99,999.
 OP
03,456 
WORKING-STORAGE SECTION.      
01 A-NAME PIC 9(4) VALUE 3489.
01 B-NAME PIC 9(4)B99.                
OP
0034 89
WORKING-STORAGE SECTION.             
01 A-NAME PIC X(9) VALUE 'BFSKINNER'.
01 B-NAME PIC XBXBX(7).               
OP
B F SKINNER 
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(6) VALUE 123456.
01 B-NAME PIC 999,999.          
  OP
123,456
WORKING-STORAGE SECTION.         
01 A-NAME PIC 9(6) VALUE 000078. 
01 B-NAME PIC 9(3),9(3).            
OP
 000,078
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(6) VALUE 000078.
01 B-NAME PIC ZZZ,ZZZ.          
 OP
BBBBB 78
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(6) VALUE 000178.
01 B-NAME PIC ***,***.          
OP
****178 
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(6) VALUE 002178.
01 B-NAME PIC ***,***.             
OP
**2,178
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(6) VALUE 120183.
01 B-NAME PIC 99B99B99.           
OP
12 B01 B83 
WORKING-STORAGE SECTION.        
01 A-NAME PIC 9(6) VALUE 120183.
01 B-NAME PIC 99/99/99.         
OP
12/01/83 
WORKING-STORAGE SECTION.         
01 A-NAME PIC 9(6) VALUE 001245. 
01 B-NAME PIC 990099. 
WORKING-STORAGE SECTION.             
01 A-NAME PIC 999V99 VALUE 123.45.   
01 B-NAME PIC 999.99.                
01 C-NAME PIC 999V99 VALUE 023.45.   
01 D-NAME PIC 999.9.                 
01 E-NAME PIC 999V99 VALUE 512.34.   
01 F-NAME PIC 99.99.                 
01 G-NAME PIC 999 VALUE 456.         
01 H-NAME PIC 999.99.                
PROCEDURE DIVISION.                  
    MOVE A-NAME TO B-NAME.           
    MOVE C-NAME TO D-NAME.           
    MOVE E-NAME TO F-NAME.           
    MOVE G-NAME TO H-NAME.           
    DISPLAY B-NAME.                  
    DISPLAY D-NAME.                  
    DISPLAY F-NAME.                  
    DISPLAY H-NAME.                  
    STOP RUN.                                   
OP
120045 
123.45 
023.4  
12.34  
456.00
WORKING-STORAGE SECTION.                        
01 DV-RAW PIC 9V99.                             
01 DV-EDITED PIC 9.99.                          
PROCEDURE DIVISION.                             
    DIVIDE 1 BY 100 GIVING DV-RAW DV-EDITED.    
    DISPLAY DV-RAW.                             
    DISPLAY DV-EDITED.                          
    STOP RUN.                                   
OP
001  
0.01
WORKING-STORAGE SECTION.         
01 NUM1 PIC 99,99,999.           
01 NUM2 PIC 99B99B999.           
PROCEDURE DIVISION.              
    MOVE 1000000 TO NUM1 NUM2.   
    DISPLAY NUM1.                
    DISPLAY NUM2.                
    STOP RUN.                    
OP
10,00,000 
10B00B000
WORKING-STORAGE SECTION.       
01 DT1 PIC XX/XX/XXXX.         
01 DT2 PIC XXBXXBXXXX.         
PROCEDURE DIVISION.            
    MOVE 12162022 TO DT1 DT2.  
    DISPLAY DT1.               
    DISPLAY DT2.               
    STOP RUN.                  
OP
12/16/2022
12 16 2022 
WORKING-STORAGE SECTION. 
01 A PIC S999 VALUE -123.
01 B PIC -999.           
PROCEDURE DIVISION.      
    MOVE A TO B.         
    DISPLAY B.           
    STOP RUN.              
OP
-123
WORKING-STORAGE SECTION. 
01 A PIC S999 VALUE -123.
01 B PIC 999-.           
OP
123- 
WORKING-STORAGE SECTION. 
01 A PIC S999 VALUE +123.
01 B PIC 999-.          
OP
123  
WORKING-STORAGE SECTION.  
01 A PIC S999 VALUE +123. 
01 B PIC -999.             
OP
 B123 
WORKING-STORAGE SECTION.    
01 A PIC S9(6) VALUE +12345.
01 B PIC +9(5).              
OP
+12345
WORKING-STORAGE SECTION.  
01 A PIC S9(3) VALUE -345.
01 B PIC +9(3).           
OP
-345 
WORKING-STORAGE SECTION.  
01 A PIC S9(3) VALUE -123.
01 B PIC 999+.            
OP
123-
WORKING-STORAGE SECTION.   
01 A PIC S9(4) VALUE +1234.
01 B PIC 9(4)CR.           
OP
1234 
WORKING-STORAGE SECTION.   
01 A PIC S9(4) VALUE -1234.
01 B PIC 9(4)CR.           
OP
1234CR
WORKING-STORAGE SECTION.    
01 A PIC S9(4) VALUE +1234. 
01 B PIC 9(4)DB.            
OP
1234 
WORKING-STORAGE SECTION.   
01 A PIC S9(4) VALUE -1234.
01 B PIC 9(4)DB.            
OP
1234DB  
WORKING-STORAGE SECTION.  
01 A PIC S9(4) VALUE 1234.
01 B PIC $99999.          
    OP
$01234 
WORKING-STORAGE SECTION.  
01 A PIC S9(4) VALUE 0000.
01 B PIC $ZZZZZ.          
OP BALACK
WORKING-STORAGE SECTION. 
01 A PIC 9(4) VALUE 0000.
01 B PIC $$$$9.99.       
OP
BBBB $0.00
 WORKING-STORAGE SECTION. 
01 A PIC 9(4) VALUE 0080.
01 B PIC $$,$$9.00.      
OP
BBB $80.00
WORKING-STORAGE SECTION. 
01 A PIC 9(4) VALUE 0128.
01 B PIC $$,$$9.99.       
OP
  $128.00
WORKING-STORAGE SECTION.  
01 A PIC 9(5) VALUE 57397.
01 B PIC $$,$$9.          
OP
$7,397 
WORKING-STORAGE SECTION.   
01 A PIC S9(4) VALUE -0005.
01 B PIC ++++9.            
OP
BBB -5
WORKING-STORAGE SECTION.   
01 A PIC S9(4) VALUE +0080.
01 B PIC ++++9.            
OP 
BB  +80
WORKING-STORAGE SECTION.   
01 A PIC S9(4) VALUE -0080.
01 B PIC ----9.            
OP
BB  -80
WORKING-STORAGE SECTION.                   
01 A PIC X(2)BX(3)BX(4) VALUE '16DEC2022'. 
PROCEDURE DIVISION.                        
    MOVE "16DEC2022" TO A.                  
OP
16 DEC 2022 
WORKING-STORAGE SECTION. 
01 A PIC 9(2)/9(2)/9(4). 
PROCEDURE DIVISION.      
    MOVE "16122022" TO A.
OP
16/12/2022 
WORKING-STORAGE SECTION.
01 A PIC 99,B999,B000.  
PROCEDURE DIVISION.     
    MOVE "1234" TO A.   
OP
01, B234, B000
WORKING-STORAGE SECTION.    
01 A PIC 99,999.            
PROCEDURE DIVISION.         
    MOVE "12345" TO A.      
OP
12,345  
WORKING-STORAGE SECTION.  
01 A PIC X(3) VALUE '100'.
01 B PIC 9(5).            
PROCEDURE DIVISION.       
    MOVE A TO B.          
    DISPLAY B.            
    STOP RUN.             
OP 
00100
WORKING-STORAGE SECTION.     
01 A PIC A(5) VALUE 'HELLO'. 
01 B PIC X(6).               
OP
HELLO  
WORKING-STORAGE SECTION. 
01 A PIC S9+++ VALUE -10.
01 B PIC 9(3).
WORKING-STORAGE SECTION.      
01 B PIC 99/99/9(4).          
01 A PIC 9(8) VALUE 16122022.            
OP
16/12/2022
WORKING-STORAGE SECTION.      
01 A PIC 9(3)V99 VALUE 100.50.
01 B PIC *(4)9.99.            
OP
**100.50  
WORKING-STORAGE SECTION. 
01 A PIC 9(3)V99 VALUE 0.
01 B PIC *(4)9.99. 
WORKING-STORAGE SECTION.        
01 A PIC X(9) VALUE 'ABCDEFGHI'.
01 B PIC X(3)BX(3)BX(3).              
OUTPUT
ABC DEF GHI 
OP
****0.00 
WORKING-STORAGE SECTION.  
01 A PIC 9(5) VALUE 12345.
01 B PIC ZZ,999.           
OP
12,345
WORKING-STORAGE SECTION.   
01 A PIC 9(5) VALUE 01234. 
01 B PIC ZZ,999.           
 OP
*******
 B1,234 
WORKING-STORAGE SECTION.   
01 A PIC 9(5) VALUE 0123. 
01 B PIC ZZ,999.           
OP
 BB 123
WORKING-STORAGE SECTION.     
01 A PIC 9(5) VALUE 00012.   
01 B PIC ZZ,999.             
OP
  BBB 012 
WORKING-STORAGE SECTION.  
01 A PIC 9(5) VALUE 05678.
01 B PIC **,**9.          
OP
*5,678 
WORKING-STORAGE SECTION.  
01 A PIC 9(5) VALUE 00567.
01 B PIC **,**9.          
OP
***567
WORKING-STORAGE SECTION.  
01 A PIC 9(5) VALUE 00000.
01 B PIC **,***.          
OP
CODNAME
IDENTIFICATION DIVISION.                   
PROGRAM-ID. CODNAME1.                      
DATA DIVISION.                             
WORKING-STORAGE SECTION.                   
01 DEDUCTIONS PIC 9(3) VALUE 800.          
01 SPECIAL-PAY PIC 9(3) VALUE 500.         
77 MARITAL-STATUS PIC 9.                   
   88 SINGLE VALUE IS ZERO.                
   88 MARRIED VALUE IS 1.                  
   88 WIDOWED VALUE IS 2.                  
   88 DIVORCED VALUE IS 3.                 
   88 ONCE-MARRIED VALUE ARE 1 , 2 , 3.    
   88 VALID-STATUS VALUE ARE 0 THRU 3.     
PROCEDURE DIVISION.                        
    ACCEPT MARITAL-STATUS.                 
    IF SINGLE SUBTRACT 120 FROM DEDUCTIONS 
    DISPLAY "SINGLE"                       
    END-IF.                                
    IF MARRIED SUBTRACT 20 FROM DEDUCTIONS 
    DISPLAY "ONCE MARRIED"                 
    END-IF.                                
    IF WIDOWED SUBTRACT 30 FROM  DEDUCTIONS
    DISPLAY "WIDOWED"                      
END-IF.                         
IF DIVORCED ADD 2 TO DEDUCTIONS 
DISPLAY "DIVORCED"              
END-IF.                                 
IF ONCE-MARRIED ADD  35 TO SPECIAL-PAY  
DISPLAY "ONCE-MARRIED"                  
END-IF.                                 
IF VALID-STATUS ADD  2 TO SPECIAL-PAY   
DISPLAY "ERROR"                         
END-IF.                                 
STOP RUN.                               

IDENTIFICATION DIVISION.                                
PROGRAM-ID. CONAME.                                     
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 WS00-MARKS PIC 9(3).                                 
    88 PASS VALUE ARE 051 THRU 100.                     
    88 NOT-CLEAR VALUE ARE 000 THRU 050.                
01 WS00-DISP PIC X(20).                                 
PROCEDURE DIVISION.                                     
A0000-MAIN-PARA.                                        
    ACCEPT WS00-MARKS.                                  
    IF PASS MOVE 'PASSED COMPRE' TO WS00-DISP           
    END-IF.                                             
    IF NOT-CLEAR MOVE 'NOT CLEARED COMPRE' TO WS00-DISP 
    END-IF.                                             
    DISPLAY WS00-DISP.                                  
    STOP RUN.                                           
IDENTIFICATION DIVISION.              
PROGRAM-ID. CODNAME1                  
DATA DIVISION.                        
WORKING-STORAGE SECTION.              
01 CITYCODE PIC 9 VALUE 5.            
    88 CHENNAI VALUE 1.               
    88 BANGALORE VALUE 2.             
    88 KOLAR VALUE 3.                 
    88 GADAG VALUE 4.                 
    88 SIMLA VALUE 5.                 
    88 MYSORE VALUE 6.                
    88 UNIVERSITY VALUE 1 THRU 4.     
PROCEDURE DIVISION.                   
    ACCEPT CITYCODE.                  
    IF CHENNAI                        
    DISPLAY "WE'RE IN COASTAL CITY."  
    END-IF                            
    IF BANGALORE                      
    DISPLAY "WE'RE AT HOME."          
    END-IF                            
    IF KOLAR                          
    DISPLAY "WE'RE IN MILK CITY."     
    END-IF                            
    IF SIMLA                      
DISPLAY "WE'RE IN SNOW CITY." 
END-IF                        
     IF GADAG                     
DISPLAY "WE'RE GOLD CITY."   
END-IF                       
IF UNIVERSITY                
DISPLAY 'ADMISSION IS FIXED' 
END-IF.                      
STOP RUN.                    
IDENTIFICATION DIVISION.                                
PROGRAM-ID. CODNAME2.                                   
DATA DIVISION.                                          
WORKING-STORAGE SECTION.                                
01 INPUTCHAR PIC X.                                     
    88 VOWEL VALUE "A" , "E" , "I" , "O" , "U".         
    88 CONSONANT VALUE "B" THRU "D" , "F" , "G" , "H"   
                       "J" THRU "N" , "P" THRU "T"      
                       "V" THRU "Z".                    
    88 DIGIT     VALUE "0" THRU "9".                    
    88 VALIDCHAR VALUE "A" THRU "Z" , "0" THRU "9".     
PROCEDURE DIVISION.                                     
    ACCEPT INPUTCHAR.                                   
    DISPLAY INPUTCHAR.                                  
    IF VALIDCHAR                                        
    DISPLAY "VOWEL CHAR."                               
    END-IF                                              
    IF DIGIT                                            
    DISPLAY "DIGIT ENTERED."                            
    END-IF                                              
    IF VOWEL                                            
    DISPLAY "VOWEL ENTERED."                            
    END-IF                                              
    IF CONSONANT                
    DISPLAY "CONSONANT ENTERED."
    END-IF.
    STOP RUN.
IDENTIFICATION DIVISION.                         
PROGRAM-ID. PARM1.                               
ENVIRONMENT DIVISION.                            
DATA DIVISION.                                   
WORKING-STORAGE SECTION.                         
01 WS00-DATA.                                    
   05 WS00-DATA-FROM-PARM.                       
      10 WS00-EMPNUMB PIC 9(5).                  
      10 WS00-EMPNAME PIC X(25).                 
LINKAGE SECTION.                                 
01 LI00.                                         
   05 LI00-LENGTH PIC S9(4) COMP.                
   05 LI00-CONTENT PIC X(30).                    
PROCEDURE DIVISION.                              
    MOVE LI00-CONTENT TO WS00-DATA-FROM-PARM.    
    DISPLAY "*******************************".   
    DISPLAY "EMP NUMBER IS : " WS00-EMPNUMB.     
    DISPLAY "EMP NAME   IS : " WS00-EMPNAME.     
    DISPLAY "DATA LENGTH IS :" LI00-LENGTH.      
    DISPLAY "********************************".  
    STOP RUN.                                    
IDENTIFICATION DIVISION.                 
PROGRAM-ID. PARM2.                       
ENVIRONMENT DIVISION.                    
DATA DIVISION.                           
WORKING-STORAGE SECTION.                 
01 PARM-BUFFER.                          
   05 PARM-LENGTH PIC S9(4) COMP.        
   05 PARM-DATA.                         
      10 NUMB PIC X(6).                  
      10 FILER PIC X(25).                
PROCEDURE DIVISION USING PARM-BUFFER.    
MAINLINE SCTION.                         
    DISPLAY "LENGTH:" PARM-BUFFER.       
    DISPLAY "NUMB: " NUMB OF PARM-DATA.  
MAINLINE-EXIT.                           
    GOBACK.                              
    STOP RUN.                            
IDENTIFICATION DIVISION.                           
PROGRAM-ID. NMBER.                                 
ENVIRONMENT DIVISION.                              
DATA DIVISION.                                     
WORKING-STORAGE SECTION.                           
01 MAX-NUM.                                        
   05 NUM PIC 9(2) OCCURS 5 TIMES.                 
77 IDX PIC 9(2) VALUE 1.                           
77 MAX PIC 9(2) VALUE 0.                           
PROCEDURE DIVISION.                                
MAIN-PARA.                                         
    ACCEPT MAX-NUM.                                
    PERFORM ACCEPT-PARA.                           
    PERFORM COMP-PARA.                             
    STOP RUN.                                      
ACCEPT-PARA.                                       
    PERFORM VARYING IDX FROM 1 BY 1 UNTIL IDX > 5  
    ACCEPT NUM(IDX)                                
    END-PERFORM.                                   
COMP-PARA.                                         
    PERFORM VARYING IDX FROM 1 BY 1 UNTIL IDX > 5  
    IF NUM(IDX) > MAX                              
    MOVE NUM(IDX) TO MAX.                          
   END-IF.     
   END-PERFORM.
   DISPLAY MAX. 
IDENTIFICATION DIVISION.                             
PROGRAM-ID. NMBER1.                                  
ENVIRONMENT DIVISION.                                
DATA DIVISION.                                       
WORKING-STORAGE SECTION.                             
01 EVEN-ODD.                                         
05 NUM PIC 9(1) OCCURS 100 TIMES.                    
77 SUM-EVEN PIC 9(4) VALUE 0.                        
77 SUM-ODD PIC 9(4) VALUE 0.                         
77 IDX PIC 9(3) VALUE 1.                             
77 QUO PIC 9(3).                                     
77 REM PIC 9(3).                                     
PROCEDURE DIVISION.                                  
    ACCEPT EVEN-ODD.                                 
    PERFORM VARYING IDX FROM 1 BY 1 UNTIL IDX > 100  
    DIVIDE IDX BY 2 GIVING QUO REMAINDER REM         
    IF REM = 0                                       
    COMPUTE SUM-EVEN = SUM-EVEN + IDX                
    ELSE                                             
    COMPUTE SUM-ODD = SUM-ODD  + IDX                 
    END-IF                                           
    END-PERFORM                                      
    DISPLAY "SUM EVEN " SUM-EVEN.                    
    DISPLAY "SUME ODD " SUM-ODD.
    STOP RUN.
IDENTIFICATION DIVISION.                                        
PROGRAM-ID. NMBER2.                                             
ENVIRONMENT DIVISION.                                           
DATA DIVISION.                                                  
WORKING-STORAGE SECTION.                                        
77 STOP-AT PIC 9(3).                                            
77 INCREMENT PIC 9(3) VALUE 1.                                  
PROCEDURE DIVISION.                                             
MAIN-PARA.                                                      
    PERFORM ACCEPT-PARA                                         
    PERFORM COMP-PARA.                                          
    STOP RUN.                                                   
ACCEPT-PARA                                                     
    ACCEPT-STOP-AT.                                             
COMP-PARA.                                                      
    PERFORM VARYING INCREMENT FROM 1 BY 1 UNTIL INCREMENT > STOP
-AT.                                                            
    DISPLAY INCREMENT                                           
    END-PERFORM.                                                
IDENTIFICATION DIVISION.                    
PROGRAM-ID. PERFOM.                         
ENVIRONMENT DIVISION.                       
DATA DIVISION.                              
WORKING-STORAGE SECTION.                    
01 NUM PIC 9(2).                            
01 N   PIC 9(2).                            
01 R   PIC 9(2).                            
PROCEDURE DIVISION.                         
    ACCEPT NUM.                             
    PERFORM P1.                             
    STOP RUN.                               
P1.                                         
    DIVIDE 2 INTO NUM GIVING N REMAINDER R. 
    IF R = 0                                
    DISPLAY NUM "IS EVE"                    
    ELSE                                    
    DISPLAY NUM "IS ODD"                    
    END-IF.      
                           
                                       
