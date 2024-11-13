DB2 
CREATE TABLE EMP1(ENPID CHAR(4) NOT NULL PRIMARY KEY,                 
                  EMPNAME CHAR(8),                                    
                  EMPSAL  DEC(8,2),                                   
                  CURRENTDATE VARCHAR(8),                             
                  HIREDATE VARCHAR(8))                                
                  IN SHRDB4.SHRTS4;                                   
CREATE INDEX EMPX ON EMP1(ENPID);                                     
CREATE UNIQUE INDEX UIDB ON EMP1(ENPID);                              
INSERT INTO EMP1 VALUES('A001','VIS',250000.00,'23-01-18','23-02-18');
INSERT INTO EMP1 VALUES('A002','RAVI',80000.00,'23-01-18','23-02-19');
INSERT INTO EMP1 VALUES('A003','BALA',50000.00,'23-01-18','23-02-20');
INSERT INTO EMP1 VALUES('A004','SURE',20000.00,'23-01-18','23-02-21');
INSERT INTO EMP1 VALUES('A005','RAJ',22000.00,'23-01-18','23-02-22'); 
INSERT INTO EMP1 VALUES('A006','MOHA',25000.00,'23-01-18','23-02-23');
INSERT INTO EMP1 VALUES('A007','KUMA',26000.00,'23-01-18','23-02-24');
INSERT INTO EMP1 VALUES('A008','GOKU',30000.00,'23-01-18','23-02-25');
INSERT INTO EMP1 VALUES('A009','SIVA',36000.00,'23-01-18','23-02-27');
SELECT ENPID FROM EMP1;                           
---------+---------+---------+---------+---------+
ENPID                                             
---------+---------+---------+---------+---------+
A001                                              
A002                                              
A003                                              
SELECT EMPNAME FROM EMP1;              
---------+---------+---------+---------
EMPNAME                                
---------+---------+---------+---------
VIS                                    
RAVI                                   
SELECT EMPSAL FROM EMP1;                
---------+---------+---------+---------+
    EMPSAL                              
---------+---------+---------+---------+
 250000.00                              
---------+---------+---------+
SELECT CURRENTDATE FROM EMP1;
CURRENTDATE                   
---------+---------+---------+
23-01-18
23-01-18
23-01-18
23-01-18
23-01-18
23-01-18
SELECT HIREDATE FROM EMP1;              
---------+---------+---------+---------+
HIREDATE   
23-02-18
23-02-19
23-02-20
23-02-21
SELECT * FROM EMP1;
ENPID  EMPNAME       EMPSAL  CURRENTDATE  HIREDATE          
---------+---------+---------+---------+---------+---------+
A001   VIS        250000.00  23-01-18     23-02-18          
A002   RAVI        80000.00  23-01-18     23-02-19          
A003   BALA        50000.00  23-01-18     23-02-20          
A004   SURE        20000.00  23-01-18     23-02-21          
A005   RAJ         22000.00  23-01-18     23-02-22          
A006   MOHA        25000.00  23-01-18     23-02-23          
A007   KUMA        26000.00  23-01-18     23-02-24          
A008   GOKU        30000.00  23-01-18     23-02-25          
A009   SIVA        36000.00  23-01-18     23-02-27          
DSNE610I NUMBER OF ROWS DISPLAYED IS 9                      
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 100

SELECT * FROM EMP1 WHERE ENPID = 'A006';           
---------+---------+---------+---------+---------+-
ENPID  EMPNAME       EMPSAL  CURRENTDATE  HIREDATE 
---------+---------+---------+---------+---------+-
A006   MOHA        25000.00  23-01-18     23-02-23

SELECT * FROM EMP1 WHERE EMPSAL > 50000;
ENPID  EMPNAME       EMPSAL  CURRENTDATE  HIREDATE 
---------+---------+---------+---------+---------+-
A001   VIS        250000.00  23-01-18     23-02-18 
A002   RAVI        80000.00  23-01-18     23-02-19
SELECT MAX(EMPSAL) FROM EMP1;  
---------+---------+---------+-
                               
---------+---------+---------+-
 250000.00                     
SELECT MIN(EMPSAL) FROM EMP1;                 
---------+---------+---------+---------+------
                                              
---------+---------+---------+---------+------
  20000.00                                    
SELECT AVG(EMPSAL) FROM EMP1; 
---------+---------+---------+
                              
---------+---------+---------+
  59888.888888888             
SELECT SUM (EMPSAL) FROM EMP1; 
---------+---------+---------+-
                               
---------+---------+---------+-
        539000.00     
SELECT ENPID,EMPSAL,EMPSAL+500 FROM EMP1;  
---------+---------+---------+---------+---
ENPID      EMPSAL                          
---------+---------+---------+---------+---
A001    250000.00    250500.00             
A002     80000.00     80500.00             
A003     50000.00     50500.00             
A004     20000.00     20500.00             
A005     22000.00     22500.00             
A006     25000.00     25500.00             
A007     26000.00     26500.00             
A008     30000.00     30500.00             
A009     36000.00     36500.00             
SELECT ENPID, EMPSAL, EMPSAL-500 FROM EMP1;
---------+---------+---------+---------+---
ENPID      EMPSAL                          
---------+---------+---------+---------+---
A001    250000.00    249500.00             
A002     80000.00     79500.00    
  
SELECT COUNT(*) FROM EMP1;    
---------+---------+---------+

       
         

DAY2
CREATE TABLE EMP4(EMPID CHAR(4) NOT NULL PRIMARY KEY,                
                  EMPNAME CHAR(8),                                   
                  LASTNAME CHAR(8),                                  
                  PHONENO DEC(10),                                   
                  EMPSAL  DEC(8,2))                                  
                  IN SHRDB4.SHRTS4;                                  
