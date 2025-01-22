Types of Black Box Testing:
•	Functionality Testing
•	Integration Testing
•	System Testing
•	Acceptance Testing
•	Smoke Testing
•	Sanity Testing
•	Regression Testing
•	Adhoc Testing
•	Exploratory Testing
•	Usability Testing
•	Performance Testing
•	Compatibility Testing
•	Accessibility Testing
•	Reliability Testing
•	Recovery Testing
•	Globalization Testing

Functionality Testing/Field level Testing/Component Testing:
      Testing each and every component thoroughly against requirement specification is called as Functionality testing.
Component: It means, text field, text area, drop down, radio button, check box, link, scrollbar, grid, Widget icon etc.
Here thoroughly means trying will all possible inputs or scenarios or cases.

Note:  
-	Always start testing the application with valid data. If the field is working for valid data then only test the component for invalid data.
-	If the component is working for one of the invalid data, we can still continue the testing for some more invalid data.


Integration Testing:
    Testing the dataflow between the dependent modules is called as Integration Testing.
    
If Module ‘A’ is able to send data & module ‘B’ is able to receive data, then integration testing
between module ‘A’ and Module ‘B’ in pass.
Types of Integration Testing:
 1.  Incremental Integration Testing:
        Incrementally adding the module and & testing the data flow between the modules is called as Incremental
        Integration Testing.

         1. a) Top-Down Incremental Integration Testing:
                  Incrementally adding the modules & test the data flow between the modules from parent module to
                  child module is called as Top-Down Incremental Integration Testing.

         1. b) Bottom-Up Incremental Integration Testing:
                  Incrementally adding the modules & test the data flow between the modules from child module to
                  parent module is called as Bottom-Up Incremental Integration Testing .

         1. c) Sandwich (Hybrid):
                  A combination of both top-down and bottom-up approaches, testing the middle layers of the system. 
     
        Note: When We don’t know  or when it is difficult to identify parent & child module we go for Non-
                   Incremental Integration Testing.

     When data flow is very complex don’t spend time in verifying parent & child module we go for Non-Incremental Integration Testing.

 2. Non-Incremental Integration Testing / Big Bang Method:
       It is an integration Testing approach in which all the modules are integrated together at once and then tested as a unit.


System Testing:
  System testing is a level of testing that validates the complete and fully integrated software. The purpose of a system testing is to evaluate the end-to-end system specification. Here end-to-end means navigate through all the feature and check whether end feature or last feature is working as expected or not is called end to end testing.
   
   When we do system testing?
•	When all basic feature and functionally stable.
•	Minimum bunch of feature should be ready.
•	Environment similar to production environment must be available.

SYSTEM INTEGRATION TESTING:
•	Verifying the data flow between two or more system or application is called as system integration testing.
•	Example: In flipkart if we are click on forget password then we get mail to change the password so there is a data flow between the modules but in the different application.
•	If we login to any application then we get otp and using that we have to login the application.






Acceptance Testing:
   Approach 1:
     It is the end to end testing done by IT Engineers sitting in customer place wherein they consider end
     to end real time business scenarios & check whether the software is capable of handling it or not.
       
     

Approach 2: User Acceptance Testing
It is an end to end testing done by end users where in they use the software for the business for a particular period of time and check whether software is capable of handling real-time business scenarios.
  





Approach 3:
It’s End to End testing done by our own Test engineers sitting in customer place wherein they refer user
scenario given by customer and check whether software is capable of handling real time business scenarios.
   

Approach 4:
It’s end to end testing done by our own Test engineers sitting in own place wherein they refer user scenario given by customer & check whether s/s is cable of handling real time business scenarios.
   

Types of Acceptance Testing:
  1) α Testing (Alpha)
  2) ß Testing (Beta)
Note: Both Testing done in product based companies.

What is Alpha & Beta Testing?
•	Alpha Testing:
                 Test Engineer will do alpha testing before they would move product for Acceptance Testing.

•	Beta Testing:
                  End user will do beta testing, based on their feedback, product will be released.

Why we do Beta release?
•	They will get thousands of free users to test the application.
•	Users will use it in variety of platforms & variety of different ways & catch defects which Test engineer cannot easily simulate within the testing team.


