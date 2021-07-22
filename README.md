# Analysis of School District Test Scores
##Overview
The purpose of this analysis was to aggregate the standardized testing data of all the high schools a city school district in order to aid the school board in decisions about budget allocation. Various metrics were calculated and displayed to show data on overall school performance, as well as average scores by grade, school spending, size, and type. The original analysis later had to be adjusted when it came to light that the ninth grade reading and math test scores for Thomas High School were altered, and therefore had to be replaced with null ("NaN") values.

##Results

###District Summary
Below is a breakdown of how the district summary changed after the scores for ninth grade reading and math test scores for Thomas High School were replaced with "NaN" values:

* Average math score decreased from 79.0 to 78.9
* Average reading score (when rounded only to the nearest 10th decimal place) appears unchanged (81.9); it's only after the code is displayed prior to reformatting the results that it becomes appearent the average score decreased from 81.87784 to 81.855796.
* Percentage of students that passed math decreased from 75.0% to 74.8%
* Percentage of students that passed reading decreased from 85.8% to 85.7%.
* Overall passing percentage decreased from 65.2% to 64.9%

Below is the original district summary (reformatted to 1 decimal place in order to match the format on the challenge code):

![image](https://user-images.githubusercontent.com/86032451/126624764-cdbb8cc6-dc49-4baa-a867-7c2fca40eef6.png)

Below is the updated district summary:

![image](https://user-images.githubusercontent.com/86032451/126624881-02207193-fed2-4017-86c1-d9d01bd26b67.png)

Below are the original and updated district summaries, respectively, prior to formatting the outputs to only 1 decimal place:

![image](https://user-images.githubusercontent.com/86032451/126625008-cf821d01-4b60-4fae-b145-ea2760b7e3d1.png)
![image](https://user-images.githubusercontent.com/86032451/126625047-8965d566-9cc6-4e9d-9813-aea412da47d9.png)

###School Summary
Within the updated challenge code there are two school summaries - the first includes the 9th "NaN" test scores within the calculations for Thomas High School, and the second has them removed from just the passing percentages. Below is a breakdown of how this affected Thomas High School within the school summary:

* Average math score was 83.418349 originally, and then 83.350937 in the updated analysis.
* Average reading score was 83.848930 originally, and then 83.896082 in the updated analysis.
* % Passing math was 93.272171 originally, 66.911315 in the first updated analysis, and then adjusted to 93.185690 after calculating it for only the 10-12 graders.
* % Passing reading was 97.308869 originally, 69.663609 in the first updated analysis, and then adjusted to 97.018739 after calculating it for only the 10-12 graders. 
* % Overall Passing was 90.948012 originally, 65.076453 in the first updated analysis, and then adjusted to 90.630324 after calculating it for only the 10-12 graders. 

Original school summary for Thomas High School:

![image](https://user-images.githubusercontent.com/86032451/126626727-93f74234-fc7e-4486-a169-e92008cb9532.png)

First updated school summary (includes 9th-grade "NaN" scores in % calculations):

![image](https://user-images.githubusercontent.com/86032451/126626809-82d731c0-fd46-45d8-8cfa-7c47f12d8538.png)

Second updated school summary (removes 9th-grade "NaN" scores in % calculations):

![image](https://user-images.githubusercontent.com/86032451/126626876-643cbf77-0338-4eb3-87a2-21988116bbb1.png)

###School standing relative to other schools
* Before replacing the % passing math, reading, and overall, Thomas High School would've been ranked 8th out of the 15 school in terms of overall passing percentage:

![image](https://user-images.githubusercontent.com/86032451/126629209-15a8eb98-7e62-4e03-bac9-9689b63c5c51.png)

* However, after updating the above calculations to only include the scores from grades 10-12, Thomas High School was able to retain it's standing as 2nd out of 15, as seen when sorting by top 5 performing high schools both before the 9th grade scores were updated to "Nan", and after they were completely removed from the % passing calculations:

![image](https://user-images.githubusercontent.com/86032451/126628409-e98e7c8c-67e5-4d46-8635-712204eb1b45.png)

![image](https://user-images.githubusercontent.com/86032451/126628472-d3d798c1-225f-415a-9952-e5455380d57b.png)

###Math and Reading Scores by Grade
* Within the "math_scores_by_grade" dataframe, the only thing that changed is that the 9th grade score for Thomas High School was updated to "nan" (originally 83.6):

![image](https://user-images.githubusercontent.com/86032451/126629424-61b513ac-bf89-453c-a767-adc62feefd56.png) ![image](https://user-images.githubusercontent.com/86032451/126629451-6c814f11-f873-48ee-a8b6-91fb74e5c017.png)

* Within the "reading_scores_by_grade" dataframe, the only thing that changed is that the 9th grade score for Thomas High School was updated to "nan" (originally 83.7):

![image](https://user-images.githubusercontent.com/86032451/126629602-b062ac21-67a5-40f1-af55-c6d529755275.png) ![image](https://user-images.githubusercontent.com/86032451/126629647-0d4d3f3c-903c-4d67-b260-05005330dcbd.png)

###Scores by School Spending
The changes in this metric after the Thomas High School 9th grade scores were updated is only apparent when viewing both the original and updated dataframe prior to formatting to a single decimal place. 

* Original dataframe:
![image](https://user-images.githubusercontent.com/86032451/126630022-8d92f074-4d68-4102-940f-2dc3c7f4bc99.png)

* Updated dataframe - after replacing Thomas High School 9th grade scores with "nan", every single metric in the $630 - 644 bucket decreased slightly:

![image](https://user-images.githubusercontent.com/86032451/126630166-bd13fd3c-5adb-441e-9bfb-71f93b04acec.png)

* When formatted to a single decimal place, however, both dataframes appear to display the same metrics:

![image](https://user-images.githubusercontent.com/86032451/126630222-d7acff1e-33de-49cd-9e9c-f17519e91629.png)

###Scores by School Size
As with "Scores by School Spending", the changes that happened within these dataframes is only apparent when not formatted to a single decimal place:

* Original dataframe:
![image](https://user-images.githubusercontent.com/86032451/126630416-a51b3f82-6b97-40d5-a1f7-d19a4a69ccb9.png)

* Updated dataframe - after replacing Thomas High School 9th grade scores with "nan" every single metric in the Medium (1000-2000) metric decreased slightly:
![image](https://user-images.githubusercontent.com/86032451/126632581-adc7d6ce-0532-4a8a-b55c-69a59ccc204a.png)

The dataframe when formatted to a single decimal place (same both before and after):
![image](https://user-images.githubusercontent.com/86032451/126633545-0eeb832a-3568-49aa-bf80-f8990abf594f.png)

###Scores by School Type
Finally, as with the previous two dataframes, the changes that happened within this one is only apparent when not formatted to a singeld decimal place:

* Original dataframe:
![image](https://user-images.githubusercontent.com/86032451/126633599-ef7c87d6-d43d-4cfe-8b58-3a7f3fdd3b7f.png)

* Updated dataframe - after replacing Thomas High School 9th grade scores with "nan" every single metric in the "Charter" type decreased slightly:
![image](https://user-images.githubusercontent.com/86032451/126633657-cb99a547-db33-41ff-850d-92b90ad88c9f.png)

* The dataframe when formatted to a single decimal place (same both before and after):
![image](https://user-images.githubusercontent.com/86032451/126633737-6afe1c95-651b-44d4-b151-0eeac65b226c.png)

##Summary
In conclusion, updating the 9th grade scores for Thomas High School to "nan" affects the school district analysis in the following ways:
* Within the school summary, Thomas High School average math and reading scores decreased slightly, with the % passing for math, reading, and overall decreasing drastically when the "nan" 9th grade scores were included in the calculation. After updating the percentages to only include 10-12 grades, however, they went back up, but were still slightly lower than what they were in the original analysis. This, in turn, caused those same metrics in the district summary to also decrease slightly.
*  Since Thomas High School fell within the $630 - 644 spending bucket, the test scores metrics within that range ended up decreasing slightly, but was only apparent before formatting the outputs to a single decimal place. 
*  Since Thomas High School fell within the Medium (1000-2000) bucket, the test scores metrics within that range ended up decreasing slightly, but was only apparent before formatting the outputs to a single decimal place. 
*  Since Thomas High School is categorized as a Charter type, the test scores metrics within that type ended up decreasing slightly, but was only apparent before formatting the outputs to a single decimal place. 







