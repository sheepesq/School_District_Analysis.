# School_District_Analysis.
## Overview of the school district analysis: Explain the purpose of this analysis.
The purpose of this analysis is to transform the information from the School.csv and Student.csv into easily readable information. We broke the data down into class size, school type, school size and school budget. 

**Results: Using bulleted lists and images of DataFrames as support, address the following questions.**

- How is the district summary affected? --> THe summary is affected because we took out the 9th Grade scores and replaced them with NaN
```
student_data_df.loc[(student_data_df['school_name'] =='Thomas High School') & (student_data_df['grade']=='9th') ,'reading_score'] =np.nan
student_data_df.loc[(student_data_df['school_name'] =='Thomas High School') & (student_data_df['grade']=='9th') ,'math_score'] =np.nan

```
- How is the school summary affected? --> The only school summmary that is affected is the Thomas High School as they now have imcomplete data.
- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools? The schools overall performance goes down. 
- How does replacing the ninth-grade scores affect the following:
- Math and reading scores by grade --> Thomas High School's Math and Reading scores 
- Scores by school spending --> the schools in the **$585-629** bin have their average scores and passing percentages go down
- Scores by school size --> The passing percentage of the medium size school decreases when the 9th graders from Thomas HS are removed as shown:
```
with 9th Grade
School Size         Average Math Score	Average Reading Score	%   Passing Math	%   Passing Reading	%      Overall Passing School Size					
Medium (1000-2000)	83.4	              83.9	                    94 	              97                     91
withouth 9th Grade
School Size         Average Math Score	Average Reading Score	%   Passing Math	%   Passing Reading	%      Overall Passing School Size					
Medium (1000-2000)	83.4	              83.9	                    88.3	            91.3	                  85.4

```
- Scores by school type --> charter school scores go down, overall passing goes from a 90 to an 87.

**Summary: Summarize four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.**

- The 9th grade students at Thomas High School tend to skew the data upwards due to their high scores.
- The score differences between District and Charer schools closed but is still a large gap.
- The average spending per student increased due to the same budget but reduced student size (now missing 9th graders)
- School ranking for thomas HS moved down. 