CREATE INDEX UID5 ON EMP4(EMPID);                                    
CREATE UNIQUE INDEX UID6 ON EMP4(EMPID);                             
INSERT INTO EMP4 VALUES('A001','VIS','VARDHAN',9876544578,500000.00);
INSERT INTO EMP4 VALUES('A002','RAVI','KUMAR',3451345782,600000.00); 
INSERT INTO EMP4 VALUES('A003','BALA','UMAR',3213345667,900000.00);  
INSERT INTO EMP4 VALUES('A004','SURE','AGAR',2344455693,100000.00);  
INSERT INTO EMP4 VALUES('A005','RAJ','VARMA',9381264036,200000.00);  
INSERT INTO EMP4 VALUES('A006','MOHA','RAJ',6309401578,300000.00);   
INSERT INTO EMP4 VALUES('A007','KUMA','KUMAR',9496572837,400000.00); 
INSERT INTO EMP4 VALUES('A008','GOKU','PAL',9481223336,500000.00);   
INSERT INTO EMP4 VALUES('A009','SIVA','KUMAR',9381263045,600000.00); 
INSERT INTO EMP4 VALUES('A011','SAIRAME','SAI',234567890,123456.78);
SELECT * FROM EMP4;                                  
---------+---------+---------+---------+---------+---
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL  
---------+---------+---------+---------+---------+---
A001   VIS       VARDHAN    9876544578.   500000.00  
A003   BALA      UMAR       3213345667.   900000.00  
SELECT * FROM EMP4 WHERE EMPSAL BETWEEN 600000.00 AND 900000.00;
---------+---------+---------+---------+---------+---------+----
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL             
---------+---------+---------+---------+---------+---------+----
A003   BALA      UMAR       3213345667.   900000.00             
A009   SIVA      KUMAR      9381263045.   600000.00   
SELECT * FROM EMP4 WHERE EMPNAME LIKE 'R%';        
---------+---------+---------+---------+---------+-
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL
---------+---------+---------+---------+---------+-
A005   RAJ       VARMA      9381264036.   200000.00
SELECT * FROM EMP4 WHERE EMPNAME LIKE'S%';          
---------+---------+---------+---------+---------+--
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL 
---------+---------+---------+---------+---------+--
A004   SURE      AGAR       2344455693.   100000.00 
A009   SIVA      KUMAR      9381263045.   600000.00 
A011   SAIRAME   SAI         234567890.   123456.78

DELETE FROM EMP1 WHERE EMPNAME='VIS';     
---------+---------+---------+---------+--
SELECT EMPNAME,UPPER(EMPNAME) FROM EMP4
---------+---------+---------+---------
EMPNAME                                
---------+---------+---------+---------
VIS       VIS                          
BALA      BALA                         
SURE      SURE                         
RAJ       RAJ                          
MOHA      MOHA                         
KUMA      KUMA                         
GOKU      GOKU                         
SIVA      SIVA                         
SAIRAME   SAIRAME                      
SELECT LASTNAME,UPPER(LASTNAME) FROM EMP4;
---------+---------+---------+---------+--
LASTNAME                                  
---------+---------+---------+---------+--
VARDHAN   VARDHAN                         
UMAR      UMAR                            
AGAR      AGAR                            
VARMA     VARMA                           
RAJ       RAJ  
KUMAR     KUMAR
PAL       PAL  
KUMAR     KUMAR
SAI       SAI  
SELECT EMPNAME ,LOWER(EMPNAME) FROM EM
---------+---------+---------+--------
EMPNAME                               
---------+---------+---------+--------
VIS       vis                         
BALA      bala                        
SURE      sure                        
RAJ       raj                         
MOHA      moha                        
KUMA      kuma                        
GOKU      goku                        
SIVA      siva                        
SELECT HEX(EMPSAL) FROM EMP1; 
---------+---------+---------+
                              
---------+---------+---------+
008000000C                    
005000000C                    
002000000C                    
002200000C                    
002500000C                    
002600000C
003000000C
003600000C
SELECT CONCAT(EMPID,EMPNAME) FROM EMP4; 
---------+---------+---------+---------+
                                        
---------+---------+---------+---------+
A001VIS                                 
A003BALA                                
A004SURE                                
A005RAJ                                 
A006MOHA                                
A007KUMA                                
A008GOKU                                
A009SIVA                                
A011SAIRAME                             
SELECT HOUR(CURRENT TIME) FROM SYSIBM.SYSDUMMY1; 
---------+---------+---------+---------+---------
         16
SELECT MINUTE(CURRENT TIME) FROM SYSIBM.SYSDUMMY1;
---------+---------+---------+---------+---------+
                                                  
---------+---------+---------+---------+---------+
         57                                       
SELECT SECONDS(CURRENT TIME) FROM SYSIBM.SYSDUMMY1; 
---------+---------+---------+---------+---------+--
DSNT408I SQLCODE = -440, ERROR:  NO FUNCTION BY THE
SELECT CURRENT DATE FROM SYSIBM.SYSDUMMY1; 
---------+---------+---------+---------+---
                                           
---------+---------+---------+---------+---
2023-01-22                                 
SELECT LENGTH(EMPNAME) FROM EMP4 WHERE EMPID='A004';  
---------+---------+---------+---------+---------+----
                                                      
---------+---------+---------+---------+---------+----
          8                                           
SELECT COUNT(*) FROM EMP4;     
---------+---------+---------+-
                               
---------+---------+---------+-
          9                    
SELECT COUNT(*)FROM EMP4 WHERE ENPID='A001';       
---------+---------+---------+---------+---------+-
DSNT408I SQLCODE = -206, ERROR:  ENPID IS NOT VALID
         USED                                      
SELECT * FROM EMP4 ORDER BY EMPID DESC;            
---------+---------+---------+---------+---------+-
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL
---------+---------+---------+---------+---------+-
A011   SAIRAME   SAI         234567890.   123456.78
A009   SIVA      KUMAR      9381263045.   600000.00
A008   GOKU      PAL        9481223336.   500000.00
A007   KUMA      KUMAR      9496572837.   400000.00
A006   MOHA      RAJ        6309401578.   300000.00
A005   RAJ       VARMA      9381264036.   200000.00
A004   SURE      AGAR       2344455693.   100000.00
A003   BALA      UMAR       3213345667.   900000.00
A001   VIS       VARDHAN    9876544578.   500000.00

SELECT * FROM EMP4 ORDER BY EMPID ASC;             
---------+---------+---------+---------+---------+-
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL
---------+---------+---------+---------+---------+-
A001   VIS       VARDHAN    9876544578.   500000.00
A003   BALA      UMAR       3213345667.   900000.00
A004   SURE      AGAR       2344455693.   100000.00
A005   RAJ       VARMA      9381264036.   200000.00

EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL
---------+---------+---------+---------+---------+-
A006   MOHA      RAJ        6309401578.   300000.00
A007   KUMA      KUMAR      9496572837.   400000.00
A008   GOKU      PAL        9481223336.   500000.00
A009   SIVA      KUMAR      9381263045.   600000.00
A011   SAIRAME   SAI         234567890.   123456.78

SELECT * FROM EMP4 ORDER BY EMPSAL DESC;            
---------+---------+---------+---------+---------+--
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL 
---------+---------+---------+---------+---------+--
A003   BALA      UMAR       3213345667.   900000.00 
A009   SIVA      KUMAR      9381263045.   600000.00 
A001   VIS       VARDHAN    9876544578.   500000.00
A008   GOKU      PAL        9481223336.   500000.00
A007   KUMA      KUMAR      9496572837.   400000.00
A006   MOHA      RAJ        6309401578.   300000.00
A005   RAJ       VARMA      9381264036.   200000.00
A011   SAIRAME   SAI         234567890.   123456.78
A004   SURE      AGAR       2344455693.   100000.00
SELECT * FROM EMP4 ORDER BY EMPSAL ASC;            
---------+---------+---------+---------+---------+-
EMPID  EMPNAME   LASTNAME       PHONENO      EMPSAL
---------+---------+---------+---------+---------+-
A004   SURE      AGAR       2344455693.   100000.00
A011   SAIRAME   SAI         234567890.   123456.78
A005   RAJ       VARMA      9381264036.   200000.00
A006   MOHA      RAJ        6309401578.   300000.00
A007   KUMA      KUMAR      9496572837.   400000.00
A008   GOKU      PAL        9481223336.   500000.00
A001   VIS       VARDHAN    9876544578.   500000.00
A009   SIVA      KUMAR      9381263045.   600000.00
A003   BALA      UMAR       3213345667.   900000.00

SELECT * FROM EMP1 ORDER BY CURRENTDATE DESC;
---------+---------+---------+---------+---------+-
ENPID  EMPNAME       EMPSAL  CURRENTDATE  HIREDATE 
---------+---------+---------+---------+---------+-
A009   SIVA        36000.00  23-01-18     23-02-27 
A008   GOKU        30000.00  23-01-18     23-02-25 
A007   KUMA        26000.00  23-01-18     23-02-24 
A006   MOHA        25000.00  23-01-18     23-02-23 
A005   RAJ         22000.00  23-01-18     23-02-22 
A004   SURE        20000.00  23-01-18     23-02-21 
A003   BALA        50000.00  23-01-18     23-02-20 
A002   RAVI        80000.00  23-01-18     23-02-19

CREATE ALIAS A1 FOR EMP1;                                               00350099
---------+---------+---------+---------+---------+---------+---------+---------+
DSNT408I SQLCODE = -552, ERROR:  TECN93 DOES NOT HAVE THE PRIVILEGE TO PERFORM  
         OPERATION CREATE ALIAS    
 
CREATE SYNONYM S9 FOR TECN93.EMP1;                                      00360099
---------+---------+---------+---------+---------+---------+---------+---------+
DSNT408I SQLCODE = -601, ERROR:  THE NAME (VERSION OR VOLUME SERIAL NUMBER) OF
  
CREATE TABLE EMP1 LIKE ENP4;                                            00370099
---------+---------+---------+---------+---------+---------+---------+---------+
DSNT408I SQLCODE = -551, ERROR:  TECN93 DOES NOT HAVE THE PRIVILEGE TO PERFORM  
         OPERATION CREATE TABLE ON OBJECT DSNDB04    
  

SELECT CURRENT DATE FROM SYSIBM.SYSDUMMY1;   
---------+---------+---------+---------+-----
       2023-01-22 

SELECT DAYS(CURRENT DATE) FROM SYSIBM.SYSDUMMY1; 
---------+---------+---------+---------+---------
                                                 
---------+---------+---------+---------+---------
     738542
      
SELECT DAYS(DATE(2023-01-01))-DAYS(DATE(2023-01-22)) FROM,                                
                   SYSIBM.SYSDUMMY1;                                    00
---------+---------+---------+---------+---------+---------+---------+----
DSNT408I SQLCODE = -104, ERROR:  ILLEGAL SYMBOL "<END-OF-STATEMENT>". SOME

SELECT CURRENT YEAR FROM SYSIBM.SYSDUMMY1;             
---------+---------+---------+---------+---------+-----
DSNT408I SQLCODE = -104, ERROR:  ILLEGAL SYMBOL "YEAR".

SELECT CURRENT MONTH FROM SYSIBM.SYSDUMMY1;  



SELECT TABLE TABLEY(EMPID CHAR(4) NOT NULL,EMPNAME CHAR(4) NOT NULL, 
                    EMPSAL DEC(6,2),PRIMARY KEY(EMPID)),             
                  WITH RESTRICT ON DROP,                             
                  IN SHRDB4.SHRTS4;  
DROP TABLE TABLEY; 
TRUNCATE TABLE EMP1; 
DROP TABLE TABLENAME;
                               
UPDATE EMPSAL 
UPDATE EMP1 SET EMPSAL=7700 WHERE EMPNAME='VIS';            
---------+---------+---------+---------+---------+---------+
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 100 
---------+---------+---------+---------+---------+---------+


  SELECT * FROM EMP1;                               
---------+---------+---------+---------+---------+      
ENPID  EMPNAME       EMPSAL  CURRENTDATE  HIREDATE
---------+---------+---------+---------+---------+
A002   RAVI        80000.00  23-01-18     23-02-19
A003   BALA        50000.00  23-01-18     23-02-20
A004   SURE        20000.00  23-01-18     23-02-21
A005   RAJ         22000.00  23-01-18     23-02-22
A006   MOHA        25000.00  23-01-18     23-02-23
A007   KUMA        26000.00  23-01-18     23-02-24
A008   GOKU        30000.00  23-01-18     23-02-25
A009   SIVA        36000.00  23-01-18     23-02-27

DELETE FROM EMP1 WHERE EMPSAL=7700                          
---------+---------+---------+---------+---------+---------+
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 100 
---------+---------+---------+---------+---------+---------+
SELECT * FROM EMP1;  
---------+---------+-
ENPID  EMPNAME       EMPSAL  CURRENTDATE  HIREDATE
---------+---------+---------+---------+---------+
A002   RAVI        80000.00  23-01-18     23-02-19
A003   BALA        50000.00  23-01-18     23-02-20
A004   SURE        20000.00  23-01-18     23-02-21
A005   RAJ         22000.00  23-01-18     23-02-22

