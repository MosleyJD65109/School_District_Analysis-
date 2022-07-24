# School_District_Analysis
## Overview of the school district analysis:
The purpose of this analysis was to inform a school district on their budget and priorities based of the results of an evaluation of school and student data. The school district discovered that the standardized test scores for ninth grade students at Thomas High School were incorrect, and they requested for updated data summaries. After further discussion, it was best to only replace the ninth grade math and reading scores at Thomas High School while keeping all other data associated with this student group intact. Both math and reading scores were replaced with "NaN", which represents a "Not-a-Number" value, for 461 student records. Although this may seem like a significant number, these score replacements did not alter data summaries tremendously overall.

## Results:
### School District Summary
```
# Adding a list of values with keys to create a new DataFrame.
district_summary_df = pd.DataFrame(
          [{"Total Schools": school_count,
          "Total Students": student_count,
          "Total Budget": total_budget,
          "Average Math Score": average_math_score,
          "Average Reading Score": average_reading_score,
          "% Passing Math": passing_math_percentage,
         "% Passing Reading": passing_reading_percentage,
        "% Overall Passing": overall_passing_percentage}])
district_summary_df
```

![School District Summary](https://user-images.githubusercontent.com/104540261/180645621-37533874-ddd7-419d-983d-4154f614e785.png)


When evaluating passing percentages and average scores among the 15 high schools in the school district, the average math score was 1% lower, the average reading score stayed the same, the percentage passing math was 1% lower, the percentage passing reading was 1% lower, and the overall passing percent was 1% lower.

### School Summary

![School Summary](https://user-images.githubusercontent.com/104540261/180645768-fd1e4938-c944-482e-b3f6-bef2fadb08b2.png)


### Top Five Performing Schools

![Top 5 Schools](https://user-images.githubusercontent.com/104540261/180646118-b89e5a23-30cc-48e6-9e5a-1bb3c4246bf8.png)

### Bottom Five Performing Schools

![Bottom 5 Schools](https://user-images.githubusercontent.com/104540261/180646123-b9df296b-6eb2-4b0e-8a0e-d77503bac9b6.png)

When assessing school summaries and performing schools, the score replacements did affect the ranking of the top five performing schools. Thomas High School ranked second place in the top five performing schools with a 91% overall passing. After replacing both math and reading scores, Thomas High School was taken out of the top five category since they now display a 65% overall passing. On the plus side, these changes did not place Thomas High School among the bottom five performing schools. Those ranks remained the same. Per the revised School Summary, Thomas High School now ranks 8th place among 15 high schools in the district.


### Average Math Scores by Grade & School

![Average Math Scores](https://user-images.githubusercontent.com/104540261/180646147-98c16b76-0afe-4f3f-91a4-722dbfa0f981.png)

### Average Reading Scores by Grade & School

![Average Reading Scores](https://user-images.githubusercontent.com/104540261/180646155-6e5f64ee-666e-4faa-aacf-831cf9fa3306.png)

Another plus side from this data replacement is that it did not change the math and reading scores by grade. Granted, both the average math and reading score summaries were stratisfied by school and grade level. As shown above, the summary tables display "NaN" for ninth grade at Thomas High School whereas the remaining data remained intact.


### School Spending Summary

![School Spending](https://user-images.githubusercontent.com/104540261/180646160-a0eb4d3b-796e-4410-8e55-d8361fbb3d53.png)

When reviewing the School Spending summary, this data change did not impact the spending ranges for either the average math scores or average reading scores. However, this data change did impact the spending ranges for passing percentages. According to the summary above, there was a 6% decrease in % passing math, a 7% decrease in % passing reading, and a 6% decrease in % overall passing in the $630-644 spending range.


### School Size Summary

![School Size](https://user-images.githubusercontent.com/104540261/180646170-c176d109-67bf-4dfa-b313-bbc02a8b4e54.png)

When reviewing the School Size summary, removing the ninth grade scores did not affect the average math and reading scores, but it did affect the passing percentages for medium-sized schools (1,000-2,000). In this category, % passing math, % passing reading, and % overall passing dropped 6% each. Before the data change, the School Size summary showed that medium-sized school had a high performance (91% overall passing) compared to small (90% overall passing) and large schools (58% overall passing). Given the data change, medium size school are the second in performance (85% overall passing).


### School Type Summary


In reviewing the last summary on School Types, this data change also affected the passing percentages that compared charter and district schools. Fortunately, it did not affect the average scores for these two school types. Removing the scores resulted in a reduction in charter school's passing percentages. Before the data change, charter schools had very high passing percentages: 94% passing math, 97% passing reading, 90% overall passing. After the data change, charter schools now have a 90% passing math, 93% passing reading, 87% overall passing. On the plus side, these rates are still far superior when compared to district schools.

