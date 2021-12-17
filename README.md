# School_District_Analysis

## Overview of School District Analysis
For this project, I was tasked to complete an analysis of 15 high schools within a city school system. The information included math and reading standardized test scores from the system's 39,170 students, as well as budget information for all schools.  The information would then be used to spot any trends and aid in future decision-making processes such as funding and priorities. The following analyses were performed during this project:

 * Ensuring completeness of school and student data
 * Calculating total budget for all schools in system
 * Calculating average reading and math testing scores for all students
 * Determining the number and percentage of students who passed:
      + Reading
      + Math
      + Reading and Math
 * Calculating the number of students per school
 * Calculating per capita spending for each school
 * Determining highest and lowest performng school based on test scores
 * Comparing performance in relation to
     + Per capita spending
     + School size
     + School type
     
After completion and submission of the initial analysis to the school board, I was notified that upon review of the analysis by the school board that the original student data appeared to be altered in the csv file I wass provided. They advised that the reading and math scores for the ninth grade students at Thomas High School appeared to be altered. I was asked to replace the data for all ninth grade students at this school with null scores (NaNs) and repeat the school district analysis without these values. 

![Ninth grade scores](https://github.com/crtallent/School_District_Analysis/blob/main/Resources/ninth_grade_png.png)

## Resources
- Data Sources: school_complete_csv, students_complete_csv
- Software: Python 3.7.11, Jupyter Notebook 7.29.0

## School District Analysis Results
Upon removing Thomas High School's ninth grade students' testing results, we can see slight differences in the following areas:

* District Summary:  
  + Number of students included in testing results decreased by 461 (number of students enrolled in ninth grade at Thomas High School)  
  + Average math score decreased by 0.1%  
  + Average reading score remained the same  
  + Percent of students passing math decreaed by 1.1%  
  + Percent of students passing reading decreased by 1.3%  
  + Percent of students passing both math and reading decreased by .1%  




 ![district summary 1]( https://github.com/crtallent/School_District_Analysis/blob/main/Resources/dist_summ1.png "District Summary with THS ninth graders") 
 ![district summary 2]( https://github.com/crtallent/School_District_Analysis/blob/main/Resources/dist_summ2.png "District Summary without THS ninth graders") 
 
 * School Summary (Thomas High School):
   + The average math score of Thomas High School students decreased by 0.1%
   + The average reading score increased by .01%
   + Percent of students passing math decreased by 0.1%
   + Percent of students passing reading decreased by 0.3%
   + Percent of students passing both math and reading decreased by 0.3%


![school_summary_1](https://github.com/crtallent/School_District_Analysis/blob/main/Resources/school_summ1.png "School Summary with THS ninth graders")
![school_summary_2](https://github.com/crtallent/School_District_Analysis/blob/main/Resources/school_summ2.png "School Summary without THS ninth graders")

* Thomas High School Ranking:
  + Thomas High School ranked as number 2 in the Top 5 performing schools with and without the scores of the ninth grade students, even though their overall passing percentage   
    decreased by 0.3%
    
'''
# Sort and show top five schools.
top_schools = per_school_summary_df.sort_values(["% Overall Passing"], ascending=False)

top_schools.head()
'''
