# School_District_Analysis
This project aims to analyze the school data using the Pandas Library and Jupyter Notebook.

## Overview of the Analysis
This analysis is to help Maria, a Data Scientist of the city school district, analyze the school data collected from various sources and provide insights based on the performance trends and patterns. These insights help to make decisions at the school and district levels. We need to aggregate the data and see the performance based on the school budgets, size, and types. The steps involved in this analysis are done by using Pandas and Jupyter Notebook. Pandas is a python library used for data manipulation and analysis; it is used with Jupyter Notebook to read raw data, Clean and inspect data, Merge datasets, Perform Calculations, and create tables. These tasks are part of Data Wrangling. Data wrangling is used to convey helpful information from the data. For this analysis, we need to calculate the district summary, school summary, average reading, and math scores in all the grade levels, display the top and bottom five schools, and school performance based on the school's budget, size, and type.

## Purpose
For this analysis, the school board has notified Maria that the file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth-graders appear to have been altered. Although the school board does not know the full extent of academic dishonesty, they want to uphold state-testing standards. So the school board asked us to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once we have replaced the math and reading scores, we need to repeat the school district analysis in the module and describe how these changes affected the overall analysis.

## Resources

*DataSources*: [schools_complete.csv](https://github.com/fathi129/School_District_Analysis/blob/master/Resources/schools_complete.csv),  [students_complete.csv](https://github.com/fathi129/School_District_Analysis/blob/master/Resources/students_complete.csv). <br>
*Software used*: Jupyter Notebook 6.4.5.<br> 
*Libraries*: Panda,Numpy. <br>
*Language*: Python 3.9.7. 

## Analysis Results
The `loc()` method is used to find the ninth graders and replace the values. After replacing the math and reading scores for the ninth graders with NaN in Thomas High School, The student data frame looked like this.<br> 
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Replacing%20with%20NaN.png" width = 700> <br>
The district summary for the updated file is calculated by finding the school count, students count, total budget, average math score,average reading score, pass percentage in math and reading, and overall pass percentage, and the results are shown below. <br><br>

***District Summary with Updated Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/District_Summary_updated.png" width = 900><br>
***District Summary with Original Analysis*** <br>
 <img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/District_Summary_original.png" width = 900><br>
 - Changing NaN to math and reading scores of all the ninth graders in Thomas High School did not significantly impact the district analysis. We could see less than a 0.5 percentage point decrease in the overall passing metric; other metrics, too, have fewer changes. As the student count of ninth graders in Thomas High school is only 461 compared to the total student count of 39170, removing math and reading scores impacts the overall passing by a less percentage.<br>
 
***School Summary with updated analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/School_Summary_THS.png" width = 900><br>
***School Summary with original analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/SchoolSummary_original.png" width = 900><br>
The school summary is calculated with the updated Thomas high School reading and math scores. We can see that the overall passing percentage is decreased to 65% from the original analysis of 91%. Which made Thomas high school go to rank 8th place from the initial analysis of 2nd place,In which it was in the top-performing schools. After recalculating the metrics by including 10th to 12th graders, the overall passing percentage of the Thomas high school has been improved, which made it to be on the top performing schools again.<br>

***School Summary with updated THS analysis including 10th - 12th graders*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/SchoolSummary_updated.png" width = 900><br>

***Top Performing Schools - Updated Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Top5.png" width = 900><br>
***Top Performing Schools - Original Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Top5_original.png" width = 900><br>
- The rank of the Thomas High School was not affected by the update.
- However, we can see some changes in average reading, math, pass percentage, and overall pass percentage by less than 0.3 percentage points in each metric.<br>
- 
***Bottom Schools - Updated Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/%20Bottom5.png" width = 900><br>
***Bottom Schools - Original Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Bottom5_original.png" width = 900><br>
- The ranking of the bottom schools was not affected by the changes we made in the Thomas High School.<br>

|    ***Math Scores - Updated Analysis***       |    ***Math Scores - Original Analysis*** |
|  ---------------------------------------      |    --------------------------------------|
|  <img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Math_Scores.png" width = 350><br >|  <img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Math_Score_original.png" width = 350><br>

|    ***Reading Scores - Updated Analysis***     |    ***Reading Scores - Original Analysis*** |
|  --------------------------------------------  |    -----------------------------------------| 
|  <img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Reading_Scores.png" width = 350><br >|  <img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Reading_Score_original.png" width = 350><br>

- When we saw the math and reading scores in all the grade levels, it dint affect the updated analysis as we changed only 9th graders to NaN.<br>

***School Spending - Updated Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Spending_range_updated.png" width = 900><br>
***School Spending - Original Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Spending_range_original.png" width = 900><br>
- To perform a school spending analysis, we need to cut the data frame into bins and label it with range. By categorizing into bins each school will fall into the respective range, then the average of all the metrics is calculated and displayed.
- We can see a slight change in the $630 - 644 spending range per student as Thomas High School falls in this range; however the change is minimal; each metric is less than 0.1 percentage points from the original.<br>

***School Size - Updated Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Schoolsize_updated.png" width = 900><br>
***School Size - Original Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Schoolsize_Original.png" width = 900><br>
- The scores based on the School size are calculated; in the medium-sized school(1000-2000), we can see the changes of less than 0.1 percentage points in all the metrics. This is because Thomas High School has a student count of 1635, which belongs to the medium-sized school group.<br>

***School Type - Updated Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Schooltype_updated.png" width = 900><br>
***School Type - Original Analysis*** <br>
<img src = "https://github.com/fathi129/School_District_Analysis/blob/master/Screenshots/Comparision/Schooltype_original.png" width = 900><br>
- Based on the school type, the scores are calculated we could see a slight change in charter school type since Thomas High School belongs to this type and the change is also less than 0.1 percentage points in each metric.<br>

## Summary
The changes in the updated school district analysis after reading and math scores are replaced with NaNs for the ninth graders at Thomas High School are
- In the District Summary Calculation, the overall passing percentage is decreased by less than 0.5 percentage points from the original analysis.
- In the School Summary results, we could see the overall passing percentage of Thomas High School is reduced to 65% from 91% of the original analysis, However by including the 10th to 12th graders in the calculation, we could see the result changed 90.6%.
- The Percentage of Passing Reading in Thomas High School decreased by less than 0.5 percentage points from the original analysis.
- By analyzing the results based on the school spending criteria, we can see that the lesser the budget spent per student, the higher the student's scores. We can also see a decrease of 0.1 percentage points in each metric in the updated analysis of $631-645.
- Based on the School size calculation, we can see that the medium-sized school performed well overall passing. When we compare the original and updated analysis, we can see a 0.1 percentage point decrease in overall passing metric in medium school size as Thomas High school belongs to this criteria.
- Based on the School type calculation, we can see that the Charter schools outperformed the District schools; however, because of the update, there is less than a 0.1 percentage point decrease in the updated analysis. Thomas High, School, belongs to a Charter school. With these insights, we can say that the changes in the ninth graders of Thomas school dint affect much in the overall school board analysis.
