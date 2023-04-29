# **University Grade Predictions**

## **keywords:** 
pandas, sklearn, regression, data cleaning, machine learning preprocessing, imputing, one-hot encoding, scaling, machine learning modeling, linear regression, decision tree, bagging, random forest, k-nearest neighbors, extreme gradient boosting, xgb, light gradient boosting machine, lgbm, gradient boosting, hyperparameter tuning, regression metrics, r2 score, feature engineering, feature selection, numpy

# Business Problem and Stakeholders

# Source of Data

The original data for this project appears on Kaggle.com: https://www.kaggle.com/datasets/Madgrades/uw-madison-courses. It was posted by user Madgrades, who obtained the data from the University of Wisconsin's registrar office (https://registrar.wisc.edu/grade-reports/). The data was extracted from PDF reports published by that office. Please see the Kaggle dataset for more information.

# Description of Data

The original data is provided in 10 .csv files on Kaggle. Collectively, they hold information on over 200,000 course sections held at the University of Wisconsin from Fall 2006 to Spring 2018. For most sections, the information includes the following:
- the instructor who taught the section (by ID, not name)
- the building and room where the section was held
- the subject the section belongs to
- the course name and number, and the course offering name and section number
- the section type
- the schedule of the section (which day(s) of the week the section met, if any, and the start time and end time)
- the year and term (Fall or Spring) the section was held
- the grade distribution for the section: counts of all grades given


# Data Visualization

## Start Times and Grades

Do students earn higher grades in classes that start later?
![later classes give out higher grades](https://user-images.githubusercontent.com/123273072/234943368-f5002587-eed3-4e30-b988-46837b54decc.png)

The answer is yes! The trend line plotted for each level of class difficulty shows a slightly positive slope. This means that students in classes that start later in the day, on average, earn higher grades than others. 

## Course Difficulty and Grades

Do students earn higher grades in easier classes? 

![are more advanced courses harder](https://user-images.githubusercontent.com/123273072/234943439-6bc09480-4581-478e-8676-6de33f089b42.png)

The answer is no! From the strip plot above, we can see that most of the average grades for all levels of difficulty cluster around the maximum 4.0. We can also see that there are fewer classes offered at the intermediate level, and even fewer at the advanced level. 

The grades for the elementary level classes do dip down a bit further into the lower values, and the advanced classes have higher grades. This is the opposite of what we thought! It looks like students are earning higher grades in more advanced classes. 

Why might this be? All students take elementary-level classes when they get into college; that's where everyone starts. Students also take elementary-level classes from subjects that they will eventually not major in, so they may not be as interested in those classes. But, as students find out what they are interested in or good at, they start taking intermediate- and advanced-level classes in those subjects. So, we are seeing the effect of better students in certain subjects doing well in their chosen fields. Students who won't do well in advanced classes in a subject don't take them.

## More Visualizations

More visualizations are available in the data_visualizations notebook in this repository.

# Machine Learning Model

# Summary and Recommendations