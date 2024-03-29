# School_District_Analysis
## Overview of the school district analysis:
The goal of this analysis was to let the school district know their budget and priorities based of the results of an evaluation of school and student data. This analysis lead to the school district discovering that the Thomas High School nith grade students standardized test scores were incorrect, and they requested for updated data summaries. Because of this, it was best to only replace the ninth grade math and reading scores at Thomas High School while keeping all other data associated with this student group intact. Both math and reading scores were replaced with "NaN", which represents a "Not-a-Number" value, for 461 student records. Although this may seem like a significant number, these score replacements did not result in any drastic change of the overall scores.



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

The assessment of the school summaries and all of the schools performance revealed that replacing the scores of the top five performing schools did not significantly affect their rankings. The second placed ranked school was Thomas High School. Thomas High School ranked second with a 91% overall passing score. When the math and reading scores were replaced the overall passing percentage dropped to 65%. This took them out of the top five performing school rankings. This was not a drastic enough change to place Thomas High School in the bottom five performing schools but it did lower their rank to 8th place.


### Average Math Scores by Grade & School

![Average Math Scores](https://user-images.githubusercontent.com/104540261/180646147-98c16b76-0afe-4f3f-91a4-722dbfa0f981.png)

### Average Reading Scores by Grade & School

![Average Reading Scores](https://user-images.githubusercontent.com/104540261/180646155-6e5f64ee-666e-4faa-aacf-831cf9fa3306.png)

Because the average reading and math scores were organized by grade level and school the data replacement did not drastically change the letter grades. In the summary table we can see "NaN" inserted into the Thomas High School ninth grade cells where as all the other remaining cells and tha data within remained unaffected.


### School Spending Summary

![School Spending](https://user-images.githubusercontent.com/104540261/180646160-a0eb4d3b-796e-4410-8e55-d8361fbb3d53.png)

The school spending summary shows us that where these changes were the most evident was in the $639-$644 spending range. In the $630-644 spending range we see a 6% drop in % passing math, a 7% drop in % passing reading, and a 6% drop in % overall passing. It is not evident that the change in data affected the spending ranges for average reading scores or average math scores.


### School Size Summary

![School Size](https://user-images.githubusercontent.com/104540261/180646170-c176d109-67bf-4dfa-b313-bbc02a8b4e54.png)

When we look at the school size data, we see that the average reading and math scores remain unaffected. But we also see that when we removed the nineth grade scores it did significantly affect the passing percentage for medium-sized schools in the (1,000-2,000) range. The data indicates that for medium-sized schools, % passing math, % passing reading, and % overall passing all decreased by 6%. Overall medium size schools, before the data change, were in the high performance range (91% overall passing). Small schools were (90 % overall passing) and large schools were (58% overall passing). When we change the data medium size schools overall passing percentage drops from 91% to 85% putting its rank second in performance.


### School Type Summary
```
# Assemble into DataFrame.
type_summary_df = pd.DataFrame({
          "Average Math Score" : type_math_scores,
          "Average Reading Score": type_reading_scores,
          "% Passing Math": type_passing_math,
          "% Passing Reading": type_passing_reading,
          "% Overall Passing": type_overall_passing})

type_summary_df
```

![School Type](https://user-images.githubusercontent.com/104540261/180788568-ca714da3-9b7e-4120-9f88-29753f8e3df1.png)

Lastly, when we look at the summary of school types, we can see that the correction to the nineth grade data affected passing percentages of charter schools and district schools. For both charter schools and district the average scores remained unaffected. In the charter schools the percentage of passing math dropped from 94% to 90%. In the percentage of passing reading ,in charter schools, the percentage dropped from 97% to 93%. Also in charter schools the overall passing percentage dropped from 90% to 87%. All in all the charter schools still out performed the district schools.