Smoke Testing:
Alternatives Names: Skim Testing, Positive Testing, Confident Testing, Health check of product, Build verification 
                                                                                                                                                                                              testing    
   Testing the Basic and Critical Feature of an application before doing through is called as Smoke
Testing.

How to do Smoke Testing?
    Here list the features to be tested as part of smoke testing and list the feature are not to be tested as part of smoke testing.

When We do Smoke Testing?
1.	Whenever we get a new build from Development Team We always start with smoke testing because adding, Modifying, removing the features or fixing the bug might have impact on basic and critical features so to find that in the beginning itself we do smoke testing.
2.	One who install product in the production server to confirm that product is installed properly he will do smoke testing.
3.	Before customer does acceptance testing he should start with smoke testing to check whether he has received product properly or not and also to check whether product is properly installed and configured or not.
4.	Developers will do smoke testing after doing WBT and before giving build to testing team.


Why we do smoke testing?
1. To check whether the product is testable or not- It means in the beginning itself we find too many
    defect then product is not testable so better stop testing and spend time in identifying some more 
     scenarios.
2. We do smoke testing in the beginning itself, if you find blocker defect communicate to developers in the
     beginning  only so that developers will get sufficient time to fix the defect.
3. We do this to check whether the product is installed properly or not.
4. To check whether we have received broken build from the development team we do smoke
     testing.
5. It is like health check of the product so we do smoke testing.


Types of smoke Testing:
    1) Formal Smoke Testing.
    2) Informal Smoke Testing.

  Formal Smoke Testing:
      The development team sends the software to the test lead. The test lead then instructs the testing team to
   do smoke testing and send report after smoke testing. Once, the testing team is done with smoke testing, they
   send the smoke testing report to the test lead.
 

 
  Informal Smoke Testing:
      Here, the test lead says product is ready and to start testing. He does not specify to do smoke testing. But, 
   still the testing team start testing the product by doing smoke testing. 

Note: Smoke testing can be done both manually and also with the help of automation tools. But the best and preferred way is to use automation tool to save time.


Sanity Testing:
•	It is a type of testing done after getting a build with minor changes in code or functionality.
•	It is usually not documented and unscripted.
•	Exercise only particular component of entire system.


Regression Testing:
       Regression Testing is a type of testing that is done to verify that a code change in the software does not impact the existing functionality of the application.
                                            (or)
       Testing the unchanged/old features to make sure that changes like adding new feature, deleting features, modifying features and fixing defects are not introduced defects in the unchanged/old features is called Regression testing.
                                         (or)
        Re-execution of test cases in the different release or builds or test cycles to make sure that a code changed in the software doesn’t impact the existing functionality of the application.


Types of Regression Testing:
1.	Unit Regression Testing
2.	Regional Regression Testing
3.	Full Regression Testing

1. Unit Regression Testing:
       Testing only that changes or modification which is done or the bug which is fixed is called as unit regression
   testing.
2. Regional Regression Testing:
      Testing the changes and impacted (affected) area is called as Regional Regression Testing.

   How did you identify impacted areas?
1.	Customer when he gives requirement he will only inform developers and TE’s about the
impacted areas.
2.	BA when he converts CRS to SRS in the SRS there will be section called impacted areas there BA will mention the list of impacted areas.
3.	Developers will give the information about impacted areas because he s a person one who is doing code which all areas code has been modified.
4.	Test engineer will interact with Test Lead, Test Manager,  senior Test Engineer, BA based on their product knowledge they will give list of impacted areas.
5.	Test Engineer will conduct impact analysis meetings.


3. Full Regression Testing:	
      Testing the changes and all remaining features of an application is called as full regression testing.


When to do full regression testing?
1. When changes are more don’t spend in doing impact analysis, test the entire project by
doing full regression testing.
2. When changes are done in the root of the product then test the entire project by doing full
regression testing.
3. Before launching the software to the customer.



Adhoc Testing/Negative Testing /Out of box testing / Monkey Testing / Gorilla Testing:
   Testing the software or application randomly is called as adhoc testing wherein we don’t refer any
