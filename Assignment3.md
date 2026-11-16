# CS 424 Assignment 3

## Task 1: Implementing Interaction

I selected the line chart from Assignment 2 because it compares occupancy patterns between the first and second floors across the five collection days.

### Static version

![Static version](figures_assignment3/task1_static.png)

The static version shows two views side by side. The first chart shows the original occupancy counts, while the second chart shows the normalized occupancy index where Monday is set to 100. This allows viewers to compare both the actual occupancy difference and the relative pattern between the two floors.

### Interactive version

![Interactive version](figures_assignment3/task1_interactive.png)

The interactive version uses the same dataset but combines the two views into one chart. A dropdown allows the viewer to switch between `Raw occupancy` and `Occupancy index`.

The raw occupancy view supports comparing the actual occupancy difference between the two floors. The occupancy index view supports comparing their relative changes over time. I expect the interaction to help users switch between these two analytical perspectives without having to compare two separate charts at the same time.

## Task 2: Evaluation Design

### Evaluation question and hypothesis

- The evaluation question is whether the interactive version helps users analyze absolute occupancy differences and relative occupancy patterns more efficiently than the static version.
- I hypothesize that the interactive version will reduce task completion time while maintaining similar accuracy because users can display only the view needed for the current task.

### Analytical tasks

I designed two analytical tasks. Each task has two comparable variants so participants do not answer the exact same question in both conditions.

#### Task 1: Compare occupancy disparity

This task asks participants to compare the occupancy difference between the first and second floors across two days.

- **Task 1A:** Which day had the larger occupancy disparity between the two floors: Monday or Friday?
  - Expected answer: **Monday**
  - Monday difference: 387 - 53 = 334
  - Friday difference: 285 - 32 = 253

- **Task 1B:** Which day had the larger occupancy disparity between the two floors: Thursday or Tuesday?
  - Expected answer: **Tuesday**
  - Thursday difference: 365 - 49 = 316
  - Tuesday difference: 422 - 48 = 374

#### Task 2: Compare relative occupancy change

This task asks participants to use the occupancy index to determine which floor experienced the larger relative change between two days.

- **Task 2A:** Between Tuesday and Thursday, which floor had the larger change in occupancy index?
  - Expected answer: **Second floor**

- **Task 2B:** Between Tuesday and Wednesday, which floor had the larger change in occupancy index?
  - Expected answer: **First floor**

### Experimental design

The study will use a within-subject design, so every participant will use both the static and interactive versions. Each participant will answer two questions with the static version and two questions with the interactive version.

To reduce learning effects, participants will be divided into two groups:

|Group|First condition|Questions|Second condition|Questions|
|---|---|---|---|---|
|A|Static|Task 1A,Task 2A|Interactive|Task 1B, Task 2B|
|B|Interactive|Task 1A,Task 2A| Static|Task 1B, Task 2B|

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