# pandas-challenge

## PyCitySchools Analysis

This code is made to analyze school districts using Pandas in Jupyter, it focuses on assessing the academic performance across several schools. The metrics involved in this assessment are average math and reading scores, budget allocating, and over-all score passing percentages. The goal of the code is to locate trends and correlations between spending and school type with academic performance, also to identify the performance levels of different schools and the grade level per school. 

## Files 

-PyCitySchools_analysis.ipynb: The Jupyter notebook with the main analysis code for data loading, cleaning, analyzing, and visuals.
-Resources/schools_complete.csv and students_complete.csv: The referenced datasets merged into one table, which the main analysis is based on

## Dependencies

- `pandas`

## Data Sources

-schools_complete.csv : dataset that contains information on schools: school name, type, size, and budget
-student_complete.csv: dataset that contains information on students: student ID, name, gender, grade, and math and reading scores


## Key Analysis Steps


1. Load Data (school and student): load into Pandas DataFrame

2. Clean Data: preprocess data to deal with any missing values, correc incorrect data types, and merge datasets

3. Calculations: 
    -average math and reading score
    -students passing math and reading percentage
    -overall passing rate--percentage of students passing math and reading
    -per-student budget and its relation to academic performance
    
4. School Summary: Create a summary of key statistics for each school: average scores, passing percentages, and budget information

5. Spending Summary: Group schools by their spending ranges and assess the influence of per-student budget on academic performance
    
6. Grade-level Summary: Break down academic performance data by grade-level to analyze any trends
    
7. School Type Summary: Compare the performance of charter schools and district schools 
   
   
## How to Use


1. Run the notebook: 
    -Open the "PyCitySchools_analysis.ipynb" notebook in Jupyter Notebook or another compatible application for the code language
    -run the cells in order--one after the other, to perform the analysis
    
2. Interpreting the Outcomes:
    -Review the output tables and data summaries produced by the notebook to identify trends and correlations to school academic performance
 
 
 ## Summary of Results
 
 - Charter schools tend to exceed district schools in academic performance in both math and reading test scores. 
 -Schools with lower per-student budgets for some reason, generally outperform schools with higher per-student budgets, indicating a more efficient use of their resources
 -Grade-level Performance unveils that reading scores typically remain stagnant or slightly better as students advance to upper grade-levels, and math scores tend to shift much more as students advance to upper grade-levels.


# References

Ln 31: "pd.cut(capita_per_school, spending_bins, labels = spending_labels)"

NumFocus, Inc. (2024). Pandas.cut. pandas.pydata. https://pandas.pydata.org/docs/reference/api/pandas.cut.html 

Ln 7: "school_dataset[(school_dataset["math_score"] >= 70)].count()["student_name"]"
Ln 9: "& (school_dataset["reading_score"] >= 70)].count()["student_name"]"
Ln 18: "school_dataset[school_dataset["math_score"] >= 70]["Student ID"].count()"
      "school_dataset[school_dataset["math_score"] >= 70].groupby("school_name")["Student ID"].count()"
Ln 24: " pd.DataFrame({
    "School Type": school_type,
    "Total Students": total_students,
    "Total School Budget": budget_per_school,
    "Per Student Budget": capita_per_school,
    "Average Math Score": Avg_math_score,
    "Average Reading Score": Avg_reading_score,
    "% Passing Math": per_school_passing_math,
    "% Passing Reading": per_school_passing_reading,
    "% Overall Passing": overall_passing_percent
}) "

Xpert Learning Assistant. (2024). Retrieved from https://bootcampspot.instructure.com/
