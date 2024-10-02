# Student Performance Data: Math and Portuguese Courses

This repository contains two datasets that track student performance in Math and Portuguese courses. The datasets are provided in CSV format:

- **student-mat.csv**: Contains data for the Math course.
- **student-por.csv**: Contains data for the Portuguese course.

## Dataset Structure

Each dataset has identical structure with 33 attributes that provide a comprehensive view of students' personal, academic, and social factors influencing their performance.

### Features

1. **school**: Student's school (binary: "GP" = Gabriel Pereira, "MS" = Mousinho da Silveira).
2. **sex**: Student's gender (binary: "F" = female, "M" = male).
3. **age**: Student's age (numeric: 15-22 years).
4. **address**: Home address type (binary: "U" = urban, "R" = rural).
5. **famsize**: Family size (binary: "LE3" = ≤3, "GT3" = >3).
6. **Pstatus**: Parent's cohabitation status (binary: "T" = living together, "A" = apart).
7. **Medu**: Mother's education (numeric: 0 = none, 1 = primary (4th grade), 2 = 5th-9th grade, 3 = secondary education, 4 = higher education).
8. **Fedu**: Father's education (numeric: same as Medu).
9. **Mjob**: Mother's job (nominal: "teacher", "health", "services", "at_home", "other").
10. **Fjob**: Father's job (nominal: same as Mjob).
11. **reason**: Reason for choosing the school (nominal: "home" = close to home, "reputation" = school reputation, "course" = course preference, "other").
12. **guardian**: Guardian (nominal: "mother", "father", "other").
13. **traveltime**: Home to school travel time (numeric: 1 = <15 min., 2 = 15-30 min., 3 = 30 min.-1 hr, 4 = >1 hr).
14. **studytime**: Weekly study time (numeric: 1 = <2 hrs, 2 = 2-5 hrs, 3 = 5-10 hrs, 4 = >10 hrs).
15. **failures**: Number of past class failures (numeric: n if 1 ≤ n < 3, otherwise 4).
16. **schoolsup**: Extra educational support (binary: "yes", "no").
17. **famsup**: Family educational support (binary: "yes", "no").
18. **paid**: Extra paid classes (binary: "yes", "no").
19. **activities**: Participation in extracurricular activities (binary: "yes", "no").
20. **nursery**: Attended nursery school (binary: "yes", "no").
21. **higher**: Plans for higher education (binary: "yes", "no").
22. **internet**: Internet access at home (binary: "yes", "no").
23. **romantic**: In a romantic relationship (binary: "yes", "no").
24. **famrel**: Quality of family relationships (numeric: 1 = very bad, 5 = excellent).
25. **freetime**: Free time after school (numeric: 1 = very low, 5 = very high).
26. **goout**: Frequency of going out with friends (numeric: 1 = very low, 5 = very high).
27. **Dalc**: Workday alcohol consumption (numeric: 1 = very low, 5 = very high).
28. **Walc**: Weekend alcohol consumption (numeric: 1 = very low, 5 = very high).
29. **health**: Current health status (numeric: 1 = very bad, 5 = very good).
30. **absences**: Number of school absences (numeric: 0-93).

### Course-specific Grades
31. **G1**: First period grade (numeric: 0-20).
32. **G2**: Second period grade (numeric: 0-20).
33. **G3**: Final grade (numeric: 0-20, this is the output target).

### Identifying Common Students
There are 382 students present in both datasets. These students can be matched by comparing the unique attributes they share, allowing for analysis across both subjects.

## Usage

To load and preprocess the datasets, you can use the following Python code:

```python
import pandas as pd

# Load datasets
math_df = pd.read_csv('student-mat.csv')
por_df = pd.read_csv('student-por.csv')

# Display the first few rows
print(math_df.head())
print(por_df.head())
