Project:
     A project refers to a temporary endeavor aimed at creating a specific software product or achieving a specific software-related objective within a defined time frame and scope. Projects have a start and end point.

Product:
     A product refers to a fully developed application or system that is released and available to users or customers. It is typically built to solve specific problems or meet specific needs and is often sold or distributed for use in various environments.

What is Software or Application?
An application is a set of programs written by a programmer to simply one’s particular business requirement.
A group of programs makes an application.

What is the software testing?
Testing the functionality of an application according to customer requirements specification is called software testing.

Why we do Software Testing?
•	In order to provide good quality of software to the customer.
•	To identify defects in the software.
•	To gain customer confidence.
•	To avoid extra costs.
•	To avoid risks.

Manual Testing:
      Testing the software or Application repeatedly or again and again manually without any tools in order to find defects in the software according to customer requirement is called as Manual Testing.

    Advantages of Manual Testing:
•	Quality will be good.
•	Programming knowledge is not required.

    Drawbacks of Manual Testing:
•	It takes more time
•	Resource utilization is more.
•	It is a tedious and monotones job.
•	There will be no consistency in testing.

Note: In order to overcome the drawbacks of manual testing, company will go for Automation. Every company when they get new project, first they will do manual testing to make sure that the quality will be good, then only they will go for Automation.


Automation Testing:
     Test Engineer will write program/script by using tools like Selenium/QTP and run the program against the application or software. Tool or program will automatically test the application and gives result as pass/fail this is called as Automation Testing.

   Tools available in the Market/Industry:
1.	Selenium --> [open source tool]
             Thought Works --> Google
         Programs: Java, Python, C#

       2. QTP [Quick Test Professional]
          (Licensed Tool) --> HP (Hawlett Packard)
       3. Silk Functional Test
       4. SAHI
       5. CANOO
       6. Rational Functional Test --> IBM
       7. OATS (Oracle Application Test Suite)
       (The Above tools are computer based)

   Mobile Based:
1.	Appium
2.	Selendroid
3.	Robotium
4.	4.Monkey Talk

   Web Services Testing:
1.	SOAP UI (User Interface)
2.	Postman
3.	Rest API


Functional Testing:
   Testing each and every component thoroughly against the CRS(Customer’s requirement specification) is known as functional testing.
  Note: Components means Text field, button, checkbox, link, radio button, dropdown ,scroll bar etc..
  Example:  Unit Testing, Integration Testing, System Testing, User Acceptance Testing (UAT), Smoke Testing, 
                     Regression Testing, Etc...

Non-Functional Testing:
    Non-Functional Testing focuses on testing aspects of the system that are not related to specific functionality but are crucial to its overall performance, reliability, scalability, usability, and other quality attributes.
   Example: Performance Testing, Security Testing, Usability Testing, Compatibility Testing, Reliability Testing ,
                    Etc…
Formal Testing:
      Formal Testing refers to a structured, methodical approach to testing that follows established processes, standards, and procedures. It is typically planned, documented, and executed in a systematic way.
  
   Example:
     System Testing, Acceptance Testing, Regression Testing, Integration Testing.

Advantages of Formal Testing:
•	High degree of reliability and traceability.
•	Better suited for complex systems and regulated industries.
•	Helps ensure that all requirements are covered and tested.
Disadvantages of Formal Testing:
•	Time-consuming and resource-intensive due to detailed documentation and planning.
•	Less flexible, as it may be harder to adapt quickly to changes.

Informal Testing:
           Informal Testing is a less structured and more ad-hoc approach to testing. It is typically performed without following a rigid process or extensive documentation, focusing more on finding defects in a less formal manner.
   Examples: Exploratory Testing, Ad-hoc Testing, Smoke Testing.

Advantages of Informal Testing:
•	Faster to execute, as there’s no need for detailed planning or documentation.
•	Flexible and adaptable to changes during the development process.
•	Can find issues that formal testing might miss, especially in areas not covered by test scripts.
Disadvantages of Informal Testing:
•	Lack of consistency, as tests may not be repeatable.
•	Limited traceability and coverage, which can lead to missed requirements.
•	Difficult to scale for larger, complex projects.
•	The lack of documentation can make it harder to track issues or results over time.






