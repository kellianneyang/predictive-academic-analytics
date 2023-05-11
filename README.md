# **University Grade Predictions**

## **keywords:** 
pandas, sklearn, regression, data cleaning, machine learning preprocessing, imputing, one-hot encoding, scaling, machine learning modeling, linear regression, decision tree, bagging, random forest, k-nearest neighbors, extreme gradient boosting, xgb, light gradient boosting machine, lgbm, gradient boosting, hyperparameter tuning, regression metrics, r2 score, feature engineering, feature selection, numpy


# Business Problem and Stakeholders

What are the factors that contribute to the average grade of a class? Do the students' hard work, dedication, and intellect determine their grades? Or, can grades be predicted by section-level variables, such as start time, class length, and subject?

Stakeholders for this problem are many and varied. Students who want a class where a good grade is virtually guaranteed, as well as their parents, are extremely interested in this problem. They would like to register for classes that are certain to give out high grades, especially if they need to take classes outside of their major course of study (the classes that they are ostensibly most interested in taking anyway). 

Certain university offices, such as career services and advising, would also benefit from answers to these questions. Career counselors would be able to suggest courses to students to explore diverse career fields that students would be more willing to take a chance on, if they knew the courses wouldn't bring their grades down. Advisors' student satisfaction ratings would rise if they could recommend courses to students that students end up getting good grades in. 

Tutoring startups will also want this data. If they can predict which courses give out the worst grades, they can target their hiring of tutors to those classes and focus their marketing efforts towards those subjects and classes as well.

# Source of Data

The original data for this project appears on Kaggle.com: https://www.kaggle.com/datasets/Madgrades/uw-madison-courses. It was posted by user Madgrades, who obtained the data from the University of Wisconsin's registrar office (https://registrar.wisc.edu/grade-reports/). The data was extracted from PDF reports published by that office. Please see the Kaggle dataset for more information.

# Description of Data

The original data is provided in 10 .csv files on Kaggle. Collectively, they hold information on over 200,000 course sections held at the University of Wisconsin from Fall 2006 to Spring 2018. For most sections, the features are:
- the instructor who taught the section (by numeric ID, not name)
- the building and room where the section was held
- the subject the section belongs to
- the course name and number, and the course offering name and section number
- the section type
- the schedule of the section (which day(s) of the week the section met, if any, and the start time and end time)
- the year and term (Fall or Spring) the section was held
- the grade distribution for the section: counts of all grades given


# Data Visualization Insights

## Classes Starting Later in the Day Give Out Higher Grades

![later classes give out higher grades](https://user-images.githubusercontent.com/123273072/234943368-f5002587-eed3-4e30-b988-46837b54decc.png)

Does the time of day a class starts affect the average grade of that class?

The answer is yes! The trend line plotted for each level of class difficulty shows a slightly positive slope. This means that students in classes that start later in the day, on average, earn higher grades than others. 

## Lower Grades in Lower-Level Courses

![are more advanced courses harder](https://user-images.githubusercontent.com/123273072/234943439-6bc09480-4581-478e-8676-6de33f089b42.png)

Do students earn higher grades in lower-level classes? 

The answer is no! From the strip plot above, we can see that most of the average grades for all levels of difficulty cluster around the maximum 4.0. We can also see that there are fewer classes offered at the intermediate level, and even fewer at the advanced level. 

The grades for the elementary level classes reach down farther into the lower values, and the advanced classes have higher grades. This is the opposite of conventional thinking that it is easier to earn higher grades in lower-level classes. It looks instead like students are earning higher grades in more advanced classes. The implication here is that students shouldn't take as many low-level courses as possible. They should consider advancing in the subjects they do well in, and not be afraid that higher-level classes in that subject will wreck their GPA. 

Why might this be? One possible explanation follows. All students take elementary-level classes when they get into college; that's where everyone starts. Students also take elementary-level classes from subjects that they will eventually not major in, so they may not be as interested in those classes. But, as students find out what they are interested in or good at, they start taking intermediate- and advanced-level classes in those subjects. So, we are seeing the effect of better students in certain subjects doing well in their chosen fields. Students who won't do well in advanced classes in a subject don't take them.

## More Insights with Visualizations

More visualizations pertinent to core data insights are available in the data_visualizations notebook in this repository.

# Machine Learning Model

The model that had the lowest errors on the out-of-sample test data was the default Random Forest Regressor. It was able to predict the average grade of a section, on a 4.0 scale, to within +/-0.16 (mean absolute error). 

This means that we can pick courses that will give high grades for students to take! If a student or parent comes and wants to pick a class to take that will have a high average grade, we can predict those courses.

# Summary and Recommendations

Take courses that are later in the day, with more experienced instructors, on higher-level classes to improve chances that the average grade of the class will be higher. Stick to subjects that usually give out higher grades like English courses; stay away from math!
