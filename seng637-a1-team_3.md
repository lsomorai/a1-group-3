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
Our group performed the following tasks in this assignment:
- Practiced pair testing
- Conducted exploratory testing on the provided ATM simulation system version 1.0 and 1.1
- Created effective defect reports
- Tracked defects in JIRA
- Executed manual test cases from a formal test suite
- Performed regression testing to verify bug fixes

Before this assignment, our group had experience of testing several school projects, and we now know what we did was mostly exploratory testing and manual functional testing. We haven't used professional bug tracking system or wrote detailed bug reports before.

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
- Primary focus:
  - Withdrawal operations
  - Deposit functionality
  - Receipt verification
  - System startup/shutdown

### Pair 2 (Cory and Rick):
- Primary focus:
  - Transfer operations
  - Balance inquiries
  - PIN validation
  - Error handling scenarios

### Shared Responsibilities:
- Both pairs will document findings in JIRA
- Cross-verification of critical bugs
- Regular sync-ups to avoid duplicate testing
- Combined review of test results

# Comparison of exploratory and manual functional testing
We found that exploratory testing is more efficient at the beginning of the testing process. It works very well to catch major defects that keep the system from working. However, we had difficulty catching more detailed defects due to lose of tracking.<br>
<br>
On the other hand, manual functional testing is more systematic and can find defects that exploratory testing missed. Compare to exploratory testing, we only found 1 more defect in manual functional testing. That defect belongs to invalid PIN handling. The manual fucntional testing part has "first time input incorrect PIN" and "second time input incorrect PIN" as 2 test cases, which is much more detailed.
<br>


[Link to the Defect Reports](document/group_3_PDF_bug_report.pdf)

# Notes and discussion of the peer reviews of defect reports
Discussion 1:
  - Defect: S6G-13 ET: Misspelling of the word "would"
    - Question: Should misspellings be considered as defects?
    - Conclusion: Yes, a customer would be confused by the misspelling.

Discussion 2:
  - Defect: S6G-7 ET: $10 will be deducted from each deposit
    - Question: Is the system designed to deduct $10 fee from each deposit?
    - Conclusion: No, it's not mentioned in the requirement.

Discussion 3:
  - Defect: S6G-16 MFT: $0.10 will be deducted from each deposit
    - Question: The deduction in S6G-7 changed from $10 to $0.10. Should we update S6G-7 or create a new defect?
    - Conclusion: Create a new defect and mark S6G-7 as done.

Notes:
- Appendix C Test Case 22 triggered a defect but it's already found during exploratory testing.
- Appendix C Test Case 11, 37, 39, 40 can not be performed because the system does not allow attempt transaction after inputing incorrect PIN.

# How the pair testing was managed and team work/effort was divided

Our group have 4 members, so we first split into 2 pairs. <br>
Pair 1: Warisa and Lucien <br>
Pair 2: Cory and Rick <br>

During exploratory testing, Pair 1 and Pair 2 both spent about 30 minutes to test the system in their own way. Then we had a discussion to compare the results. We found 12 defects in this step. 10 were noticed by both pairs. <br>  

During manual functional testing, Pair 1 took care of test cases 1-20 and Pair 2 took care of test cases 21-40. We found 2 more defects in this step. We had many discussions about how to properly record the defects and defect classification. <br>

# Difficulties encountered, challenges overcome, and lessons learned
- Sometime we lost track of steps to reproduce the defect.
- Initially we didn't know how to properly use JIRA.

# Comments/feedback on the lab and lab document itself
The overall assignment is well designed. We now feel much more confident about the testing process and JIRA usage. <br>
<br>
While using JIRA, we are not sure if we should keep function being tested, steps to reproduce, and expected result all in the description field or creating new fields.<br>
<br>

