# J296 Data Journalism Final Project: What factors affect recidivism?

## By Mar Segura

### Data analysis process:

-Download the dataset

-Go through the data to identify relevant columns to the analysis and to identify any possible mistakes or elements that should be cleaned before starting the analysis.

**<em>Question 1: What is the percentage of paroled prisoners who recidivated?</em>**

**Step-by-step answer:**
1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Recidivism_within_3years” and the values to “Recidivism_within_3years” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Selecting “show as”-”% of a column” in values, the percentage of recidivists will be shown next to “true”.

<img width="814" alt="Recidivism rate" src="https://user-images.githubusercontent.com/99926488/166185502-8f48f347-400e-4214-9738-36959861d51c.png">


**<em>Question 2: Does the number of programs prisoners attended affect recidivism?</em>**

**Step-by-step answer**

1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Program_Attendances” and the values to “Program_Attendances” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Copy the numbers and paste them in a new colum under the name “Num_total_prog”, which has the numbers of all prisoners by the number of programs they attended.
4. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them in a new colum under the name “Num_rec_prog”, which has the number of recidivist prisoners by the number of programs they attended.
5. In a new colum under the name “Per_rec_by_prog”, divide the “Num_rec_prog” colum into the “Num_total_prog” and multiply by one hundred. This colum expresses the percentage of recidivists by number of programs attended.


<img width="815" alt="Recidivism by program attendance" src="https://user-images.githubusercontent.com/99926488/166185527-5721bab7-8371-43c9-9ff3-6d61c9abdd69.png">



<em>Question 2.1: Is the number of programs attended affected by the number of years in prison?</em>

When sharing my findings with an expert, he suggested the number of program prisoners attended might be affected by the years they spent in prison. If that was the case, m



**<em>Question 3: Does the level of education affect recidivism?</em>**

**Step-by-step answer:**
1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Education_Level” and the values to “Education_Level” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Copy the numbers and paste them in a new colum under the name “Num_total_edu”, which has the numbers of all prisoners by their education level.
4. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them in a new colum under the name “Num_rec_edu”, which has the number of recidivist prisoners by their education level.
5. In a new colum under the name “Per_rec_by_edu”, divide the “Num_rec_edu” colum into the “Num_total_edu” and multiply by one hundred. This colum expresses the percentage of recidivists by education level.

<img width="813" alt="Recidivism by education level" src="https://user-images.githubusercontent.com/99926488/166185649-02499d52-d1f7-465f-aaff-cb491c4a8c19.png">

