>   **SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group 8      |
|-----------------|
| Jeff Wheeler                |   
| Ryan Baker             |   


**Table of Contents**

[1 Introduction](#introduction)

[2 High-Level Testing Plan](<#high-level-testing-plan>)

[3 Comparison of exploratory and manual functional testing](#comparison-of-exploratory-and-manual-functional-testing)

[4 Notes and discussion of the peer reviews of defect reports](#notes-and-discussion-of-the-peer-reviews-of-defect-reports)

[5 Difficulties encountered, challenges overcome, and lessons learned](#difficulties-encountered-challenges-overcome-and-lessons-learned)

[6 Comments/feedback on the lab and lab document itself](#commentsfeedback-on-the-lab-and-lab-document-itself)

# Introduction

In this lab, our group will be conducting software testing on an ATM simulation system using exploratory, manual function, and regression testing methods. Azure DevOps was the issue tracking system used to create and update bug work items and to generate the final defect report after the testing was completed. Prior to this lab, both group members had some experience with exploratory testing for checking high-level software requirements.

# High-Level Testing Plan

## Test Types

To test the system under test (SUT), three types of testing will be used:
 - Exploratory testing
 - Manual Function testing
 - Regression testing

Each of these test types, provide a slightly different approach to detecting defects in the SUT. Exploratory testing will address the requirement given in appendix B at a high-level. Manual function testing will be completed using the test suite in appendix C and is a methodical approach to testing the software. Regression testing will be performed on updated version 1.1, to verify whether identified bugs have been resolved and to find if any new bugs have been created.

## Testing Scope

For exploratory testing, the requirements from the table below will be tested. These high level requirements are defined in appendix B, of the assignment 1 readme file.

| High level requirements                                           | User    |
|------------------------------------------------------------------|---------|
| Make cash withdrawal from any account, in multiples of 20        | Customer|
| Deposit to any account                                            | Customer|
| Transfer money between accounts linked to card                   | Customer|
| Abort transaction in process by pressing cancel instead of responding | Customer|
| Communicate transactions to bank and get bank verification        | ATM     |
| For deposits, send confirmation to bank that envelope has been deposited | ATM     |
| If pin is invalid after 3 attempts, card is retained by machine and account is locked | ATM     |
| Display reasons for any failed transactions, prompt for another transaction | ATM     |
| Provide receipt for successful transactions                       | ATM     |
| Key-operated switch that allows operator to start and stop machine| ATM     |
| When turned on prompts for total cash in machine                  | ATM     |
| Logs transactions internally starting when ATM is started up. Never contains pin number. | ATM     |

Each of these requirements will be tested from the inital state of the ATM being turned on and idle. During the process of testing each requirement, any defects that are found will be reported using Azure DevOps bug reporting feature. Each of the reported bugs will include the following details:
 - Testing Type
 - Function
 - Software Version
 - Severity of bug
 - Initial system state
 - Steps to reproduce defect
 - Expected outcome and actual outcome

Manual function testing (MFT) will be conducted after the exploratory testing phase is complete. The test suite from appendix C will be used. New bugs will be tracked in the system, making note that the bug is found using  MFT. Any bugs that had already been tracking in the exploratory phase will not be duplicated, but a note will be added that the bug was also found using MFT. The reported bugs will contain the same details as in the exploratory testing phase.

Regression testing will be the final step in the testing process. Using version 1.1, each of the identified bugs from the exploratory testing and MFT will be re-run. If the bug has been corrected, then the bug status will be changed to 'Resolved'. If the bug still exists, then the bug status will be changed to 'Active' and V1.1 will be appended to the software version. Once this is done, the testing will be redone on the remaining test cases from the test suite in appendix C to identify any new bugs and will be reported with the same details as the previous bugs.

## Testing Logistics

### Initial Program Exploration
To familiarize ourselves with the program as a whole, each student individually followed steps 1-12 in the 'Familiarization with the ATM System' subsection of the 'Instructions' section.

### Pair Programming
For each of the high level functions listed above, one student attempted to complete the high level function as described, and the other student made notes of any bugs that were encountered, paying careful attention to details like display, log, and state information.

### Manual Function Testing
 To conduct the manual function testing, each student was assigned 20 tests from the test suite in appendix C to drive the testing, while the other student kept track of the preformed tests and created reports for any bugs found. The execution order of the tests was done in order of the test cases 1 - 40.

### Regression Testing
 For the last phase of testing, each student ran version 1.1 of the SUT and the existing bug reports were split between the students to review and update. When redoing the manual function testing, each student conducted 20 tests. The first student did test cases 1-20, and the other student did test cases 21-40. New bugs were reported by the student that found them.

# Comparison of exploratory and manual functional testing

As a team, we found 12 bugs in the ATM software. 5 of them were found in using exploratory testing, and the remainder were found using manual function testing. Most of the bugs found in the exploratory testing were also found when doing manual function testing.

Both methods were useful in identifying defects in the software. Manual function testing was more time consuming but was valuable in detecting additional bugs that were missed in the exploratory phase. For our group, the manual function testing was the most effective approach. Exploratory testing still is a worthwhile method to use, as it can find bugs that may not arise when strictly sticting to a test suite that focuses on function requirements. The table below outlines some of the differences between the testing types.

### Comparison Table
|          | Exploratory Testing                                  | Manual Functional Testing                                  |
|-----------------|------------------------------------------------------|------------------------------------------------|
| **Benefits**    | Discover hidden bugs, quick feedback | Consistent test coverage, easy to document |
| **Tradeoffs**   | Less repeatable, harder to track | Time-consuming, may miss unexpected issues |
| **Effectiveness**| Effective for finding complex or unexpected issues | Effective for testing specific requirements |
| **Efficiency**  | Can start testing right away, faster to find bugs but may miss requirements | Need a detailed test suit before beginning testing, but will capture all requirements |
| **Flexibility** | Highly flexible | Little to no flexibility |
| **Scope**       | Wide or undefined scope, testers can explore different areas of the application | Detailed scope, testing specific features or functions defined in the test suite |

# Notes and discussion of the peer reviews of defect reports

Peer reviews created the following benefits when reviewing the defect reports:
 - Ensured the steps to recreate the bug were clear and reproducable
 - Feedback was used to fix any defect reports that were unclear or had missing details
 - Seeing how each defect report was created led to more consistent report writing
 - Sparked discussion on how to write the defect reports and assisted with group understanding
 - Early reviews of the reports, caught errors that improved the quality of further reports

# Difficulties encountered, challenges overcome, and lessons learned

The group has intially set out to use Jira as the issue tracking system but ran into hurdles when creating the organization and found the bug reports to lack the information we needed to capture. To avoid these issues, we switched to Azure DevOps and found the overall experience better suited to this assignment. In the future, Azure DevOps would be our preferred method for issue tracking.

When creating the first defect reports, we did not have a clear method for how to capture all of the details needed for the reports. The peer review was helpful in identifying initial gaps and setting a standard for the reports going forward. If this was not done, there may have been additional work on the back end to standardize the reports. 

# Comments/feedback on the lab and lab document itself

Overall, the assignment was a good introduction to testing and learning how to use an issue tracking system was valuable. It was clear from the lab how much work can be involved in testing even a simple software progam. The lab document had detailed instructions and expectations for learning goals. It also had a clear marking rubric that assisted in completing the submission documents.
