EDIT       TECN93.VVH1.PDS1(PSTOPS) - 01.00                Columns 00001 00072 
1
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                            
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //                                                                      
000900 //* PROGRAM FOR DATA COPYING FROM PS TO PS                              
****** **************************** Bottom of Data ****************************
OUT PUT:
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 HELLO THIS IS JUST A SIMPLE PS FILE                                     
000200 VISHNU                                                                  
000300 VARDHAN                                                                 
000400 RAM                                                                     
000500 KRISHNA                                                                 
000600 RAVE                                                                    
000700 APPLE                                                                   
000800 ASDFGHJKL;                                                              
****** **************************** Bottom of Data ****************************
2
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                            
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                       
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //                                                                      
000900 //* PS TO PDS                                                           
****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ****************************
==MSG> -Warning- The UNDO command is not available until you change          
==MSG>           your edit profile using the command RECOVERY ON.            
==MSG> -CAUTION- Profile is set to STATS ON. Statistics did not exist for    
==MSG>           this member, but will be generated if data is saved.        
000001 HELLO THIS IS JUST A SIMPLE PS FILE                                   
000002 VISHNU                                                                
000003 VARDHAN                                                               
000004 RAM                                                                   
000005 KRISHNA                                                               
000006 RAVE                                                                  
000007 APPLE                                                                 
000008 ASDFGHJKL;                                                            
****** **************************** Bottom of Data **************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                       
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M4),DISP=SHR                       
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //                                                                      
000900 //*PDS TO PDS IN THIS WECAN COPY ONLYDATA NO MEMBER                     
001000                                                                         
****** **************************** Bottom of Data ****************************
                                                                               
 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.PDS1(M4) - 01.00                    Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 ==MSG> -CAUTION- Profile is set to STATS ON. Statistics did not exist for      
 ==MSG>           this member, but will be generated if data is saved.          
 000001 HELLO THIS IS JUST A SIMPLE PS FILE                                     
 000002 VISHNU                                                                  
 000003 VARDHAN                                                                 
 000004 RAM                                                                     
 000005 KRISHNA                                                                 
 000006 RAVE                                                                    
 000007 APPLE                                                                   
 000008 ASDFGHJKL;                                                              
 ****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=SYSUID                                           
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PDS1(M4),DISP=SHR                       
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS3,DISP=SHR                            
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //*PDS(M4) TO PS3                                                       
****** **************************** Bottom of Data ****************************
EDIT       TECN93.VVH1.PS3                                 Columns 00001 00
****** ***************************** Top of Data **************************
==MSG> -Warning- The UNDO command is not available until you change        
==MSG>           your edit profile using the command RECOVERY ON.          
000100 HELLO THIS IS JUST A SIMPLE PS FILE                                 
000200 VISHNU                                                              
000300 VARDHAN                                                             
000400 RAM                                                                 
000500 KRISHNA                                                             
000600 RAVE                                                                
000700 APPLE                                                               
000800 ASDFGHJKL;                                                          
****** **************************** Bottom of Data ************************
 //TECN93VV JOB  NOTIFY=&SYSUID                    