Types of Environment:
1.	Development Environment:
    It is a setup which is used to build the application, it has hardware, software and network.

2.	Testing Environment:
     It is a setup which is used to test the application, it has hardware, software and network.

3.	Production Environment:
    It is a set up which is used to run the software for the business, it has hardware and network.


What is release or first release or 1 release?
  Starting from gathering the requirements following by developing the software and testing the software for many cycles and deploying the software into the production server is called release.

What is test cycle?
•	It is an effort duration to start and complete the testing.
•	The testing cycle duration can be 1 day or 2 day or 3 day and on.
•	It depends on size of the application, complexity off the application and size of the testing team.

What is Re-spin?
•	Getting more than one build in a test cycle is called re-spin.
•	Generally whenever test engineer found blocker bugs, development team will give re-spin.

What is Patch?
•	It is a set of modified programs.
	It’s a small software which contains new program modified program & deleted programs.
	When We install patch it go and replace with old software.
 Example: Whatsapp Update, Facebook Update. Etc.

What is Build?
  The process of converting source code file into Executable file is called build.
  When you compile all the program we get Binaries and & When We Compress all the
   Binaries we will get build.

    We will get a build below formats:
       .exe
       .jar (java archive)
       .war (Web Application Archive)
       .tar (tap archive)
       .apk (android)
       .ipa (IOS)


Hot fix:
   In production server while using the software, if customer finds any Blocker/Critical defect then customer will immediately communicate defect to the company so that developer will immediately fix the defect and test engineer will immediately test the defect and patch will be given to production server this process is called as hot fix.

RCA(Root Cause Analysis) Technique / Ishikawa Method / Fishbone Technique:
   Once after Hot fix is completed as a team we try to identify the root cause of the defect, document the root cause, keep it in the common folder where everybody can access and present the document to the entire team. This process is called Ishikawa method or cause and effect diagram. Since the solution is given in the form of fish bone. It is also called as Fish bone Technique.

Defect seeding:
   Intensely introduce the defect in the modules and check whether the test engineer is capable to catching/identifying  those defect or not.

Defect Masking:
   One defect is hiding another defect is called defect masking.

Defect Pesticide:
    If Test engineer stop testing the software by looking in the requirement or same test cases we can’t catch or we can’t identify new defect in the software.

Defect Clustering:
      Test Engineer he will find more number of defect in smaller module then the largest module this process is called as defect clustering.


Defect Cascading:
    One defect is introducing another defect is know defect Cascading.

Defect leakage:
     If the defect is identify by customer or end-user during the production stage.

Latent defect:
   If the same defect is identify by end-user or customer after using the software for certain period of time. That is called latent defect. 







Note:
1. Whenever we get a new build we have to test new features first because probability finding defect is more.
2. Next we have to do integration testing b/w new features and old feature.
3. We should retest the defect which is fixed.
4. Test the old Features.

Why do we get old defect in new module?
  1) Changes are there Test Engineer would have missed in the previous cycle & Catching in current cycle.
  2) Chances are there fixing one defect might introduce another
  3) Adding new features may introduce defect in old feature


RTM: (Requirement Traceability Matrix) (or) CRM (Cross Reference Matrix)
   -> It is a documents which ensures that every requirement has at least one test case.
   -> Test cases are written by looking at the requirements and application is tested by executing test cases. If any requirement is missed i.e. test cases are not written for a particular requirement, then that particular feature is not tested which may have some bugs. Just to ensure that all the requirements are converted traceability matrix is written.

      Types of Requirement Traceability Matrix (RTM):
      1. Forward traceability matrix:
              It maps requirements to test cases.

       2. Backward traceability matrix:
              It maps the test case to the requirement.

       3. Bidirectional traceability matrix:
              This combines both forward and backward traceability. It ensures that:
                  Every requirement is covered by test cases (forward traceability).
                  Every test case is linked to a requirement (backward traceability).

         Advantages of Traceability Matrix:
           - Test Coverage will be good.
           - We will get to know which feature should be tested manually and automatically.
           - Whenever the requirement changes we will get the know which are the test cases and automation     
              Scripts needs to be change

          Disadvantages of Traceability Matrix:
