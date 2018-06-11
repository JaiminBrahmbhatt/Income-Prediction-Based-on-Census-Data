### Supervised Learning
# Predicting Income from Census Data

------

![census](http://funkydigitalagency.co.uk/wp-content/uploads/2016/04/Charity-Hands.png)

## Overview  

In this project, we employ several supervised learning algorithms to accurately model individuals' income using data collected from the 1994 U.S. Census. We choose the best candidate algorithm from preliminary results and further optimize this algorithm to best model the data. Our goal with this implementation is to construct a model that accurately predicts whether an individual makes more than $50,000. This sort of task can arise in a non-profit setting, where organizations survive on donations. Understanding an individual's income can help a non-profit better understand how large donation to request, or whether or not they should reach out, to begin. While it can be difficult to determine an individual's general income bracket directly from public sources, we can infer this value from other publicly available features.


## Dataset

The modified census dataset consists of approximately 32,000 data points, with each data point having 13 features. This dataset is a modified version of the dataset published in the paper *"Scaling Up the Accuracy of Naive-Bayes Classifiers: a Decision-Tree Hybrid",* by Ron Kohavi. You may find this paper [online](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf), with the original dataset hosted on [UCI](https://archive.ics.uci.edu/ml/datasets/Census+Income).

**Features**
- `age`: Age
- `workclass`: Working Class (Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked)
- `education_level`: Level of Education (Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool)
- `education-num`: Number of educational years completed
- `marital-status`: Marital status (Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse)
- `occupation`: Work Occupation (Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces)
- `relationship`: Relationship Status (Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried)
- `race`: Race (White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black)
- `sex`: Sex (Female, Male)
- `capital-gain`: Monetary Capital Gains
- `capital-loss`: Monetary Capital Losses
- `hours-per-week`: Average Hours Per Week Worked
- `native-country`: Native Country (United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands)

**Target Variable**
- `income`: Income Class (<=50K, >50K)

## Models

The three models that seem appropriate for the specific problem and will be evaluated are: 
- Logistic Regression
- Support Vector Machines (SVM)
- Gradient Boosting  

After evaluating their performance, we concluded that Gradient Boosting is the most appropriate

![models](images/plots.png)

## Results

By fine-tuning its parameters we were able to achieve:  
- Accuracy Score: 0.8719
- F-score: 0.7547  
(both on the testing data)  

We were also able to conclude on the five most important features.  

![features](images/top_5.png)

-----

#### Notes
- Adapted from a Supervised Learning assignement during my study for Udacity's [Machine Learning Engineer NanoDegree](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009t)  
- The template and helper code provided by Udacity and can be found on [this](https://github.com/udacity/machine-learning/tree/master/projects/finding_donors) GitHub repository.