SELECT TIMESTAMP(CURRENT TIME) FROM SYSIBM.SYSDUMMY1;

SQLCODE = -171, ERROR:  THE DATA TYPE, LENGTH, OR VALUE OF ARGUMENT 1
OF TIMESTAMP IS INVALID     
                                         

  
                                                                                                 

DAY 3
CREATE TABLE DEPARTMENT(DEPTNO CHAR(4) NOT NULL PRIMARY KEY,          
                  DEPTNAME CHAR(8),                                   
                  MGRNO  DEC(8,2),                                    
                  ADMRDEPT CHAR(4),                                   
                  LOCATION CHAR(4))                                   
                  IN SHRDB4.SHRTS4;                                   
CREATE INDEX DEPA ON DEPARTMENT(DEPTNO);                              
CREATE UNIQUE INDEX DEPB ON DEPARTMENT(DEPTNO);                       
NSERT INTO DEPARTMENT VALUES('A001','SPIFYCOM',00001.00,'0001','HYD');
INSERT INTO DEPARTMENT VALUES('B002','PLANNING',00002.00,'0002','BL');
INSERT INTO DEPARTMENT VALUES('C003','INFORMAT',00003.00,'0003','HY');
INSERT INTO DEPARTMENT VALUES('D004','DEVELOPM',00004.00,'0004','HY');
INSERT INTO DEPARTMENT VALUES('E005','MANUFACT',00005.00,'0005','HY');
INSERT INTO DEPARTMENT VALUES('F006','OPERATIO',00001.00,'0001','HY');
SELECT * FROM DEPARTMENT;                         
---------+---------+---------+---------+---------+
DEPTNO  DEPTNAME       MGRNO  ADMRDEPT  LOCATION  
---------+---------+---------+---------+---------+
A001    SPIFYCOM        1.00  0001      HYD       
B002    PLANNING        2.00  0002      BL        
C003    INFORMAT        3.00  0003      HY        
D004    DEVELOPM        4.00  0004      HY        
E005    MANUFACT        5.00  0005      HY        
F006    OPERATIO        1.00  0001      HY        
SELECT DEPTNO,DEPTNAME,ADMRDEPT FROM DEPARTMENT;
---------+---------+---------+---------+--------
DEPTNO  DEPTNAME  ADMRDEPT                      
---------+---------+---------+---------+--------
A001    SPIFYCOM  0001                          
B002    PLANNING  0002                          
C003    INFORMAT  0003                          
D004    DEVELOPM  0004                          
E005    MANUFACT  0005                          
F006    OPERATIO  0001
SELECT DEPTNO,DEPTNAME,ADMRDEPT FROM DEPARTMENT ORDER BY ADMRDEPT ASC;
---------+---------+---------+---------+---------+---------+---------+
DEPTNO  DEPTNAME  ADMRDEPT                                            
---------+---------+---------+---------+---------+---------+---------+
F006    OPERATIO  0001                                                
A001    SPIFYCOM  0001                                                
B002    PLANNING  0002                                                
C003    INFORMAT  0003                                                
D004    DEVELOPM  0004                
E005    MANUFACT  0005                
SELECT DEPTNO,DEPTNAME,ADMRDEPT FROM DEPARTMENT ORDER BY ADMRDEPT DESC;
---------+---------+---------+---------+---------+---------+---------+-
DEPTNO  DEPTNAME  ADMRDEPT                                             
---------+---------+---------+---------+---------+---------+---------+-
E005    MANUFACT  0005                                                 
D004    DEVELOPM  0004                                                 
C003    INFORMAT  0003                                                 
B002    PLANNING  0002                
A001    SPIFYCOM  0001                
F006    OPERATIO  0001               
SELECT DEPTNO ,ADMRDEPT FROM DEPARTMENT WHERE ADMRDEPT='0005';  
DEPTNO  ADMRDEPT                                             
---------+---------+---------+---------+---------+---------+-
E005    0005                                                 
SELECT DEPTNO,DEPTNAME FROM DEPARTMENT WHERE DEPTNO NOT LIKE 'D%';
---------+---------+---------
DEPTNO  DEPTNAME             
---------+---------+---------
A001    SPIFYCOM             
B002    PLANNING             
C003    INFORMAT             
E005    MANUFACT             
F006    OPERATIO             
SELECT DEPTNAME FROM DEPARTMENT WHERE DEPTNO NOT LIKE 'O%'
---------+---------+---------+---------+---------+--------
DEPTNAME                                                  
---------+---------+---------+---------+---------+--------
SPIFYCOM                                                  
PLANNING                                                  
INFORMAT                                                  
DEVELOPM                                                  
MANUFACT                                                  
OPERATIO                                                  
SELECT  DEPTNO,DEPTNAME,MGRNO FROM DEPARTMENT WHERE MGRNO IS NULL;
---------+---------+---------+---------+---------+---------+------
DEPTNO  DEPTNAME       MGRNO                                      
---------+---------+---------+---------+---------+---------+------
CREATE ALIAS A1 FOR EM;                                                 002600
---------+---------+---------+---------+---------+---------+---------+--------
DSNT408I SQLCODE = -552, ERROR:  TECN93 DOES NOT HAVE THE PRIVILEGE TO PERFORM
         OPERATION CREATE ALIAS                                               
DSNT418I SQLSTATE   = 42502 SQLSTATE RETURN CODE                              
DSNT415I SQLERRP    = DSNXODD2 SQL PROCEDURE DETECTING ERROR                  
DSNT416I SQLERRD    = 40 0  0  -1  0  0 SQL DIAGNOSTIC INFORMATION            
DSNT416I SQLERRD    = X'00000028'  X'00000000'  X'00000000'  X'FFFFFFFF'      
         X'00000000'  X'00000000' SQL DIAGNOSTIC INFORMATION      
            
CONSTRAINTS:
CREATE TABLE NOTNULL(EMPID CHAR(4) NOT NULL,EMPNAME CHAR(10)NOT NULL, 
                     EMPSAL DEC(8,2),PRIMARY KEY(EMPID))              
                     IN SHRDB4.SHRTS4;                                
