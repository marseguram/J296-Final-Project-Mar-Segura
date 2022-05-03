# J296 Data Journalism Final Project: What factors affect recidivism?

## By Mar Segura

[Link to article](https://github.com/marseguram/J296-Final-Project-Mar-Segura/blob/main/Article.md)

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
3. Copy the numbers and paste them into a new column under the name “Num_total_prog”, which has the numbers of all prisoners by the number of programs they attended.
4. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them into a new column under the name “Num_rec_prog”, which has the number of recidivist prisoners by the number of programs they attended.
5. In a new column under the name “Per_rec_by_prog”, divide “Num_rec_prog” (D2) into “Num_total_prog” (C2) and multiply by one hundred. This column expresses the percentage of recidivists by number of programs attended.


<img width="815" alt="Recidivism by program attendance" src="https://user-images.githubusercontent.com/99926488/166185527-5721bab7-8371-43c9-9ff3-6d61c9abdd69.png">


**<em>Question 3: Does the level of education affect recidivism?</em>**

**Step-by-step answer:**
1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Education_Level” and the values to “Education_Level” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Copy the numbers and paste them into a new column under the name “Num_total_edu”, which has the numbers of all prisoners by their education level.
4. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them into a new column under the name “Num_rec_edu”, which has the number of recidivist prisoners by their education level.
5. In a new column under the name “Per_rec_by_edu”, divide “Num_rec_edu” (D2) into the “Num_total_edu” (C2) and multiply by one hundred. This column expresses the percentage of recidivists by education level.

<img width="813" alt="Recidivism by education level" src="https://user-images.githubusercontent.com/99926488/166185649-02499d52-d1f7-465f-aaff-cb491c4a8c19.png">

**<em>Question 4: Does employment affect recidivism?</em>**

**Step-by-step answer:**

1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and find the “Jobs_Per_Year” column.
2. To determine whether a person had a job or not create a new column under the name “Jobyesorno” with an IF statement with this formula =IF(AY2>=0.001,"YES","NO").

<img width="904" alt="screenshot if statement" src="https://user-images.githubusercontent.com/99926488/166407528-dc261fe3-4988-483e-99da-d2efc8197c75.png">

3. Now create a pivot table and set the row to “Jobyesorno” and the values to “Jobyesorno” as well. On values, it is important to select “Summarize by”-”COUNTA”.
4. Some of the incarcerated people are job exempt and should not be included in this analysis. To exclude them create a filter under “Employment_Exempt” and select “false”.
5. Copy the numbers and paste them into a new column under the name “Num_total_job”, which has the numbers of all prisoners by their employment status.
6. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them into a new column under the name “Num_rec_job”, which has the number of recidivist prisoners by their employment status.
7. In a new column under the name “Per_rec_by_job”, divide “Num_rec_job” (D2) into “Num_total_job” (C2) and multiply by one hundred. This column expresses the percentage of recidivists by employment status.

<img width="796" alt="screenshot pivot table jobyesorno" src="https://user-images.githubusercontent.com/99926488/166407560-12daa752-1219-4823-a15d-666c199dcb04.png">

**<em>Question 5: Does gang affiliation affect recidivism?</em>**

**Step-by-step answer:**

1. Go to the initial tab “NIJ_s_Recidivism_Challenge_Full” and create a pivot table.
2. On the pivot table, set the row to “Gang_Affiliated” and the values to “Gang_Affiliated” as well. On values, it is important to select “Summarize by”-”COUNTA”.
3. Copy the numbers and paste them into a new column under the name “Num_total_gang”, which has the numbers of all prisoners by their gang affiliation.
4. Now create a filter in the pivot table under “Recidivism_within_3years”. In “Status” select “show per value” and then “true”. Copy the numbers and paste them into a new column under the name “Num_rec_gang”, which has the number of recidivist prisoners by their education level.
5. In a new column under the name “Per_rec_by_gang”, divide the “Num_rec_gang” (D2) column into the “Num_total_gang” (C2) and multiply by one hundred. This column expresses the percentage of recidivists by gang affiliation.

<img width="790" alt="screenshot pivot table gang" src="https://user-images.githubusercontent.com/99926488/166407602-11afefaa-ef42-4318-8844-7688bde8e9d4.png">
