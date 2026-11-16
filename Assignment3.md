# CS 424 Assignment 3

## Task 1: Implementing Interaction

I selected the line chart from Assignment 2 because it compares occupancy patterns between the first and second floors across the five collection days.

### Static version

![Static version](AS3_figures/task1_static.png)

The static version shows two views side by side. The first chart shows the original occupancy counts, while the second chart shows the normalized occupancy index where Monday is set to 100. This allows viewers to compare both the actual occupancy difference and the relative pattern between the two floors.

### Interactive version

![Interactive version](AS3_figures/task1_interactive.png)

The interactive version uses the same dataset but combines the two views into one chart. A dropdown allows the viewer to switch between `Raw occupancy` and `Occupancy index`.

The raw occupancy view supports comparing the actual occupancy difference between the two floors. The occupancy index view supports comparing their relative changes over time. I expect the interaction to help users switch between these two analytical perspectives without having to compare two separate charts at the same time.

## Task 2: Evaluation Design

### Evaluation question and hypothesis

- The evaluation question is whether the interactive version helps users analyze absolute occupancy differences and relative occupancy patterns more efficiently than the static version.
- I hypothesize that the interactive version will reduce task completion time while maintaining similar accuracy because users can display only the view needed for the current task.

### Analytical tasks

I designed two analytical tasks. Each task has two comparable variants so participants do not answer the exact same question in both conditions.

#### Task 1: Compare changes in occupancy disparity

- **Task 1A:** Which interval had the larger change in occupancy disparity between the two floors: Monday to Wednesday or Wednesday to Friday?
  - Expected answer: **Wednesday to Friday**
  - Monday disparity: 387 - 53 = 334
  - Wednesday disparity: 405 - 58 = 347
  - Friday disparity: 285 - 32 = 253
  - Monday to Wednesday change: |347 - 334| = 13
  - Wednesday to Friday change: |253 - 347| = 94

- **Task 1B:** Which interval had the larger change in occupancy disparity between the two floors: Monday to Thursday or Tuesday to Friday?
  - Expected answer: **Tuesday to Friday**
  - Monday disparity: 334
  - Thursday disparity: 365 - 49 = 316
  - Tuesday disparity: 422 - 48 = 374
  - Friday disparity: 253
  - Monday to Thursday change: |316 - 334| = 18
  - Tuesday to Friday change: |253 - 374| = 121

#### Task 2: Compare relative occupancy variation

For this task, range means the highest occupancy index minus the lowest occupancy index.

- **Task 2A:** Across Monday, Tuesday, and Wednesday, which floor had the larger range in occupancy index?
  - Expected answer: **First floor**
  - First floor range: about 109.4 - 90.6 = 18.8
  - Second floor range: about 109.0 - 100 = 9.0

- **Task 2B:** Across Monday, Tuesday, and Thursday, which floor had the larger range in occupancy index?
  - Expected answer: **Second floor**
  - First floor range: about 100 - 90.6 = 9.4
  - Second floor range: about 109.0 - 94.3 = 14.7


### Experimental design

The study will use a within-subject design, so every participant will use both the static and interactive versions. Each participant will answer two questions with the static version and two questions with the interactive version.

To reduce learning effects, participants will be divided into two groups:

|Group|First condition|Questions|Second condition|Questions|
|---|---|---|---|---|
|A|Static|Task 1A,Task 2A|Interactive|Task 1B,Task 2B|
|B|Interactive|Task 1A,Task 2A|Static|Task 1B,Task 2B|

Five participants will be assigned to each group. This balances the presentation order and distributes the question variants across both conditions.

### Measurements

For every question, I will record:

- **Accuracy:** whether the participant gives the correct answer.
- **Completion time:** the number of seconds from when the question is presented until the participant gives an answer.

I will also record short observations if a participant appears confused by the occupancy index, has difficulty using the dropdown, or has difficulty deciding which view to use.

### Procedure

Participants will first receive a short explanation of the visualization controls without being shown the answers to any analytical questions. They will then complete the four questions according to their assigned condition order.

Only one condition will be shown at a time. For each question, I will start timing when the participant receives the question and stop timing when they provide their final answer. I will record the answer, whether it is correct, and the completion time in seconds.

Before the main study, I will conduct a pilot with one or two participants to check whether the instructions are clear, the questions have appropriate difficulty, and the timing procedure works correctly.


## Task 3: Conducting the Evaluation

### Pilot evaluation
I conducted a pilot evaluation with one participant before the main study. The participant completed all four questions correctly.

The participant reported that the interactive visualization was easier to view because it displayed one graph at a time, while the static version showed two graphs side by side. The participant also found Task 1 more difficult than Task 2 because Task 1 required more calculation steps.

The completion times were 46 and 19 seconds for the two static questions, and 40 and 15 seconds for the two interactive questions. The participant did not report any problems understanding or using the dropdown.

Based on the pilot, the questions and visualization were understandable, so I kept the revised tasks for the main study.

### Main study
I conducted the main study with 10 participants. Five participants completed the static condition first, while the other five completed the interactive condition first. Each participant answered four questions and recorded their completion time for each question.

### Collected data
I recorded participant ID, group, condition, task, answer, correctness, and completion time. The results are stored in data/evaluation_results.csv, while the pilot data is stored in data/pilot_results.csv.

## Task 4: Quantitative Analysis

### Overall results

The interactive condition had a mean accuracy of **0.70** and a mean completion time of **37.8 seconds**. The static condition had a mean accuracy of **0.75** and a mean completion time of **39.0 seconds**.

Overall, the interactive version was about **1.2 seconds faster**, but its accuracy was **5 percentage points lower**.

### Accuracy

![Accuracy comparison](AS3_figures/task4_accuracy.png)

Accuracy was similar between the two conditions, with the static version slightly higher overall.

Task difficulty had a larger effect than the condition. Task 2 had high accuracy in both versions, while Task 1 produced more incorrect and `No answer` responses. For example, Task 2B had an accuracy of **1.0** in both conditions.

### Completion time

![Completion time comparison](AS3_figures/task4_completion.png)

Participants were slightly faster overall with the interactive version. However, this pattern was not consistent across every task. For Task 1A, the interactive mean time was **53.4 seconds**, compared with **62.8 seconds** for static. In Task 1B, the interactive version was slower at **50.4 seconds**, compared with **43.2 seconds** for static.

### Differences across participants and tasks

Performance also varied across participants. Some participants completed the interactive condition faster, while others were faster with the static condition. Accuracy also varied, with some participants performing equally in both conditions and others performing better in one condition.

Task 1 was generally more difficult and slower than Task 2. This is consistent with the pilot observation that Task 1 required more calculation steps.

### Interpretation

My hypothesis was that the interactive version would reduce completion time while maintaining similar accuracy. The results provide limited support for this hypothesis. The interactive version was slightly faster overall, but its accuracy was also slightly lower.

Because the differences were small and performance varied across tasks and participants, the results do not show that one version was clearly better than the other.