+---------+---------+---------+---------+---------+--
STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0     
+---------+---------+---------+---------+---------+--
CREATE INDEX NOTNULLI ON NOTNULL(EMPID);
+---------+---------+---------+---------+---------+--
STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0     
+---------+---------+---------+---------+---------+--
CREATE UNIQUE INDEX NOTNULLA ON NOTNULL(EMPID);
+---------+---------+---------+---------+---------+
STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0   

INSERT INTO NOTNULL VALUES('W001','VISHNU',450000.25);   
INSERT INTO NOTNULL VALUES('W002','SAIKUMAR',847020.23); 
INSERT INTO NOTNULL VALUES('W003','ROMAN',550000.25);    
INSERT INTO NOTNULL VALUES('W004','AJSTYLES',642000.25); 
INSERT INTO NOTNULL VALUES('W001','VISHNU',450000.25); 
  
WITH SAME NAME
INSERT INTO NOTNULL VALUES('W001','VISHNU',450000.25);                  00100
---------+---------+---------+---------+---------+---------+---------+-------
DSNT408I SQLCODE = -803, ERROR:  AN INSERTED OR UPDATED VALUE IS INVALID     
         BECAUSE INDEX IN INDEX SPACE NOTNULLA CONSTRAINS COLUMNS OF THE TABL
         SO NO TWO ROWS CAN CONTAIN DUPLICATE VALUES IN THOSE COLUMNS.       
         RID OF EXISTING ROW IS X'00001B9A01'.                               

SELECT * FROM NOTNULL;             
---------+---------+---------+-----
EMPID  EMPNAME         EMPSAL      
---------+---------+---------+-----
W001   VISHNU       450000.25      
W002   SAIKUMAR     847020.23      
W003   ROMAN        550000.25      
W004   AJSTYLES     642000.25      

CREATE TABLE PRIMARYKEY(EMPID CHAR(4) NOT NULL,EMPNAME CHAR(10)NOT NULL,
                        EMPSAL DEC(8,2),PRIMARY KEY(EMPID))             
                        IN SHRDB4.SHRTS4;                               
---------+---------+---------+---------+---------+---------+---------+--
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0               
---------+---------+---------+---------+---------+---------+---------+--
        CREATE TABLE UNIKE1(EMPID CHAR(4) UNIQUE NOT NULL,         
EMPNAME CHAR (10) NOT NULL, EMPSAL DEC(6,2))               
                   IN SHRDB4.SHRTS4;                       
---------+---------+---------+---------+---------+---------
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0  
---------+---------+---------+---------+---------+---------
---------+---------+---------+---------+---------+---------
DSNE617I COMMIT PERFORMED, SQLCODE IS 0                    
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0  
CREATE INDEX UNI123 ON UNIKE1(EMPID);                       
---------+---------+---------+---------+---------+---------+
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0   
---------+---------+---------+---------+---------+---------+
---------+---------+---------+---------+---------+---------+
DSNE617I COMMIT PERFORMED, SQLCODE IS 0                     
CREATE UNIQUE INDEX UNI122 ON UNIKE1(EMPID);                 
---------+---------+---------+---------+---------+---------+-
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0    

INSERT INTO UNIKE1 VALUES('T001','UDAY',9000.00); 
INSERT INTO UNIKE1 VALUES('S002','SAI',7000.00); 
---------+---------+---------+---------+---------+-------
DSNE617I COMMIT PERFORMED, SQLCODE IS 0                  
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE IS 0
SELECT * FROM UNIKE1;          
---------+---------+---------+-
EMPID  EMPNAME       EMPSAL   
---------+---------+---------+
T001   UDAY         9000.00   
S002   SAI          7000.00   

INSERT INTO UNIKE1 VALUES('T001','UDAY',9000.00); 
SQLCODE = -803, ERROR:  AN INSERTED OR UPDATED VALUE IS INVALID     
BECAUSE INDEX IN INDEX SPACE UNI122 CONSTRAINS COLUMNS OF THE TABLE 
SO NO TWO ROWS CAN CONTAIN DUPLICATE VALUES IN THOSE COLUMNS.       
RID OF EXISTING ROW IS X'00001BDA01'.                               

CREATE TABLE CHECKKEY(EMPID CHAR(4) NOT NULL CHECK (EMPID LIKE 'A%'), 
                      EMPNAME CHAR(10) NOT NULL, EMPSAL DEC(6,2),     
                      PRIMARY KEY(EMPID))                             
                      IN SHRDB4.SHRTS4;    
   STARTING LETTER SHOUD A%                        
SELECT * FROM CHECKKEY;     
---------+---------+--------
EMPID  EMPNAME       EMPSAL 
---------+---------+--------
A001   VISHNU       4500.25 
AS02   SAIKUMA      8470.23 
AC03   ROMAN        5500.21 
ACV4   AJSTYLES     6420.22

SELECT CHECK (SALARY > 5000.00);                                        00340046
---------+---------+---------+---------+---------+---------+---------+---------+
DSNT408I SQLCODE = -104, ERROR:  ILLEGAL SYMBOL ">". SOME SYMBOLS THAT MIGHT    
         BE LEGAL ARE: CONCAT || / MICROSECONDS MICROSECOND SECONDS SECOND      
         MINUTES                                                                
CREATE SYNONYM RS1 FOR TECN93.EMP4;                       
---------+---------+---------+---------+---------+--------
DSNE616I STATEMENT EXECUTION WAS SUCCESSFUL, SQLCODE I



SUPPLIER,PARTS AND SHIPMENT TABLE

CREATE TABLE SUP(SNO CHAR(4) NOT NULL, SNAME CHAR(10) NOT NULL,  
         SSTATUS CHAR(3) NOT NULL, SCITY CHAR(10) NOT NULL,      
         PRIMARY KEY(SNO))                                       
         IN SHRDB4.SHRTS4;                                       