//STEP1    EXEC PGM=IEBGENER                      
//SYSUT1   DD   *                                 
WELCOME TO VISHNUS FILE OF DATA                   
//SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M6),DISP=SHR 
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   DUMMY                             
/*                                                
//                                                
//* PROGRAM DATA TO A FILE  
 EDIT       TECN93.VVH1.PDS1(M6) - 01.00                    Columns 00001 00072 
 ****** ***************************** Top of Data ******************************                      
 000400 WELCOME TO VISHNUS FILE OF DATA                                         
 ****** **************************** Bottom of Data ****************************
//TECN93VV JOB  NOTIFY=&SYSUID    
//STEP1    EXEC PGM=IEBGENER      
//SYSUT1   DD   *                 
WELCOME VISHNU                    
//SYSUT2   DD   SYSOUT=*          
//SYSPRINT DD   SYSOUT=*          
//SYSIN    DD   DUMMY             
/*                                
//                                
//*PROGRAM DDATA TO SPOOL         
********************************* TOP OF DATA **********************************
WELCOME VISHNU                                                          00040000
******************************** BOTTOM OF DATA ********************************
//TECN93VV JOB  NOTIFY=TECN93,CLASS=A,PRTY=5       
//STEP01   EXEC PGM=IEBGENER                       
//SYSUT1   DD   *                                  
WELCOME TO TECSACON                                
//SYSUT2   DD   DSN=TECN93.CRAJ5.PS1,DISP=OLD      
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   DUMMY                              
/*                                                 
//TECN93HH JOB  NOTIFY=TECN93,CLASS=A,PRTY=10      
//STEP02   EXEC PGM=IEBGENER                       
//SYSUT1   DD   *                                  
WELCOME TO TECSACON                                
//SYSUT2   DD   DSN=TECN93.CRAJ5.PS2,DISP=OLD      
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   DUMMY                              
/*                                                 
//                                                 
//*PROGRAM TO SHOW THE PRIARTY OF SAME CLASS       

 11 NOV 2022 JOB EXECUTION DATE                          
           8 CARDS READ                                  
          41 SYSOUT PRINT RECORDS                        
           0 SYSOUT PUNCH RECORDS                        
           2 SYSOUT SPOOL KBYTES                         
        0.00 MINUTES EXECUTION TIME                      
       1 //TECN93HH JOB  NOTIFY=TECN93,CLASS=A,PRTY=10   
       2 //STEP02   EXEC PGM=IEBGENER                    
       3 //SYSUT1   DD   *                               
       4 //SYSUT2   DD   DSN=TECN93.CRAJ5.PS2,DISP=OLD   
       5 //SYSPRINT DD   SYSOUT=*                        
       6 //SYSIN    DD   DUMMY                           
         /*                    
-------------------------------------------------------------------------------
EDIT       TECN93.VVH1.PDS2(COMPLETA) - 01.02              Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBCOPY                                             
000210 //SYSPRINT DD   SYSOUT=*                                                
000300 //DD1      DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
000400 //DD2      DD   DSN=TECN93.VVH1.PDS2,DISP=SHR                           
000500 //SYSIN    DD   *                                                       
000600     COPY INDD=DD1,OUTDD=DD2                                             
000700 /*                                                                      
000800 //*PROGRAM FOR COPING COMPLET PDS MEMBERS                               
****** **************************** Bottom of Data ****************************
-------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.PDS2(COMPRES) - 01.01               Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBCOPY                                             
 000300 //DD1      DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
 000400 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   *                                                       
 000700     COPY INDD=DD1,OUTDD=DD1                                             
 000900 /*                                                                      
 001000 //*PROGRAM FOR COMPRESSING THE PDS FILE                                 
 ****** **************************** Bottom of Data ****************************
I COMPRESSING  PDS  OUTDD=DD1      VOL=ZAPRD6 DSN=TECN93.VVH1.PDS1  
I FOLLOWING MEMBER(S) MOVED IN DATA SET REFERENCED BY DD1           
 COPY     HAS BEEN SUCCESSFULLY MOVED                               
 DATAPDS  HAS BEEN SUCCESSFULLY MOVED                               
 M2       HAS BEEN SUCCESSFULLY MOVED                               
 M4       HAS BEEN SUCCESSFULLY MOVED                               
 M6       HAS BEEN SUCCESSFULLY MOVED                               
 OUTP     HAS BEEN SUCCESSFULLY MOVED                               
 PDSM     HAS BEEN SUCCESSFULLY MOVED                               
 PDSTOPS  HAS BEEN SUCCESSFULLY MOVED                               
 PRTY     HAS BEEN SUCCESSFULLY MOVED                               
 PSTOPDS  HAS BEEN SUCCESSFULLY MOVED                               
 PSTOPS   HAS BEEN SUCCESSFULLY MOVED                               
 PS2      HAS BEEN SUCCESSFULLY MOVED                               
 SPOOL    HAS BEEN SUCCESSFULLY MOVED                               
 TIME     HAS BEEN SUCCESSFULLY MOVED                               
 EDIT       TECN93.VVH1.PDS2(EXCLUDE) - 01.01               Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBCOPY                                             
 000300 //SYSPRINT DD   SYSOUT=*                                                
 000400 //DD1      DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
 000500 //DD2      DD   DSN=TECN93.VVH1.PDS2,DISP=SHR                           
 000600 //SYSIN    DD   *                                                       
 000700     COPY INDD=DD1,OUTDD=DD2                                             
 000800     EXCLUDE MEMBER=(M6,M10,M7)                                          
 000900 /*                                                                      
 001000 //*PROGRAM FOR COPING FROM PDS BY EXCLUDING FEW MEMBERS                 
 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.PDS2(SELECTME) - 01.01              Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBCOPY                                             
 000300 //SYSPRINT DD   SYSOUT=*                                                
 000400 //DD1      DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
 000500 //DD2      DD   DSN=TECN93.VVH1.PDS2,DISP=SHR                           
 000600 //SYSIN    DD   *                                                       
 000700     COPY INDD=DD1,OUTDD=DD2                                             
 000800     SELECT MEMBER=(M8,M9)                                               
 000900 /*                                                                      
 001000 //*PROGRAM FOR COPING THE SELECTED FROM ONE PDS TO ANOTHER PDS MEMBER   
 ****** **************************** Bottom of Data ****************************
                                                                                
 
EDIT       TECN93.VVH1.PDS2(RENAME) - 01.04                Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBCOPY                                             
000300 //SYSPRINT DD   SYSOUT=*                                                
000400 //DD1      DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
000500 //DD2      DD   DSN=TECN93.VVH1.PDS2,DISP=SHR                           
000600 //SYSIN    DD   *                                                       
000700     COPY INDD=DD1,OUTDD=DD2                                             
000800     SELECT MEMBER=((M12,VISHNU),R)                                      
000900 /*                                                                      
001000 //*PROGRAM FOR RENAMING A MEMBER USING IEB COPY                         
****** **************************** Bottom of Data ****************************              
2
EDIT       TECN93.VVH1.SORTPDS1(SORTCOPY) - 01.03          Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP01   EXEC PGM=SORT                                                
000300 //SORTIN   DD   DSN=TECN93.VVH1.SORTPS1,DISP=SHR                        
000400 //SORTOUT  DD   DSN=TECN93.VVH1.SORTPS2,DISP=SHR                        
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSOUT   DD   SYSOUT=*                                                
000700 //SYSIN    DD   *                                                       
000800    SORT FIELDS=COPY                                                     
000900 /*                                                                      
001000 //*COPING THE RECRDS USING SORT UITILTY                                 
****** **************************** Bottom of Data ****************************
 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.SORTPDS1(SORTADD) - 01.03           Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP01   EXEC PGM=SORT                                                
 000300 //SYSOUT   DD   SYSOUT=*                                                
 000400 //SORTIN   DD   *                                                       
 000500 05 09 99 77                                                             
 000600 09 06 55 66                                                             
 000700 12 10 88 99                                                             
 000800 //SORTOUT  DD   SYSOUT=*                                                
 000900 //SYSIN    DD   *                                                       
 001000     INREC FIELDS=((1,2,ZD,ADD,4,2,ZD,ADD,7,2,ZD,ADD,10,2,ZD),EDIT(TT))  
 001100     SORT FIELDS=COPY                                                    
 001200 /*                                                                      
 001300 //*ADDITION PROGRAM                                                     
 ****** **************************** Bottom of Data ****************************
                                                                                
********************************* TOP OF DATA *****
90                                                 
36                                                 
09                                                 
******************************** BOTTOM OF DATA ***
                                                   
000100 //TECN93VV JOB  NOTIFY=&SYSUID                  
000200 //STEP01   EXEC PGM=SORT                        
000300 //SYSOUT   DD   SYSOUT=*                        
000400 //SORTIN   DD   *                               
000500 05 09                                           
000600 09 06                                           
000700 12 10                                           
000800 //SORTOUT  DD   SYSOUT=*                        
000900 //SYSIN    DD   *                               
001000     INREC FIELDS=((1,2,ZD,SUB,4,2,ZD),EDIT(TT)) 
001100     SORT FIELDS=COPY                            
001200 /*                                              
001300 //*SUBSTRACTION PROGREM                         
 //TECN93VV JOB  NOTIFY=&SYSUID                     
 //STEP01   EXEC PGM=SORT                           
 //SYSOUT   DD   SYSOUT=*                           
 //SORTIN   DD   *                                  
 05 09                                              
 09 06                                              
 12 10                                              
 //SORTOUT  DD   SYSOUT=*                           
 //SYSIN    DD   *                                  
     INREC FIELDS=((1,2,ZD,MUL,4,2,ZD),EDIT(TT))    
     SORT FIELDS=COPY                               
 /*                                                 
 //*MULTIPACTION PROGRAM                            
//TECN93VV JOB  NOTIFY=&SYSUID                               
//STEP01   EXEC PGM=SORT                                     
//SYSOUT   DD   SYSOUT=*                                     
//SORTIN   DD   *                                            
05 09                                                        
09 06                                                        
12 10                                                        
//SORTOUT  DD   SYSOUT=*                                     
//SYSIN    DD   *                                            
    INREC FIELDS=((1,2,ZD,DIV,4,2,ZD),EDIT(TT))              
    SORT FIELDS=COPY                                         
/*                                                           
//*DIVISION PROGRAM                                          
//TECN93VV JOB  NOTIFY=&SYSUID                                 
//STEP01   EXEC PGM=SORT                                       
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS14,DISP=SHR              
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS15,DISP=SHR              
//SYSOUT   DD   SYSOUT=*                                       
//SYSPRINT DD   SYSOUT=*                                       
//SYSIN    DD   *                                              
      SORT FIELDS=(1,4,CH,A,18,2,CH,A)                         
/*                                                             
//* THIS IS PGM=1=4=18=2                                       
//TECN93VV JOB  NOTIFY=&SYSUID                                     
//STEP01   EXEC PGM=SORT                                           
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS3,DISP=SHR                   
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS4,DISP=SHR                   
//SYSPRINT DD   SYSOUT=*                                           
//SYSOUT   DD   SYSOUT=*                                           
//SYSIN    DD   *                                                  
   SORT FIELDS=COPY,                                               
   SKIPREC=4,                                                      
   STOPAFT=5                                                       
/*                                                                 
//TECN93VV JOB  NOTIFY=&SYSUID                                          
//STEP01   EXEC PGM=SORT                                                
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS3,DISP=SHR                        
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS4,DISP=SHR                        
//SYSPRINT DD   SYSOUT=*                                                
//SYSOUT   DD   SYSOUT=*                                                
//SYSIN    DD   *                                                       
   SORT FIELDS=COPY,                                                    
   SKIPREC=4,                                                           
   STOPAFT=5                                                            
/*                                                                      
//TECN93VV JOB  NOTIFY=&SYSUID                                          
//STEP01   EXEC PGM=SORT                                                
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS3,DISP=SHR                        
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS4,DISP=SHR                        
//SYSPRINT DD   SYSOUT=*                                                
//SYSOUT   DD   SYSOUT=*                                                
//SYSIN    DD   *                                                       
   SORT FIELD=COPY                                                      
/*                                                                      
//*COPY LIST 5 RECORDS AT FIRST AND FOUR RECORDS AT THE LAST PLACE  
//TECN93VV JOB  NOTIFY=&SYSUID                                
//STEP01   EXEC PGM=SORT                                      
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS3,DISP=SHR              
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS4,DISP=SHR              
//SYSOUT   DD   SYSOUT=*                                      
//SYSPRINT DD   SYSOUT=*                                      
//SYSIN    DD   *                                             
   SORT FIELDS=(6,10,CH,A),                                   
     SKIPREC=2                                                
/*                                                            
//*THIS IS TO SORT THE RECORDS IN ASCENDING ORDER             
//TECN93VV JOB  NOTIFY=&SYSUID                              
//STEP01   EXEC PGM=SORT                                    
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS5,DISP=SHR            
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS6,DISP=SHR            
//SYSPRINT DD   SYSOUT=*                                    
//SYSOUT   DD   SYSOUT=*                                    
//SYSIN    DD   *                                           
   SORT FIELDS=COPY                                         
   INCLUDE COND=(6,5,CH,EQ,C'VARUN')                        
/*                                                          
//* INCLUDE RECORDS                                         
//TECN93VV JOB  NOTIFY=&SYSUID                             
//STEP01   EXEC PGM=SORT                                   
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS5,DISP=SHR           
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS6,DISP=SHR           
//SYSPRINT DD   SYSOUT=*                                   
//SYSOUT   DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
   SORT FIELDS=(1,4,CH,D),                                 
   SKIPREC=0,                                              
   STOPAFT=3                                               
/*                                                         
//*SKIP FIRST THEN STOPAFTER AND THEN SORTING              
//TECN93VV JOB  NOTIFY=&SYSUID                                
//STEP01   EXEC PGM=SORT                                      
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS16,DISP=SHR             
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS17,DISP=SHR             
//SYSOUT   DD   SYSOUT=*                                      
//SYSPRINT DD   SYSOUT=*                                      
//SYSIN    DD   *                                             
   SORT FIELDS=COPY,SKIPREC=2                                 
     OMIT COND=(1,6,CH,EQ,C'VEMULA')                          
/*                                                            
//*THIS COPY,SKIP,OMIT                                        
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP02                     
//STEP01   EXEC PGM=SORT                                          
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS1,DISP=SHR                  
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS8,DISP=SHR                  
//SYSPRINT DD   SYSOUT=*                                          
//SYSOUT   DD   SYSOUT=*                                          
//SYSIN    DD   *                                                 
   SORT FIELDS=(1,6,CH,A)                                         
/*                                                                
//*COPINGRECORDS USING SORT UTILITY                               
//STEP02   EXEC PGM=SORT                                          
//SORTIN   DD   DSN=TECN93.VVH1.SORTPS9,DISP=SHR                  
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS10,DISP=SHR                 
//SYSPRINT DD   SYSOUT=*                                          
//SYSOUT   DD   SYSOUT=*                                          
//SYSIN    DD   *                                                 
   SORT FIELDS=(1,10,CH,A)                                        
/*                                                                
//TECN93VV JOB  NOTIFY=&SYSUID                                  
//STEP01   EXEC PGM=SORT                                        
//SORTIN1  DD   DSN=TECN93.VVH1.SORTPS8,DISP=SHR                
//SORTIN2  DD   DSN=TECN93.VVH1.SORTPS13,DISP=SHR               
//SORTOUT  DD   DSN=TECN93.VVH1.SORTPS12,DISP=SHR               
//SYSPRINT DD   SYSOUT=*                                        
//SYSOUT   DD   SYSOUT=*                                        
//SYSIN    DD   *                                               
   MERGE FIELDS=(1,10,CH,A)                                     
/*                                                              
//*MARGING RECORDS                                                  







3
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.DD1,DISP=SHR                            
000400 //SYSUT2   DD   DSN=TECN93.VVH1.DD2,DISP=SHR                            
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
****** **************************** Bottom of Data ****************************
                                                                               
 //TECN93VV JOB  NOTIFY=&SYSUID                
 //STEP1    EXEC PGM=IEBGENER                  
 //SYSUT1   DD   DSN=TECN93.VVH1.DD1,DISP=SHR  
 //SYSUT2   DD   DSN=TECN93.VVH1.DD2,DISP=OLD  
 //SYSPRINT DD   SYSOUT=*                      
 //SYSIN    DD   DUMMY                         
 /*                                            
 //TECN93VV JOB  NOTIFY=&SYSUID                    
 //STEP1    EXEC PGM=IEBGENER                      
 //SYSUT1   DD   DSN=TECN93.VVH1.DD1,DISP=SHR      
 //SYSUT2   DD   DSN=TECN93.VVH1.DD2,DISP=MOD      
 //SYSPRINT DD   SYSOUT=*                          
 //SYSIN    DD   DUMMY                             
 /*                                                
//TECN93VV JOB  NOTIFY=&SYSUID                                      
//STEP1    EXEC PGM=IEBGENER                                        
//SYSUT1   DD   DSN=TECN93.VVH1.DD1,DISP=(SHR,KEEP,DELETE)          
//SYSUT2   DD   DSN=TECN93.VVH1.DD2,DISP=(MOD,DELETE,DELETE)        
//SYSPRINT DD   SYSOUT=*                                            
//SYSIN    DD   DUMMY                                               
/*                                                                  EDIT       TECN93.VVH1.PDSDD1(IEF14PS) - 01.02             Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEFBR14                                             
000300 //SYSUT1   DD   DSN=TECN93.DD.PS,DISP=(NEW,CATLG,DELETE),               
000310 //  VOL=SER=ZAPRD6,                                                     
000400 //  SPACE=(TRK,(1,1,0),RLSE),                                           
000410 //  DCB=(LRECL=80,RECFM=FB,BLKSIZE=800),                                
000420 //  UNIT=3390                                                           
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
****** **************************** Bottom of Data ****************************
 //TECN93VV JOB  NOTIFY=&SYSUID                                
 //STEP1    EXEC PGM=IEFBR14                                   
 //SYSUT1   DD   DSN=TECN93.DD.PDS,DISP=(NEW,CATLG,DELETE),    
 //  VOL=SER=ZAPRD6,                                           
 //  SPACE=(TRK,(1,1,10),RLSE),                                
 //  DCB=(LRECL=80,RECFM=FB,BLKSIZE=800),                      
 //  UNIT=3390                                                 
 //SYSPRINT DD   SYSOUT=*                                      
 //SYSIN    DD   DUMMY                                         
 /*   
          
              
//TECN93VV JOB  NOTIFY=&SYSUID                                          
//IEFBR14  EXEC PGM=IEFBR14                                             
//IEF1     DD   DSN=TECN93.VVH1.PS5,DISP=(NEW,CATLG,DELETE),            
//  VOL=SER=ZAPRD6,                                                     
//  SPACE=(TRK,(1,1,0),RLSE),                                           
//  DCB=(LRECL=80,RECFM=FB,BLKSIZE=800),                                
//  UNIT=3390                                                           
//SYSPRINT DD   SYSOUT=*                                                
//SYSIN    DD   DUMMY                                                   
/*                                                                      
//STEP2    EXEC PGM=IEBGENER                                            
//SYSUT1   DD   *                                                       
   HELLO TECSACON TECHNOLOGIES                                          
//SYSUT2   DD   DSN=TECN93.VVH1.PS5,DISP=SHR                            
//SYSPRINT DD   SYSOUT=*                                                
//SYSIN    DD   DUMMY                                                   
/*                                                                      
//* CREATING OF PS AND LODING DATA INTO IT IN SINGLE PROGRAM                                                                     
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=IEHLIST2            
//IEHLIST1 EXEC PGM=IEHLIST                                
//IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390          
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
   LISTVTOC DSNAME=TECN93.VVH1.PS1,VOL=3390=ZAPRD6         
/*                                                         
//IEHLIST2 EXEC PGM=IEHLIST                                
//IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390          
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
   LISTVTOC DSNAME=TECN93.VVH1.PDS2,VOL=3390=ZAPRD6        
/*                                                         
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=IEHLIST2            
//IEHLIST3 EXEC PGM=IEHLIST                                
//IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390          
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
   LISTPS DSNAME=TECN93.VVH1.PS1,VOL=3390=ZAPRD6           
/*                                                         
//* THIS IS A PROGRAM OF LISTVTOC  PDS                     
//IEHLIST4 EXEC PGM=IEHLIST                                      
//IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390                
 //SYSPRINT DD   SYSOUT=*                                    
 //SYSIN    DD   *                                           
    LISTPDS  DSNAME=TECN93.VVH1.PDS1,VOL=3390=ZAPRD6         
/* 
                      
//TECN93VV JOB  NOTIFY=&SYSUID                                          
//IEFBR14  EXEC PGM=IEFBR14                                            
//SYSUT1   DD   *                                                       
   HELLO TECSACON                                                       
//SYSUT2   DD   DSN=TECN93.VVH1.PS1,DISP=(NEW,CATLG,DELETE),            
//  VOL=SER=ZAPRD6,                                                     
//  SPACE=(TRK,(1,1,0),RLSE),                                           
//  DCB=(LRECL=80,RECFM=FB,BLKSIZE=800),                                
//  UNIT=3390                                                           
//SYSPRINT DD   SYSOUT=*                                                
//SYSIN    DD   DUMMY                                                   
/*                                                                      
//* CREATING OF PS AND LODING DATA IN SAME STEP USING IEBGENER UTILITY   
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP2                   
//STEP1    EXEC PGM=IEHPROGM                                   
//SYSPRINT DD   SYSOUT=*                                       
//IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390              
//SYSIN    DD   *                                              
   SCRATCH MEMBER=M1,DSNAME=TECN93.VVH1.PDS2,VOL=3390=ZAPRD6   
/*                                                             
//*THIS IS PROGRRAM OF SCRATCH PDS                             
//*THIS PROGRAM OF SCRATCH APDS MEMBERS                        
//STEP2    EXEC PGM=IEHPROGM                                   
//SYSPRINT DD   SYSOUT=*                                       
//IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390              
//SYSIN    DD   *                                              
   SCRATCH=DSNAME=TECN93.VVH1.PS,VOL=3390=ZAPRD6               
/*                                                             
//*THIS IS PROGRAM OF SCRACICH APS MEMBER                      
 EDIT       TECN93.VVH1.PDSDD1(UNCATCAT) - 01.23            Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP4                            
 000200 //STEP1    EXEC PGM=IEHPROGM                                            
 000300 //SYSPRINT DD   SYSOUT=*                                                
 000400 //IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390                       
 000500 //SYSIN    DD   *                                                       
 000600     UNCATLG DSNAME=TECN93.VVH1.PDS52                                    
 000700 /*                                                                      
 000701 //*UN CATLG THE FILE PDS52                                              
 000703 //STEP2    EXEC PGM=IEHPROGM                                            
 000704 //SYSPRINT DD   SYSOUT=*                                                
 000705 //IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390                       
 000706 //SYSIN    DD   *                                                       
 000707     CATLG DSNAME=TECN93.VVH1.PDS52,VOL=3390=ZAPRD6                      
 000708 /*                                                                      
 000709 //*CATLG THE FILE PDS52                                                 
 000710 //STEP3    EXEC PGM=IEHPROGM                                            
 000720 //SYSPRINT DD   SYSOUT=*                                                
 000730 //IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390                       
 000740 //SYSIN    DD   *                                                       
 000750     UNCATLG DSNAME=TECN93.VVH1.PS29                                     
 000760 /*                                                                      
 000770 //STEP4    EXEC PGM=IEHPROGM                                            
 000780 //SYSPRINT DD   SYSOUT=*                                                
000790 //IEH1     DD   DISP=OLD,VOL=SER=ZAPRD6,UNIT=3390                    
000800 //SYSIN    DD   *                                                    
000900     CATLG DSNAME=TECN93.VVH1.PS29                                    
001000 /*                                                                   
****** **************************** Bottom of Data *************************   
4
-------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.TDCPDS1(TEMPDATA) - 01.03           Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP01   EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS1,DISP=SHR                         
 000400 //SYSUT2   DD   DSN=&&TEMP                                              
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   DUMMY                                                   
 000700 /*                                                                      
 000800 //*CREATION OF TEMP DATA SET                                            
 ****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP01   EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS1,DISP=SHR                         
000400 //SYSUT2   DD   DSN=&&TEMP,DISP=(,PASS)                                 
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //STEP02   EXEC PGM=IEBGENER                                            
000900 //SYSUT1   DD   DSN=&&TEMP,DISP=OLD                                     
001000 //SYSUT2   DD   DSN=TECN93.VVH1.TDCPS2,DISP=SHR                         
001100 //SYSPRINT DD   SYSOUT=*                                                
001200 //SYSIN    DD   DUMMY                                                   
001300 /*                                                                      
001400 //*                                                                     
****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
000400 //SYSUT2   DD   DSN=                                                    
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //STEP2    EXEC PGM=IEBGENER                                            
000900 //SYSUT1   DD   DSN=*.STEP1.SYSUT2,DISP=SHR                             
001000 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                            
001100 //SYSPRINT DD   SYSOUT=*                                                
001200 //SYSIN    DD   DUMMY                                                   
001300 /*                                                                      
001400 //*THIS IS PROGRAM FOR DSN= NOT GIVEN                                   
****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP01   EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS1,DISP=SHR                         
000400 //SYSUT2   DD   DSN=&&TECN,DISP=(,PASS)                                 
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 /*                                                                      
000800 //STEP02   EXEC PGM=IEBGENER                                            
000900 //SYSUT1   DD   DSN=*.STEP01.SYSUT2,DISP=SHR                            
001000 //SYSUT2   DD   DSN=TECN93.VVH1.TDPS3,DISP=SHR                          
001100 //SYSPRINT DD   SYSOUT=*                                                
001200 //SYSIN    DD   DUMMY                                                   
001300 /*                                                                      
001400 //*OMITTING THE DATA SET NAME AND REFERRING BACK IN NEXT STEP           
****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP01   EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS1,DISP=SHR                         
000310 //SYSUT2   DD   DSN=TECN93.VVHI.TDCPS2,DISP=OLD                         
000400 //SYSPRINT DD   SYSOUT=*                                                
000500 //SYSIN    DD   DUMMY                                                   
000600 /*                                                                      
000700 //STEP02   EXEC PGM=IEBGENER                                            
000800 //SYSUT1   DD   DSN=*.STEP1.SYSUT2,DISP=SHR                             
000810 //SYSUT2   DD   DSN=TECN93.VVH1.TDCPS4,DISP=OLD                         
000900 //SYSPRINT DD   SYSOUT=*                                                
001000 //SYSIN    DD   DUMMY                                                   
001100 /*                                                                      
001200 //* REFERRING BACK A EXISTING DATASET NAME                              
****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000200 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000300 //STEP01   EXEC PGM=IEFBR14                                             
000400 //DD1      DD   DSN=TECN93.VVH1.TDCPS7,DISP=(NEW,CATLG,DELETE),         
000500 //  VOLUME=SER=ZAPRD6,                                                  
000600 //  UNIT=3390,                                                          
000700 //  SPACE=(TRK,(1,1,0),RLSE),                                           
000800 //  DCB=(LRECL=80,RECFM=FB,BLKSIZE=800)                                 
001300 //DD1      DD   DSN=TECN93.VVH1.TDCPS8,DISP=(NEW,CATLG,DELETE),         
001400 //  VOLUME=REF=*.STEP01.DD1,                                            
001500 //  DCB=*.DD1,                                                          
001510 //  UNIT=3390,                                                          
001600 //  SPACE=(TRK,(1,1,0),RLSE)                                            
001800 //SYSPRINT DD   SYSOUT=*                                                
001900 //SYSIN    DD   DUMMY                                                   
002000 /*                                                                      
002100 //*REFERRING BACK A VOLUME AND DCB AT A SAME STEP                       
****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.TDCPDS1(CONCPSPS) - 01.02           Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS1,DISP=SHR                         
 000400 //         DD   DSN=TECN93.VVH1.TDCPS2,DISP=SHR                         
 000500 //         DD   DSN=TECN93.VVH1.TDCPS4,DISP=SHR                         
 000600 //SYSUT2   DD   DSN=TECN93.VVH1.TDCPS5,DISP=SHR                         
 000700 //SYSPRINT DD   SYSOUT=*                                                
 000800 //SYSIN    DD   DUMMY                                                   
 000900 //*CONCATING PS FILES                                                   
 ****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.TDCPDS1(COPDSPDS) - 01.02           Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPDS1(M1),DISP=SHR                    
 000400 //         DD   DSN=TECN93.VVH1.TDCPDS2(M1),DISP=SHR                    
 000500 //         DD   DSN=TECN93.VVH1.TDCPDS3(M1),DISP=SHR                    
 000600 //SYSUT2   DD   DSN=TECN93.VVH1.TDCPDS4(M1),DISP=SHR                    
 000700 //SYSPRINT DD   SYSOUT=*                                                
 000800 //SYSIN    DD   DUMMY                                                   
 000900 //*CONCATING PDS FILES                                                  
 ****** **************************** Bottom of Data ****************************
EDIT       TECN93.VVH1.TDCPDS1(COPSPDS) - 01.05            Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPDS1(M1),DISP=SHR                    
000400 //         DD   DSN=TECN93.VVH1.TDCPS1,DISP=SHR                         
000500 //         DD   DSN=TECN93.VVH1.TDCPDS3(M1),DISP=SHR                    
000600 //SYSUT2   DD   DSN=TECN93.VVH1.TDCPS7,DISP=SHR                         
000700 //SYSPRINT DD   SYSOUT=*                                                
000800 //SYSIN    DD   DUMMY                                                   
000900 //*CONCATING PS AND PDS FILES                                           
****** **************************** Bottom of Data ****************************
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP01   EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=OLD                            
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=OLD                            
000500 //SYSABEND DD   DSN=TECN93.VVH1.PS,DISP=SHR                             
000600 //SYSUDUMP DD   DSN=TECN93.VVH1.PS,DISP=OLD                             
000700 //SYSMDUMP DD   DSN=TECN93.VVH1.PS,DISP=OLD                             
000800 //SYSPRINT DD   SYSOUT=*                                                
000900 //SYSIN    DD   DUMMY                                                   
001000 /*                                                                      
001100 //* ABEND PROGRAM                                                       
****** **************************** Bottom of Data ****************************
5
EDIT       TECN93.VVH1.GDGPDS(GDGBASE) - 01.09             Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IDCAMS                                              
 000300 //SYSPRINT DD   SYSOUT=*                                                
 000400 //SYSIN    DD   *                                                       
 000500     DEFINE GDG -                                                        
 000600     (NAME(TECN93.VVH1.GDG)-                                             
 000700     LIMIT(3)-                                                           
 000800     EMPTY-                                                              
 000900     NOSCRATCH)                                                          
 001000 /*                                                                      
 001100 //*THIS IS BASE PROGRAM                                                 
 ****** **************************** Bottom of Data ****************************
-------------------------------------------------------------------------------
EDIT       TECN93.VVH1.GDGPDS(MODLE) - 01.03               Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEFBR14                                             
000300 //DD1      DD   DSN=TECN93.VVH1.GDG.MODEL,                              
000400 //       DISP=(NEW,CATLG,DELETE),                                       
000500 //       SPACE=(TRK,(1,1)),                                             
000600 //       DCB=(RECFM=FB,LRECL=80,BLKSIZE=800),                           
000700 //       UNIT=3390,                                                     
000800 //       VOL=SER=ZAPRD6                                                 
000900 //SYSPRINT DD   SYSOUT=*                                                
001000 //SYSIN    DD   DUMMY                                                   
001100 /*                                                                      
001200 //*THIS MODEL PROGRAM                                                   
****** **************************** Bottom of Data ****************************
                                                                               
 EDIT       TECN93.VVH1.GDGPDS(GDG1) - 01.10                Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEFBR14                                             
 000300 //DD1      DD   DSN=TECN93.VVH2.GDG(+1),                                
 000400 //      DISP=(NEW,CATLG,DELETE),                                        
 000500 //      SPACE=(TRK,(1,1)),                                              
 000600 //      DCB=TECN93.VVH1.GDG.MODEL,                                      
 000700 //      UNIT=3390,                                                      
 000800 //      VOL=SER=ZAPRD6                                                  
 000900 //SYSPRINT DD   SYSOUT=*                                                
 001000 //SYSIN    DD   DUMMY                                                   
 001100 /*                                                                      
 ****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.GDGPDS(LOAD1) - 01.23               Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=SYSUID                                           
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.GDG.GDGPS1,DISP=SHR                     
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.GDG.G0003V00,DISP=SHR                   
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   DUMMY                                                   
 000700 /*                                                                      
 ****** **************************** Bottom of Data ****************************
                                                                                
 EDIT       TECN93.VVH1.GDGPDS(LODNUMB) - 01.00             Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   SYSOUT=*                                                
 000400     12345                                                               
 000500     678910                                                              
 000600     234567890                                                           
 000700     23455678                                                            
 000800 //SYSUT2   DD   DSN=TECN93.VVH1.GOOO1VOO,DISP=SHR                       
 000900 //SYSPRINT DD   SYSOUT=*                                                
 001000 //SYSIN    DD   DUMMY                                                   
 001100 /*                                                                      
 001200 //*LODING THE DATA IN TO IT                                             
 ****** **************************** Bottom of Data ****************************

EDIT       TECN93.VVH1.GDGPDS(MULTPLGD) - 01.01            Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
000200 //STEP1    EXEC PGM=IEFBR14                                             
000300 //DD1      DD   DSN=TECN93.VVH1.GDG(+1),DISP=(NEW,CATLG,DELETE),        
000400 //       UNIT=3390,VOL=SER=ZAPRD6,                                      
000500 //       SPACE=(TRK,(1,1),RLSE),                                        
000600 //       DCB=(LRECL=80,RECFM=FB,BLKSIZE=800)                            
000800 //DD2      DD   DSN=TECN93.VVH1.GDG(+2),DISP=(NEW,CATLG,DELETE),        
000900 //       UNIT=3390,VOL=SER=ZAPRD6,                                      
001000 //       SPACE=(TRK,(1,1),RLSE),                                        
001100 //       DCB=(LRECL=80,RECFM=FB,BLKSIZE=800)                            
001200 //DD3      DD   DSN=TECN93.VVH1.GDG(+3),DISP=(NEW,CATLG,DELETE),        
001300 //       UNIT=3390,VOL=SER=ZAPRD6,                                      
001400 //       SPACE=(TRK,(1,1),RLSE),                                        
001500 //       DCB=(LRECL=80,RECFM=FB,BLKSIZE=800)                            
001600 //SYSPRINT DD   SYSOUT=*                                                
001700 //SYSIN    DD   DUMMY                                                   
001800 /*                                                                      
001900 //*CREATING MANY GDG GENERATIONS IN A SINGLE STEP                       
****** **************************** Bottom of Data ****************************
 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.GDGPDS(M5) - 01.05                  Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.GDGPS1,DISP=SHR                         
 000310 //SYSUT2   DD   DSN=TECN93.VVH2.GDG.G0005V00,                           
 000400 //      DISP=(OLD,CATLG,DELETE),                                        
 000500 //      SPACE=(TRK,(1,1)),                                              
 000600 //      DCB=TECN93.VVH1.GDG.MODEL,                                      
 000700 //      UNIT=3390,                                                      
 000800 //      VOL=SER=ZAPRD6                                                  
 001200 //DD2      DD   DSN=TECN93.VVH2.GDG.G0006V00,                           
 001500 //      DISP=(OLD,CATLG,DELETE),                                        
 001600 //      SPACE=(TRK,(1,1)),                                              
 001700 //      DCB=TECN93.VVH1.GDG.MODEL,                                      
 001800 //      UNIT=3390,                                                      
 001900 //      VOL=SER=ZAPRD6                                                  
 002100 //DD2      DD   DSN=TECN93.VVH2.GDG.G0007V00,                           
 002200 //      DISP=(OLD,CATLG,DELETE),                                        
 002300 //      SPACE=(TRK,(1,1)),                                              
 002400 //      DCB=TECN93.VVH1.GDG.MODEL,                                      
 002500 //      UNIT=3390,                                                      
 002600 //      VOL=SER=ZAPRD6                                                  
 002700 //SYSPRINT DD   SYSOUT=*                                                
 002800 //SYSIN    DD   DUMMY                                                   

 EDIT       TECN93.VVH1.GDGPDS(ALTERGDG) - 01.11            Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY93,RESTART=STEP2                                  
 000200 //STEP1    EXEC PGM=IDCAMS                                              
 000300 //SYSPRINT DD   SYSOUT=*                                                
 000400 //SYSIN    DD   *                                                       
 000500     DELETE TECN93.VVH1.GDG.G0007V00                                     
 000600 /*                                                                      
 000800 //STEP2    EXEC PGM=IDCAMS                                              
 000900 //SYSPRINT DD   SYSOUT=*                                                
 001000 //SYSIN    DD   *                                                       
 001100     ALTER TECN93.VVH1.GDG LIMIT(9)                                      
 001200 /*                                                                      
 001400 //STEP3    EXEC PGM=IDCAMS                                              
 001500 //SYSPRINT DD   SYSOUT=*                                                
 001600 //SYSIN    DD   *                                                       
 001700     ALTER TECN93.VVH1.GDG,EMPTY NOSCRATCH                               
 001800 /*                                                                      
 002000 //STEP4    EXEC PGM=IDCAMS                                              
 002100 //SYSPRINT DD   SYSOUT=*                                                
 002200 //SYSIN    DD   *                                                       
 002300     DELETE TECN93.VVH1.GDG PURGE                                        
 002400 /*                                                                      
 002600 //STEP5    EXEC PGM=IDCAMS                                              
 002700 //SYSPRINT DD   SYSOUT=*                                                
002800 //SYSIN    DD   *                                                       
002900     DELETE TECN93.VVH1.GDG PURGE FORCE                                  
003000 /*                                                                      
003100 //*                                                                     
003200 //STEP6    EXEC PGM=IDCAMS                                              
003300 //SYSPRINT DD   SYSOUT=*                                                
003400 //SYSIN    DD   *                                                       
003500     LISTCAT GDG ENTRIES(TECN93.VVH1.GDG)ALL                             
003600 /*                                                                      
003700 //STEP7    EXEC PGM=IDCAMS                                              
003800 //SYSPRINT DD   SYSOUT=*                                                
003900 //SYSIN    DD   *                                                       
004100     ALTER TECN93.VVH1.GDG,EMPTY SCRATCH                                 
004200 /*                                                                      
004300 //STEP8    EXEC PGM=IDCAMS                                              
004400 //SYSPRINT DD   SYSOUT=*                                                
004500 //SYSIN    DD   *                                                       
004600     ALTER TECN93.VVH1.GDG,NOEMPTY SCRATCH                               
004700 /*                                                                      
004800 //STEP9    EXEC PGM=IDCAMS                                              
004900 //SYSPRINT DD   SYSOUT=*                                                
005000 //SYSIN    DD   *                                                       
005100     ALTER TECN93.VVH1.GDG,NOEMPTY NOSCRATCH                             
005200 /*                                                                      

EDIT       TECN93.VVH1.PROC1(PROC) - 01.01                 Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //VISHNU1  PROC                                                         
000200 //STEP01   EXEC PGM=IEBGENER                                            
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000700 //VISHNU1 PEND                                                          
****** **************************** Bottom of Data ****************************
6
EDIT       TECN93.VVH1.PROC1(PROC) - 01.02                 Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //VISHNU1  PROC                                                         
 000200 //STEP01   EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   DUMMY                                                   
 000700 //VISHNU1 PEND                                                          
 000800 //*PROC CATALOGED PROCEDURE BASE                                        
 ****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.PROC1(PROCPR) - 01.07               Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //PROCLIB  JCLLIB ORDER=TECN93.VVH1.PROC1                               
 000300 //PROCSTEP EXEC PROC=VISHNU1                                            
 000400 //SYSPRINT DD   SYSOUT=*                                                
 000500 //SYSIN    DD   DUMMY                                                   
 000600 /*                                                                      
 000700 //*PROC CATALOGED PROCEDURE MAIN                                        
 ****** **************************** Bottom of Data ****************************
                                                                                
 EDIT       TECN93.VVH1.PROC(M3) - 01.01                    Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP PROC                                                             
 000300 //STEP01   EXEC PGM=IEBGENER                                            
 000400 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 000500 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000600 //SYSPRINT DD   SYSOUT=*                                                
 000700 //SYSIN    DD   DUMMY                                                   
 000800 //STEP PEND                                                             
 000900 //STEP02   EXEC PROC=STEP                                               
 001000 //SYSPRINT DD   SYSOUT=*                                                
 001100 //SYSIN    DD   DUMMY                                                   
 001200 //*THIS IS A PROGRM OF INTREAM PROCEDURE                                
 ****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.PROC1(M3) - 01.02                   Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEPA PROC                                                            
 000300 //STEP01   EXEC PGM=IEBGENER                                            
 000400 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 000500 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000600 //SYSPRINT DD   SYSOUT=*                                                
 000700 //SYSIN    DD   DUMMY                                                   
 000800 //STEPA PEND                                                            
 000801 //STEPB PROC                                                            
 000810 //STEP02   EXEC PGM=IEBGENER                                            
 000820 //SYSUT1   DD   DSN=TECN93.VVH1.PS,DISP=SHR                             
 000830 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000840 //SYSPRINT DD   SYSOUT=*                                                
 000850 //SYSIN    DD   DUMMY                                                   
 000860 //STEPB PEND                                                            
 000900 //STEP03   EXEC PROC=STEPB                                              
 001000 //SYSPRINT DD   SYSOUT=*                                                
 001100 //SYSIN    DD   DUMMY                                                   
 001200 //*THIS IS A PROGRM OF INTREAM PROCEDURE                                
 ****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.PROC1(M4) - 01.06                   Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEPA PROC                                                            
 000300 //STEP01   EXEC PGM=IEBGENER                                            
 000400 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 000500 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000600 //SYSPRINT DD   SYSOUT=*                                                
 000700 //SYSIN    DD   DUMMY                                                   
 000800 //STEPA PEND                                                            
 000900 //STEPB PROC                                                            
 001000 //STEP02   EXEC PGM=IEBGENER                                            
 001100 //SYSUT1   DD   DSN=TECN93.VVH1.PSC,DISP=SHR                            
 001200 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 001300 //SYSPRINT DD   SYSOUT=*                                                
 001400 //SYSIN    DD   DUMMY                                                   
 001500 //STEPB PEND                                                            
 001501 //*                                                                     
 001510 //PROCLIB  JCLLIB ORDER=TECN93.VVH1.PROC                                
 001600 //STEP01   EXEC PROC=M1                                                 
 001700 //SYSPRINT DD   SYSOUT=*                                                
 001800 //SYSIN    DD   DUMMY                                                   
 001900 //*THIS IS A PROGRM OF PROGRAM FOR COLIN JCLLIB AND PROC=M1             
 ****** **************************** Bottom of Data ****************************
                                                                                
 Command ===>                                                  Scroll ===> CSR  
  F1=Help      F2=Split     F3=Exit      F5=Rfind     F6=Rchange   F7=Up        
  F8=Down      F9=Swap     F10=Left     F11=Right    F12=Cancel                 
 EDIT       TECN93.VVH1.PROC1(OVERRIN) - 01.01              Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //VISHNU1  PROC                                                         
 000200 //STEP01   EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   DUMMY                                                   
 000700 //VISHNU1 PEND                                                          
 ****** **************************** Bottom of Data ****************************
 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.PROC1(OVERMAI) - 01.00              Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //PROCLIB  JCLLIB ORDER=TECN93.VVH1.PROC1                               
 000300 //PROCSTEP EXEC PROC=VISHNU1,REGION.STEP1=500K                          
 000400 //SYSPPINT DD   SYSOUT=*                                                
 000500 //SYSIN    DD   DUMMY                                                   
 000600 /*                                                                      
 000700 //*OVERRIDING THE PRAMETER                                              
 ****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.PROC1(NULLMIN) - 01.02              Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //PROCLIB  JCLLIB ORDER=TECN93.VVH1.PROC1                               
 000300 //PROCSTEP EXEC PROC=APPLE,TIME.STEP1=                                  
 000400 //SYSPPINT DD   SYSOUT=*                                                
 000500 //SYSIN    DD   DUMMY                                                   
 000600 /*                                                                      
 000700 //*NULLIFYING THE PRAMETER                                              
 ****** **************************** Bottom of Data ****************************
                                                                                
EDIT       TECN93.VVH1.PROC1(NULL) - 01.01                 Columns 00001 00072 
****** ***************************** Top of Data ******************************
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //APPLE PROC                                                            
000200 //STEP01   EXEC PGM=IEBGENER,TIME=(12,12)                               
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   DUMMY                                                   
000710 //STEP02   EXEC PGM=IEBGENER,TIME=(12,10)                               
000720 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
000730 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
000740 //SYSPRINT DD   SYSOUT=*                                                
000750 //SYSIN    DD   DUMMY                                                   
000800 //APPLE PEND                                                            
****** **************************** Bottom of Data ****************************
 EDIT       TECN93.VVH1.PROC(SET) - 01.02                   Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //SET PROC                                                              
 000110 //STEP1    EXEC PGM=IEBGENER                                            
 000200 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 000300 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 000400 //SYSPRINT DD   SYSOUT=*                                                
 000500 //SYSIN    DD   DUMMY                                                   
 000600 //SET PEND                                                              
 ****** **************************** Bottom of Data ****************************
                                                                                
 EDIT       TECN93.VVH1.PROC(SET1) - 01.05                  Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //PROCLIB  JCLLIB ORDER=TECN93.VVH1.PROC                                
 000300 //PROCSTEP EXEC PROC=SET                                                
 000400 //S1 SET T1=TECN93.VVH1.PSA                                             
 000500 //S2 SET T2=TECN93.VVH1.PSB                                             
 000600 //SYSUT1   DD   DSN=&T1                                                 
 000700 //SYSUT2   DD   DSN=&T2                                                 
 000800 //SYSPRINT DD   SYSOUT=*                                                
 000900 //SYSIN    DD   DUMMY                                                   
 001000 //*                                                                     
 001100 //*SET PROGRAM                                                          
 ****** **************************** Bottom of Data ****************************
                                                                                


 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.PDSC(M1) - 01.05                    Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP05                           
 000200 //STEP01   EXEC PGM=IEBCOMPR                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS02,DISP=SHR                           
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   *                                                       
 000700      COMPARE TYPORG=PS                                                  
 000800 /*                                                                      
 000810 //*                                                                     
 000900 //*PROGRAM FOR COMPARE PS FILES                                         
 001100 //STEP02   EXEC PGM=IEBGENER                                            
 001200 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 001300 //SYSUT2   DD   DSN=TECN93.VVH1.PS02,DISP=SHR                           
 001400 //SYSPRINT DD   SYSOUT=*                                                
 001500 //SYSIN    DD   DUMMY                                                   
 001600 /*                                                                      
 001610 //*PROGRAM FOR COPY FIRTSTHEN COMPARE PS                                
 001700 //STEP03   EXEC PGM=IEBCOPY                                             
 001710 //SYSUT1   DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
 001720 //SYSUT2   DD   DSN=TECN93.VVH1.PDS33,DISP=SHR                          
 001730 //SYSPRINT DD   SYSOUT=*                                                
 001740 //SYSIN    DD *                                                         
 001741     COPY INDD=SYSUT1,OUTDD=SYSUT2                                       
001750 /*                                                                      
001760 //*PROGRAMFORCOPYPDS FIRST THEN COMPRE PDS                              
001800 //STEP04   EXEC PGM=IEBCOMPR                                            
001900 //SYSUT1   DD   DSN=TECN93.VVH1.PDS1,DISP=SHR                           
002000 //SYSUT2   DD   DSN=TECN93.VVH1.PDS33,DISP=SHR                          
002100 //SYSPRINT DD   SYSOUT=*                                                
002200 //SYSIN    DD   *                                                       
002300      COMPARE TYPORG=PO                                                  
002400 /*                                                                      
002500 //*                                                                     
002600 //*PROGRAM FOR COMPARE PDS FILES                                        
****** **************************** Bottom of Data ****************************
 -------------------------------------------------------------------------------
 EDIT       TECN93.VVH1.PDSC(M2) - 01.00                    Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                            
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   DUMMY                                                   
 000700 /*                                                                      
 000800 //STEP2    EXEC PGM=IEBGENER                                            
 000900 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                            
 001000 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,ISP=SHR                             
 001100 //SYSPRINT DD   SYSOUT=*                                                
 001200 //SYSIN    DD   DUMMY                                                   
 001300 /*                                                                      
 001400 //STEP3    EXEC PGM=IEBGENER                                            
 001500 //SYSUT1   DD   DSN=TECN93.VVH1.PS3,DISP=SHR                            
 001600 //SYSUT2   DD   DSN=TECN93.VVH1.PS4,DISP=SHR                            
 001700 //SYSPRINT DD   SYSOUT=*                                                
 001800 //SYSIN    DD   DUMMY                                                   
 001900 /*                                                                      
 002000 //STEP4    EXEC PGM=IEBGENER                                            
 002100 //SYSUT1   DD   DSN=TECN93.VVH1.PS5,DISP=SHR                            
 002200 //SYSUT2   DD   DSN=TECN93.VVH1.PS6,DISP=SHR                            
 002300 //SYSPRINT DD   SYSOUT=*                                                
002400 //SYSIN    DD   DUMMY                                                   
****** **************************** Bottom of Data ****************************


COUD
 EDIT       TECN93.VVH1.CONDPDS(M2) - 01.01                 Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGE                                               
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                            
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   DUMMY                                                   
 000700 /*                                                                      
 000800 //STEP2    EXEC PGM=IEBGENER,COND=ONLY                                  
 000900 //SYSUT1   DD   DSN=TECN93.VVH1.PSC,DISP=SHR                            
 001000 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 001100 //SYSPRINT DD   SYSOUT=*                                                
 001200 //SYSIN    DD   DUMMY                                                   
 001300 /*                                                                      
 001400 //STEP3    EXEC PGM=IEBGENER                                            
 001500 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 001600 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                       
 001700 //SYSPRINT DD   SYSOUT=*                                                
 001800 //SYSIN    DD   DUMMY                                                   
 001900 /*                                                                      
 002000 //STEP4    EXEC PGM=IEBGENER                                            
 002100 //SYSUT1   DD   *                                                       
 002200 WELCOME VISHNU                                                          
 002300 //SYSUT2   DD   SYSOUT=*                                                
 002400 //SYSPRINT DD   SYSOUT=*                            
 002500 //SYSIN    DD   DUMMY                               
 002600 /*                                                  
 002700 //TECN93VV JOB  NOTIFY=&SYSUID                      
 002800 //STEP01   EXEC PGM=IEBGENER                        
 002900 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS22,DISP=SHR    
 003000 //SYSUT2   DD   DSN=&&TEMP                          
 003100 //SYSPRINT DD   SYSOUT=*                            
 003200 //SYSIN    DD   DUMMY                               
 003300 /*                                                  

EDIT       TECN93.VVH1.CONDPDS(M1) - 01.10                 Columns 00001 000
****** ***************************** Top of Data ***************************
==MSG> -Warning- The UNDO command is not available until you change         
==MSG>           your edit profile using the command RECOVERY ON.           
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                       
000200 //STEP1    EXEC PGM=IEBGENER                                         
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                         
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                         
000500 //SYSPRINT DD   SYSOUT=*                                             
000600 //SYSIN    DD   DUMMY                                                
000700 /*                                                                   
000820 //STEP2    EXEC PGM=IEBGENER,COND=(0,EQ)                             
000830 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                         
000840 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                         
000850 //SYSPRINT DD   SYSOUT=*                                             
000860 //SYSIN    DD   DUMMY                                                
000870 /*                                                                   
001100 //STEP3    EXEC PGM=IEBGENER                                         
001200 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                         
001300 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                    
001400 //SYSPRINT DD   SYSOUT=*                                             
001500 //SYSIN    DD   DUMMY                                                
001600 /*                                                                   
001620 //STEP4    EXEC PGM=IEBGENER                                         
001630 //SYSUT1   DD   *                                                    
001640 WELCOME VISHNU                                                       
001650 //SYSUT2   DD   SYSOUT=*                                             
001660 //SYSPRINT DD   SYSOUT=*                                
001670 //SYSIN    DD   DUMMY                                   
001680 /*                                                      
001681 //TECN93VV JOB  NOTIFY=&SYSUID                          
001682 //STEP01   EXEC PGM=IEBGENER                            
001683 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS22,DISP=SHR        
001684 //SYSUT2   DD   DSN=&&TEMP                              
001685 //SYSPRINT DD   SYSOUT=*                                
001686 //SYSIN    DD   DUMMY                                   
001687 /*                                                      

IF END IF
 EDIT       TECN93.VVH1.CONDPDS(M3) - 01.01                 Columns 00001 00072 
 ****** ***************************** Top of Data ******************************
 ==MSG> -Warning- The UNDO command is not available until you change            
 ==MSG>           your edit profile using the command RECOVERY ON.              
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 000200 //STEP1    EXEC PGM=IEBGENER                                            
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                            
 000500 //SYSPRINT DD   SYSOUT=*                                                
 000600 //SYSIN    DD   *                                                       
 000610 //   IF RC=00 THEN                                                      
 000700 /*                                                                      
 000800 //STEP2    EXEC PGM=IEBGENER                                            
 000900 //SYSUT1   DD   DSN=TECN93.VVH1.PSC,DISP=SHR                            
 001000 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                            
 001100 //SYSPRINT DD   SYSOUT=*                                                
 001200 //SYSIN    DD   *                                                       
 001300 //   ENDIF                                                              
 001310 /*                                                                      
 001320 //                                                                      
 001400 //STEP3    EXEC PGM=IEBGENER                                            
 001500 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                            
 001600 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                       
 001700 //SYSPRINT DD   SYSOUT=*                                                
 001800 //SYSIN    DD   DUMMY                                                   
 001900 /*                                                                      
 002000 //STEP4    EXEC PGM=IEBGENER  
001900 /*                                                 
002000 //STEP4    EXEC PGM=IEBGENER                       
002100 //SYSUT1   DD   *                                  
002200 WELCOME VISHNU                                     
002300 //SYSUT2   DD   SYSOUT=*                           
002400 //SYSPRINT DD   SYSOUT=*                           
002500 //SYSIN    DD   DUMMY                              
002600 /*                                                 
002700 //TECN93VV JOB  NOTIFY=&SYSUID                     
002800 //STEP01   EXEC PGM=IEBGENER                       
002900 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS22,DISP=SHR   
003000 //SYSUT2   DD   DSN=&&TEMP                         
003100 //SYSPRINT DD   SYSOUT=*                           
003200 //SYSIN    DD   DUMMY                              
003300 /*                                                 

IF ELSE IF
 EDIT       TECN93.VVH1.CONDPDS(M4) - 01.02                 Columns 00001 0007
 ****** ***************************** Top of Data ****************************
 ==MSG> -Warning- The UNDO command is not available until you change          
 ==MSG>           your edit profile using the command RECOVERY ON.            
 000100 //TECN93VV JOB  NOTIFY=&SYSUID                                        
 000200 //STEP1    EXEC PGM=IEBGENER                                          
 000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                          
 000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                          
 000500 //SYSPRINT DD   SYSOUT=*                                              
 000600 //SYSIN    DD   *                                                     
 000700 //   IF RC=00 THEN                                                    
 000800 /*                                                                    
 000900 //STEP2    EXEC PGM=IEBGENER                                          
 001000 //SYSUT1   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                          
 001100 //SYSUT2   DD   DSN=TECN93.VVH1.PSC,DISP=SHR                          
 001200 //SYSPRINT DD   SYSOUT=*                                              
 001300 //SYSIN    DD   *                                                     
 001400 //   ELSE                                                             
 001500 /*                                                                    
 001700 //STEP3    EXEC PGM=IEBGENER                                          
 001800 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                          
 001900 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                     
 002000 //SYSPRINT DD   SYSOUT=*                                              
 002100 //SYSIN    DD   DUMMY                                                 
 002110 //  ENDIF                                                             
 002200 /*                                                                    
 002210 //                                                                    
002300 //STEP4    EXEC PGM=IEBGENER                            
002400 //SYSUT1   DD   *                                       
002500 WELCOME VISHNU                                          
002600 //SYSUT2   DD   SYSOUT=*                                
002700 //SYSPRINT DD   SYSOUT=*                                
002800 //SYSIN    DD   DUMMY                                   
002900 /*                                                      
003000 //TECN93VV JOB  NOTIFY=&SYSUID                          
003100 //STEP01   EXEC PGM=IEBGENER                            
003200 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS22,DISP=SHR        
003300 //SYSUT2   DD   DSN=&&TEMP                              
003400 //SYSPRINT DD   SYSOUT=*                                
003500 //SYSIN    DD   DUMMY                                   
003600 /*                                                      
****** ***************************** Top of Data ******************************
EDIT       TECN93.VVH1.CONDPDS(M1) - 01.10                 Columns 00001 000
****** ***************************** Top of Data ***************************
==MSG> -Warning- The UNDO command is not available until you change         
==MSG>           your edit profile using the command RECOVERY ON.           
000100 //TECN93VV JOB  NOTIFY=&SYSUID                                       
000200 //STEP1    EXEC PGM=IEBGENER                                         
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                         
000400 //SYSUT2   DD   DSN=TECN93.VVH1.PS2,DISP=SHR                         
000500 //SYSPRINT DD   SYSOUT=*                                             
000600 //SYSIN    DD   DUMMY                                                
000700 /*                                                                   
000820 //STEP2    EXEC PGM=IEBGENER,COND=(0,EQ)                             
000830 //SYSUT1   DD   DSN=TECN93.VVH1.PSA,DISP=SHR                         
000840 //SYSUT2   DD   DSN=TECN93.VVH1.PSB,DISP=SHR                         
000850 //SYSPRINT DD   SYSOUT=*                                             
000860 //SYSIN    DD   DUMMY                                                
000870 /*                                                                   
001100 //STEP3    EXEC PGM=IEBGENER                                         
001200 //SYSUT1   DD   DSN=TECN93.VVH1.PS1,DISP=SHR                         
001300 //SYSUT2   DD   DSN=TECN93.VVH1.PDS1(M2),DISP=SHR                    
001400 //SYSPRINT DD   SYSOUT=*                                             
001500 //SYSIN    DD   DUMMY                                                
001600 /*                                                                   
001620 //STEP4    EXEC PGM=IEBGENER                                         
001630 //SYSUT1   DD   *                                                    
001640 WELCOME VISHNU                                                       
001650 //SYSUT2   DD   SYSOUT=*                                             
001660 //SYSPRINT DD   SYSOUT=*                                
001670 //SYSIN    DD   DUMMY                                   
001680 /*                                                      
001681 //TECN93VV JOB  NOTIFY=&SYSUID                          
001682 //STEP01   EXEC PGM=IEBGENER                            
001683 //SYSUT1   DD   DSN=TECN93.VVH1.TDCPS22,DISP=SHR        
001684 //SYSUT2   DD   DSN=&&TEMP                              
001685 //SYSPRINT DD   SYSOUT=*                                
001686 //SYSIN    DD   DUMMY                                   
001687 /*                                                      
==MSG> -Warning- The UNDO command is not available until you change            
==MSG>           your edit profile using the command RECOVERY ON.              
000100 //TECN93VV JOB  NOTIFY=SYSUID,RESTART=STEP2                             
000200 //STEP1    EXEC PGM=IEBEDIT                                             
000300 //SYSUT1   DD   DSN=TECN93.VVH1.PDSC(M2),DISP=SHR                       
000400 //SYSUT2   DD   SYSOUT=(*,INTRDR)                                       
000500 //SYSPRINT DD   SYSOUT=*                                                
000600 //SYSIN    DD   *                                                       
000700      EDIT TYPE=EXCLUDE,STEPNAME=(STEP2,STEP3)                           
000800 /*                                                                      
000810 //*                                                                     
000900 //*PROGRAM TO EDIT PDS MEMBERS EXCLUDE                                  
001000 //STEP2    EXEC PGM=IEBEDIT                                             
001100 //SYSUT1   DD   DSN=TECN93.VVH1.PDSC(M2),DISP=SHR                       
001200 //SYSUT2   DD   SYSOUT=(*,INTRDR)                                       
001300 //SYSPRINT DD   SYSOUT=*                                                
001400 //SYSIN    DD   *                                                       
001500      EDIT TYPE=INCLUDE,STEPNAME=(STEP1,STEP3)                           
001600 /*                                                                      
001700 //*PROGRAM TO EDIT PDS MEMBERS INCLUDE                                  
****** **************************** Bottom of Data ****************************
                                                                                                                         
                     
                                   
