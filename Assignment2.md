# CS 424 Assignment 2

## Task 1: Revisit Data and Questions
### Data review
The dataset I use for Assignment 2 is the same as in CS 424 Assignment 1, with 10 observations collected on the first and second floors of the UIC Richard J. Daley Library in a 5-day period at 4 pm. I reviewed the data again and did not find any missing or inconsistent values that need to be changed. Limitations include a small dataset, approximate rather than exact occupancy counts, and noise levels measured by my feelings.

### Questions for Assignment 2
1. What is the occupancy disparity on each day between the two floors?
2. Is there a similar pattern between the occupancy of the two floors?
3. Is there a relation between the noise level and occupancy level for each floor?

I decided to keep the 1st, 2nd, and 3rd questions but remove the 4th because the small dataset makes it easy to directly identify the day with the highest and lowest numbers of occupants. 

## Task 2: Prepare the Data
I used Pandas to inspect the old dataset in Excel to find missing values, duplicate rows, and other issues. No major errors were found in the main attributes used for analysis and visualization. 
The notes attribute contained a blank value because it recorded only when something unusual occurred. To avoid representing blank cells as NaN in the CSV, I replace them with a new value called Normal, indicating that no unusual event was noted for that observation. 

## Task 3: Explore the Data
### Occupancy comparison
![Occupancy comparison](figures/task3_bar.png)

The bar chart shows that the second floor had a much higher occupancy count than the first floor on every day. The difference between the two floors was very large throughout the 5-day period, although occupancy on both floors was lowest on Friday.

### Occupancy trend
![Occupancy trend](figures/task3_line.png)

Two floors didn’t follow the same pattern during the 5-day period. The second floor reached its highest occupancy on Tuesday, 9/22 and then decreased for the rest of the week, while the first floor reached its highest occupancy on Wednesday, 9/23. Both floors showed a noticeable decrease by Friday, 9/25.

### Occupancy and noise level
![Occupancy and noise level](figures/task3_noise.png)

The first floor was recorded as quiet on all 5 days, so there is not enough variation to detect a relationship with occupancy on that floor. On the second floor, higher occupancy observations were recorded as Noisy, and lower occupancy observations were recorded as Moderate. This suggests a possible relationship between higher occupancy and higher perceived noise on the second floor, although the dataset is too small to support a strong conclusion.

## Task 4: Implement visualization alternatives
### Direction 1
![Direction 1](figures/task4_bar.png)

This bar chart compares occupancy between two floors during the period. Three attributes used are date, floor, and occupancy_count. The value labels on top of the bar help viewers read more easily. This design already works well for direct comparison, so I decided to keep it.

### Direction 2
![Direction 2](figures/task4_line.png)

This graph represents the occupancy pattern over time for each floor using date, floor, and occupancy_count with points and lines over the five days. Separating the two floors into separate graphs was necessary due to the discrepancy in occupancy levels. It became easier to interpret both graphs this way, so I will continue working with it. 

### Direction 3
![Direction 3](figures/task4_noise.png)

This heatmap includes date, floor, occupancy_count, and noise_level. Position encodes date and floor, color encodes noise_level, while the numbers in the boxes are occupancy_count. I created this visualization to combine occupancy and noise into a single compact representation. But due to a small dataset, the heatmap appears quite constrained, and the color encoding is difficult to interpret. 

## Task 5: Interaction and multiple views

I considered adding a floor filter, but it's not very useful for a small dataset. Switching between floors would make comparison less direct than showing both views at the same time.
Instead, I used multiple views in the small-multiple line chart. Separating the two floors makes the pattern within each floor easier to see while still allowing direct visual comparison. For this dataset, static multiple views were more useful than interaction.

## Task 6: 
