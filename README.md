# School District Analysis

## Overview 
The school board has notified Maria that there is evidence of academic dishonesty with regards to the ninth grade math and reading scores at Thomas High School. Those scores need to be excluded, and the school board requested to have the analysis run again. 

To do this, I used Python in Jupyter Notebooks. My input files were schools_complete.csv and students. complete.csv. 
## Results
What I did first was replace the 9th grade scores at Thomas High School with nulls. I used the numpy Pandas library for this task. After loading the library, I used loc to find the Thomas High School ninth graders, and  The code was:

```
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "reading_score"]=np.nan 
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "math_score"]=np.nan 
```
I then ran through the analysis again.
-  **The district summary was affected in this way:**
	
	- Passing math percentages were down by .2%.
	- Passing reading percentages were down by .1%.
	- Overall math and reading percentages were down by .3%.
	
-  **The school summary was affected in this way**:
   - The average passing math percentage went down by .5%.
   -  The average passing reading percentage went down by .3%.
   -  The average overall percentage went down by .3%.
   
- **How did it affect Thomas High School in relation to the other schools? **
Thomas High School was not affected, as the margin was so slight that it stayed the second top school.

  *Before:*
  
  ![](./Resources/before_school_summary.png)  
  
  *After:*
  
  ![](./Resources/aschool_summary.png)  
  
- **How replacing the ninth grade scores affected the following**:

  - Math and reading scores by grade: 9th graders for Thomas High School had none; nothing else was changed.
  - Scores by school spending: No change
  - Scores by school size: No change
  - Scores by school type: No change

## Summary
There are four major changes to be made in the updated school district analysis:
- Average math scores went down by .5%.
- Average reading scores went down by .3%.
- Overall scores went down by .3%.

I am not sure if it was worth our while since the 9th grade math scores were such a small percentage of the total.



