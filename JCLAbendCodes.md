JCL Abend Codes
S0CB    -    Attempting to divide by 0 and not using ON SIZE ERROR

S002    -    Very large record length/ wrong record length

Sx22    -    Job has been cancelled. The value of x will vary depending on the way the job was

    cancelled.

S222    -    Means job was cancelled by a user or operator without a dump. If a TSO session times

    out you will probably get an S522 abend code.

S222    -    The job was cancelled (by subsystem or operator) because it violated some restriction

S322    -    Indicates a Time Out abend. Program has taken more CPU time than the default limit for

       the JOB Class could indicate an infinite loop

S522    -    JOB or TSO session exceeded maximum job wait time OR operator did not mount the

    require tape within allowed time limit  

S806    -    Load module not found

S837    -    Space problem, Allotted space is not enough for data set
S913    -    You are trying to access a dataset, which you are not authorized to use.
S0C1    -    Operation Exception. Check for subscript errors, missing DD card, file not opened.

    (Missing / Misspelled DD name, Read / Write to un-opened dataset, Read to dataset that opened in       OUTPUT mode, Write to dataset that opened in INPUT mode. Called sub-program not found)

SOC4    -    1. Index exceeds the size of table

       2. Trying to use File Section variables without opening the file

     (Missing Select statement (during compile), Bad Subscript / index, Protection Exception, 
      Missing   parameters on called sub-program, Read / Write to un-opened file,
      Move data from  / to un-opened file)
SOC5    -    1. Bad Subscript / Index

    2. Close an un-opened dataset

    3. Bad exit from a perform statement

SOC7    -    1. Moving non-numeric value to numeric field

                 2. Not initializing the numeric variables before first use

SB37    -   Insufficient disk space (End of volume and no further volume specified)

SD37    -   Insufficient disk space. (No secondary allocation was specified)

SE37    -   Insufficient disk space. (Max. of 16 extents already allocated)

U1026   -   COBOL sort failed.

U1056   -   Program didn't close a file before ending





JCL ABEND Codes Complete List: 
 
 SB37
 SD37
 SE37
Space Abends
SB37 -  Insufficient disk space
SD37 -  Insufficient disk space
SE37 -  Insufficient disk space.
The maximum number of extents would be exceeded. For instance, when exceeding 16 extents of a PDS.
An E37 on tape datasets is most often caused when the number of requested volumes is exceeded. The default is 5, therefore a request for the sixth volume will fail with a E37
 S80A
 S804
 S822
S80A, S804 Region too small for the program to run
S822 - When the requested region is not available
 S122                              
The job was canceled because it violated some restriction. A dump was requested
 S222                    
The job was cancelled because it violated some restriction. No dump was requested.
 S322
The job used more CPU time than it should have. Either the estimate is wrong or the program is in an  uncontrolled loop.
 S522
Job was waiting too long.
 S722
Too many lines of print.
 S706
The program on the library was not executable.
See linkage editor report that put the program on library
 S806
Program not on the library. May need a JOBLIB or STEPLIB.
 S0C1
Executing a program with an unresolved external reference.
Calling a program and the program was not included during link edit.
An uncontrolled loop moved data on top of instructions.
Reading a file that is not open
Your SORTIN DCB was not correct
Mixing compile options RES and NORES in different modules
 S0C4
An uncontrolled loop moved data on top of instructions.
referencing a field in a record of a closed file
referencing an item in Linkage-Section when there was no PARM= in the JCL.
Calling/called programs have different length for items passed in Linkage Section
with COBOL Sort, doing a STOP RUN or GOBACK while
an input or output procedure is still running
 S0C5
See reasons as for 0C4.
Falling through into an ENTRY statement
Transferring control into the middle of a SORT procedure.
S0C7
Program attempting to do math on illegal data.
Data is not numeric, but should be.
Moving ZEROS to group item whose subordinate items
are packed-decimal
Uninitialized packed-decimal fields.
Record description is wrong. Field starts or ends in the wrong place in the record.
Find record description of creating program.
S0C8
 
S0C9
 
S0CA
 Decimal point overflow error
S0CB
 Attempting to divide by 0 and not using ON SIZE ERROR
S0CC
 Floating Pointing
S0CD
 Exponent overflow and Underflow execptions
S013
 
S878
 
S913
 
SB14
 
S001-4
Input file record length is not equal to the length stated in the DD or the FD
Wrong length record.
IO error, damaged tape, device malfunction.
With disk, reading a dataset that was allocated but never written to.
Writing to input file
Concatenation of files with different record lengths or record formats.
SOC1-5    
Reading after the end of the file by non-COBOL program.
COBOL intercepts this and displays "QSAM error, status 92".
Out of space on output disk file.

 

SAM File Status Codes
 

00        -           SUCCESSFUL COMPLETION

02        -           DUPLICATE KEY, NON-UNIQUE ALT INDEX

04        -           READ, WRONG LENGTH RECORD 

05        -           OPEN, FILE NOT PRESENT

10        -           END OF FILE

20        -           INVALID KEY VSAM KSDS OR RRDS

21        -           SEQUENCE ERROR, ON WRITE OR CHANGING KEY ON REWRITE

22        -           DUPLICATE KEY

23        -           RECORD NOT FOUND - (when we are trying to access a record with key)

          or FILE NOT FOUND

35        -           OPEN, FILE NOT PRESENT

          When we will use this code in our program?

          There are situations where file should be read if exist,
          write if it does not when you don’t know whether file exists are not,
          first you will open file in I-O mode and check status code.
          if it is 35 then open that file for output file.
          Other wise you will continue with your logic
39        -           LOGIC ERROR 

41        -           OPENING A FILE THAT IS ALREADY OPENED 

42        -           CLOSEING A FILE WITHOUT OPEN. 

43        -           DELETE OR REWRITE & NO GOOD READ FIRST

46        -           SEQUENTIAL READ WITHOUT POSITIONING

47        -           READING FILE NOT OPEN AS INPUT/IO/EXTEND

48        -           WRITE WITHOUT OPEN IN IO MODE

49        -           DELETE OR REWRITE WITHOUT OPEN IN IO MODE

92        -           LOGIC ERROR / OPENING A OPEN FILE  / READING OUTPUT FILE  / WRITING INTO

          A INPUT FILE  / DEL or REW BUT NO PRIOR READ

94        -           SEQUENTIAL READ AFTER END OF FILE  / NO CURRENT REC POINTER FOR SEQ 

96        -           MISSING DD STATEMENT IN JCL 

97        -           OPEN OK, FILE INTEGRITY VERIFIED

                      When we will use this in our programs?

          We use this code whenever we open the file,
          if status code is 00 or 97 we will proceed with our logic,
          other wise, call error routine. Usually, it may come when file was not closed.
          for example,
                                     

          IF WS-FILE-STATUS NOT = '00' AND '97'

        PERFORM ERROR-ROUTINE

          END-IF.





                                                                                                                                                                             
    



                                                                                                                                           
                                                                                





                                                
                                                                                                                                                             






                                                                                                                                                                                                      

