Test Plan
Test Plan is a document which derives all future testing activities of the project
1. OBJECTIVE
2. SCOPE
3. APPROACH
4. TESTING METHODOLOGIES
5. ASSUMPTION
6. RISKS
7. BACKUP PLAN
8. ROLES & RESPONSIBILITY	
9. TEST ENVIRONMENT
     10. ENTRY & EXIT CRITERIA
     11. SCHEDULE
     12. DEFECT TRACKING
     13. TEST AUTOMATION
     14. DELIVERABLE
     15. TEMPLATES
     16. EFFORT ESTIMATION
 
1. OBJECTIVE: 
        It gives the aim of preparing test plan i.e. why we are preparing this test plan.


2. SCOPE:
      In the planning stage we decide which feature to test and which not to test due to the limited time available for the project.

2.0 Feature to be tested
   -----------------------------
   -----------------------------
2.1 Feature not to be tested
      ---------------------------
      ---------------------------
Features not to be tested:
a) “HELP” is a feature developed and written by another technical writer. So we will not test this feature
b) Third party modules of the application
c) The application might be having link to some other application. Here our scope of testing is limited to 
     -> Check whether link exists.
     -> If it goes to home page of the corresponding application when we click on the links

3. APPROACH:
       The way we go about testing the product in future
   a) by writing high level scenarios
   b) by writing flow graphs


4. Testing methodologies:
       Depending upon the application, we decide what type of testing we do for the various features of the application.


5. Assumption:
      When writing test plan, certain assumption would be made like technology, resources etc.


6. Risks: 
      If the assumptions fail, risks are involved


7. Contingency plan or Mitigation plan or Backup plan:
      To overcome the risk, a contingency plan has to be made. At least to reduce the percentage from 100% to 20%
Always assumption, risks, backup plan are specified to the project.
The different types of risks involved are:
	Resource point of view
	Technical point of view
	Customer point of view


8. Schedule: 
     This section contains when exactly each activity should start and end.

9. Roles and Responsibility:
   9.1 Test manager
•	Writes a review test plan
•	Test manager will interact with customer, management development team and testing team sign off  release note
•	Handle issues and escalation
•	Test manager will be involved in the effect estimation
•	Approve test case (not always)

    9.2 Test Lead
•	Test lead will write or review test plan
•	Test lead will interact with development team, testing team, management and customers.
•	Allocate works to test engineer and ensure that they are completing the work within the schedule.
•	Consolidate reports sent by test engineers of communicate it to development team.
•	Test lead will be involved in review test case
•	Test Lead will be involved in approving test case
•	Test Lead will be involved in testing complex feature
     
   9.3 Test Engineer
•	involved in system study
•	involved in identifying scenarios
•	conducting brainstorming meeting and updating scenarios
•	converting test scenarios into test case
•	involved in reviewing test case
•	giving review comments & fixing the review comments
•	involved in execution of the test case
•	involved in identified the defects & communicate defects to dev team using defect tracking tool
•	involved is tracking the defects
•	involved in selecting test case for regression testing
•	involved in conducting bug triage meeting
•	involved in performing traceability matrix

   9.4 Test Engineer (automation engineer)
•	Setup and install the product
•	Identify test cases to be automated
•	Automate identified test case using automation tool like selenium, UFT, etc.
•	Execute and maintain automation script


10. Defect Tracking:
         In this section we mention how to communicate the defects found during testing to the development team and also how development team should respond to it.
This section contains
     10.1 Procedure to track the defects
     10.2 Severity level
     10.3 Priority level
     10.4 Defect tracking tool to be used


11. Test Environment:
         In this section we mention what are the hardware and software needs to be used in order to setup test environment.
        11.1 Hardware:
                       Server side: Sun starcat 1500
                                   Ram: 8 Gb
                          Hard Disk: 1 Tb
              
        11.2 Software:
             11.2.1 Server:
                                      OS: Linux
                      Web Server: Tomcat
          Application Server: WebSphere
              Database server: Oracle (or) MS-SQL Server
              
                    11.2.2 Client:
                                   OS: Windows7, Windows8, Windows10
                         Browser: Chrome , Firefox

             11.3 Procedure to install the software


