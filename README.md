# Overview

School board believes that some students have shown evidence of dishonesty, especially 9th graders in Thomas High School on their math and reading grades. Purpose is to update the math and reading scores for Thomas High School to NaN/N.A.. Also, Maria requested to rerun the whole analysis after updating the grades for 9th graders.

# Analysis

After updating the coding as below:

Step 2. Use the loc method on the student_data_df to select all the reading scores from the 9th grade at Thomas High School and replace them with NaN.
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th") & (student_data_df["reading_score"] > 0), "reading_score"] = np.nan

Step 3. Refactor the code in Step 2 to replace the math scores with NaN.
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th") & (student_data_df["math_score"] > 0), "math_score"] = np.nan

The results would show up as below:

![9th NaN grade tail](https://user-images.githubusercontent.com/89154507/132963442-fbc9ced6-3507-4826-86f5-5e75fe29778e.png)


# District Summary
Original:
![Original](https://user-images.githubusercontent.com/89154507/132963643-6da46ff4-168b-463f-ae76-6a923508e4cd.png)


Updated:
![District Summary](https://user-images.githubusercontent.com/89154507/132963605-bbadb95c-8805-41ca-839a-e97fe28e5f6b.png)

As in district summary, only few basis points have decreased from the original summary, in both math & readings, leading decrease in overall passing %.


# School Summary

The overall passing percentage for the school summary increased by 25%+ 

Original school summary:
![Original school summary](https://user-images.githubusercontent.com/89154507/132963747-bf446319-87dc-427d-be29-99b347e10749.png)

Updated school summary:
![Revised school summary](https://user-images.githubusercontent.com/89154507/132963795-57b6056c-5ecc-48f0-b7b4-5357e48b1f39.png)

After replacing the 9th graders grades from the overall report, the school's overall passing grade would drastically increase.

The math and reading scores by grade didn't significantly change. The effect of the change is minimal as 9th grade students in Thomas High School have much less students when ccompared to other school district schools. 
There are no changes to the School Spending Summary, School size, nor School Type summary.


# Conclusion
Overall, after replacing the Thomas High School ninth-graders' scores with the value NaN, there were some minor changes:


The four major changes in the school district analysis have minor decreases in the District Summary and Thomas High School's Average Math Score, % Passing Math, % Passing Reading, and % Overall Passing.
