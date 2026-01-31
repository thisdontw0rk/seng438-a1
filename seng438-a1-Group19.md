>   **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: Group Number      |
|-----------------|
| Student 1 name  Haseeb Tahir           |   
| Student 2 name  Mustafa Ayobi        |   
| Student 3 name  Shaheer Shakir            |   
| Student 4 name  Moyo Ogunjobi          |   


**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

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

In this lab, our group practiced multiple testing approaches—exploratory testing, manual functional (scripted) testing, and regression testing—using a simulated ATM system across two releases (v1.0 and v1.1). We tracked our findings in **Atlassian Jira**, which helped us experience a realistic defect reporting workflow and forced us to document issues in a reproducible way. Exploratory testing made up most of our early work because it allowed us to freely explore system behavior and try both typical user actions and unusual inputs. We then used the provided scripted test suite to run structured manual functional tests and recorded clear pass/fail outcomes. Finally, we performed regression testing in v1.1 by rechecking issues found in v1.0 to determine whether they were fixed or still present. Before this lab, we understood the basic definitions of these testing styles, but we did not have much hands-on experience applying them in a coordinated team workflow or documenting defects at an industry level of detail.

# High-level description of the exploratory testing plan

Our exploratory testing plan was based on the high-level requirements and the core user-facing functionality of the ATM. The goal was to gain broad coverage quickly while still leaving room to dig deeper into areas that seemed more failure-prone. We started by confirming the system could be powered on, initialized, and used to log in with valid credentials. From there, we focused on the four main transactions—withdrawal, deposit, transfer, and inquiry—because they represent the majority of real user interactions and require correct balance updates and clear user messaging. We primarily followed common user paths first (a typical successful transaction flow), then intentionally explored edge cases such as invalid authentication inputs, cancellation at different points in a transaction, and unusual values that could trigger unexpected behavior. As we discovered issues, we immediately recorded the system state, exact steps, expected behavior, and actual behavior so defects could be reproduced and compared later during scripted and regression testing.

# Comparison of exploratory and manual functional testing

Exploratory testing is valuable because it gives testers flexibility to follow the system’s behavior in real time and use judgment to decide what to try next. This approach is especially useful early in testing, when the goal is to learn the system quickly and expose unexpected problems that may not be included in a predefined test suite. It also encourages trying edge cases and “weird” inputs that reveal robustness issues. However, exploratory testing can be less repeatable and less systematic: without a fixed script, coverage depends on the tester’s choices, and it can be harder to guarantee that all requirements were tested unless careful notes are kept.

Manual functional (scripted) testing, in contrast, is structured and consistent. Because each test includes a clear initial state, steps, and expected outcome, it is easier to execute as a team, easier to reproduce across different testers, and easier to repeat during regression testing after changes. The tradeoff is that scripted tests may miss defects outside the defined paths and may not naturally encourage probing unusual scenarios unless the suite explicitly includes them.

Overall, exploratory testing helped us discover a wide range of behaviors and potential defects, while scripted testing helped us verify requirements in a repeatable way and provided a strong baseline for regression testing. Using both methods together gave us reliable verification.

# Notes and discussion of the peer reviews of defect reports

When both pairs completed their initial defect reports, we held a peer review to improve consistency and eliminate redundancy. We compared our reported issues and found that some defects overlapped across pairs, especially when both groups tested the same high-traffic features like withdrawals and transfers. To avoid duplicate reporting, we merged repeated findings into a single defect entry when appropriate and ensured the final report contained one for each issue.

Peer review also improved defect quality. In several cases, one pair’s report contained strong reproduction steps but lacked a clear initial state, while the other pair’s report had the initial state but needed clearer expected vs. actual outcomes. By reviewing together, we standardized the structure of our bug reports and made sure each defect clearly stated: (1) the function being tested, (2) the starting conditions, (3) exact steps and inputs, and (4) the expected versus actual result. This process made the defect set more readable and more useful for regression testing in v1.1.

# How the pair testing was managed and team work/effort was divided

We used pair testing by assigning one person as the “driver” and the other as the “observer/recorder.” The driver operated the ATM application and executed test steps, while the observer focused on watching for inconsistencies, tracking which tests were completed, and documenting outcomes. Roles were rotated within pairs to keep the workload balanced and to ensure both members gained experience executing tests and writing defect reports.

Across the full team, effort was divided by phase: both pairs performed exploratory testing independently to maximize coverage, then we collaborated as a group during scripted testing to ensure consistent pass/fail recording and avoid duplication. During regression testing, we divided the retesting of defects across team members and then consolidated the results into a final set of updated statuses and notes.

# Difficulties encountered, challenges overcome, and lessons learned

One of the main challenges was developing a good exploratory testing approach without a predefined script. We had to decide what to prioritize, how deeply to test each feature, and how to balance “common user paths” with edge cases. Another challenge was learning Jira efficiently—especially how to write complete defect reports and keep issue details consistent across multiple reporters. Regression testing also introduced complexity because some defects appeared partially changed rather than clearly fixed, which required careful retesting and clear documentation of what behavior differed between versions.

A major lesson learned was the importance of writing defects in a way that someone else can reproduce them without guessing. Defect reporting quality depends on clarity: initial state, exact inputs, and a clean comparison of expected vs. actual results. We also learned that exploratory testing is particularly effective at uncovering unexpected system behavior, while scripted testing is essential for consistent verification and repeatable regression. Finally, gaining familiarity with Jira improved our ability to organize, track, and communicate defects in a structured and realistic workflow.

# Comments/feedback on the lab and lab document itself

Overall, the lab was a useful introduction to practical software testing because it closely resembled real-world testing workflows: explore the system, execute structured tests, report defects in an issue tracker, and re-test after changes. The staged structure made the process easy to follow, and the requirement to log issues in Jira provided meaningful practice in professional defect tracking. One improvement that could make the lab even clearer would be including an example of a “high-quality” defect report (with ideal level of detail) so teams can calibrate what is expected early. It would also help to clarify how to record passing scripted tests (as execution evidence) without accidentally treating them as defects in the issue tracker.