12. Entry and Exit Criteria:
      Entry Criteria and Exit Criteria are crucial components of a test plan as they define the conditions under which testing starts and ends. They help ensure that testing activities are performed systematically and that all necessary preconditions are met before testing begins and all required goals are achieved before testing concludes.
  
     12.1 Entry Criteria
        Entry Criteria specify the conditions that must be met before testing can begin. These conditions ensure that the test environment and resources are ready, and that the system is in an appropriate state for testing.
     Common Entry Criteria:
       -> Requirements Specification Available: All necessary documentation (e.g., functional, technical, or user stories) is available and has been reviewed.
       -> Test Plan Approved: The test plan must be reviewed and approved by relevant stakeholders, including the testing team, project managers, and other stakeholders.
       -> Test Environment set up: The test environment (hardware, software, networks, etc.) must be configured and ready for testing. This could include setting up test servers, databases, and network connections.
         -> Test Data Available: The necessary test data should be created, validated, and ready for execution.
Test Case Design Completed: Test cases, scripts, and scenarios should be designed, reviewed, and approved, ensuring that they fully cover the requirements.
         -> Tools and Resources Available: Any tools required for test execution (such as automation tools, performance testing tools, etc.) must be installed and configured.
         -> Team Members Assigned: All testing roles, including testers, test leads, and other relevant personnel, must be assigned and available to begin testing.
         -> Risk Mitigation: Any high-priority risks that could impact testing must have mitigation strategies in place.

      12.2 Exit Criteria
          Exit Criteria define the conditions under which testing is considered complete. These criteria ensure that testing has been sufficiently carried out and that all necessary testing tasks have been performed.

      Common Exit Criteria:
         -> Test Case Execution Completed: All planned test cases have been executed, and their results are documented. This includes both manual and automated test cases.
         -> Defects Resolved: All critical and high-priority defects identified during testing must be resolved, or a documented risk acceptance decision must be made if defects remain open.
        -> Test Coverage Achieved: A predefined level of test coverage (such as requirements coverage, code coverage, or feature coverage) has been achieved.
        -> Test Results Analyzed: Test results should be analyzed, and any anomalies or discrepancies should be documented and communicated. This includes analyzing test metrics and defect trends.
       -> Pass/Fail Criteria Met: The pass/fail criteria defined at the beginning of the test phase have been met (e.g., the number of passed tests is above a specified threshold).
       -> No Major Risks Pending: Any identified risks have been addressed or accepted by the stakeholders. No critical issues should remain unresolved.
       -> Final Test Report Delivered: A comprehensive test summary report should be delivered, including results, defect status, test coverage, and an overall test evaluation.
       -> Compliance with Acceptance Criteria: The system meets the acceptance criteria defined by the business, product owners, or clients.
       -> All Requirements Validated: The system has been validated against the requirements, ensuring that the product is working as intended and that any gaps or deviations have been addressed.
        -> Approval from Stakeholders: The project team or stakeholders (e.g., product owners, managers) must formally approve the completion of testing activities.


13) Test Automation:-
       13.1 Features to be automated.
       13.2 Features not be automated
       13.3 Which is the automation tool you are planning to use.
       13.4 What is the automation framework you are Planning to use
14) Deliverables-
       It is the output from the testing team. It contains what we will deliver to the Customer at the end of the Project. It has the following sections.

     V14.1 Test Plan
     V14.2 Test cases
     V14.3 Test Scripts
     V14.4 Traceability matrix
     V14.5 Defect Report
     V14.6 Test Execution Report
     V14.7 Graphs and Metrics
     V14.8 Release Note

     V14.8 Release Note:
         Release Note is a document Prepared during release of the project and signed by Test manager.

     The release notes contains,
       1) List of Pending / open bugs
       2) List of features added, modified or deleted
       3) Platforms (OS, Browsers, Hardware) in which the Product is tested.
       4) Platform in which the Product is not tested.
       5) List of bugs fixed  in current release which were fond in Previous release production.
       6) Procedure to install the software.
       7) Version of the Software


15) Template:
       This section contains all the templates for the documents which will be used in the Project.

        The various documents which will be covered in the template section are,
            • Test case
            • Traceability Matrix.
            • Test Execution Report.
            • Defect Report.
            • Test Case Review Template.


16) Effort Estimation:
          Effort estimation is the Process of Predicting the most realistic amount of effort (expressed in terms of person-hours or money) required to develop, testing and maintains software.
