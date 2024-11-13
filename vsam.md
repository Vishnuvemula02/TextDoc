//TECN93VV JOB  NOTIFY=&SYSUID                     
//STEP1    EXEC PGM=IDCAMS                         
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   *                                  
     DEFINE CLUSTER(NAME(TECN93.VVH2.VSAM.KSDS)-    
     TRK(1,1)-                                     
     VOL(ZAPRD6)-                                  
     RECORDSIZE(80,80)-                            
     CISZ(4096)-                                   
     KEYS(4,0)-                                    
     INDEXED)                                      
/*                                                 
//*THIS IS CREATION OF VASM KSDS FILE              

OUT PUT :
TECN93.VVH2.VSAM.KSDS      
TECN93.VVH2.VSAM.KSDS.DATA 
TECN93.VVH2.VSAM.KSDS.INDEX

//TECN93VV JOB  NOTIFY=&SYSUID                    
//STEP1    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
     DEFINE CLUSTER(NAME(TECN93.VVH2.VSAM.ESDSA)- 
     TRK(1,1)-                                    
     VOL(ZAPRD6)-                                 
     RECORDSIZE(80,80)-                           
     CISZ(4096)-                                  
     NONINDEXED)                                  
//                                                

OUT PUT :TECN93.VVH2.VSAM.ESDS       
                    TECN93.VVH2.VSAM.ESDS.DATA  
 
 //TECN93VV JOB  NOTIFY=&SYSUID                      
//STEP1    EXEC PGM=IDCAMS                          
//SYSPRINT DD   SYSOUT=*                            
//SYSIN    DD   *                                   
     DEFINE CLUSTER(NAME(TECN93.VVH2.VSAM.RRDS2)-   
     TRK(1,1)-                                      
     VOL(ZAPRD6)-                                   
     RECORDSIZE(80,80)-                             
     CISZ(4096)-                                    
     NUMBERED)                                      
/*                                                  
//*THIS IS CREATION OF VASM RRDSS FILE              

OUT PUT :  TECN93.VVH2.VSAM.RRDS      
                     TECN93.VVH2.VSAM.RRDS.DATA 

//TECN93VV JOB  NOTIFY=&SYSUID                        
//STEP1    EXEC PGM=IDCAMS                            
//SYSPRINT DD   SYSOUT=*                              
//SYSIN    DD   *                                     
     DEFINE CLUSTER(NAME(TECN93.VVH2.VSAM.VRRDS2)-    
     TRK(1,1)-                                        
     VOL(ZAPRD6)-                                     
     RECORDSIZE(80,80)-                               
     CISZ(4096)-                                      
     NUMBERED)                                        
/*                                                    
//*THIS IS CREATION OF VASM VRRDS FILE                

OUT PUT:TECN93.VVH2.VSAM.VRRDS      
                  TECN93.VVH2.VSAM.VRRDS.DATA

//TECN93VV JOB  NOTIFY=&SYSUID                    
//STEP1    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
     DEFINE CLUSTER(NAME(TECN93.VVH2.VSAM.LDS)-   
     TRK(1,1)-                                    
     VOL(ZAPRD6)-                                 
     CISZ(4096)-                                  
     LINEAR)                                      
/*                                                
//*THIS IS CREATION OF VASM LDSFILE               

OUT PUT:  TECN93.VVH2.VSAM.LDS      
                    TECN93.VVH2.VSAM.LDS.DATA 
 
COPY PROGRAME:                                                                           PRINT CH IDS(/)
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP2        
//STEP1    EXEC PGM=IDCAMS                          
//SYSPRINT DD   SYSOUT=*                            
//DD1      DD   DSN=TECN93.VVH2.PS1,DISP=SHR        
//DD2      DD   DSN=TECN93.VVH2.VSAM.KSDS,DISP=OLD  
//SYSIN    DD   *                                   
      REPRO-                                        
      INFILE(DD1)OUTFILE(DD2)                       
/*
 KEY OF RECORD - A001                                                           
 A001 SUDHAKAR      KGF       95969897942 HR                             0000010
0                                                                               
 ***                                                                            
 KEY OF RECORD - A002                                                           
 A002 VISHNUVARDHAN ONGOL                 ADMIN                          0000020
0                                                                               
 KEY OF RECORD - A003                                                           
 A003 RAJ           KOLAR     98969594933 FINANCE                        0000030
0                                                                               
 KEY OF RECORD - A004                                                           
 A004 KIRAN         BANGALORE 99556667778 HR                             0000040
0                                                                               
 KEY OF RECORD - A005                                                           
 A005 VARUN         HYDRABAD  88888777777 ACC                            0000050
0                                                                               
 KEY OF RECORD - A006                                                           
 A006 SAI           TTD       55555555555 ASS                            0000060
0                                                                               
 IDC0005I NUMBER OF RECORDS PROCESSED WAS 6                                     
 ***                                                                            

 //TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP5         
 //STEP1    EXEC PGM=IDCAMS                           
 //SYSPRINT DD   SYSOUT=*                             
 //DD1      DD   DSN=TECN93.VVH2.PS1,DISP=SHR         
 //DD2      DD   DSN=TECN93.VVH2.VSAM.ESDS,DISP=OLD   
 //SYSIN    DD   *                                    
       REPRO-                                         
       INFILE(DD1)OUTFILE(DD2)                        
 /*                                                   
 RBA OF RECORD -                0                                               
A001 SUDHAKAR      KGF       95969897942 HR                             0000010
                                                                               
***                                                                            
 RBA OF RECORD -               80                                               
 A002 VISHNUVARDHAN ONGOL                 ADMIN                          0000020
0                                                                               
 RBA OF RECORD -              160                                               
 A003 RAJ           KOLAR     98969594933 FINANCE                        0000030
0                                                                               
 RBA OF RECORD -              240                                               
 A004 KIRAN         BANGALORE 99556667778 HR                             0000040
0                                                                               
 RBA OF RECORD -              320                                               
 A005 VARUN         HYDRABAD  88888777777 ACC                            0000050
0                                                                               
 RBA OF RECORD -              400                                               
 A006 SAI           TTD       55555555555 ASS                            0000060
0                                                                               
 RBA OF RECORD -              480                                               
 A005 RAM           YTD       00000000000 ZXXX                           0000070
0                                                                               
 RBA OF RECORD -              560                                               
 A006 KRISHNA       TAM       12345678910 VVVV                           0000080
0                                                                               
 RBA OF RECORD -              640                                               
 (4,0)(5,17)        (20,9)    (30,10)     (42,7)                         0000090
0                                                                               
 IDC0005I NUMBER OF RECORDS PROCESSED WAS 9                                     
 ***                                                                            


 //TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP6        
 //STEP1    EXEC PGM=IDCAMS                          
 //SYSPRINT DD   SYSOUT=*                            
 //DD1      DD   DSN=TECN93.VVH2.PS1,DISP=SHR        
 //DD2      DD   DSN=TECN93.VVH2.VSAM.RRDS,DISP=SHR  
 //SYSIN    DD   *                                   
       REPRO-                                        
       INFILE(DD1)OUTFILE(DD2)                       
 /*                                                  
 RELATIVE RECORD NUMBER - 1                                                     
 A001 SUDHAKAR      KGF       95969897942 HR                             0000010
0                                                                               
 ***                                                                            
RELATIVE RECORD NUMBER - 2                                                     
A002 VISHNUVARDHAN ONGOL                 ADMIN                          0000020
                                                                               
RELATIVE RECORD NUMBER - 3                                                     
A003 RAJ           KOLAR     98969594933 FINANCE                        0000030
                                                                               
RELATIVE RECORD NUMBER - 4                                                     
A004 KIRAN         BANGALORE 99556667778 HR                             0000040
                                                                               
RELATIVE RECORD NUMBER - 5                                                     
A005 VARUN         HYDRABAD  88888777777 ACC                            0000050
                                                                               
RELATIVE RECORD NUMBER - 6                                                     
A006 SAI           TTD       55555555555 ASS                            0000060
                                                                               
RELATIVE RECORD NUMBER - 7                                                     
A005 RAM           YTD       00000000000 ZXXX                           0000070
                                                                               
RELATIVE RECORD NUMBER - 8                                                     
A006 KRISHNA       TAM       12345678910 VVVV                           0000080
                                                                               
RELATIVE RECORD NUMBER - 9                                                     
(4,0)(5,17)        (20,9)    (30,10)     (42,7)                         0000090
                                                                               
IDC0005I NUMBER OF RECORDS PROCESSED WAS 9                                     
***                                                                            
 //TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP5           
 //STEP1    EXEC PGM=IDCAMS                             
 //SYSPRINT DD   SYSOUT=*                               
 //DD1      DD   DSN=TECN93.VVH2.PS1,DISP=SHR           
 //DD2      DD   DSN=TECN93.VVH2.VSAM.VRRDS,DISP=OLD    
 //SYSIN    DD   *                                      
       REPRO-                                           
       INFILE(DD1)OUTFILE(DD2)                          
 /*                                                     
 RELATIVE RECORD NUMBER - 1                                                     
 A001 SUDHAKAR      KGF       95969897942 HR                             0000010
0                                                                               
 ***                                                                            
RELATIVE RECORD NUMBER - 2                                                     
A002 VISHNUVARDHAN ONGOL                 ADMIN                          0000020
                                                                               
RELATIVE RECORD NUMBER - 3                                                     
A003 RAJ           KOLAR     98969594933 FINANCE                        0000030
                                                                               
RELATIVE RECORD NUMBER - 4                                                     
A004 KIRAN         BANGALORE 99556667778 HR                             0000040
                                                                               
RELATIVE RECORD NUMBER - 5                                                     
A005 VARUN         HYDRABAD  88888777777 ACC                            0000050
                                                                               
RELATIVE RECORD NUMBER - 6                                                     
A006 SAI           TTD       55555555555 ASS                            0000060
                                                                               
RELATIVE RECORD NUMBER - 7                                                     
A005 RAM           YTD       00000000000 ZXXX                           0000070
                                                                               
RELATIVE RECORD NUMBER - 8                                                     
A006 KRISHNA       TAM       12345678910 VVVV                           0000080
                                                                               
RELATIVE RECORD NUMBER - 9                                                     
(4,0)(5,17)        (20,9)    (30,10)     (42,7)                         0000090
                                                                               
IDC0005I NUMBER OF RECORDS PROCESSED WAS 9                                     
***                                                                            
//TECN93VV JOB  NOTIFY=&SYSUID                      
//STEP1    EXEC PGM=IDCAMS                          
//SYSPRINT DD   SYSOUT=*                            
//DD1      DD   DSN=TECN93.VVH2.PS3LDS,DISP=SHR     
//DD2      DD   DSN=TECN93.VVH2.VSAM.LDS,DISP=OLD   
//SYSIN    DD   *                                   
      REPRO-                                        
      INFILE(DD1)OUTFILE(DD2)                       
/*
                               Data Set Utility                                
                                                                               
    A Allocate new data set                 C Catalog data set                 
    R Rename entire data set                U Uncatalog data set               
    D Delete entire data set                S Short data set information       
blank Data set information                  V VSAM Utilities                   
                                                                               
ISPF Library:                                                                  
   Project  . . TECN93           Enter "/" to select option                    
   Group  . . . VVH2             /  Confirm Data Set Delete                    
   Type . . . . LDSPS                                                          
                                                                               
Other Partitioned, Sequential or VSAM Data Set:                                
   Name  . . . . . . .                                                         
   Volume Serial . . .           (If not cataloged, required for option "C")   
                                                                               
Data Set Password  . .           (If password protected)                       

                            Allocate New Data Set                              
                                                                   More:     + 
Data Set Name  . . . : TECN93.VVH2.LDSPS                                       
                                                                               
Management class . . .                (Blank for default management class)     
Storage class  . . . .                (Blank for default storage class)        
 Volume serial . . . . ZAPRD6         (Blank for system default volume) **     
 Device type . . . . .                (Generic unit or device address) **      
Data class . . . . . .                (Blank for default data class)           
 Space units . . . . . TRACK          (BLKS, TRKS, CYLS, KB, MB, BYTES         
                                       or RECORDS)                             
 Average record unit                  (M, K, or U)                             
 Primary quantity  . . 1              (In above units)                         
 Secondary quantity    1              (In above units)                         
 Directory blocks  . . 0              (Zero for sequential data set) *         
 Record format . . . . FB                                                      
 Record length . . . . 4096                                                    
 Block size  . . . . . 8192                                                    
 Data set name type                   (LIBRARY, HFS, PDS, LARGE, BASIC, *      
                                       EXTREQ, EXTPREF or blank)               
 Expiration date . . .                (YY/MM/DD, YYYY/MM/DD                    
Enter "/" to select option             YY.DDD, YYYY.DDD in Julian form         
   Allocate Multiple Volumes           DDDD for retention period in days       
                                       or blank)                               
                                                                               
( * Specifying LIBRARY may override zero directory block)                      
                                                                               
Command ===>                                                                   
 F1=Help      F2=Split     F3=Exit      F7=Backward  F8=Forward   F9=Swap      
F10=Actions  F12=Cancel                                                        

 RBA OF RECORD -                0                  
 A001 SUDHAKAR           ONGOLE    9987654321  HR  
  



 RBA OF RECORD -             4096                     
 A002 SUDHA              KGF       9933332222  ADMIN                                                   
 ***


RBA OF RECORD -             8192                         
A003 KIRAN              BANGALORE 9987654391  FINANCE    



RBA OF RECORD -            12288                  
A004 VINAY SRINVASREDDY MYSORE    2987654321  HR  
                                                  


RBA OF RECORD -            16384                   
A005 RAJ                KOLAR     0000112222  ACC  



RBA OF RECORD -            20480                    
(4,0)(18,5)             (9,25)    (10,35)     (7,47)
IDC0005I NUMBER OF RECORDS PROCESSED WAS 6  


//TECN93VV JOB  NOTIFY=&SYSUID         
//STEP1    EXEC PGM=IDCAMS                             
//DD1      DD   DSN=TECN93.VVH2.VSAM.KSDS,DISP=SHR     
//DD2      DD   DSN=TECN93.VVH2.PS4,DISP=OLD           
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
    REPRO-                                             
    INFILE(DD1)OUTFILE(DD2)-                           
    FROMKEY(A003)TOKEY(AOO5)                           
/*                                                     
 //*KSDS FROMKEYSTOKEYS       
OUT PUT: A004 KIRAN         BANGALORE 99556667778 HR          
 A005 VARUN         HYDRABAD  88888777777 ACC         
 A006 SAI           TTD       55555555555 ASS         
 A001 SUDHAKAR      KGF       95969897942 HR          
 A002 VISHNUVARDHAN ONGOL                 ADMIN       
 A003 RAJ           KOLAR     98969594933 FINANCE     


//TECN93VV JOB  NOTIFY=&SYSUID  
//STEP2   EXEC PGM=IDCAMS                             
//DD1      DD   DSN=TECN93.VVH2.VSAM.RRDS1,DISP=SHR    
//DD2      DD   DSN=TECN93.VVH2.PS4,DISP=OLD           
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
    REPRO-                                             
    INFILE(DD1)OUTFILE(DD2)-                           
    FROMNUMBER(2)TONUMBER(4)                           
/*                                                     
//*RRDS1FROMNUMBERTONUMBER
OUT PUT:
 A002 VISHNUVARDHAN ONGOL                 ADMIN      
 A003 RAJ           KOLAR     98969594933 FINANCE    
 A004 KIRAN         BANGALORE 99556667778 HR          
   
//STEP7    EXEC PGM=IDCAMS                          
//DD1      DD   DSN=TECN93.VVH2.VSAM.VRRDS1,DISP=SHR
//DD2      DD   DSN=TECN93.VVH2.PS6,DISP=OLD       
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   *                                  
    REPRO-                                         
    INFILE(DD1)OUTFILE(DD2)-                       
    FROMNUMBER(2)TONUMBER(4)                       
/*                                                 
//* VRRDS FROMNUMBERTONUMBER 
OUT PUT:
 A002 VISHNUVARDHAN ONGOL                 ADMIN     
 A003 RAJ           KOLAR     98969594933 FINANCE   
 A004 KIRAN         BANGALORE 99556667778 HR                              


//STEP3    EXEC PGM=IDCAMS                         
//DD1      DD   DSN=TECN93.VVH2.VSAM.ESDS,DISP=SHR 
//DD2      DD   DSN=TECN93.VVH2.PS4,DISP=OLD       
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   *                                  
    REPRO-                                         
    INFILE(DD1)OUTFILE(DD2)-                       
    FROMADDRESS(80)TOADDRESS(240)                  
/*                                                 
//*  ESDS FROMADDRESSTOADDRESS 
 OUT PUT:
A002 VISHNUVARDHAN ONGOL                 ADMIN    
A003 RAJ           KOLAR     98969594933 FINANCE  
A004 KIRAN         BANGALORE 99556667778 HR       

                    
//STEP4    EXEC PGM=IDCAMS                         
//DD1      DD   DSN=TECN93.VVH2.VSAM.ESDS1,DISP=SHR
//DD2      DD   DSN=TECN93.VVH2.PS4,DISP=OLD       
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   *                                  
    REPRO-                                         
    INFILE(DD1)OUTFILE(DD2)-                       
    SKIP(3)-                                       
 /*  
 //*SKIP()COUN() ESDS1   
OUT PUT:
 A004 KIRAN         BANGALORE 99556667778 HR          
 A005 VARUN         HYDRABAD  88888777777 ACC         
 A006 SAI           TTD       55555555555 ASS         
 A001 SUDHAKAR      KGF       95969897942 HR          
 A002 VISHNUVARDHAN ONGOL                 ADMIN       
 A003 RAJ           KOLAR     98969594933 FINANCE                                                     
                            
 //STEP5    EXEC PGM=IDCAMS                          
 //DD1      DD   DSN=TECN93.VVH2.VSAM.KSDS1,DISP=SHR 
 //DD2      DD   DSN=TECN93.VVH2.PS5,DISP=OLD        
 //SYSPRINT DD   SYSOUT=*                            
 //SYSIN    DD   *                                   
     REPRO-                                          
     INFILE(DD1)OUTFILE(DD2)-                        
     SKIP(3)-                                        
     COUNT(6)                                        
 /*                                                  
 //* SKIP()COUNT() KSDS1                             
 //STEP6    EXEC PGM=IDCAMS                          
 //DD1      DD   DSN=TECN93.VVH2.VSAM.VRRDS1,DISP=SHR
 //DD2      DD   DSN=TECN93.VVH2.PS6,DISP=OLD        
 //SYSPRINT DD   SYSOUT=*                            
 //SYSIN    DD   *                                   
     REPRO-                                          
     INFILE(DD1)OUTFILE(DD2)-                        
     SKIP(3)-                                        
     COUNT(6)                                        
 /*                                                  
 //* SKIP()COUNT() VRRDS1                            
 //STEP8    EXEC PGM=IDCAMS                          
//DD1      DD   DSN=TECN93.VVH2.VSAM.RRDS1,DISP=SHR  
//DD2      DD   DSN=TECN93.VVH2.PS6,DISP=OLD         
//SYSPRINT DD   SYSOUT=*                             
//SYSIN    DD   *                                    
    REPRO-                                           
    INFILE(DD1)OUTFILE(DD2)-                         
    SKIP(2)-                                         
    COUNT(6)                                         
//*SKIP()COUNT() RRDS1      
VSAM 2 
//TECN93VV JOB  NOTIFY=&SYSUID      
//STEP1    EXEC PGM=IDCAMS          
//SYSPRINT DD   SYSOUT=*            
//SYSIN    DD   *                   
     ALTER TECN93.VVH2.KSDS3.DATA-  
      INHIBIT                       
     ALTER TECN93.VVH2.KSDS3.INDEX- 
      INHIBIT                       
OUT PUT:
THE DATASET NOT OPEN



 //STEP2    EXEC PGM=IDCAMS                               
 //DD1      DD   DSN=TECN93.VVH2.PS1,DISP=SHR             
 //DD2      DD   DSN=TECN93.VVH2.VSAM.KSDS3,DISP=MOD      
 //SYSPRINT DD   SYSOUT=*                                 
 //SYSIN    DD   *                                        
     REPRO-                                               
     INFILE(DD1)OUTFILE(DD2)                              
 //                                                       
 //*COPY  TO INHIBIT                                      



KEY OF RECORD - A001                       
A001 SUDHAKAR      KGF       95969897942 HR

KEY OF RECORD - A002                            
A002 VISHNUVARDHAN ONGOL                 ADMIN  
                                                
KEY OF RECORD - A003                            
A003 RAJ           KOLAR     98969594933 FINANCE
                                                
KEY OF RECORD - A004                            
A004 KIRAN         BANGALORE 99556667778 HR     
                                                
KEY OF RECORD - A005                            
A005 VARUN         HYDRABAD  88888777777 ACC    
                                                
KEY OF RECORD - A006                            
A006 SAI           TTD       55555555555 ASS    
                                                
IDC0005I NUMBER OF RECORDS PROCESSED WAS 6
//STEP3    EXEC PGM=IDCAMS 

                         
//DD1      DD   DSN=TECN93.VVH2.PS1,DISP=SHR        
//DD2      DD   DSN=TECN93.VVH2.VSAM.KSDS3,DISP=MOD 
 //SYSPRINT DD   SYSOUT=*                  
 //SYSIN    DD   *                         
     ALTER TECN93.VVH2.VSAM.KSDS3.DATA-    
     UNINHIBIT                             
     ALTER TECN93.VVH2.VSAM.KSDS3.INDEX-   
     UNINHIBIT                             
 /*                                        
 //*UNINHIBIT 

                             
//STEP4    EXEC PGM=IDCAMS               
//SYSPRINT DD   SYSOUT=*                 
//SYSIN    DD   *
    ALTER TECN93.VVH2.VSAM.KSDS3.DATA- 
    NEWNAME(TECN93.VVH2.KSDS1.33.DATA)                         
    ALTER TECN93.VVH2.VSAM.KSDS2.INDEX-  
    NEWNAME(TECN93.VVH2.KSDS1.INDEX)     
                                         
/*                                       
//*INDEX NEW NAME

 
  //STEP5    EXEC PGM=IDCAMS                 
//SYSPRINT DD   SYSOUT=*                   
//SYSIN    DD   *                          
    ALTER TECN93.VVH2.VSAM.KSDS3-          
    NEWNAME(TECN93.VVH2.KSDS1.33)          
    ALTER TECN93.VVH2.VSAM.KSDS3.DATA-     
    NEWNAME(TECN93.VVH2.KSDS1.33.DATA)     
    ALTER TECN93.VVH2.VSAM.KSDS3.INDEX-    
    NEWNAME(TECN93.VVH2.KSDS1.33. INDEX)   
//  



//TECN93VV JOB  NOTIFY=SYSUID,RESTART=STEP2                 
//STEP1    EXEC PGM=IDCAMS                                  
//SYSPRINT DD   SYSOUT=*                                    
//SYSIN    DD   *                                           
      DELETE TECN93.VVH2.VSAM.VRRDS1CLUSTER                 
/*                                                          
//*DELETING CLUSTER                                         
//STEP2    EXEC PGM=IDCAMS                                  
//SYSPRINT DD   SYSOUT=*                                    
//SYSIN    DD   *                                           
      DELETE TECN93.VVH2.AIXNM1                             
/*                                                          
//*DELETING ALTERNATE INDEX                                 
/*                                                          
//STEP3    EXEC PGM=IDCAMS                                  
//SYSPRINT DD   SYSOUT=*                                    
//SYSIN    DD   *                                           
      DELETE TECN93.VVH2.VSAM.AIXPATH                       
/*                                                          
//*DELETING PATH                                            
/*                                                          
//STEP4    EXEC PGM=IDCAMS                                  
//SYSPRINT DD   SYSOUT=*                                    
//SYSIN    DD   *                         
      DELETE TECN93.VVH2.VSAM.KSDS        
/*                                        
//*DELETING   CLUSTER ERASE               
/*                                        
//STEP5    EXEC PGM=IDCAMS                
//SYSPRINT DD   SYSOUT=*                  
//SYSIN    DD   *                         
      DELETE TECN93.VVH2.VSAM.KSDS1       
/*                                        
//*DELETING   CLUSTER PURGE               
/*

//TECN93VV JOB  NOTIFY=&SYSUID                     
//STEP1    EXEC PGM=IDCAMS                         
//SYSPRINT DD   SYSOUT=*                           
//SYSIN    DD   *                                  
     ALTER TECN93.VVH2.KSDS1.DATA-                 
     ADDVOLUMES(ZAPRD4)                            
     ALTER TECN93.VVH2.KSDS1.INDEX-                
     ADDVOLUMES(ZAPRD4)                            
/*                                                 
LIST CAT  :

 //TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP2                   
 //STEP1    EXEC PGM=IDCAMS                                     
 //SYSPRINT DD   SYSOUT=*                                       
 //SYSIN    DD   *                                              
      LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)                    
 /*  
//* DISPLAYS PRIMARY AND SECONDARY QUNTITY UNITS    
       
OUT PUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 10:12:07
                                                                                
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)                             00040002
CLUSTER ------- TECN93.VVH2.KSDS1                                               
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.319                    
       RELEASE----------------2     EXPIRATION------0000.000                    
       BWO STATUS--------(NULL)     BWO TIMESTAMP-----(NULL)                    
       BWO---------------(NULL)                                                 
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       DATA-----TECN93.VVH2.KSDS1.DATA                                          
       INDEX----TECN93.VVH2.KSDS1.INDEX                                         
   DATA ------- TECN93.VVH2.KSDS1.DATA                                          
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.319                    
       RELEASE----------------2     EXPIRATION------0000.000                    
       ACCOUNT-INFO-----------------------------------(NULL)                    
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       CLUSTER--TECN93.VVH2.KSDS1                                               
     ATTRIBUTES                                                                 
       KEYLEN-----------------4     AVGLRECL--------------80     BUFSPACE-------
       RKP--------------------0     MAXLRECL--------------80     EXCPEXIT-------
       SHROPTNS(1,3)   RECOVERY     UNIQUE           NOERASE     INDEXED       N
       UNORDERED        NOREUSE     NONSPANNED                                  
     STATISTICS   
       
            
 //STEP2    EXEC PGM=IDCAMS                                     
 //SYSPRINT DD   SYSOUT=*                                       
 //SYSIN    DD   *                                              
      ALTER TECN93.VVH2.KSDS1.DATA FREESPACE(20,10)             
 //                                                             
 //* DISPLAYS PRIMARY AND SECONDARY QUNTITY UNITS               


EXPORT IMPORT
                                       
//TECN93VV JOB  NOTIFY=&SYSUID              
//STEP1    EXEC PGM=IDCAMS                  
//SYSPRINT DD   SYSOUT=*                    
//DD1      DD   DSN=TECN93.VVH2.EXPS,DISP=SH
//SYSIN    DD   *                           
     EXPORT TECN93.VVH2.KSDS.EXP-           
     OUTFILE(DD1)-                          
     TEMPORARY-                             
     NOINHIBITTARGET-                       
     NOINHIBITSOURCE                        
/*                                          
//STEP2    EXEC PGM=IDCAMS                  
//SYSPRINT DD   SYSOUT=*                    
//SYSIN    DD   *                           
      IMPORT INDATASET(TECN93.VVH2.EXPS)-   
      OUTDATASET(TECN93.VVH2.KSDS.EXP)      
/*                                          
OUT PUT:
09.54.51 JOB16071 $HASP165 TECN93VV ENDED AT N1  MAXCC=0 CN(INTERNAL)  
 KEY OF RECORD - A001                                
 A001 RAKESHKUMAR 9987654329 ENGINEER     BANGALORE  
0                                                    
 ***                                                 
KEY OF RECORD - A002                                      
A002 ANIL        9987652222 SR.ARCHITECT CHENNAI          
                                                          
KEY OF RECORD - A003                                      
A003 VIJAY       9287635439 ENGINEER     MYSORE           
                                                          
KEY OF RECORD - A004                                      
A004 RAMAY       9966777884 EMPLOYE      HYDERABED        
                                                          
KEY OF RECORD - A005                                      
A005 KRISHNA     9995556778 EMPLOYE      KARANATAKA       
                                                          
KEY OF RECORD - A006                                      
A006 VIKAS       9998876534 SHOPKEPPER   BHARE            
                                                          
KEY OF RECORD - A007                                      
A007 VARUN       5654345635 SHOPKEPPER   OSORE            
                                                          
KEY OF RECORD - A008                                      
A008 VISHNU      1234566434 ITEMPLOY     MYHYD            
                                                          
KEY OF RECORD - A009                                      
A009 RAMESH      9876431234 EMPLOYE      ANDRAPRADESHE    
                                                          
KEY OF RECORD - 4,0                                       
4,0  11,6        10,18      12,29        13,42            
                                                          
IDC0005I NUMBER OF RECORDS PROCESSED WAS 10               

...C.....................................................................
........................................                                 
.........................................................................
........................................                                 
...........................$...............*.............................
........................................                                 
............................................................             
RECORD SEQUENCE NUMBER - 3                                               
.Y.4CTECN93.VVH2.KSDS.EXP                        ........................
........................................                                 
.........................................................................
........................................                                 
.........................................................................
........................................     


//STEP3    EXEC PGM=IDCAMS                         
//SYSPRINT DD   SYSOUT=*                           
//DD1      DD   DSN=TECN93.VVH2.EXPS1,DISP=SHR     
//SYSIN    DD   *                                  
     EXPORT TECN93.VVH2.KSDS.EXP-                  
     OUTFILE(DD1)-                        
     PERMANENT-                           
     NOINHIBITTARGET-                     
     NOINHIBITSOURCE                      
/*                                        
//STEP4    EXEC PGM=IDCAMS                
//SYSPRINT DD   SYSOUT=*                  
//SYSIN    DD   *                         
      IMPORT INDATASET(TECN93.VVH2.EXPS1)-
      OUTDATASET(TECN93.VVH2.KSDS.EXP)    
/*                                        

KEY OF RECORD - A002                                      
A002 ANIL        9987652222 SR.ARCHITECT CHENNAI          
                                                          
KEY OF RECORD - A003                                      
A003 VIJAY       9287635439 ENGINEER     MYSORE           
                                                          
KEY OF RECORD - A004                                      
A004 RAMAY       9966777884 EMPLOYE      HYDERABED        
                                                          
KEY OF RECORD - A005                                      
A005 KRISHNA     9995556778 EMPLOYE      KARANATAKA       
                                                          
KEY OF RECORD - A006                                      
A006 VIKAS       9998876534 SHOPKEPPER   BHARE            
                                                          
KEY OF RECORD - A007                                      
A007 VARUN       5654345635 SHOPKEPPER   OSORE            
                                                          
KEY OF RECORD - A008                                      
A008 VISHNU      1234566434 ITEMPLOY     MYHYD            
                                                          
KEY OF RECORD - A009                                      
A009 RAMESH      9876431234 EMPLOYE      ANDRAPRADESHE    
                                                          
KEY OF RECORD - 4,0                                       
4,0  11,6        10,18      12,29        13,42            
                                                          
IDC0005I NUMBER OF RECORDS PROCESSED WAS 10               

...C.....................................................................
........................................                                 
.........................................................................
........................................                                 
...........................$...............*.............................
........................................                                 
............................................................             
RECORD SEQUENCE NUMBER - 3                                               
.Y.4CTECN93.VVH2.KSDS.EXP                        ........................
........................................                                 
.........................................................................
........................................                                 

SECOND MT  EXPORT IMPORT:
 

 //TECN93VV JOB  NOTIFY=&SYSUID                                          
 //STEP1    EXEC PGM=IDCAMS                                              
 //SYSPRINT DD   SYSOUT=*                                                
 //SYSIN    DD   *                                                       
      REPRO-                                                             
      IDS(TECN93.VVH2.TECSACON.KSDS)-                                    
      ODS(TECN93.VVH2.EXPS)-                                             
      IF LASTCC=0THEN                                                    
      DELETE-                                                            
      (TECN93.VVH2.TECSACON.KSDS)-                                       
      REUSE-                                                             
      DEFINECLUSTER(NAME(TECN93.VVH2.TECSACON.KSDS)-                     
      TRK(1,1)-                                                          
      VOL(ZAPRD6)-                                                       
      CISZ(4096)-                                                        
      RECORDSIZE(80,80)-                                                 
      KEYS(4,0)-                                                         
      INDEXED)                                                           
      REPRO-                                                             
      IDS(TECN93.VVH2.EXPS)-                                             
      ODS(TECN93.VVH2.TECSACON.KSDS)                                     
 /*                                                                      

REUSE:

//TECN93VV JOB  NOTIFY=&SYSUID                                     
//STEP1    EXEC PGM=IDCAMS                                         
//SYSPRINT DD   SYSOUT=*                                           
//SYSIN    DD   *                                                  
     DEFINE CLUSTER(NAME(TECN93.VVH2.TECSACON.KSDS)-               
     TRK(1,1)-                                                     
     VOL(ZAPRD6)-                                                  
     FREESPACE(10,20)-                                             
     SPANNED-                                                      
     REUSE-                                                        
     RECORDSIZE(80,80)-                                            
     CISZ(4096)-                                                   
     KEYS(4,0)                                                     
     INDEXED)                                                      
/* 

//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP2     
//STEP1    EXEC PGM=IDCAMS                       
//SYSPRINT DD   SYSOUT=*                         
//SYSIN    DD   *                                
     ALTER TECN93.VVH2.TECSACON.KSDS-            
     NOREUSE                                     
/*                                               
//STEP2    EXEC PGM=IDCAMS                       
//SYSPRINT DD   SYSOUT=*                         
//SYSIN    DD   *                                
     ALTER TECN93.VVH2.TECSACON.KSDS-            
     NOREUSE                                     
/*  


IF PGM:

//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP2      
//STEP1    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
     REPRO-                                       
     IDS (TECN93.VVH2.KSDS)-                      
     ODS (TECN93.VVH2.PS)                         
      IF LASTCC=00-                               
      THEN-                                       
     PRINT LISTCAT ALLENTRIES(TECN93.VVH2.KSDS)-  
     ELSE DO                                      
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)-      
     LISTCAT ENTRIES(TECN93.VVH2.RRDS)-           
     LISTCAT ENTRIES(TECN93.VVH2.ESDS)-           
     END                                          
/*                                                
//* THIS PGM FOR IF MAX=00 THEN,ELSE DO,END       


//STEP2    EXEC PGM=IDCAMS                     
//SYSPRINT DD   SYSOUT=*                       
//SYSIN    DD   *                              
     REPRO-                                    
     IDS (TECN93.VVH2.KSDS)-                   
     ODS (TECN93.VVH2.P)                       
     IDS (TECN93.VVH2.RRDS)-                   
     ODS (TECN93.VVH2.PS1)                     
      IF LASTCC=4-                             
       THEN-                                           
DO SET MAXCC=0                                   
PRINT LISTCAT ALLENTRIES(TECN93.VVH2.KSDS)-      
ELSE DO                                          
LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)-          
LISTCAT ENTRIES(TECN93.VVH2.RRDS)-               
LISTCAT ENTRIES(TECN93.VVH2.ESDS)-               
END  
/*            
VSAM 3
//TECN93VV JOB  NOTIFY=&SYSUID                       
//STEP1    EXEC PGM=IDCAMS                           
//SYSPRINT DD   SYSOUT=*                             
//SYSIN    DD   *                                    
    DEFINE CLUSTER(NAME(TECN93.VVH2.KSDS.VISHNU)+    
    TRK(1,1)+                                        
    VOL(ZAPRD6)+                                     
    KEYS(4,0)+                                       
    RECORDSIZE(80,80)+                               
    CISZ(4096)+                                      
    INDEXED)                                         
/*                                                   
OUT PUT:

16.29.44 JOB19683 ---- MONDAY,    21 NOV 2022 ----                              
16.29.44 JOB19683  IRR010I  USERID TECN93   IS ASSIGNED TO THIS JOB.            
16.29.44 JOB19683  ICH70001I TECN93   LAST ACCESS AT 16:22:35 ON MONDAY, NOVEMBE
16.29.44 JOB19683  $HASP373 TECN93VV STARTED - INIT 1    - CLASS A - SYS SYS1   
16.29.44 JOB19683  IEF403I TECN93VV - STARTED - TIME=16.29.44                   
16.29.44 JOB19683  IEF404I TECN93VV - ENDED - TIME=16.29.44                     
16.29.44 JOB19683  $HASP395 TECN93VV ENDED                                      
------ JES2 JOB STATISTICS ------                                               
  21 NOV 2022 JOB EXECUTION DATE                                                
            6 CARDS READ                                                        
           61 SYSOUT PRINT RECORDS                                              
            0 SYSOUT PUNCH RECORDS                                              
            3 SYSOUT SPOOL KBYTES                                               
         0.00 MINUTES EXECUTION TIME                                            
        1 //TECN93VV JOB  NOTIFY=&SYSUID                                        
          IEFC653I SUBSTITUTION JCL - NOTIFY=TECN93                             
        2 //STEP1    EXEC PGM=IDCAMS                                            
        3 //SYSPRINT DD   SYSOUT=*                                              
        4 //SYSIN    DD   *                                                     
ICH70001I TECN93   LAST ACCESS AT 16:22:35 ON MONDAY, NOVEMBER 21, 2022         
IEF236I ALLOC. FOR TECN93VV STEP1                                               
IEF237I JES2 ALLOCATED TO SYSPRINT                                              
IEF237I JES2 ALLOCATED TO SYSIN                                                 
IEF142I TECN93VV STEP1 - STEP WAS EXECUTED - COND CODE 0000                     
IEF285I   TECN93.TECN93VV.JOB19683.D0000102.?          SYSOUT                   
IEF285I   TECN93.TECN93VV.JOB19683.D0000101.?          SYSIN                    
IEF373I STEP/STEP1   /START 2022325.1629                                        
IEF374I STEP/STEP1   /STOP  2022325.1629 CPU    0MIN 00.06SEC SRB    0MIN 00.00S
IEF375I  JOB/TECN93VV/START 2022325.1629                                        
IEF376I  JOB/TECN93VV/STOP  2022325.1629 CPU    0MIN 00.06SEC SRB    0MIN 00.00S
IDCAMS  SYSTEM SERVICES                                           TIME: 16:29:44
                                                                                
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)                           00050001
CLUSTER ------- TECN93.VVH2.KSDS.VISHNU                                         
     IN-CAT --- USERCAT.Z110.TRAINING                                           
   DATA ------- TECN93.VVH2.KSDS.VISHNU.DATA                                    
     IN-CAT --- USERCAT.Z110.TRAINING                                           
   INDEX ------ TECN93.VVH2.KSDS.VISHNU.INDEX                                   
     IN-CAT --- USERCAT.Z110.TRAINING                                           
IDCAMS  SYSTEM SERVICES                                           TIME: 16:29:44
         THE NUMBER OF ENTRIES PROCESSED WAS:                                   
                   AIX -------------------0                                     
                   ALIAS -----------------0                                     
                   CLUSTER ---------------1                                     
                   DATA ------------------1                                     
                   GDG -------------------0                                     
                   INDEX -----------------1                                     
                   NONVSAM ---------------0                                     
                   PAGESPACE -------------0                                     
                   PATH ------------------0                                     
                   SPACE -----------------0                                     
                   USERCATALOG -----------0                                     
                   TAPELIBRARY -----------0                                     
                   TAPEVOLUME ------------0                                     
                   TOTAL -----------------3                                     
         THE NUMBER OF PROTECTED ENTRIES SUPPRESSED WAS 0                       
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0              

 //TECN93VV JOB  NOTIFY=&SYSUID                    
//STEP1    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)     
/*                                                
OUT PUT:

16.38.54 JOB19708 ---- MONDAY,    21 NOV 2022 ----                             
16.38.54 JOB19708  IRR010I  USERID TECN93   IS ASSIGNED TO THIS JOB.           
16.38.55 JOB19708  ICH70001I TECN93   LAST ACCESS AT 16:37:41 ON MONDAY, NOVEMB
16.38.55 JOB19708  $HASP373 TECN93VV STARTED - INIT 1    - CLASS A - SYS SYS1  
16.38.55 JOB19708  IEF403I TECN93VV - STARTED - TIME=16.38.55                  
16.38.55 JOB19708  IEF404I TECN93VV - ENDED - TIME=16.38.55                    
16.38.55 JOB19708  $HASP395 TECN93VV ENDED                                     
------ JES2 JOB STATISTICS ------                                              
  21 NOV 2022 JOB EXECUTION DATE                                               
            6 CARDS READ                                                       
           61 SYSOUT PRINT RECORDS                                             
            0 SYSOUT PUNCH RECORDS                                             
            3 SYSOUT SPOOL KBYTES                                              
         0.00 MINUTES EXECUTION TIME                                           
        1 //TECN93VV JOB  NOTIFY=&SYSUID                                       
          IEFC653I SUBSTITUTION JCL - NOTIFY=TECN93                            
        2 //STEP1    EXEC PGM=IDCAMS                                           
        3 //SYSPRINT DD   SYSOUT=*                                             
        4 //SYSIN    DD   *                                                    
ICH70001I TECN93   LAST ACCESS AT 16:37:41 ON MONDAY, NOVEMBER 21, 2022        
IEF236I ALLOC. FOR TECN93VV STEP1                                              
IEF237I JES2 ALLOCATED TO SYSPRINT                                             
IEF237I JES2 ALLOCATED TO SYSIN                                                
IEF142I TECN93VV STEP1 - STEP WAS EXECUTED - COND CODE 0000                    
IEF285I   TECN93.TECN93VV.JOB19708.D0000102.?          SYSOUT                  
IEF285I   TECN93.TECN93VV.JOB19708.D0000101.?          SYSIN                   
IEF373I STEP/STEP1   /START 2022325.1638                                       
IEF374I STEP/STEP1   /STOP  2022325.1638 CPU    0MIN 00.05SEC SRB    0MIN 00.00S
IEF375I  JOB/TECN93VV/START 2022325.1638                                        
IEF376I  JOB/TECN93VV/STOP  2022325.1638 CPU    0MIN 00.05SEC SRB    0MIN 00.00S
IDCAMS  SYSTEM SERVICES                                           TIME: 16:38:55
                                                                                
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)                           00050001
CLUSTER ------- TECN93.VVH2.KSDS.VISHNU                                         
     IN-CAT --- USERCAT.Z110.TRAINING                                           
   DATA ------- TECN93.VVH2.KSDS.VISHNU.DATA                                    
     IN-CAT --- USERCAT.Z110.TRAINING                                           
   INDEX ------ TECN93.VVH2.KSDS.VISHNU.INDEX                                   
     IN-CAT --- USERCAT.Z110.TRAINING                                           
IDCAMS  SYSTEM SERVICES                                           TIME: 16:38:55
         THE NUMBER OF ENTRIES PROCESSED WAS:                                   
                   AIX -------------------0                                     
                   ALIAS -----------------0                                     
                   CLUSTER ---------------1                                     
                   DATA ------------------1                                     
                   GDG -------------------0                                     
                   INDEX -----------------1                                     
                   NONVSAM ---------------0                                     
                   PAGESPACE -------------0                                     
                   PATH ------------------0                                     
                   SPACE -----------------0                                     
                   USERCATALOG -----------0                                     
                   TAPELIBRARY -----------0                                     
                   TAPEVOLUME ------------0                                     
                   TOTAL -----------------3                                     
         THE NUMBER OF PROTECTED ENTRIES SUPPRESSED WAS 0                       
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       


 //TECN93VV JOB  NOTIFY=&SYSUID 
//STEP2    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS.VISHNU) 
//                                                
OUT PUT:
16.38.54 JOB19708 ---- MONDAY,    21 NOV 2022 ----                             
16.38.54 JOB19708  IRR010I  USERID TECN93   IS ASSIGNED TO THIS JOB.           
16.38.55 JOB19708  ICH70001I TECN93   LAST ACCESS AT 16:37:41 ON MONDAY, NOVEMB
16.38.55 JOB19708  $HASP373 TECN93VV STARTED - INIT 1    - CLASS A - SYS SYS1  
16.38.55 JOB19708  IEF403I TECN93VV - STARTED - TIME=16.38.55                  
16.38.55 JOB19708  IEF404I TECN93VV - ENDED - TIME=16.38.55                    
16.38.55 JOB19708  $HASP395 TECN93VV ENDED                                     
------ JES2 JOB STATISTICS ------                                              
  21 NOV 2022 JOB EXECUTION DATE                                               
            6 CARDS READ                                                       
           61 SYSOUT PRINT RECORDS                                             
            0 SYSOUT PUNCH RECORDS                                             
            3 SYSOUT SPOOL KBYTES                                              
         0.00 MINUTES EXECUTION TIME                                           
        1 //TECN93VV JOB  NOTIFY=&SYSUID                                       
          IEFC653I SUBSTITUTION JCL - NOTIFY=TECN93                            
        2 //STEP1    EXEC PGM=IDCAMS                                           
        3 //SYSPRINT DD   SYSOUT=*                                             
        4 //SYSIN    DD   *                                                    
ICH70001I TECN93   LAST ACCESS AT 16:37:41 ON MONDAY, NOVEMBER 21, 2022        
IEF236I ALLOC. FOR TECN93VV STEP1                                              
IEF237I JES2 ALLOCATED TO SYSPRINT                                             
IEF237I JES2 ALLOCATED TO SYSIN                                                
IEF142I TECN93VV STEP1 - STEP WAS EXECUTED - COND CODE 0000                    
IEF285I   TECN93.TECN93VV.JOB19708.D0000102.?          SYSOUT                  
IEF285I   TECN93.TECN93VV.JOB19708.D0000101.?          SYSIN                   
IEF373I STEP/STEP1   /START 2022325.1638                                       
IEF374I STEP/STEP1   /STOP  2022325.1638 CPU    0MIN 00.05SEC SRB    0MIN 00.00
IEF375I  JOB/TECN93VV/START 2022325.1638                                       
IEF376I  JOB/TECN93VV/STOP  2022325.1638 CPU    0MIN 00.05SEC SRB    0MIN 00.00
IDCAMS  SYSTEM SERVICES                                           TIME: 16:38:5
                                                                               
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)                           0005000
CLUSTER ------- TECN93.VVH2.KSDS.VISHNU                                        
     IN-CAT --- USERCAT.Z110.TRAINING                                          
   DATA ------- TECN93.VVH2.KSDS.VISHNU.DATA                                   
     IN-CAT --- USERCAT.Z110.TRAINING                                          
   INDEX ------ TECN93.VVH2.KSDS.VISHNU.INDEX                                  
     IN-CAT --- USERCAT.Z110.TRAINING                                          
IDCAMS  SYSTEM SERVICES                                           TIME: 16:38:5
         THE NUMBER OF ENTRIES PROCESSED WAS:                                  
                   AIX -------------------0                                    
                   ALIAS -----------------0                                    
                   CLUSTER ---------------1                                    
                   DATA ------------------1                                    
                   GDG -------------------0                                    
                   INDEX -----------------1                                    
                   NONVSAM ---------------0                                    
                   PAGESPACE -------------0                                    
                   PATH ------------------0                                    
                   SPACE -----------------0                                    
                   USERCATALOG -----------0                                    
                   TAPELIBRARY -----------0                                    
                   TAPEVOLUME ------------0                                    
                   TOTAL -----------------3                                    
         THE NUMBER OF PROTECTED ENTRIES SUPPRESSED WAS 0                      
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                      

//STEP3    EXEC PGM=IDCAMS                     
//SYSPRINT DD   SYSOUT=*                       
//SYSIN    DD   *                              
     LISTCAT LEVEL(TECN93.VVH2.KSDS.VISHNU)    
//                                             

OUT PUT:

IDCAMS  SYSTEM SERVICES                                           TIME: 16:52:20
                                                                                
     LISTCAT LEVEL(TECN93.VVH2.KSDS.VISHNU)                             00150002
IDCAMS  SYSTEM SERVICES                                           TIME: 16:52:20
                             LISTING FROM CATALOG -- USERCAT.Z110.TRAINING      
CLUSTER ------- TECN93.VVH2.KSDS.VISHNU                                         
     IN-CAT --- USERCAT.Z110.TRAINING                                           
DATA ---------- TECN93.VVH2.KSDS.VISHNU.DATA                                    
     IN-CAT --- USERCAT.Z110.TRAINING                                           
INDEX --------- TECN93.VVH2.KSDS.VISHNU.INDEX                                   
     IN-CAT --- USERCAT.Z110.TRAINING                                           
IDCAMS  SYSTEM SERVICES                                           TIME: 16:52:20
                             LISTING FROM CATALOG -- USERCAT.Z110.TRAINING      
         THE NUMBER OF ENTRIES PROCESSED WAS:                                   
                   AIX -------------------0                                     
                   ALIAS -----------------0                                     
                   CLUSTER ---------------1                                     
                   DATA ------------------1                                     
                   GDG -------------------0                                     
                   INDEX -----------------1                                     
                   NONVSAM ---------------0                                     
                   PAGESPACE -------------0                                     
                   PATH ------------------0                                     
                   SPACE -----------------0                                     
                   USERCATALOG -----------0                                     
                   TAPELIBRARY -----------0                                     
                   TAPEVOLUME ------------0                                     
                   TOTAL -----------------3                                     
         THE NUMBER OF PROTECTED ENTRIES SUPPRESSED WAS 0                       

//STEP4    EXEC PGM=IDCAMS                                
//SYSPRINT DD   SYSOUT=*                                  
//SYSIN    DD   *                                         
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)CLUSTER ALL  
//                                                        

OUT PUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 16:57:12
                                                                                
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)CLUSTER ALL                00200002
CLUSTER ------- TECN93.VVH2.KSDS.VISHNU                                         
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                    
       RELEASE----------------2     EXPIRATION------0000.000                    
       BWO STATUS--------(NULL)     BWO TIMESTAMP-----(NULL)                    
       BWO---------------(NULL)                                                 
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       DATA-----TECN93.VVH2.KSDS.VISHNU.DATA                                    
       INDEX----TECN93.VVH2.KSDS.VISHNU.INDEX                                   
IDCAMS  SYSTEM SERVICES                                           TIME: 16:57:12
         THE NUMBER OF ENTRIES PROCESSED WAS:                                   
                   AIX -------------------0                                     
                   ALIAS -----------------0                                     
                   CLUSTER ---------------1                                     
                   DATA ------------------0                                     
                   GDG -------------------0                                     
                   INDEX -----------------0                                     
                   NONVSAM ---------------0                                     
                   PAGESPACE -------------0                                     
                   PATH ------------------0                                     
                   SPACE -----------------0                                     
                   USERCATALOG -----------0                                     
                   TAPELIBRARY -----------0                                     
                   TAPEVOLUME ------------0                                     


//STEP5    EXEC PGM=IDCAMS 
//SYSPRINT DD   SYSOUT=*                                  
//SYSIN    DD   *                                         
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)DATA ALL     
//                                                        

IDCAMS  SYSTEM SERVICES                                           TIME: 17:02:48
                                                                                
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)DATA ALL                   00250002
   DATA ------- TECN93.VVH2.KSDS.VISHNU.DATA                                    
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                    
       RELEASE----------------2     EXPIRATION------0000.000                    
       ACCOUNT-INFO-----------------------------------(NULL)                    
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       CLUSTER--TECN93.VVH2.KSDS.VISHNU                                         
     ATTRIBUTES                                                                 
       KEYLEN-----------------4     AVGLRECL--------------80     BUFSPACE-------
       RKP--------------------0     MAXLRECL--------------80     EXCPEXIT-------
       SHROPTNS(1,3)   RECOVERY     UNIQUE           NOERASE     INDEXED       N
       UNORDERED        NOREUSE     NONSPANNED                                  
     STATISTICS                                                                 
       REC-TOTAL--------------0     SPLITS-CI--------------0     EXCPS----------
       REC-DELETED------------0     SPLITS-CA--------------0     EXTENTS--------
       REC-INSERTED-----------0     FREESPACE-%CI----------0     SYSTEM-TIMESTAM
       REC-UPDATED------------0     FREESPACE-%CA----------0          X'00000000
       REC-RETRIEVED----------0     FREESPC------------49152                    
     ALLOCATION                                                                 
       SPACE-TYPE---------TRACK     HI-A-RBA-----------49152                    
       SPACE-PRI--------------1     HI-U-RBA---------------0                    
       SPACE-SEC--------------1                                                 
     VOLUME                                                                     
       VOLSER------------ZAPRD6     PHYREC-SIZE---------4096     HI-A-RBA-------

      DEVTYPE------X'3010200F'     PHYRECS/TRK-----------12     HI-U-RBA----
      VOLFLAG------------PRIME     TRACKS/CA--------------1                 
      EXTENTS:                                                              
      LOW-CCHH-----X'005C000B'     LOW-RBA----------------0     TRACKS------
      HIGH-CCHH----X'005C000B'     HIGH-RBA-----------49151                 
DCAMS  SYSTEM SERVICES                                           TIME: 17:02
        THE NUMBER OF ENTRIES PROCESSED WAS:                                
                  AIX -------------------0                                  
                  ALIAS -----------------0                                  
                  CLUSTER ---------------0                                  
                  DATA ------------------1                                  
                  GDG -------------------0                                  
                  INDEX -----------------0                                  
                  NONVSAM ---------------0                                  
                  PAGESPACE -------------0                                  
                  PATH ------------------0                                  
                  SPACE -----------------0                                  
                  USERCATALOG -----------0                                  
                  TAPELIBRARY -----------0                                  
                  TAPEVOLUME ------------0                                  
                  TOTAL -----------------1                                  
        THE NUMBER OF PROTECTED ENTRIES SUPPRESSED WAS 0                    
DC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                    
                                                                            
DC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0            
******************************* BOTTOM OF DATA *****************************

//STEP6    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)INDEX ALL     
/*                                                         

OUT PUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 17:09:42
                                                                                
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)INDEX ALL                  00300003
   INDEX ------ TECN93.VVH2.KSDS.VISHNU.INDEX                                   
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                    
       RELEASE----------------2     EXPIRATION------0000.000                    
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       CLUSTER--TECN93.VVH2.KSDS.VISHNU                                         
     ATTRIBUTES                                                                 
       KEYLEN-----------------4     AVGLRECL---------------0     BUFSPACE-------
       RKP--------------------0     MAXLRECL------------4089     EXCPEXIT-------
       SHROPTNS(1,3)   RECOVERY     UNIQUE           NOERASE     NOWRITECHK     
       NOREUSE                                                                  
     STATISTICS                                                                 
       REC-TOTAL--------------0     SPLITS-CI--------------0     EXCPS----------
       REC-DELETED------------0     SPLITS-CA--------------0     EXTENTS--------
       REC-INSERTED-----------0     FREESPACE-%CI----------0     SYSTEM-TIMESTAM
       REC-UPDATED------------0     FREESPACE-%CA----------0          X'00000000
       REC-RETRIEVED----------0     FREESPC------------49152                    
     ALLOCATION                                                                 
       SPACE-TYPE---------TRACK     HI-A-RBA-----------49152                    
       SPACE-PRI--------------1     HI-U-RBA---------------0                    
       SPACE-SEC--------------1                                                 
     VOLUME                                                                     
       VOLSER------------ZAPRD6     PHYREC-SIZE---------4096     HI-A-RBA-------
       DEVTYPE------X'3010200F'     PHYRECS/TRK-----------12     HI-U-RBA-------
       VOLFLAG------------PRIME     TRACKS/CA--------------1                    
       EXTENTS:                                                                 
       LOW-CCHH-----X'005D0002'     LOW-RBA----------------0     TRACKS---------
       HIGH-CCHH----X'005D0002'     HIGH-RBA-----------49151                    
IDCAMS  SYSTEM SERVICES                                           TIME: 17:09:42
         THE NUMBER OF ENTRIES PROCESSED WAS:                                   
                   AIX -------------------0                                     
                   ALIAS -----------------0                                     
                   CLUSTER ---------------0                                     
                   DATA ------------------0                                     
                   GDG -------------------0                                     
                   INDEX -----------------1                                     
                   NONVSAM ---------------0                                     
                   PAGESPACE -------------0                                     
                   PATH ------------------0                                     
                   SPACE -----------------0                                     
                   USERCATALOG -----------0                                     
                   TAPELIBRARY -----------0                                     
                   TAPEVOLUME ------------0                                     
                   TOTAL -----------------1                                     
         THE NUMBER OF PROTECTED ENTRIES SUPPRESSED WAS 0                       
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       
                                                                                
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0               
******************************** BOTTOM OF DATA ********************************
                                                                                


//STEP2    EXEC PGM=IDCAMS                               
//SYSPRINT DD   SYSOUT=*                                 
//SYSIN    DD   *                                        
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU1)+      
     TRK(1,1)+                                           
     VOL(ZAPRD6)+                                        
     KEYS(4,0)+                                          
     CISZ(4096)+                                         
     NONINDEXED)                                         
/*                                                       
OUT PUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 17:31:26
                                                                                
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU1)+                     00160000
     TRK(1,1)+                                                          00170000
     VOL(ZAPRD6)+                                                       00180000
     KEYS(4,0)+                                                         00190000
     CISZ(4096)+                                                        00210000
     NONINDEXED)                                                        00220000
IDC3013I DUPLICATE DATA SET NAME                                                
IDC3009I ** VSAM CATALOG RETURN CODE IS 8 - REASON CODE IS IGG0CLEH-38          
IDC3003I FUNCTION TERMINATED. CONDITION CODE IS 12                              
                                                                                
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 12              
******************************** BOTTOM OF DATA ********************************
                                                                                
//STEP3    EXEC PGM=IDCAMS      
//SYSPRINT DD   SYSOUT=*        
//SYSIN    DD   *               
LISTCAT ALL ENTRIES(TECN93.VVH2.ESDS.VISHNU1) 
 /*
OUT PUT:

IDCAMS  SYSTEM SERVICES                                           TIME: 17:31:2
                                                                               
     LISTCAT ALL ENTRIES(TECN93.VVH2.ESDS.VISHNU1)                      0024300
CLUSTER ------- TECN93.VVH2.ESDS.VISHNU1                                       
     IN-CAT --- USERCAT.Z110.TRAINING                                          
     HISTORY                                                                   
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                   
       RELEASE----------------2     EXPIRATION------0000.000                   
       BWO STATUS--------(NULL)     BWO TIMESTAMP-----(NULL)                   
       BWO---------------(NULL)                                                
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                   
     ASSOCIATIONS                                                              
       DATA-----TECN93.VVH2.ESDS.VISHNU1.DATA                                  
   DATA ------- TECN93.VVH2.ESDS.VISHNU1.DATA                                  
     IN-CAT --- USERCAT.Z110.TRAINING                                          
     HISTORY                                                                   
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                   
       RELEASE----------------2     EXPIRATION------0000.000                   
       ACCOUNT-INFO-----------------------------------(NULL)                   
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                   
     ASSOCIATIONS                                                              
       CLUSTER--TECN93.VVH2.ESDS.VISHNU1                                       
     ATTRIBUTES                                                                
       KEYLEN-----------------4     AVGLRECL------------4089     BUFSPACE------
       RKP--------------------0     MAXLRECL------------4089     EXCPEXIT------
       SHROPTNS(1,3)   RECOVERY     UNIQUE           NOERASE     NONINDEXED    
       UNORDERED        NOREUSE     NONSPANNED                                 
     STATISTICS                                                                
       REC-TOTAL--------------0     SPLITS-CI--------------0     EXCPS---------                                             
 REC-DELETED------------0     SPLITS-CA--------------0     EXTENTS------
 REC-INSERTED-----------0     FREESPACE-%CI----------0     SYSTEM-TIMEST
 REC-UPDATED------------0     FREESPACE-%CA----------0          X'000000
 REC-RETRIEVED----------0     FREESPC------------49152                  
LLOCATION                                                               
 SPACE-TYPE---------TRACK     HI-A-RBA-----------49152                  
 SPACE-PRI--------------1     HI-U-RBA---------------0                  
 SPACE-SEC--------------1                                               
OLUME                                                                   
 VOLSER------------ZAPRD6     PHYREC-SIZE---------4096     HI-A-RBA-----
 DEVTYPE------X'3010200F'     PHYRECS/TRK-----------12     HI-U-RBA-----
 VOLFLAG------------PRIME     TRACKS/CA--------------1                  
 EXTENTS:                                                               
 LOW-CCHH-----X'00650004'     LOW-RBA----------------0     TRACKS-------
 HIGH-CCHH----X'00650004'     HIGH-RBA-----------49151                  
  SYSTEM SERVICES                                           TIME: 17:31:
   THE NUMBER OF ENTRIES PROCESSED WAS:                                 
             AIX -------------------0                                   
             ALIAS -----------------0                                   
             CLUSTER ---------------1                                   
             DATA ------------------1                                   
             GDG -------------------0                                   
             INDEX -----------------0                                   
             NONVSAM ---------------0                                   
             PAGESPACE -------------0                                   
             PATH ------------------0                                   
             SPACE -----------------0                                   
             USERCATALOG -----------0                                   
             TAPELIBRARY -----------0                                   
             TAPEVOLUME ------------0 

//STEP5    EXEC PGM=IDCAMS                             
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU2)+    
     TRK(1,1)+                                         
     VOL(ZAPRD6)+                                      
     RECORDSIZE(80,80)+                                
     CISZ(4096)+                                       
     NONINDEXED)                                       
//      
OUT PUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 18:46:44
                                                                                
     LISTCAT ALL ENTRIES(TECN93.VVH2.ESDS.VISHNU4)                      00290005
CLUSTER ------- TECN93.VVH2.ESDS.VISHNU4                                        
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                    
       RELEASE----------------2     EXPIRATION------0000.000                    
       BWO STATUS--------(NULL)     BWO TIMESTAMP-----(NULL)                    
       BWO---------------(NULL)                                                 
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       DATA-----TECN93.VVH2.ESDS.VISHNU4.DATA                                   
   DATA ------- TECN93.VVH2.ESDS.VISHNU4.DATA                                   
     IN-CAT --- USERCAT.Z110.TRAINING                                           
     HISTORY                                                                    
       DATASET-OWNER-----(NULL)     CREATION--------2022.325                    
       RELEASE----------------2     EXPIRATION------0000.000                    
       ACCOUNT-INFO-----------------------------------(NULL)                    
     PROTECTION-PSWD-----(NULL)     RACF----------------(NO)                    
     ASSOCIATIONS                                                               
       CLUSTER--TECN93.VVH2.ESDS.VISHNU4                                        
     ATTRIBUTES                                                                 
       KEYLEN-----------------0     AVGLRECL------------4089     BUFSPACE-------
       RKP--------------------0     MAXLRECL------------
4089     EXCPEXIT-------
       SHROPTNS(1,3)   RECOVERY     UNIQUE           NOERASE     NONINDEXED    N
       UNORDERED        NOREUSE     NONSPANNED                                  
     STATISTICS                                                                 
       REC-TOTAL--------------0     SPLITS-CI--------------0     EXCPS---------- 


//TECN93VV JOB  NOTIFY=&SYSUID                             
//STEP1    EXEC PGM=IDCAMS                                 
//SYSRINT  DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
    DEFINE CLUSTER+                                        
    (NAME(TECN93.VVH2.VISHNU.CLUSTER)+                     
    TRK(1,1)+                                              
    VOLUMES(ZAPRD6)+                                       
    RECORDSIZE(80,80)+                                     
    KEYS(4,0)+                                             
    CISZ(4096)+                                            
    INDEXED)+                                              
    DATA                                                   
    (NAME TECN93.VVH2.VISHNU.DATA1)                        
    INDEX                                                  
    (NAME TECN93.VVH2.VISHNU.INDEX)                        
/*                                                         
//*BY THIS WE CAN CHANGE NAME OF THE DATA,INDEX NAMES 


//STEP2    EXEC PGM=IDCAMS                     
//SYSRINT  DD   SYSOUT=*                       
//SYSIN    DD   *                              
    DEFINE CLUSTER(NAME(TECN93.VVH2.VSAMSPDS)+
    TRK(1,1)+ 
     VOLUMES(ZAPRD6)+                                   
    RECORDSIZE(80,80)+                                 
    KEYS(4,0)+                                         
    CISZ(4096))                                        
/*                                                     
//*THIS PGM IS FOR DEFAULT VALUE INDEXED&IXD           

OUT PUT:TECN93.VVH2.VSAMSPDS        
                  TECN93.VVH2.VSAMSPDS.DATA   
                  TECN93.VVH2.VSAMSPDS.INDEX  


//STEP3    EXEC PGM=IDCAMS                    
//SYSPRINT DD   SYSOUT=*                      
//SYSIN    DD   *                             
    DEFINE CLUSTER(NAME(TECN93.VVH2.SPANED)+  
    TRK(1,1)+                                 
    VOLUMES(ZAPRD6)+                          
    KEYS(4,0)+                                
    RECORDSIZE(80,80)+                        
    CISZ(4096)+                               
    INDEXED)                                  
/*                                            
OUT PUT :
IDCAMS  SYSTEM SERVICES                                           TIME: 19:40:17
                                                                                
    DEFINE CLUSTER(NAME(TECN93.VVH2.SPANED)+                            00214004
    TRK(1,1)+                                                           00215004
    VOLUMES(ZAPRD6)+                                                    00216004
    KEYS(4,0)+                                                          00216104
    RECORDSIZE(80,80)+                                                  00217004
    CISZ(4096)+                                                         00219004
    INDEXED)                                                            00219104
IDC0508I DATA ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                          
IDC0509I INDEX ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                         
IDC0512I NAME GENERATED-(D) TECN93.VVH2.SPANED.DATA                             
IDC0512I NAME GENERATED-(I) TECN93.VVH2.SPANED.INDEX                            
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       
                                                                                
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0               
******************************** BOTTOM OF DATA ********************************
//STEP4    EXEC PGM=IDCAMS                     
//SYSPRINT DD   SYSOUT=*                       
//SYSIN    DD   *                              
    DEFINE CLUSTER(NAME(TECN93.VVH2.SPN)+      
    TRK(1,1)+                                  
    VOLUMES(ZAPRD6)+                           
    KEYS(4,0)+                                 
    RECORDSIZE(80,80)+                         
    SPANED+                                    
    CISZ(4096)+
    INDEXED) 
/*


//TECN93VV JOB  NOTIFY=&SYSUID                    
//STEP1    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.FOR1)+ 
    TRK(1,1)+                                     
    VOLUMES(ZAPRD6)+                              
    FOR(10)+                                      
    KEYS(4,0)+                                    
    RECORDSIZE(80,80)+                            
    CISZ(4096)+                                   
    INDEXED)                                      
/*
//* AFTER 10 DAYS THE DATA SET WILL  DE DELETED                                             
OUT PUT:                                
    IDCAMS  SYSTEM SERVICES                                           TIME: 19:56:28
                                                                                
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.FOR1)+                       00040001
    TRK(1,1)+                                                           00050001
    VOLUMES(ZAPRD6)+                                                    00060001
    FOR(10)+                                                            00061001
    KEYS(4,0)+                                                          00070001
    RECORDSIZE(80,80)+                                                  00080001
    CISZ(4096)+                                                         00090001
    INDEXED)                                                            00100001
IDC0508I DATA ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                          
IDC0509I INDEX ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                         
IDC0512I NAME GENERATED-(D) TECN93.VVH2.VISHNU.FOR1.DATA                        
IDC0512I NAME GENERATED-(I) TECN93.VVH2.VISHNU.FOR1.INDEX                       
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       
                                                                                
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0               
******************************** BOTTOM OF DATA ********************************                                                                            

//STEP2    EXEC PGM=IDCAMS                       
//SYSPRINT DD   SYSOUT=*                         
//SYSIN    DD   *                                
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.TO)+  
    TRK(1,1)+                                    
    VOLUMES(ZAPRD6)+                             
    TO(2022328)+                                 
    KEYS(4,0)+                                   
    RECORDSIZE(80,80)+                           
    CISZ(4096)+                                  
    INDEXED)                                     
/*                                               
//  *   TO 2022 328 THE DATA SET WILL BE SEEN                                        

OUTPUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 19:58:5
                                                                               
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.TO)+                         0010400
    TRK(1,1)+                                                           0010500
    VOLUMES(ZAPRD6)+                                                    0010600
    TO(2022328)+                                                        0010700
    KEYS(4,0)+                                                          0010800
    RECORDSIZE(80,80)+                                                  0010900
    CISZ(4096)+                                                         0010910
    INDEXED)                                                            0010920
IDC0508I DATA ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                         
IDC0509I INDEX ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                        
IDC0512I NAME GENERATED-(D) TECN93.VVH2.VISHNU.TO.DATA                         
IDC0512I NAME GENERATED-(I) TECN93.VVH2.VISHNU.TO.INDEX                        
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                      
                                                                               
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0              
******************************** BOTTOM OF DATA *******************************
//STEP3    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.REUSE)-         
    TRK(1,1)-                                              
    VOLUMES(ZAPRD6)-                                       
    KEYS(4,0)-                                             
    RECORDSIZE(80,80)-                                     
    REUSE-                                                 
    CISZ(4096)-                                            
    INDEXED)                                               
/*                                                         
//                                                         

OUT PUT:
IDCAMS  SYSTEM SERVICES                                           TIME: 20:10:16
                                                                                
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.REUSE)-                      00114001
    TRK(1,1)-                                                           00115001
    VOLUMES(ZAPRD6)-                                                    00116001
    KEYS(4,0)-                                                          00118001
    RECORDSIZE(80,80)-                                                  00119001
    REUSE-                                                              00119101
    CISZ(4096)-                                                         00119201
    INDEXED)                                                            00119301
IDC0508I DATA ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                          
IDC0509I INDEX ALLOCATION STATUS FOR VOLUME ZAPRD6 IS 0                         
IDC0512I NAME GENERATED-(D) TECN93.VVH2.VISHNU.REUSE.DATA                       
IDC0512I NAME GENERATED-(I) TECN93.VVH2.VISHNU.REUSE.INDEX                      
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       
                                                                                
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0               
******************************** BOTTOM OF DATA ********************************

//STEP4    EXEC PGM=IDCAMS                               
//SYSPRINT DD   SYSOUT=*                                 
//SYSIN    DD   *                                        
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.REUSE)-       
    TRK(1,1)-                                            
    VOLUMES(ZAPRD6)-                                     
    KEYS(4,0)-                                           
    RECORDSIZE(80,80)-                                   
    CISZ(4096)-                                          
        INDEXED)   
/*             
//* NO REUSE   

//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP4                        
//STEP1    EXEC PGM=IDCAMS                                          
//SYSRINT  DD   SYSOUT=*                                            
//SYSIN    DD   *                                                   
    DEFINE CLUSTER+                                                 
    (NAME(TECN93.VVH2.VISHNU.CLUSTER)+                              
    TRK(1,1)+                                                       
    VOLUMES(ZAPRD6)+                                                
    RECORDSIZE(80,80)+                                              
    KEYS(4,0)+                                                      
    CISZ(4096)+                                                     
    INDEXED)+                                                       
    DATA                                                            
    (NAME TECN93.VVH2.VISHNU.DATA1),VOLUME(ZAPRD4)+                 
    INDEX                                                           
    (NAME TECN93.VVH2.VISHNU.INDEX),VOLUME(ZAPRD4)                  
/*                                                                  
//*BY THIS WE CAN CHANGE NAME OF THE DATA,INDEX NAMES,ADDING VOLUME


IF PGM:

//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP2      
//STEP1    EXEC PGM=IDCAMS                        
//SYSPRINT DD   SYSOUT=*                          
//SYSIN    DD   *                                 
     REPRO-                                       
     IDS (TECN93.VVH2.KSDS)-                      
     ODS (TECN93.VVH2.PS)                         
      IF LASTCC=00-                               
      THEN-                                       
     PRINT LISTCAT ALLENTRIES(TECN93.VVH2.KSDS)-  
     ELSE DO                                      
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)-      
     LISTCAT ENTRIES(TECN93.VVH2.RRDS)-           
     LISTCAT ENTRIES(TECN93.VVH2.ESDS)-           
     END                                          
/*                                                
//* THIS PGM FOR IF MAX=00 THEN,ELSE DO,END       


//STEP2    EXEC PGM=IDCAMS                     
//SYSPRINT DD   SYSOUT=*                       
//SYSIN    DD   *                              
     REPRO-                                    
     IDS (TECN93.VVH2.KSDS)-                   
     ODS (TECN93.VVH2.P)                       
     IDS (TECN93.VVH2.RRDS)-                   
     ODS (TECN93.VVH2.PS1)                     
      IF LASTCC=4-                             
       THEN-                                           
DO SET MAXCC=0                                   
PRINT LISTCAT ALLENTRIES(TECN93.VVH2.KSDS)-      
ELSE DO                                          
LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)-          
LISTCAT ENTRIES(TECN93.VVH2.RRDS)-               
LISTCAT ENTRIES(TECN93.VVH2.ESDS)-               
END  
/*        
 VSAM 4
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP5    
//STEP1    EXEC PGM=IDCAMS                      
//SYSPRINT DD   SYSOUT=*                        
//SYSIN    DD   *                               
     DEFINE AIX(NAME(TECN93.VVH2.AIXNM2)-       
     RELATE(TECN93.VVH2.AIX.KSDS)-              
     TRK(1,1)-                                  
     VOL(ZAPRD6)-                               
     RECORDSIZE(24,24)-                         
     CISZ(4096)-                                
     KEYS(11,4)-                                
     NONUNIQUEKEY-                              
     UPGRADE)                                   
/*                                              
//* THIS IS PGM =NAME                           
//STEP2    EXEC PGM=IDCAMS                      
//SYSPRINT DD   SYSOUT=*                        
//SYSIN    DD   *                               
     DEFINE AIX(NAME(TECN93.VVH2.AIXPH)-        
     RELATE(TECN93.VVH2.AIX.KSDS)-              
     TRK(1,1)-                                  
     VOL(ZAPRD6)-                               
     RECORDSIZE(19,19)-                         
     CISZ(4096)-      
     KEYS(10,18)-     
     UNIQUEKEY- 
     UPGRADE)                                
/*                                           
//* THIS IS PGM =PHONE NUMBER                
//STEP3    EXEC PGM=IDCAMS                   
//SYSPRINT DD   SYSOUT=*                     
//SYSIN    DD   *                            
     DEFINE AIX(NAME(TECN93.VVH2.AIXDSG)-    
     RELATE(TECN93.VVH2.AIX.KSDSB)-          
     TRK(1,1)-                               
     VOL(ZAPRD6)-                            
     RECORDSIZE(25,25)-                      
     CISZ(4096)-                             
     KEYS(12,29)-                            
     NONUNIQUEKEY-                           
     UPGRADE)                                
/*                                           
//* THIS IS PGM =DSG                         
//STEP4    EXEC PGM=IDCAMS                   
//SYSPRINT DD   SYSOUT=*                     
//SYSIN    DD   *                            
     DEFINE AIX(NAME(TECN93.VVH2.AIXPLC)-    
     RELATE(TECN93.VVH2.AIX.KSDSB)-          
     TRK(1,1)-                               
     VOL(ZAPRD6)-                          
     RECORDSIZE(22,22)-                    
     CISZ(4096)-                           
     KEYS(13,42)-                          
     UNIQUEKEY-                            
     UPGRADE)                              
/*                                         
//* THIS IS PGM = PLCE                     
//STEP5    EXEC PGM=IDCAMS                 
//SYSPRINT DD   SYSOUT=*                   
//SYSIN    DD   *                          
     DEFINE AIX(NAME(TECN93.VVH2.AIXNME)-  
     RELATE(TECN93.VVH2.VSAM.ESDSA)-       
     TRK(1,1)-                             
     VOL(ZAPRD6)-                          
     RECORDSIZE(24,24)-                    
     CISZ(4096)-                           
     KEYS(11,4)-                           
     NONUNIQUEKEY-                         
     UPGRADE)                              
//                                         
//* THIS IS ESDS AIX                       


//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP5             
//STEP1    EXEC PGM=IDCAMS                               
//SYSPRINT DD   SYSOUT=*                                 
//DD1      DD   DSN=TECN93.VVH2.AIX.KSDS,DISP=OLD        
//DD2      DD   DSN=TECN93.VVH2.AIXNM,DISP=OLD           
//SYSIN    DD   *                                        
    BLDINDEX-                                            
    INFILE(DD1)OUTFILE(DD2)                              
/*                                                       
//STEP2    EXEC PGM=IDCAMS                               
//SYSPRINT DD   SYSOUT=*                                 
//DD1      DD   DSN=TECN93.VVH2.AIX.KSDS,DISP=OLD        
//DD2      DD   DSN=TECN93.VVH2.AIXPH,DISP=OLD           
//SYSIN    DD   *                                        
    BLDINDEX-                                            
    INFILE(DD1)OUTFILE(DD2)                              
/*                                                       
//STEP3    EXEC PGM=IDCAMS                               
//SYSPRINT DD   SYSOUT=*                                 
//DD1      DD   DSN=TECN93.VVH2.AIX.KSDSB,DISP=OLD       
//DD2      DD   DSN=TECN93.VVH2.AIXDSG,DISP=OLD          
//SYSIN    DD   *                                        
    BLDINDEX-                                            
    INFILE(DD1)OUTFILE(DD2)       
/*                                
//STEP4    EXEC PGM=IDCAMS        
//SYSPRINT DD   SYSOUT=*                                
//DD1      DD   DSN=TECN93.VVH2.AIX.KSDSB,DISP=OLD      
//DD2      DD   DSN=TECN93.VVH2.AIXPLC,DISP=OLD         
//SYSIN    DD   *                                       
    BLDINDEX-                                           
    INFILE(DD1)OUTFILE(DD2)                             
/*                                                      
//STEP5    EXEC PGM=IDCAMS                              
//SYSPRINT DD   SYSOUT=*                                
//DD1      DD   DSN=TECN93.VVH2.VSAM.ESDSA,DISP=OLD     
//DD2      DD   DSN=TECN93.VVH2.AIXNME,DISP=OLD         
//SYSIN    DD   *                                       
    BLDINDEX-                                           
    INFILE(DD1)OUTFILE(DD2)                             
//                                                      

//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP5               
//STEP1    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
      DEFINE PATH(NAME(TECN93.VVH2.AIX.PATH)-              
             PATHENTRY(TECN93.VVH2.AIXNM)-                 
             UPDATE)                                       
/*                                                         
//STEP2    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
      DEFINE PATH(NAME(TECN93.VVH2.AIX.PATH.PH)-           
             PATHENTRY(TECN93.VVH2.AIXPH)-                 
             UPDATE)                                       
/*                                                         
//STEP3    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
      DEFINE PATH(NAME(TECN93.VVH2.AIX.PATH.GSD)-          
             PATHENTRY(TECN93.VVH2.AIXGSD)-                
             UPDATE)                                       
/*                                                         
//*    
//STEP4    EXEC PGM=IDCAMS       
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
      DEFINE PATH(NAME(TECN93.VVH2.AIX.PATH.PLC)-      
             PATHENTRY(TECN93.VVH2.AIXPLC)-            
             UPDATE)                                   
/*                                                     
//STEP5    EXEC PGM=IDCAMS                             
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
      DEFINE PATH(NAME(TECN93.VVH2.AIX.PATH.ESDS)-     
             PATHENTRY(TECN93.VVH2.AIXNME)-            
             UPDATE)                                   
//                                                     


//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP6               
//STEP1    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)              
/*                                                         
//*                                                        
//STEP2    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS.VISHNU)          
/*                                                         
//STEP3    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     LISTCAT LEVEL(TECN93.VVH2.KSDS.VISHNU)                
/*                                                         
//STEP4    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)CLUSTER ALL   
/*                                                         
//STEP5    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                
//SYSIN    DD   *                                       
     LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)DATA ALL   
 /*                                                     
 //STEP6    EXEC PGM=IDCAMS                             
 //SYSPRINT DD   SYSOUT=*                               
 //SYSIN    DD   *                                      
      LISTCAT ENTRIES(TECN93.VVH2.KSDS.VISHNU)INDEX ALL 
 /*                                                     



//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP4               
//STEP1    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU)+         
     TRK(1,1)+                                             
     VOL(ZAPRD6)+                                          
     KEYS(4,0)+                                            
     RECORDSIZE(80,80)+                                    
     CISZ(4096)+                                           
     NONINDEXED)                                           
/*                                                         
//STEP2    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                   
//SYSIN    DD   *                                          
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU4)+        
     TRK(1,1)+                                             
     VOL(ZAPRD6)+                                          
     KEYS(4,0)+                                            
     CISZ(4096)+                                           
     NONINDEXED)                                           
/*                                                         
//STEP3    EXEC PGM=IDCAMS                                 
//SYSPRINT DD   SYSOUT=*                                      
//SYSIN    DD   *                                             
     LISTCAT ALL ENTRIES(TECN93.VVH2.ESDS.VISHNU1)            
/*                                                              
//STEP4    EXEC PGM=IDCAMS                                      
//SYSPRINT DD   SYSOUT=*                                        
//SYSIN    DD   *                                               
     LISTCAT ALL ENTRIES(TECN93.VVH2.ESDS.VISHNU7)              
//*                                                             
//                                                              
//STEP5    EXEC PGM=IDCAMS                                      
//SYSPRINT DD   SYSOUT=*                                        
//SYSIN    DD   *                                               
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU7)+             
     TRK(1,1)+                                                  
     VOL(ZAPRD6)+                                               
     RECORDSIZE(80,80)+                                         
     CISZ(4096)+                                                
     NONINDEXED)                                                
/*                                                              
//STEP6    EXEC PGM=IDCAMS                                      
//DD1      DD   DSN=TECN93.VVH2.PS3LDS,DISP=OLD                 
//DD2      DD   DSN=TECN93.VVH2.ESDS.VISHNU2,DISP=OLD           
//SYSPRINT DD   SYSOUT=*                                        
//SYSIN    DD   *                                               
     REPRO-                                                     
          INFILE(DD1)OUTFILE(DD2)       
     ODS(TECN93.VVH2.ESDS.VISHNU2) 
/*                                 
//*                                                    
//STEP7    EXEC PGM=IDCAMS                             
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
     DEFINE CLUSTER(NAME(TECN93.VVH2.ESDS.VISHNU2)+    
     TRK(1,1)+                                         
     VOL(ZAPRD6)+                                      
     RECORDSIZE(80,80)+                                
     CISZ(4096)+                                       
     NONINDEXED)                                       
/*                                                     

//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP4            
//STEP1    EXEC PGM=IDCAMS                              
//SYSRINT  DD   SYSOUT=*                                
//SYSIN    DD   *                                       
    DEFINE CLUSTER+                                     
    (NAME(TECN93.VVH2.VISHNU.CLUSTER)+                  
    TRK(1,1)+                                           
    VOLUMES(ZAPRD6)+                                    
    RECORDSIZE(80,80)+                                  
    KEYS(4,0)+                                          
    CISZ(4096)+                                         
    INDEXED)+                                           
    DATA                                                
    (NAME TECN93.VVH2.VISHNU.DATA1)                     
    INDEX                                               
    (NAME TECN93.VVH2.VISHNU.INDEX)                     
/*                                                      
//*BY THIS WE CAN CHANGE NAME OF THE DATA,INDEX NAMES   
//STEP2    EXEC PGM=IDCAMS                              
//SYSPRINT DD   SYSOUT=*                                
//SYSIN    DD   *                                       
    DEFINE CLUSTER(NAME(TECN93.VVH2.VSAMSPDS)+          
    TRK(1,1)+                                                                                               
    VOLUMES(ZAPRD6)+         
    RECORDSIZE(80,80)+       
    KEYS(4,0)+  
    CISZ(4096))                                           
/*                                                        
//*THIS PGM IS FOR DEFAULT VALUE INDEXED&IXD              
//*                                                       
//STEP3    EXEC PGM=IDCAMS                                
//SYSPRINT DD   SYSOUT=*                                  
//SYSIN    DD   *                                         
    DEFINE CLUSTER(NAME(TECN93.VVH2.SPANED)+              
    TRK(1,1)+                                             
    VOLUMES(ZAPRD6)+                                      
    KEYS(4,0)+                                            
    RECORDSIZE(80,80)+                                    
    CISZ(4096)+                                           
    INDEXED)                                              
/*                                                        
//STEP4    EXEC PGM=IDCAMS                                
//SYSPRINT DD   SYSOUT=*                                  
//SYSIN    DD   *                                         
    DEFINE CLUSTER(NAME(TECN93.VVH2.SPN)+                 
    TRK(1,1)+                                             
    VOLUMES(ZAPRD6)+                                      
    KEYS(4,0)+                                            
    RECORDSIZE(80,80)+                                                                     
     SPANED+                 
    CISZ(4096)+             
    INDEXED)
/*
//
//TECN93VV JOB  NOTIFY=&SYSUID,RESTART=STEP3           
//STEP1    EXEC PGM=IDCAMS                             
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.FOR1)+      
    TRK(1,1)+                                          
    VOLUMES(ZAPRD6)+                                   
    FOR(10)+                                           
    KEYS(4,0)+                                         
    RECORDSIZE(80,80)+                                 
    CISZ(4096)+                                        
    INDEXED)                                           
/*                                                     
//* FOR 10 DAYS THE DATA SET WILL BE PRESENT           
//STEP2    EXEC PGM=IDCAMS                             
//SYSPRINT DD   SYSOUT=*                               
//SYSIN    DD   *                                      
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.TO)+        
    TRK(1,1)+                                          
    VOLUMES(ZAPRD6)+                                   
    TO(2022328)+                                       
    KEYS(4,0)+                                         
    RECORDSIZE(80,80)+                                 
        CISZ(4096)+               
    INDEXED)                  
/*                            
/*                                                    
//*TO 2022328 DAY THE DATA SET WILL BE DELETED        
//STEP3    EXEC PGM=IDCAMS                            
//SYSPRINT DD   SYSOUT=*                              
//SYSIN    DD   *                                     
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.REUSE)-    
    TRK(1,1)-                                         
    VOLUMES(ZAPRD6)-                                  
    KEYS(4,0)-                                        
    RECORDSIZE(80,80)-                                
    REUSE-                                            
    CISZ(4096)-                                       
    INDEXED)                                          
/*                                                    
//* REUSE                                             
//STEP4    EXEC PGM=IDCAMS                            
//SYSPRINT DD   SYSOUT=*                              
//SYSIN    DD   *                                     
    DEFINE CLUSTER(NAME(TECN93.VVH2.VISHNU.REUSE)-    
    TRK(1,1)-                                         
    VOLUMES(ZAPRD6)-                                  
    KEYS(4,0)-                                        
    RECORDSIZE(80,80)-                                
    CISZ(4096)-                                       
/*               
//* NO REUSE


//TECN93VV JOB  NOTIFY=&SYSUID                              
//STEP1    EXEC PGM=IDCAMS                                  
//SYSPRINT DD   SYSOUT=*                                    
//SYSIN    DD   *                                           
     REPRO-                                                 
     IDS (TECN93.VVH2.KSDS)-                                
     ODS (TECN93.VVH2.VSAM.ESDS)                            
      IF LASTCC=0 THEN-                                     
     PRINT-                                                 
     IDS (TECN93.VVH2.KSDS)                                 
     ELSE                                                   
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)                 
     END IF                                                 
/*                                                          
//                                                          
//* THIS PGM FOR IF MAX=00 THEN,ELSE DO,END                 
//STEP2    EXEC PGM=IDCAMS                                  
//SYSPRINT DD   SYSOUT=*                                    
//SYSIN    DD   *                                           
     REPRO-                                                 
     IDS(TECN93.VVH2.KSDS)-                                 
     ODS(TECN93.VVH2.VSAM.ESDS)                             
      IF LASTCC=4-                                      
           THEN-                       
     DO SET MAXCC=0               
     PRINT-                       
PRINT-                                 
IDS (TECN93.VVH2.VSAM.ESDS)CHAR-       
ELSE                                   
LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1) 
END IF                                 
IDCAMS  SYSTEM SERVICES                                           TIME: 20:07:22
                                                                                
     REPRO-                                                             00050000
     IDS (TECN93.VVH2.KSDS)-                                            00060000
     ODS (TECN93.VVH2.VSAM.ESDS)                                        00070005
IDC0005I NUMBER OF RECORDS PROCESSED WAS 10                                     
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       
                                                                                
      IF LASTCC=0 THEN-                                                 00080004
     PRINT-                                                             00100003
     IDS (TECN93.VVH2.KSDS)                                             00101004
IDCAMS  SYSTEM SERVICES                                           TIME: 20:07:22
LISTING OF DATA SET -TECN93.VVH2.KSDS                                           
KEY OF RECORD - C1F0F0F1                                                        
000000  C1F0F0F1 40D9C1D2 C5E2C8D2 E4D4C1D9   40F9F9F8 F7F6F5F4 F3F2F940 C5D5C7C
000020  D5C5C5D9 40404040 40C2C1D5 C7C1D3D6   D9C54040 40404040 40404040 4040404
000040  40404040 40404040 F0F0F0F0 F0F1F0F0                                     
                                                                                
KEY OF RECORD - C1F0F0F2                                                        
000000  C1F0F0F2 40C1D5C9 D3404040 40404040   40F9F9F8 F7F6F5F2 F2F2F240 E2D94BC
000020  D9C3C8C9 E3C5C3E3 40C3C8C5 D5D5C1C9   40404040 40404040 40404040 4040404
000040  40404040 40404040 F0F0F0F0 F0F2F0F0                                     
                                                                                
KEY OF RECORD - C1F0F0F3                                                        
000000  C1F0F0F3 40E5C9D1 C1E84040 40404040   40F9F2F8 F7F6F3F5 F4F3F940 C5D5C7C
000020  D5C5C5D9 40404040 40D4E8E2 D6D9C540   40404040 40404040 40404040 4040404
000040  40404040 40404040 F0F0F0F0 F0F3F0F0                                     
                                                                                
KEY OF RECORD - C1F0F0F4                                                        


IDCAMS  SYSTEM SERVICES                                           TIME: 20:09:15
                                                                                
     REPRO-                                                             00210002
     IDS(TECN93.VVH2.KSDS)-                                             00220005
     ODS(TECN93.VVH2.VSAM.ESDS)                                         00230005
IDC0005I NUMBER OF RECORDS PROCESSED WAS 10                                     
IDC0001I FUNCTION COMPLETED, HIGHEST CONDITION CODE WAS 0                       
                                                                                
      IF LASTCC=4-                                                      00240002
      THEN-                                                             00250002
     DO SET MAXCC=0                                                     00251002
                                                                                
     PRINT-                                                             00252005
     IDS (TECN93.VVH2.VSAM.ESDS)CHAR-                                   00253005
     ELSE                                                               00270005
IDC3211I KEYWORD 'ELSE' IS IMPROPER                                             
IDC3216I ABOVE TEXT BYPASSED UNTIL NEXT COMMAND                                 
                                                                                
     LISTCAT ALL ENTRIES(TECN93.VVH2.KSDS1)                             00280005
IDC0204I PRECEDING COMMAND BYPASSED DUE TO CONDITION CODES                      
                                                                                
     END IF                                                             00310005
                                                                                
IDC0002I IDCAMS PROCESSING COMPLETE. MAXIMUM CONDITION CODE WAS 0               
******************************** BOTTOM OF DATA ********************************