kind of formal documents like testcase or scenarios.

Why We do Adhoc Testing
1. Chances are there when they product is launched end-users might use the application randomly
and find the defect to avoid that test engineer should only test the application randomly.
2. If you see the requirement and test the application number of defects that you are going to catch
will be less so think out of the requirement in order to catch more defects.
3. We do adhoc Testing to increase the defect count.
4. Since end-user will not look in to the requirement so Test Engineer should do adhoc testing.
5. We do this to improve test coverage.
6. We do this to some how break the product


When We do Adhoc Testing
1. While doing smoke testing we should not do adhoc testing because smoke testing is pure
positive and adhoc is negative.
2. While doing Functional Testing/ Integration Testing/ System Testing  either in between or at the end if you have some time we can do adhoc testing if time is not there document the adhoc scenarios and communicate to Test Lead.
3. Once after software is tested as per the requirement then we can do adhoc testing.
4. Once after Software is tested for 10-15 cycles as per the requirement and if it is stable then we can
do adhoc testing.
5. While doing Functional Testing/ Integration Testing/ System Testing  if you come up with good and creative adhoc scenarios stop doing Functional Testing/ Integration Testing/ System Testing  and test for adhoc scenario and don’t spend too much of time in doing adhoc testing immediately switch back to Functional Testing/ Integration Testing/ System Testing .

Why We should not do adhoc testing in early stage itselt?
1. As a Test Engineer first we should check whether the software testable or not so we should not do adhoc testing.
2. Since customer always use software in the positive way first so we should do positive testing not
adhoc testing.
3. In the Beginning only if you spend more time in doing adhoc testing, at the end you might not
get sufficient time to do positive testing.

Types of Adhoc Testing:
1. Buddy Testing:
Here Test engineer will sit with developer and come up with creative scenario and test the software.
2. Pair Testing:
Here Test engineer will sit with another test engineer and come up with creative scenarios and test the software.
3. Monkey Testing: Test engineer will test the software without applying any kind of login.


Exploratory Testing:
        Explore the application understand each and every feature based on understanding identify all possible scenarios and document it, refer the document and text the application.

When do we do Exploratory Testing?
•	When there is no requirement.
•	When they don’t understand requirement.
•	When there is no sufficient time then we go for exploratory testing.

 Below are some tips/ Tricks (Exploratory Testing):
•	Divide the application into modules and divide the modules into different pages. Start your exploratory testing from the pages. This will give the right coverage. 
•	Make a checklist of all the feature & put a check mark when it is covered.
•	Start with basic scenarios and then gradually enhance it to add more features to test it.
•	Test all the input fields.
•	Test for all the error messages.
•	Test all the negative scenarios.


Usability Testing /Yellow Box Testing/GUI (Graphical User Interface)/Cosmetic Testing:
•	Testing the user-friendliness of the application or software is called as Usability Testing. 
•	No special training is required in order to use the application 
•	The number of clicks (clicking actions) performed on an application should be less.

  How to do Usability Testing?
•	I will check whether look & feel of the application is good or not.
•	I will check whether application is simple to understand or not, i.e., i will check is taking less time to understand or not.
•	Important feature or frequently used feature must be given to user within 3 clicks.
•	Important feature or frequently used feature must be easily accessible. 
                Ex: Frequently used feature should be present either at left navigation bar or top navigation bar.
•	To do any simple activity in the application it should take less number of actions.





 For What kind of Application we do Usability Testing?
•	Those Application Used by Multiple Users of n number of Users We need to do Usability Testing.
•	Those applications which generates lot of revenue we have to do Usability Testing. 
•	Those applications which are used by the multiple users without providing training to end-users how to use the application, i.e., we can expect themselves to learn about the application. 


Performance Testing:
        Verifying the stability & response time of an application by applying load is called as performance testing.
           1. STABILITY: Ability of an application to respond to the users (efficiency)
           2. RESPONSE TIME: Over all time taken by the application to respond to the user. 
 
              RESPONSE TIME = T1 + T2 + T3 
        