-	Complexity in Large Projects
-	Time-Consuming
-	Difficulty in Managing Changes



What are the Characteristics of Good Test Engineer?
     Test Engineer should have test to Break Attitude.
•	Test Engineer Should be Able to See the Products from Customer Point of View, Business Point of View, End User Point of View and Developers Point of View.
•	Test Engineer should have good Knowledge of Domain.
•	Test Engineer should have very Good Knowledge of Technology so that we can come up with Better Shortcuts to do Testing.

Review in Software:
             A review is a process of systematically evaluating a work product (such as code, design, requirements, or documentation) to ensure it meets specified standards, is correct, and is free from defects. Reviews are typically conducted to improve the quality of the software by identifying issues early in the development cycle, ensuring compliance with guidelines, and ensuring that the product aligns with project requirements.

The Importance of a Review:
•	Defect Identification: Catch defects early in the development process.
•	Quality Assurance: Ensure the software meets the desired quality standards.
•	Improvement: Encourage feedback and collaborative improvements.
•	Knowledge Sharing: Spread knowledge and expertise among team members.

Types of Reviews in Software Development:
      There are several types of reviews that are commonly conducted throughout the software development lifecycle:
1.	Code Review:  To evaluate the source code written by a developer, ensuring that it meets coding standards, is 
                           efficient, and is free of bugs.
2.	Peer Review:  A review process where colleagues (peers) evaluate the work of each other (e.g., code, 
                          documentation,  or design).
3.	Walkthrough:  A less formal type of review where the author of the work (like a developer or designer) presents 
                           their work to others, explaining their design or approach.
4.	Inspection: A formal, rigorous review process aimed at identifying defects in the product. This is one of the most 
                     structured types of review.
5.	Static Analysis Review: To use automated tools to analyze the software without executing it, looking for issues 
                                           like bugs, code smells, and violations of coding standards.
6.	Requirement Review: To assess the clarity, correctness, and completeness of the software requirements to ensure that they are aligned with business goals and customer needs.
7.	Test Case Review: To ensure that test cases are effective in validating the requirements and functionality of the 
                                  software.
8.	Design Review: To evaluate the software design to ensure that it meets the requirements and is robust, 
                              Scalable, and maintainable.







Review Objective:
     The review objective refers to the specific goals or purposes that a review process aims to achieve. A review is conducted to assess the quality, correctness, and completeness of a software product or its components (such as code, requirements, test cases, design documents, etc.). The review objective defines what the reviewers are looking to accomplish during the review process.

Key Characteristics of an Review:
1.	Data-Driven: The review is based on measurable facts, such as metrics, test results, or clear criteria.
2.	Unbiased: The reviewer’s personal preferences, opinions, or emotions do not influence the evaluation. The focus is on facts, not interpretations.
3.	Clear Criteria: Established standards, guidelines, or requirements serve as the basis for the review. For example, the code may be evaluated based on adherence to coding standards or performance benchmarks.
4.	Consistency: The same review process and criteria are applied every time, ensuring that reviews are conducted consistently and fairly across different projects or phases.
Examples of Objective Review:
•	Code Review: Reviewing the code against coding standards, performance requirements, or security guidelines without personal biases.
•	Test Case Review: Evaluating test cases based on their ability to cover all requirements, edge cases, and boundary conditions, using clear guidelines.
•	Requirements Review: Assessing the clarity, completeness, and correctness of requirements based on predefined specifications or business goals.
Why is an Objective Review Important?
•	Accuracy: Ensures that the review process is grounded in clear, measurable facts, minimizing misunderstandings or errors caused by subjective interpretation.
•	Fairness: By eliminating personal biases, an objective review fosters a more fair and equitable evaluation process.
•	Improved Quality: Objective reviews help to identify flaws and improvements based on objective data, leading to better quality outcomes in the software development process.
(As a Tester we do following review)
TEST CASE REVIEW PROCESS:
•	Test case review process is an important process to follow in software testing, test case ensures that each and every functionality mentioned in software requirement specification (SRS) is covered
•	Test case should be effective and also follow the scenarios to write test cases. to success and complete of any test cases every test case should be reviewed
•	There are different types of test case review process

   Test case reviews can be done in 3 ways:
