# J296 Data Journalism Final Project: What factors affect recidivism?

## By Mar Segura

### Data analysis process:

-Download the dataset

-Go through the data to identify relevant columns to the analysis and to identify any possible mistakes or elements that should be cleaned before starting the analysis.

<em>Question 1: What is the percentage of paroled prisoners who recidivated?</em>

Step-by-step answer:
1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Recidivism_within_3years” and the values to “Recidivism_within_3years” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Selecting “show as”-”% of a column” in values, the percentage of recidivists will be shown next to “true”.



<em>Question 2: Does the number of programs prisoners attended affect recidivism?</em>

Step-by-step answer

1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Program_Attendances” and the values to “Program_Attendances” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Copy the numbers and paste them in a new colum under the name “Num_total_prog”, which has the numbers of all prisoners by the number of programs they attended.
4. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them in a new colum under the name “Num_rec_prog”, which has the number of recidivist prisoners by the number of programs they attended.
5. In a new colum under the name “Per_rec_by_prog”, divide the “Num_rec_prog” colum into the “Num_total_prog” and multiply by one hundred. This colum expresses the percentage of recidivists by number of programs attended.



<em>Question 2.1: Is the number of programs attended affected by the number of years in prison?</em>

When sharing my findings with an expert, he suggested the number of program prisoners attended might be affected by the years they spent in prison. If that was the case,

<em>Question 3: Does the level of education affect recidivism?</em>

-Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
-On the pivot table, set the row to “Education_Level” and the values to “Education_Level” as well. On values, it is important to select “Summarize by”-”COUNTA”.
-Copy the numbers and paste them in a new colum under the name “Num_total_edu”, which has the numbers of all prisoners by their education level.
-Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them in a new colum under the name “Num_rec_edu”, which has the number of recidivist prisoners by their education level.
-In a new colum under the name “Per_rec_by_edu”, divide the “Num_rec_edu” colum into the “Num_total_edu” and multiply by one hundred. This colum expresses the percentage of recidivists by education level.