3. LOAD: Number of users using the application at a time.
    NOTE: On single user applications performance testing can be done manually and on multiuser application performance testing is done using automation tools
TOOLS USED IN PERFORMANCE TESTING
•	J METER (JAVA METER)
•	LOAD RUNNER
•	NEO LOAD
•	SILK PERFORMER 
   ( All the above tools are licensed)
    NOTE: On multiuser application mandatory to perform performance testing. when the application is stable on base platform the performance testing can be done.









How to do performance testing using load runner tool?
  Requirement: 100000 users should use the application at the same time and response time should be within 2 seconds.
     

•	When 80 k users used the application the stability & response time was stable in the application
•	After 80 k users the response time increased where the stability is not the same hence we raise it as a defect to the developer
According to the requirement expected result should be as following:
 






TYPES OF PERFORMANCE TESTING:
         1. LOAD TESTING: Verifying the stability and response time of an application by applying less number of
                                           load and equal number of loads.
                      Example: No. of users = 1,00,000 (Requirements)
                                       Less load à 9,95,000 à within 2 seconds
                                       Equal load à 1,00,000 à within 2 seconds

          2. STRESS TESTING: Verifying the stability and response time of an application by applying more number of
                                                load than the designed user.
                        Example: No. of users = 1,00,000 (Requirements)
                                          No. of users à 1,00,100 à Response time can increase but the application should 
                                                                                                 continue working.
                                          No. of users à 2,00,000 à Application should not crash but instead throw an error
                                                                                            message. 
Note:
   In stress testing testers verify three conditions
•	If the application is still working
•	If the application has crashed
•	Is it displaying error message accordingly, if any of these conditions are missing then raise it as a defect.

  3. VOLUME TESTING:  Verifying the stability & response time of an application by transferring huge volume of data from place to another place
 
Example:
        Customer requirement:
            EVERY 24TH HOUR DATA TRANSFER SHOULD HAPPEN TO BACKUP SERVER WHERE MAXIMUM DATA IS 1 TB OR LESS THAN & TIME SHOULD BE WITHIN 1 MINUTE.
•	1 MB DATA = 2 MINUTES à DEFECT
•	1 MB DATA = 10 SECONDS à [PASS]
•	1 GB DATA = 45 SECONDS à [PASS]
•	1 TB DATA = 1.5 MINUTES à DEFECT

    4. SOAK TESTING:
              Verifying the stability & response time of an application for continuous period of time by applying load.
 
 


Compatibility Testing / Configuration Testing / Portability Testing:
        Testing the functionality of an application in different software and hardware environment is called compatibility testing.

Why we do compatibility testing?
•	To check whether software works consistently in all the platforms
•	Usually, developing team and testing team use the same platform while developing the software, but once after the application is released in the production server the customer may use our product in different platforms and they may find bugs in the application and hence we do compatibility testing.


When do we perform compatibility testing?
•	When the application is relatively stable on the base platform we perform compatibility testing


How to do compatibility testing?
      Here we will execute manual test cases as automation scripts in different platforms and do compatibility testing.
 

Work Allocation In Compatibility Testing:
 



How to setup the environment for compatibility testing:
    Compatibility testing defects:
•	Scattered content
•	Alignment issues
•	Broken frames
•	Change in look and feel of the application
•	Object overlapping
•	Change in font size, style, color.


      Types of software compatibility testing
•	Browser compatibility testing
•	Hardware compatibility testing
•	Network compatibility testing
•	Mobile devices compatibility testing
•	Operating system compatibility testing


       HARDWARE: 
              It is to test the application/ software compatibility with the different hardware configurations.
•	Test on different processors
•	Test on different ram
•	Test on different motherboard
•	Test on different vga card


         NETWORK:
             It is to check the application in a different network like 3g,4g,5g wifi, etc.



        MOBILE DEVICES:
It is to check if the application is compatible with mobile devices and their platform like android, ios, windows, etc

        OPERATING SYSTEM:
it is to check if the application is compatible with different operating system like window,linux,mac,etc



