>   **SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 3      |
|-----------------|
| Warisa Khaophong                |   
| Lucien Somorai              |   
| Cory Wu               |   
| Rick Zhang                |   

[Link to the Defect Reports](document/group_3_PDF_bug_report.pdf)

**Table of Contents**

(When you finish writing, update the following list using right click, then
"Update Field")

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan	1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing	1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports	1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided	1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned	1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself	1](#_Toc439194683)

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



# How the pair testing was managed and team work/effort was divided

Our group have 4 members, so we first split into 2 pairs. <br>
Pair 1: Warisa and Lucien <br>
Pair 2: Cory and Rick <br>

During exploratory testing, Pair 1 and Pair 2 both spent about 30 minutes to test the system in their own way. Then we had a discussion to compare the results. We found 12 defects in this step. 10 were noticed by both pairs. <br>  

During manual functional testing, Pair 1 took care of test cases 1-20 and Pair 2 took care of test cases 21-40. We found 2 more defects in this step. We had many discussions about how to properly record the defects and defect classification. <br>

# Difficulties encountered, challenges overcome, and lessons learned

Text…

# Comments/feedback on the lab and lab document itself
The overall assignment is well designed. We now feel much more confident about the testing process and JIRA usage. <br>
<br>
While using JIRA, we are not sure if we should keep function being tested, steps to reproduce, and expected result all in the description field or creating new fields.<br>
<br>

