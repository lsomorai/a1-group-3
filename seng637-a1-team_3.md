>   **SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 3      |
|-----------------|
| Warisa Khaophong                |   
| Lucien Somorai              |   
| Cory Wu               |   
| Rick Zhang                |   

[Link to the Defect Reports](document/group_3_PDF_bug_report.pdf)

# Table of Contents

[1. Introduction](#introduction)

[2. High-level description of the exploratory testing plan](#high-level-description-of-the-exploratory-testing-plan)

[3. Comparison of exploratory and manual functional testing](#comparison-of-exploratory-and-manual-functional-testing)

[4. Notes and discussion of the peer reviews of defect reports](#notes-and-discussion-of-the-peer-reviews-of-defect-reports)

[5. How the pair testing was managed and team work/effort was divided](#how-the-pair-testing-was-managed-and-team-workeffort-was-divided)

[6. Difficulties encountered, challenges overcome, and lessons learned](#difficulties-encountered-challenges-overcome-and-lessons-learned)

[7. Comments/feedback on the lab and lab document itself](#commentsfeedback-on-the-lab-and-lab-document-itself)

# Introduction
In this assignment, our group carried out several key tasks to gain hands-on experience with both the testing process and professional bug-tracking tools. Our activities included:
- Practiced pair testing
- Conducted exploratory testing on the provided ATM simulation system versions 1.0 and 1.1
- Created effective defect reports
- Tracked defects in JIRA
- Executed manual test cases from a formal test suite
- Performed regression testing to verify bug fixes

Before this assignment, our group had prior experience testing various school projects, most of which involved a combination of exploratory and manual functional testing. However, we now realize that our previous testing efforts lacked the structure of professional testing processes. In particular, we had never used a bug-tracking system like JIRA, nor had we written detailed bug reports that adhered to industry standards. This assignment has provided us with valuable insights into these professional practices, giving us the skills and experience needed to handle real-world testing scenarios.

# High-level description of the exploratory testing plan

## Test Types
1. Functional Testing
   - Core transactions (withdrawals, deposits, transfers, inquiries)
   - Receipt generation
   - Card handling
   - Envelope handling
   - Cash handling

2. Security Testing
   - PIN validation
   - Card retention rules
   - Transaction limits

3. Error Handling Testing
   - Invalid inputs
   - Insufficient funds
   - Transaction cancellation

## Scope of Testing

### In Scope
1. Main Functions:
   - Withdrawals (checking, savings)
   - Deposits (envelope handling, amount verification)
   - Transfers between accounts
   - Balance inquiries
   - Receipt generation

2. Error Scenarios:
   - Invalid PIN handling
   - Insufficient funds management
   - Negative amount inputs
   - Card detention cases
   - Transaction limits

3. Special Features:
   - Money Market Account inquiry
   - Multiple transactions
   - System startup/shutdown

### Out of Scope
- Backend system
- Hardware component testing
- Network communication testing
- Database persistence

## Test Logistics

### Pair 1 (Warisa and Lucien):
Primary focus:
- Withdrawal operations
- Deposit functionality
- Receipt verification
- System startup/shutdown

### Pair 2 (Cory and Rick):
Primary focus:
- Transfer operations
- Balance inquiries
- PIN validation
- Error handling scenarios

### Shared Responsibilities:
- Both pairs documented findings in JIRA
- Cross-verification of critical bugs
- Regular sync-ups to avoid duplicate testing
- Combined review of test results

# Comparison of exploratory and manual functional testing
We found that exploratory testing is highly efficient, particularly at the beginning of the testing process, as it allows testers to quickly dive into the system without predefined scripts and test cases. This method works well for uncovering major defects that prevent the system from functioning properly, such as crashes, system freezes, or critical errors that affect user interaction. Its unstructured nature gives testers the freedom to approach the system from various angles, enabling us to identify high-impact issues early on.<br>
<br>
However, one of the main challenges we faced during exploratory testing was the difficulty in tracking and documenting more detailed defects. Since exploratory testing lacks the structured format that test cases provide, it became harder to consistently record the exact steps, expected results, and other relevant details for each defect. This resulted in some defects being difficult to reproduce, making it hard to communicate the issues within our team.
<br>
<br>
In contrast, manual functional testing provided a more systematic approach to defect identification. By using predefined test cases that cover specific functionalities, this approach allowed us to identify defects that exploratory testing might have missed. The structure of the test cases ensured that we were testing the system in a consistent and comprehensive way, with clearly defined inputs, actions, and expected outcomes.
<br>
<br>
Although manual functional testing was more thorough, it revealed only one additional defect compared to exploratory testing. This defect was related to the handling of invalid PIN entries, which had been overlooked during exploratory testing. Specifically, the test cases for “first-time incorrect PIN input” and “second-time incorrect PIN input” provided more detailed coverage for this scenario, ensuring that edge cases like multiple incorrect PIN attempts were properly tested. These test cases were essential in revealing that the system was not handling invalid PIN inputs as expected, something that might have been missed in the exploratory testing process.


[Link to the Defect Reports](document/group_3_PDF_bug_report.pdf)

# Notes and discussion of the peer reviews of defect reports
Discussion 1:
  - Defect: S6G-13 ET: Misspelling of the word "would"
  - Question: Should misspellings be considered as defects?
  - Conclusion: Yes, as a misspelling could confuse customers.

Discussion 2:
  - Defect: S6G-7 ET: $10 is deducted from each deposit
  - Question: Is the system designed to deduct a $10 fee from each deposit?
  - Conclusion: No, this behavior is not mentioned in the requirements.

Discussion 3:
  - Defect: S6G-16 MFT: $0.10 is deducted from each deposit
  - Question: The deduction in S6G-7 changed from $10 to $0.10. Should we update S6G-7 or create a new defect?
  - Conclusion: Create a new defect and mark S6G-7 as resolved.

Notes:
- Appendix C Test Case 6, 22 triggered a defect but it's already found during exploratory testing.
- Appendix C Test Case 11, 37, 39, 40 could not be executed because the system does not allow transactions after an incorrect PIN attempt.

# How the pair testing was managed and team work/effort was divided

Our group consisted of four members, so we split into two pairs: <br>
- Pair 1: Warisa and Lucien <br>
- Pair 2: Cory and Rick <br>

To begin with, we engaged in exploratory testing. During this phase, both pairs worked independently for approximately 30 minutes, thoroughly exploring the system’s functionality and behavior. This allowed each pair to develop a perspective on how the system behaved under various conditions. After this testing session, the pairs reconvened and compared their findings. We identified a total of 12 defects during this review, 10 of which were common across both pairs. This reinforced the validity of our observations and gave us a clearer understanding of the defects that required attention. <br>  

During manual functional testing, we divided the test cases: <br>
- Pair 1: Test cases 1-20 
- Pair 2: Test cases 21-40. 

Each pair was responsible for executing their assigned test cases while documenting the results carefully. This division of work allowed us to test a wide range of functionalities without duplicating efforts. During this phase, we identified two additional defects that were missed during exploratory testing, further refining our understanding of the system’s defects. <br>

# Difficulties encountered, challenges overcome, and lessons learned
During the course of the assignment, one of the primary difficulties we encountered was keeping track of the steps to reproduce defects. In the early stages, we faced challenges in documenting and retracing the exact conditions under which the defects occurred. This led to some confusion and delays in identifying the root causes. However, we learned the importance of maintaining clear, detailed, and consistent logs of test cases and defects. We implemented a systematic approach to record not only the defect but also the specific state and sequence of actions that triggered it. This practice significantly improved our ability to track and reproduce issues efficiently.<br>
  
Another challenge we faced was a lack of familiarity with JIRA, particularly in its initial setup and usage for managing tasks and bugs. At first, we struggled with navigating its interface and understanding how to organize issues effectively. This led to some inefficiency in task assignment and progress tracking. Over time, we overcame this challenge by dedicating time to learning the tool’s functionalities, seeking help from online resources, and exploring best practices for creating, updating, and categorizing issues. As a result, our workflow became much more streamlined, and we were able to use JIRA to its full potential for this assignment.

# Comments/feedback on the lab and lab document itself
The overall assignment was well-designed. It provided a structured approach to testing and gave us the opportunity to apply what we’ve learned in a real-world context. As a result, we now feel much more confident and capable when it comes to the testing process, especially in using tools like JIRA for task management and bug tracking. The hands-on nature of the assignment allowed us to see the importance of thorough documentation and organization in software testing, which we will carry forward into future projects and assignments. <br>

However, while using JIRA, we encountered a bit of uncertainty regarding the best practices for structuring the information within the issues. Specifically, we were unsure whether it was better to include details like functions being tested, steps to reproduce, and expected results in the description field of the ticket, or if it would be more effective to create separate fields for each of these elements. This confusion led to some inconsistency in how we documented our tests initially. We would appreciate further clarification on how to organize this information in a way that would best serve the testing processes.<br>

The assignment description itself was clear, well-structured, and easy to follow. It provided a solid overview of what was expected from the assignment and detailed instructions that helped guide us step by step. We appreciated how the lab was designed to progressively build our understanding of the testing workflow.