CREATE INDEX SUP1I ON SUP(SNO);                                  
CREATE UNIQUE INDEX SUP1UI ON SUP(SNO);                          
NSERT INTO SUP VALUES('S1','ROOPDHAR','40','BANGALORE');         
INSERT INTO SUP VALUES('S2','UDAY','60','BANGALORE');            
INSERT INTO SUP VALUES('S3','SHASHI','50','HYDERABAD');          
INSERT INTO SUP VALUES('S4','MADHAVAN','30','CHENNAI');          
INSERT INTO SUP VALUES('S5','MYTHRA','90','CHENNAI');            
INSERT INTO SUP VALUES('S6','GEETHA','70','HYDERABAD');          
INSERT INTO SUP VALUES('S7','CHANDU','20','HYDERABAD');          
INSERT INTO SUP VALUES('S8','LAVANYA','40','BANGALORE');         
INSERT INTO SUP VALUES('S9','RAVI','65','CHENNAI');              
INSERT INTO SUP VALUES('S10','CHICHU','85','BANGALORE');         
SELECT * FROM SUP;                      
---------+---------+---------+---------+
SNO   SNAME       SSTATUS  SCITY        
---------+---------+---------+---------+
S1    ROOPDHAR    40       BANGALORE    
S2    UDAY        60       BANGALORE    
S3    SHASHI      50       HYDERABAD    
S4    MADHAVAN    30       CHENNAI      
S5    MYTHRA      90       CHENNAI    
S6    GEETHA      70       HYDERABAD  
S7    CHANDU      20       HYDERABAD  
S8    LAVANYA     40       BANGALORE  
S9    RAVI        65       CHENNAI    
S10   CHICHU      85       BANGALORE  
CREATE TABLE PAR(PNO CHAR(4) NOT NULL, PNAME CHAR(10) NOT NULL, 
         PCOLOUR CHAR(6) NOT NULL, PWEIGHT CHAR(3) NOT NULL,    
         PCITY CHAR(10) NOT NULL, PRIMARY KEY(PNO))             
         IN SHRDB4.SHRTS4;    
CREATE INDEX PAR1 ON PAR(PNO);                                  
CREATE UNIQUE INDEX PARU1 ON PAR(PNO);
SELECT * FROM PAR;                             
---------+---------+---------+---------+-------
PNO   PNAME       PCOLOUR  PWEIGHT  PCITY      
---------+---------+---------+---------+-------
P1    NUT         BLUE     10       WARANGAL   
P2    BOLT        BLACK    12       GUNTUR     
P3    SCREW       PINK     15       KURNOL     
P4    BOLT        RED      13       THIRUPATHI 
P5    CAM         RED      18       HYDERABAD  
P6    PIN         BLUE     4        BANGALORE  
CREATE TABLE SHIP(SNO CHAR(4),PNO CHAR(4),QTY CHAR(4),            
         FOREIGN KEY(SNO) REFERENCES SUP(SNO) ON DELETE RESTRICT, 
         FOREIGN KEY(PNO) REFERENCES PAR(PNO) ON DELETE RESTRICT) 
         IN SHRDB4.SHRTS4;                                        
CREATE INDEX SHIPI ON SHIP(SNO);                                  
CREATE UNIQUE INDEX SHIPU ON SHIP(SNO);                           
INSERT INTO SHIP VALUES('S1','P1','200');                         
INSERT INTO SHIP VALUES('S2','P5','400');                         
INSERT INTO SHIP VALUES('S3','P6','100');                         
INSERT INTO SHIP VALUES('S4','P3','600');                         
INSERT INTO SHIP VALUES('S5','P2','500');                         
SELECT * FROM SHIP; 
---------+---------+
SNO   PNO   QTY     
---------+---------+
S1    P1    200     
S2    P5    400     
S3    P6    100     
S4    P3    600     
S5    P2    500     
SELECT PNAME FROM PAR; 
---------+---------+---
PNAME                  
---------+---------+---
NUT                    
BOLT                   
SCREW                  
BOLT                   
CAM
PIN
SELECT DISTINCT SSTATUS FROM SUP;
---------+---------+---------+---
SSTATUS                          
---------+---------+---------+---
20                               
30                               
40                               
50                               
60                               
65                               
70                               
85                               
90   

                            
SELECT * FROM SUP WHERE SCITY ='BANGALORE' AND SSTATUS < '50'; 
---------+---------+---------+---------+---------+---------+---
SNO   SNAME       SSTATUS  SCITY                               
---------+---------+---------+---------+---------+---------+---
S1    ROOPDHAR    40       BANGALORE                           
S8    LAVANYA     40       BANGALORE                           
SELECT SNO,SSTATUS FROM SUP WHERE SCITY='HYDERABAD'    
             ORDER BY SSTATUS DESC;                    
---------+---------+---------+---------+---------+-----
SNO   SSTATUS                                          
---------+---------+---------+---------+---------+-----
S6    70 
S3    50 
S7    20
SELECT SNO SSTATUS FROM SUP WHERE SCITY = 'CHENNAI'; 
---------+---------+---------+---------+---------+---
SSTATUS                                              
S4      
S5      
S9      
SELECT PNO FROM SHIP;
---------+---------+-
PNO                  
---------+---------+-
P1                   
P5                   
P6                   
P3                   
P2                   

SELECT DISTINCT PCOLOUR FROM PAR; 
---------+---------+---------+----
PCOLOUR                           
---------+---------+---------+----
BLACK                             
BLUE                              
PINK                              
























**** UNION AND JOINS ****                                           
 TABLE A EMP                                                        
CREATE TABLE EMP(EMPID CHAR (2) NOT NULL PRIMARY KEY,               
             FIRSTNAME CHAR(10) NOT NULL,                           
             LASTNAME CHAR (10) NOT NULL,                           
             DATEOFJOINING CHAR (10) NOT NULL,                      
             DEPT CHAR (6) NOT NULL,                                
             SALARY DEC(8,2))                                       
             IN SHRDB4.SHRTS4;                                      