1. SELF REVIEW:  It is done by the tester himself who has written the test case. he can verify whether all the requirements are covered or not by looking into SRS/FRD(functional requirement document)
2. PEER REVIEW: It is done by another tester who hasn’t written those test cases but is familiar with the system under test. Also known as maker & checker review.
3. REVIEW BY A SUPERVISOR: It is done by a team lead or manager who is superior to the tester who has written the test cases and has greater knowledge about the requirements and system under test.


WHILE REVIEWING THE REVIEWER CHECKS THE FOLLOWING:
1. TEMPLATE: He checks whether the template is as per decided for the project.
2. HEADER: (a) Check whether all the attributes are captured or not.
                      (b) Check whether all the attributes in the header are fixed or not.
                      (c) Checks whether all the attributes in the header are relevant or not.
3. BODY:  (a) Check whether all possible scenarios are covered or not.
                  (b) Check whether the flow of test case is good or not.
                  (c) Check whether the test case design techniques are applied or not.
                  (d) The test cases should be organized in such a way that it should take less time to execute.
                  (e) Check whether the test case is simple to understand and execute.
                  (f) Check whether proper navigation steps are written or not.
4. Footer: (a) Review Summary: A summary of the review findings, such as issues discovered or 
                         suggestions for improvement.
                   (b) Feedback/Comments: Space for reviewers to leave specific feedback or suggestions.
                   (c) Status: The current status of the test case after review (e.g., Approved, Pending Changes, 
                                       Rejected).
                   (d) Action Items: Any follow-up tasks or actions that need to be taken based on the review 
                                                  findings.
                   (e) Sign-Off: Signatures or approvals from the reviewers or stakeholders to finalize the 
                                           review process.  

POINTS TO REMEMBER/ TIPS WHILE REVIEWING TEST CASES:
•	WHILE REVIEWING TEST CASES, IT IS BETTER TO HAVE A COPY OF SRS / FRD WITH YOU FOR THE REFERENCE
•	IF YOU ARE NOT SURE ABOUT ANY TEST CASES OR EXPECTED RESULT, IT IS BETTER TO DISCUSS WITH THE CLIENT OR YOUR SUPERVISOR BEFORE MAKING ANY DECISION
•	IF POSSIBLE THAN TRY TO EXECUTE TEST CASES ON THE SUT(SYSTEM UNDER TEST) TO HAVE A BETTER UNDERSTANDING OF THE RESULTS AND EXECUTION STEPS
•	IT IS ALWAYS BETTER TO HAVE A FACE TO FACE MEETING WITH THE TESTER TO MAKE HIM UNDERSTAND ALL THE REVIEW FEEDBACK PROPERLY
•	IT IS RECOMMENDED TO FOLLOW VERSION NUMBER IN REVIEW PROCESS


   GUIDELINES TO WRITE BODY OF THE TEST CASES:
•	WE SHOULD START WRITING TEST CASES USING NAVIGATION STEPS
•	WE SHOULD NOT HARDCORE TEST DATA
•	WE SHOULD NOT MERGE MULTIPLE STEPS INTO SINGLE STEP
•	WE SHOULD NOT SPLIT SINGLE STEP INTO MULTIPLE STEPS
•	WE SHOULD NOT ENTER DATA INTO ACTUAL RESULTS & STATUS COLUMN UNTIL TEST EXECUTION IS DONE.






