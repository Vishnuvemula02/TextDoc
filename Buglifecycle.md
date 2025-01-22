                                      Bug Life Cycle (BLC) /  Defect Life Cycle (DLC) 
•	What is a defect?
It is a mismatch in the expected and actual behavior of an application.

Example:-
1. Unable to create account even after entering valid data to all the required fields.
2. Added Products are not displayed in the cart.

•	Defect/Bug Occurs in the application because of the following reasons:-
	Wrong Implementation.
	Missing Implementation.
	Extra Implementation.

•	What is the major difference between error, defect and failure?
Error:
  If the developers find that there is a mismatch in the actual and expected behavior of an application in the development phase then they call it an Error.

Defect:
  If the Testers find that there is a mismatch in the actual and expected behavior of an application in the Testing phase then they call it as a Defect.

Failure:
  If Customers/Clients or end users find that there is a mismatch in the actual and expected behavior of an application in the Production phase then they call it as a Failure.

•	Difference between Bug and defect?
 
 
Bug Life Cycle (BLC) /  Defect Life Cycle (DLC) definition:
	Defect life cycle or bug life cycle is the specific set of states that a bug goes through in its entire life. This starts as soon as any new defect is found by a tester and comes to an end when a tester closes that defect assuring that it won’t get reproduced again.

Bug Life Cycle Status:
    The number of states that a defect goes through varies from project to project. Below lifecycle diagram covers all possible states.
           


Note: 
  New, Assigned, Open, Fixed, Retest, Reopened, Closed Statues already taught in the class.

1. Rejected: 
   If the developer team rejects a defect if they feel that defect is not considered a genuine defect, and then they mark the status as ‘Rejected’. The cause of rejection may be misunderstanding of requirement , referring to old requirement , because of extra features , improper installation of the product , Duplicate Defect, NOT a Defect or Non-Reproducible.
Test engineer Approach:
  Whenever the developer says invalid , first we reconfirm by going through the requirement once again and update the status accordingly i.e.
   Closed: If really the bug is invalid
   ReOpen: If the bug is valid
  
2. Duplicate:
     Sometimes it may happen that the defect is repeated twice or the defect is the same as any other defect then it is marked as a ‘Duplicate’ state and then the defect is ‘Rejected’.
Reason for Duplicate:
	Common features
	Dependent features
How to avoid duplicate bugs?
  As soon as bug found search in bug repository, if the bug is exist don’t report the bug.


3. Postponed (or) Deferred:
   All defects have a bad impact on developed software and also they have a level based on their impact on software. If the developer team feels that the defect that is identified is not a prime priority and it can get fixed in further updates or releases then the developer team can mark the status as ‘Deferred’. This means from the current defect life cycle it will be terminated.
Why do you get postponed status? 
	If we find a bug during the end of the release (could be major or minor but cannot be Critical) developers won’t have time to fix the bug. Such a bug will be postponed and fixed in the next release and the bug status will be “Postponed”.
	If the tester finds a bug in a feature where in developers are expecting changes for customers side those defects will get the status postponed.


4. Can’t be Fixed: 
   If the developer team fails to fix the defect due to Technology support, the Cost of fixing a bug is more, lack of required skill, or due to any other reasons then the developer team marks the defect as in ‘Can’t be fixed’ state.

Test Engineer Approach:
   If the status is given as cannot be fixed then test engineer checks whether if it is blocker and critical bug, if it’s a blocker or critical bug then test engineer will change the status of the bug to reopen. If it’s a minor bug test engineer will give the status as closed.


5. Not-Reproducible:
   Test engineers are able to see the defect but the same defect is not able to see by the developer team, then developer lead will change the status of the bug as Not-Reproducible.

Why we get Not-Reproducible defect?
	Because of platform mismatch.
	Because of improper defect  report .
	Because of data mismatch.
	Because of inconsistent.
	Because of version mismatch.


6. Request For Enhancement(RFE):
        Test engineer finds a bug and sends it to development team when development team look at the report sent by the test engineer , they know it’s a bug , but they say it’s not a bug because it’s not a part of the requirement.



                                                              Severity and Priority
Severity:
   It is a impact of a defect on the customer business.

They are different severity levels are:
	Blocker: This defect indicates complete shut-down of the process, Nothing can proceed futher. 
	Critical: It is a highly severe defect and collapses the system. However , certain parts of the system 
               Remain functional.
	Major: It causes some undesirable behavior ,  but the system is still functional.
	Minor: It won’t cause any major break-down of the system.

Priority:
  Priority is defined as the order in which a defect should be fixed, Higher the priority the sooner the defect should be resolved.
They are different Priority levels are:
	High: The defect must be resolved as soon as possible as it affect the system severely and cannot be
           used until it is fixed.
	Medium: During the normal course of the development activities defect should be resolved. It can wait 
                  until a new version is created. 
	Low: The defect is an irritant but repair can be done once the more serious defect has been fixed.



Example for High Severity and High Priority defects:
	Place order functionality is not working in online shopping application.
	Unable to select current location and destination location in OLA application.
	Join meeting option is not working in zoom application.
	Send request option is disable in facebook application.
	Send message feature is not working in whatsapp application.
	The user performs adding an item to the cart, the number of quantities added is incorrect/wrong product gets added.
	ATM vending currency feature where in after entering the correct username and the password, the machine does not dispense money but deducted the amount from your account.

Example for Low Severity and Low Priority defects:
	Spelling mistakes in the confirmation message.
	Alignment issues in the archived project page.
	Confirmation message is not displayed after logout from gmail application.

Example for High Severity and Low Priority defects:
	Blank page is displayed on click help link
	External links provided in the application is not working.
	Unable to install what’sApp application for 30th time.

Example for Low Severity and High Priority defects:
	Spelling mistakes in the company name.
	Logo of the company























Defect Report
 
     Defect report, also known as bug report , is a document that identifies and describes a defect detected by a tester. The purpose of a defect report is to state the problem as clearly as possible so that developers can replicate that defect easily and fix it.

How to write Defect Report/Bug Report:
   While reporting the bug to developer, your bug report should contain the following information.

   Defect ID: 
   Release Name:
   Build ID:
   Module Name:
   Status:
   Severity:
   Priority:
  Test Environment:
  Test Data:
  Brief Description:
  Detailed Description:
  Expected Result:
  Actual Result:
  Attachment:
  Created Date:
