# Hiring Process Analytics

This project analyzes various aspects of the hiring process for a multinational company (MNC) like Google. The analysis includes trends in the number of positions, hiring and rejection rates, salaries, and more. The primary tools used for this analysis are MS Excel formulas and functions.

## Table of Contents

- [Project Overview](#project-overview)
- [Approach](#approach)
- [Tech-Stack Used](#tech-stack-used)
- [Insights](#insights)
  - [Gender Hiring Statistics](#gender-hiring-statistics)
  - [Average Salary Analysis](#average-salary-analysis)
  - [Salary Class Intervals](#salary-class-intervals)
  - [Department Proportions](#department-proportions)
  - [Post Tiers Representation](#post-tiers-representation)
- [Result](#result)
- [Acknowledgements](#acknowledgements)

## Project Overview

The hiring process is a fundamental and crucial function of a company. This project involves analyzing hiring data to answer various questions, such as:

- How many males and females are hired?
- What is the average salary offered?
- What are the class intervals for salaries in the company?
- What is the proportion of people working in different departments?
- How can different post tiers be represented using charts?

## Approach

1. **Download the dataset**: Obtain the dataset containing the hiring data.
2. **Apply MS Excel formulas**: Use Excel formulas to perform the analysis.
3. **Analyze the results**: Interpret the results obtained from the formulas.
4. **Document findings**: Note down the findings and insights from the analysis.

## Tech-Stack Used

- **MS Excel 2013**: Used for all data analysis and visualization tasks.

## Insights

### Gender Hiring Statistics

To determine the number of males and females hired, apply the following formulas:

- `=COUNTIFS(E2:E7168, "Male", C2:C7168, "Hired")`
- `=COUNTIFS(E2:E7168, "Female", C2:C7168, "Hired")`

### Average Salary Analysis

To calculate the average salary offered in the company, use the following approach:

1. Calculate the overall average salary:
   ```excel
   =AVERAGE(G2:G7168)
   ```
2. Calculate the department-wise average salary:
   ```excel
   =AVERAGEIF(E2:E7168, "Finance Department", G2:G7168)
   =AVERAGEIF(E2:E7168, "General Management", G2:G7168)
   ```
   Repeat for other departments.

### Salary Class Intervals

To draw class intervals for salaries:

1. Find the maximum and minimum salaries.
2. Calculate the range (MAX - MIN) and divide it by 5 to get the interval increment.
3. Use the `CONCATENATE`, `LEFT`, and `RIGHT` functions to create the class intervals:
   ```excel
   =CONCATENATE(K23, "-", K23+K26)
   =CONCATENATE(RIGHT(K28), 5+1, "-", RIGHT(K28)+K26)
   ```

### Department Proportions

To draw pie charts or bar graphs showing the proportion of people working in different departments, use the following formula:

```excel
=COUNTIFS(E2:E7168, "Finance Department", C2:C7168, "Hired")
=COUNTIFS(E2:E7168, "General Management", C2:C7168, "Hired")
```

### Post Tiers Representation

To represent different post tiers using charts, apply:

```excel
=COUNTIFS(F2:F7168, "b9", C2:C7168, "Hired")
=COUNTIFS(F2:F7168, "c-10", C2:C7168, "Hired")
```

## Result

Through this project, significant insights were gained regarding the hiring process and data analysis using MS Excel. Key learnings include:

- Usage of `CONCATENATE`, `LEFT`, and `RIGHT` functions.
- Creating and interpreting various types of charts.
- Applying advanced Excel formulas for data analysis.

## Acknowledgements

Thank you for reviewing this project. It was an enlightening experience that enhanced my skills in data analysis and MS Excel.

**Author**: Ayush Yadav

---

Feel free to reach out for any questions or further discussions on this project.
