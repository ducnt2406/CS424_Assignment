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