Accessibility Testing:
•	Verifying if the applications functionality is accessible or usable for physically challenged users or disabled user is called as accessibility testing
•	Verifying if the application is the same for physically challenged users or disabled users is called accessibility testing.
•	It is also called as ADT (American disability testing) testing introduced in 1990 and also called as 508 act testing

 How to do accessibility testing?
     We normal testers cannot perform accessibility testing hence we rely on automation tools.
    Some Of The Tools Are:
•	WAVE WEB ACCESSIBILTY
•	ACHECKER
•	AVIEWER
•	INFOCUS




Example:
•	The condition which is verified in accessibility testing are speech recognization- google map etc
•	Magnification such as zoom in, zoom out
•	Color, font, style of the application gui (graphical user interface ) standard
•	Voice recognition
•	Reading recognition
•	Subtitles

  REAL TIME APPLICATIONS:
•	Google maps provides both voice recognition and seeing the navigation
•	Subtitles in application

NOTE:
•	Used specifically for web application and web based application.
•	It is mandatory for multi user application and it is done when the application is relatively stable.





Reliability Testing:
        Verify the functionality of the application for a continuous period of time is called as reliability testing
Why to do reliability testing?
•	Checking if the application is failing at any point
•	To identify why it is failing
•	How many times it is failing


How to do reliability testing?
     We use automation tools where the testers write the specific scripts for the tool to check the application if it is failing at any point of time.
  
   SOME OF THE TOOLS ARE
•	WEIBULL++ à Reliability Data Analysis
•	RGA à Reliability Growth Analysis
•	RCM à Reliability Centered Maintenance 

When to do reliability testing?
•	When the application is stable we perform reliability testing.
•	Some of the real time examples are
•	Social media application: facebook, instagram, whatsapp,etc
•	Gaming application : pubg, temple run, etc
•	Media entertainment : hotstar , reflex etc
•	Educational domain : byju’s

Note: 
      It is not a mandatory testing and is done based on the customer domain and the type of application 


Recovery Testing:
•	Verifying how fast the application recovers back from a crash/ disaster/ failure back to the normal stage is called as recovery testing.
•	Only trained testers perform recovery testing since they know how to crash the application and also to recover back to the normal stage
      Example for Recovery:
•	Trying to downloading a song through wi-fi of 3 mb download has happened for 1.8 mb then wi-fi off due to power off, after some time power was back, wi-fi got connected, it should start downloading from 1.8 mb onwards
•	If a laptop is closed or drained out of battery while an application is in running, once we switch it on again it should display the same application from where it got crashed.
          restore all 				open a new tab
•	These are called error log message , crash message, log message

How to do Recovery testing?
•	Trained testers create a crash or disaster by in building forced defects & checking if the application is failing.
•	We verify log message or errors log message with instruction it displayed (if not displayed rise it as a defect)
•	Testers end the process or kill the process which has caused the disaster
•	We will verify after killing the process (end now) if the application is recovering back to the previous setting without any data loss.


Globalization Testing:
•	Developing the software to support multiple languages is called globalization testing.
                                                    (or)
•	Testing the software which is developed to supports multiple languages is called globalization testing.

There are two types Globalization testing:
1. Internationalization testing (i18n testing)
2. Localization testing (l10n testing)



Internationalization testing (i18n testing):
•	Here we check whether the content is displayed in right language or not.
•	Here we also check the content is displayed in right position or not.
•	We add prefix to the property file in order to check the content is displayed in right language.
•	We add suffix to the property file in order to check the content is displayed in right position or not.
•	Adding prefix &suffix to the property file is called pseudo translation

  Localization testing (l10n testing):
•	Here  we check whether the content is changing locally according to country standards or not
         Example: currency format, date format, time format, phone number format, pin code format



Security testing / Vulnerability Testing:
  Security testing is a type of software testing aimed at identifying and fixing vulnerabilities in a system or application to ensure that it is protected from external threats, unauthorized access, data breaches, and other potential security risks. The primary goal is to verify that the system's data and resources are protected from various security attacks and unauthorized use.
 
 Types of Security Testing:
•	Vulnerability Scanning
•	Penetration Testing (Pen Test)
•	Risk Assessment
•	Security Auditing
•	Authentication Testing
•	Authorization Testing
•	Session Management Testing
