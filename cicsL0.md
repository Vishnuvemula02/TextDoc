

Mainframe Operating System                               z/OS V1.10            
                                                                                
                                                                                
                                                                                
                       SSSS H    H  AAA  RRR  EEEE                              
                       S    H    H A   A R  R E                                 
                        SS  HHHHHH AAAAA RRR  EEEE                              
                          S H    H A   A R R  E                                 
                       SSSS H    H A   A R  R EEEE                              
                                                                                
                                                                                
                                                                                
                  Welcome to Share Tech Mainframe System!                       
                                                                                
                                                                                
                                                                                
         TSO      - Logon to TSO/ISPF        NETVIEW  - Netview System          
         CICS     - CICS Region                                                 
         IMS      - IMS Region                                                  
                                                                                
Enter your choice==> TSO TECN93                                                 
                                                                                
                                                                                
Your IP(27.7.187.202   :63435), SNA LU(        )       01/30/23 17:38:58        
------------------------------- TSO/E LOGON -----------------------------------
                                                                               
                                                                               
   Enter LOGON parameters below:                   RACF LOGON parameters:      
                                                                               
   Userid    ===> TECN93                                                       
                                                                               
   Password  ===> ****                             New Password ===>           
                                                                               
   Procedure ===> DBSPROC9                         Group Ident  ===>           
                                                                               
   Acct Nmbr ===> ACCT#                                                        
                                                                               
   Size      ===> 6102                                                         
                                                                               
   Perform   ===>                                                              
                                                                               
   Command   ===> ispf                                                         
                                                                               
   Enter an 'S' before each option desired below:                              
           -Nomail         -Nonotice        -Reconnect        -OIDcard         
                                                                               
PF1/PF13 ==> Help    PF3/PF15 ==> Logoff    PA1 ==> Attention    PA2 ==> Reshow
You may request specific help information by entering a '?' in any entry field

HELLO1 PGM

IDENTIFICATION DIVISION.                                   
PROGRAM-ID. HELLO1.                                        
ENVIRONMENT DIVISION.                                      
DATA DIVISION.                                             
WORKING-STORAGE SECTION.                                   
01 WS-LEN PIC S9(4) COMP.                                  
01 WS-TEXT PIC X(35).                                      
PROCEDURE DIVISION.                                        
    MOVE 35 TO WS-LEN.                                     
    MOVE 'WELCOME TO TECSACON TECHNOLOGIES' TO WS-TEXT.    
 EXEC CICS SEND                                            
    FROM (WS-TEXT)                                         
    LENGTH (WS-LEN)                                        
   ERASE                                                   
 END-EXEC.                                                 
 EXEC CICS                                                 
   RETURN                                                  
 END-EXEC.        

//TECN93VV JOB ,,NOTIFY=&SYSUID                                         
//JOBPROC  JCLLIB ORDER=IBMUSER.ALL1                                    
//CICSCOB  EXEC CICSCOB1,                                               
//         SRCLIB=TECN93.VISHNU.CICSPDS,         --> SOURCE PDS LIBRARY 
//         MEM=HELLO1,                     --> PROGRAM NAME             
//         COPYLIB=TECN93.VISHNU.COPYLIB,        --> COPYBOOK PDS LIB   
//*        BMSLIB=TECN54.RAHUL.CICSPDS,           --> BMS MAP LIB       
//         LOADLIB=CICS.APPLI.LOADLIB             **  DO NOT CHANGE  ** 
/*                                                                      
8.17.07 JOB00534 $HASP165 TECN93VV ENDED AT N1  MAXCC=4 CN(INTERNAL)
**          
                  Welcome to Share Tech Mainframe System!                       
                                                                                
                                                                                
                                                                                
         TSO      - Logon to TSO/ISPF        NETVIEW  - Netview System          
         CICS     - CICS Region                                                 
         IMS      - IMS Region                                                  
                                                                                
Enter your choice==> CICS                                                       
                                                                                
                                                                                
Your IP(115.99.90.71   :64415), SNA LU(        )       01/30/23 18:20:36        
                           Signon to CICS                       APPLID CICS    
                                                                               
WELCOME TO CICS                                                                
                                                                               
                                                                          
                                                  Type your userid and password, then press ENTER:                               
                                                                               
         Userid . . . .             Groupid . . .                              
         Password . . .                                                        
         Language . . .                                                        
                                                                               
     New Password . . .                                                        

                                               
                                               
                                               
DFHCE3549 Sign-on is complete (Language ENU).  
                                                        
CEDA DEF PROG(HELL01) D(APPLE)






  DEF PROG(HELL01) D(APPLE)                                                     
  OVERTYPE TO MODIFY                                        CICS RELEASE = 0650 
   CEDA  DEFine PROGram( HELL01   )                                             
    PROGram      ==> HELL01                                                     
    Group        ==>                                                            
    DEscription  ==> APPLE                                                      
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
   MESSAGES: 1 SEVERE  1 ERROR                                                  
                                                      SYSID=CICS APPLID=CICS    
                                                                                
 PF 1 HELP 2 COM 3 END             6 CRSR 7 SBH 8 SFH 9 MSG 10 SB 11 SF 12 CNCL






 CEDA DEF TRANS(1431) PROG(HELLO1) D(APPLE)                  

DEF TRANS(1431) PROG(HELLO1) D(APPLE)                  
            
OVERTYPE TO MODIFY                                        CICS RELE
 CEDA  DEFine TRANSaction( 1431 )                                  
  TRANSaction  ==> 1431                                            
  Group        ==>                                                 
  DEscription  ==> APPLE                                           
  PROGram      ==> HELLO1                                          
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
 MESSAGES: 1 SEVERE  1 ERROR   






DIS G(PACK)                                                                   
ENTER COMMANDS                                                                
 NAME     TYPE         GROUP                                   DATE   TIME    
 HELLO    PROGRAM      PACK     I                              23.030 17.09.57
 HELLO1   PROGRAM      PACK      I                             23.030 16.03.33
 8096     TRANSACTION  PACK                                    23.030 17.13.27
 9876     TRANSACTION  PACK                                    23.030 16.04.44
ENTER COMMANDS                                                                
 NAME     TYPE         GROUP                                   DATE   TIME    
 HELLO    PROGRAM      PACK     *                           INSTALL SUCCESSFUL
 HELLO1   PROGRAM      PACK     *                           INSTALL SUCCESSFUL
 8096     TRANSACTION  PACK                                    23.030 17.13.27
 9876     TRANSACTION  PACK                                    23.030 16.04.44

1431 
 OUT PUT 
WELCOME TO TECSACON TECHNOLOGIES   

CESF SINE OFF