CREATE INDEX TED1 ON EMP(EMPID);                                    
CREATE UNIQUE INDEX TED2 ON EMP(EMPID);                             
INSERT INTO EMP VALUES ('01','RAJ','KUMAR','2FEB23','OPE',3456.);   
INSERT INTO EMP VALUES ('02','CHANDAN','RAY','4FEB23','ADM',3456.); 
INSERT INTO EMP VALUES ('03','ABHILASH','JOSHI','7FEB23','HR',36.); 
INSERT INTO EMP VALUES ('04','AJIT','RAY','2FEB22','SUP',9456.77);  
INSERT INTO EMP VALUES ('05','PRAVEEN','KUMAR','2APR21','OPE',9765);
INSERT INTO EMP VALUES ('06','RAHUL','DEY','9FEB23','ACC',1236.77); 
INSERT INTO EMP VALUES ('07','VISHNU','VAR','8FEB23','DEVE',9999.); 
INSERT INTO EMP VALUES ('08','GOPI','SUNDAR','2MAR23','ADM',8888.); 
INSERT INTO EMP VALUES ('09','SURAJ','SINGH','6MAR23','ADM',7777.); 
INSERT INTO EMP VALUES ('10','SOURAV','PAUL','9APR23','OPE',5555.);
SELECT * FROM EMP;                                                      
---------+---------+---------+---------+---------+---------+---------+--
EMPID  FIRSTNAME   LASTNAME    DATEOFJOINING  DEPT        SALARY        
01     RAJ         KUMAR       2FEB23         OPE        3456.00  
02     CHANDAN     RAY         4FEB23         ADM        3456.00  
03     ABHILASH    JOSHI       7FEB23         HR           36.00  
04     AJIT        RAY         2FEB22         SUP        9456.77  
05     PRAVEEN     KUMAR       2APR21         OPE        9765.00  
06     RAHUL       DEY         9FEB23         ACC        1236.77  
07     VISHNU      VAR         8FEB23         DEVE       9999.00  
08     GOPI        SUNDAR      2MAR23         ADM        8888.00  
09     SURAJ       SINGH       6MAR23         ADM        7777.00  
10     SOURAV      PAUL        9APR23         OPE        5555.00  

TABLE B CLG                                                     
CREATE TABLE CLG(DEPTNO CHAR (2) NOT NULL,                       
             DEPTNANME CHAR(10) NOT NULL,                        
         TOTALSTUDENT  CHAR (10) NOT NULL,                         
         JOIN CHAR (10) NOT NULL,                                  
         PASSOUT CHAR (10) NOT NULL,                               
         PRIMARY KEY(DEPTNO))                                      
         IN SHRDB4.SHRTS4;                                         
CREATE INDEX TCLG1 ON CLG(DEPTNO);                                 
CREATE UNIQUE INDEX TCLG2 ON CLG(DEPTNO);                          
INSERT INTO CLG VALUES ('11','ADMIN','','AUG2014','JUN2018');      
INSERT INTO CLG VALUES ('12','HR','','AUG2014','JUN2018');         
INSERT INTO CLG VALUES ('13','SALES','','AUG2014','JUN2018');      
INSERT INTO CLG VALUES ('14','PURCHASE','','AUG2014','JUN2018');   
INSERT INTO CLG VALUES ('15','ACCONTANT','','AUG2014','JUN2018');  
INSERT INTO CLG VALUES ('06','MARKETING','','AUG2014','JUN2018');  
INSERT INTO CLG VALUES ('07','METALLURGY','','AUG2014','JUN2018'); 
INSERT INTO CLG VALUES ('08','MINING','','AUG2014','JUN2018');     
INSERT INTO CLG VALUES ('09','IT','','AUG2014','JUN2018');         
INSERT INTO CLG VALUES ('10','BIOTEC','','AUG2014','JUN2018');     
*INSERT INTO CLG VALUES ('11','BIOTEC','','AUG2015','JUN2019');    
*INSERT INTO CLG VALUES ('12','BIOTEC','','AUG2015','JUN2019');    
SELECT *FROM CLG;                                                       
---------+---------+---------+---------+---------+---------+---------+--
DEPTNO  DEPTNANME   TOTALSTUDENT  JOIN        PASSOUT                   
---------+---------+---------+---------+---------+---------+---------+--
11      ADMIN                     AUG2014     JUN2018                   
12      HR                        AUG2014     JUN2018                   
13      SALES                     AUG2014     JUN2018
14      PURCHASE                  AUG2014     JUN2018
15      ACCONTANT                 AUG2014     JUN2018
06      MARKETING                 AUG2014     JUN2018
07      METALLURGY                AUG2014     JUN2018
08      MINING                    AUG2014     JUN2018
09      IT                        AUG2014     JUN2018
10      BIOTEC                    AUG2014     JUN2018
--**** FULL OUTER JOIN ****                                             
SELECT FIRSTNAME,DEPTNANME FROM EMP FULL OUTER JOIN CLG ON EMPID=DEPTNO;
---------+---------+---------+---------+---------+---------+---------+--
FIRSTNAME   DEPTNANME                                                   
---------+---------+---------+---------+---------+---------+---------+--
RAJ         ---------- 
CHANDAN     ---------- 
ABHILASH    ---------- 
AJIT        ---------- 
PRAVEEN     ---------- 
RAHUL       MARKETING  
VISHNU      METALLURGY 
GOPI        MINING     
SURAJ       IT         
FIRSTNAME   DEPTNANME  
---------+---------+---
SOURAV      BIOTEC     
----------  ADMIN      
----------  HR         
----------  SALES      
----------  PURCHASE   
----------  ACCONTANT  
--****INNER JOIN *****
SELECT FIRSTNAME,DEPTNANME FROM EMP INNER JOIN CLG ON EMPID=DEPTNO;    
---------+---------+---------+---------+---------+---------+---------+-
FIRSTNAME   DEPTNANME                                                  
---------+---------+-------
RAHUL       MARKETING      
VISHNU      METALLURGY     
GOPI        MINING         
SURAJ       IT             
SOURAV      BIOTEC      
SELECT FIRSTNAME,DEPTNANME FROM EMP RIGHT OUTER JOIN CLG ON            
EMPID=DEPTNO; 
---------+---------+---
FIRSTNAME   DEPTNANME  
---------+---------+---
RAHUL       MARKETING  
VISHNU      METALLURGY 
GOPI        MINING     
SURAJ       IT         
SOURAV      BIOTEC     
FIRSTNAME   DEPTNANME  
---------+---------+---
----------  ADMIN      
----------  HR         
----------  SALES      
----------  PURCHASE   
----------  ACCONTANT  




SELECT FIRSTNAME,DEPTNANME,EMPID,DEPTNO FROM EMP RIGHT OUTER JOIN CLG ON0
                         EMPID=DEPTNO;                                  0
---------+---------+---------+---------+---------+---------+---------+---
FIRSTNAME   DEPTNANME   EMPID  DEPTNO                                    
---------+---------+---------+---------+---------+---------+---------+---
RAHUL       MARKETING   06     06                                        
VISHNU      METALLURGY  07     07                                        
GOPI        MINING      08     08                                        
SURAJ       IT          09     09                                        
SOURAV      BIOTEC      10     10                                        
----------  ADMIN       -----  11                                        
----------  HR          -----  12                                        
----------  SALES       -----  13                                        
----------  PURCHASE    -----  14                                        
----------  ACCONTANT   -----  15     
SELECT FIRSTNAME,DEPTNANME,EMPID,DEPTNO FROM EMP LEFT OUTER JOIN CLG ON 0
                         EMPID=DEPTNO;                                  0
---------+---------+---------+---------+---------+---------+---------+---
FIRSTNAME   DEPTNANME   EMPID  DEPTNO                                    
---------+---------+---------+---------+---------+---------+---------+---
RAJ         ----------  01     ------                                    
CHANDAN     ----------  02     ------                                    
ABHILASH    ----------  03     ------                                    
AJIT        ----------  04     ------                                    
PRAVEEN     ----------  05     ------                                    
RAHUL       MARKETING   06     06                                        
VISHNU      METALLURGY  07     07                                        
GOPI        MINING      08     08                                        
SURAJ       IT          09     09                                        
SOURAV      BIOTEC      10     10                                        
                                   
  INSERT INTO CLG VALUES ('11','BIOTEC','','AUG2015','JUN2019');          00410024
---------+---------+---------+---------+---------+---------+---------+---------+
DSNT408I SQLCODE = -803, ERROR:  AN INSERTED OR UPDATED VALUE IS INVALID        
         BECAUSE INDEX IN INDEX SPACE TCLG2 CONSTRAINS COLUMNS OF THE TABLE SO  
         NO TWO ROWS CAN CONTAIN DUPLICATE VALUES IN THOSE COLUMNS.             
--**** UNIONS ****
SELECT * FROM EMP;                                                     
---------+---------+---------+---------+---------+---------+---------+-
EMPID  FIRSTNAME   LASTNAME    DATEOFJOINING  DEPT        SALARY       
01     RAJ         KUMAR       2FEB23         OPE        3456.00  
02     CHANDAN     RAY         4FEB23         ADM        3456.00  
03     ABHILASH    JOSHI       7FEB23         HR           36.00  
04     AJIT        RAY         2FEB22         SUP        9456.77  
05     PRAVEEN     KUMAR       2APR21         OPE        9765.00  
06     RAHUL       DEY         9FEB23         ACC        1236.77  
07     VISHNU      VAR         8FEB23         DEVE       9999.00  
08     GOPI        SUNDAR      2MAR23         ADM        8888.00  
09     SURAJ       SINGH       6MAR23         ADM        7777.00  
10     SOURAV      PAUL        9APR23         OPE        5555.00  
SELECT *FROM CLG;                                           
---------+---------+---------+---------+---------+---------+
DEPTNO  DEPTNANME   TOTALSTUDENT  JOIN        PASSOUT       
---------+---------+---------+---------+---------+---------+
11      ADMIN                     AUG2014     JUN2018       
12      HR                        AUG2014     JUN2018       
13      SALES                     AUG2014     JUN2018 
14      PURCHASE                  AUG2014     JUN2018 
15      ACCONTANT                 AUG2014     JUN2018 
06      MARKETING                 AUG2014     JUN2018 
07      METALLURGY                AUG2014     JUN2018 
08      MINING                    AUG2014     JUN2018 
09      IT                        AUG2014     JUN2018 
10      BIOTEC                    AUG2014     JUN2018 
SELECT EMPID FROM EMP UNION SELECT DEPTNO FROM CLG; 
---------+---------+---------+---------+---------+--
                                                    
---------+---------+---------+---------+---------+--
01
02                                                  
03                                                  
04                                                  
05                                                  
06                                                  
07                                                  
08                                                  
09                                                  
10                                                  
11                                                  
12                                                  
13 
14 
15
SELECT FIRSTNAME FROM EMP UNION SELECT DEPTNANME FROM CLG; 
---------+---------+---------+---------+---------+---------
                                                           
---------+---------+---------+---------+---------+---------
ABHILASH                                                   
ACCONTANT                                                  
ADMIN                                                      
AJIT                                                       
BIOTEC                                                     
CHANDAN                                                    
GOPI                                                       
HR                                                         
IT                                                         
MARKETING                                                  
METALLURGY                                                 
MINING   
PRAVEEN  
PURCHASE 
RAHUL    
RAJ      
SALES    
SOURAV   
SURAJ    
VISHNU   
SELECT EMPID,FIRSTNAME FROM EMP UNION SELECT DEPTNO,DEPTNANME FROM CLG;
---------+---------+---------+---------+---------+---------+---------+-
                                                                       
---------+---------+---------+---------+---------+---------+---------+-
01  RAJ                                                                
02  CHANDAN                                                            
03  ABHILASH                                                           
04  AJIT                                                               
05  PRAVEEN                                                            
06  MARKETING                                                          
06  RAHUL                                                              
07  METALLURGY                                                         
07  VISHNU                                                             
08  GOPI                                                               
08  MINING    
09  IT        
09  SURAJ     
10  BIOTEC    
10  SOURAV    
11  ADMIN     
12  HR        
13  SALES     
14  PURCHASE  
15  ACCONTANT
SELECT EMPID,FIRSTNAME FROM EMP UNION ALL SELECT DEPTNO,DEPTNANME FROM 
                       CLG;                                            
---------+---------+---------+---------+---------+---------+---------+-
                                                                       
---------+---------+---------+---------+---------+---------+---------+-
01  RAJ                                                                
02  CHANDAN                                                            
03  ABHILASH                                                           
04  AJIT                                                               
05  PRAVEEN                                                            
06  RAHUL                                                              
07  VISHNU                                                             
08  GOPI                                                               SELECT EMPID,FIRSTNAME FROM EMP UNION ALL SELECT DEPTNO,DEPTNANME FROM 
                       CLG;                                            
---------+---------+---------+---------+---------+---------+---------+-
                                                                       
---------+---------+---------+---------+---------+---------+---------+-
01  RAJ                                                                
02  CHANDAN                                                            
03  ABHILASH                                                           
04  AJIT                                                               
05  PRAVEEN                                                            
06  RAHUL                                                              
07  VISHNU                                                             
08  GOPI                                                               
 


