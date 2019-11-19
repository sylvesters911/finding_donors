# finding_donors
Finding donors project was a project that was performed as a first assignment on my data science degree. The README file consist of the contents that is provided by the Udactiy course [here](https://github.com/sylvesters911/finding_donors/blob/master/finding_donors.ipynb) and summarized in the README file. 

##### Table of Content
1. [Installation](#Installation)
2. [Project Summary](#Project-Summary)
3. [Data](#Data)
4. [Evaluate the Results](#Results)
5. [Acknowledgements](#Acknowledgements)

## Installation
The code should run using the stadard Python packages (Python versions 3.*).

This project also uses the following packages:

1. Python
2. NumPy
3. pandas
4. scikit-learn (v0.17)
5. Matplotlib

## Project Summary
This project uses several supervised algorithms this is spesified in the code to model an individuals' income. The data that is used was collected from the 1994 U.S. Census. The model will be further optimize to best model the data. 

The goal with this implementation is to accurately predict if an individual makes more than $50,000. Understanding an individual's income can help a the company to get the maximum donation or not contact the individual with features that is available either from direct sources or public information. 

The dataset for this project originates from the UCI Machine Learning Repository [here](https://archive.ics.uci.edu/ml/datasets/Census+Income). The datset was donated by Ron Kohavi and Barry Becker, after being published in the article "Scaling Up the Accuracy of Naive-Bayes Classifiers: A Decision-Tree Hybrid". You can find the article by Ron Kohavi online [here](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf). The data we investigate here consists of small changes to the original dataset, such as removing the 'fnlwgt' feature and records with missing or ill-formatted entries.

## Data
A cursory investigation of the dataset will determine how many individuals fit into either group, and will tell us about the percentage of these individuals making more than \$50,000. The following as computed and assessed:

The total number of records, 45222'
The number of individuals making more than \$50,000 annually, 11208.
The number of individuals making at most \$50,000 annually, 34014.
The percentage of individuals making more than \$50,000 annually, 24.78439697492371%.

The following Features was explored:
1. age: continuous.
2. workclass: Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked.
3. education: Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool.
4. education-num: continuous.
4. marital-status: Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse.
6. occupation: Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces.
7. relationship: Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried.
8. race: Black, White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other.
9. sex: Female, Male.
10. capital-gain: continuous.
11. capital-loss: continuous.
12. hours-per-week: continuous.
13. native-country: United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands.

Before data can be used as input for machine learning algorithms, it often must be cleaned, formatted, and restructured — this is typically known as preprocessing. 

Fortunately, for this dataset, there are no invalid or missing entries we must deal with, however, there are some qualities about certain features that must be adjusted. This preprocessing can help tremendously with the outcome and predictive power of nearly all learning algorithms.

A dataset may sometimes contain at least one feature whose values tend to lie near a single number, but will also have a non-trivial number of vastly larger or smaller values than that single number. Algorithms can be sensitive to such distributions of values and can underperform if the range is not properly normalized. 

It is common practice to apply a logarithmic transformation on the data so that the very large and very small values do not negatively affect the performance of a learning algorithm. Using a logarithmic transformation significantly reduces the range of values caused by outliers. Care must be taken when applying this transformation however: The logarithm of 0 is undefined, so we must translate the values by a small amount above 0 to apply the the logarithm successfully.

In addition to performing transformations on features that are highly skewed, it is often good practice to perform some type of scaling on numerical features. Applying a scaling to the data does not change the shape of each feature's distribution however, normalization ensures that each feature is treated equally when applying supervised learners. Note that once scaling is applied, observing the data in its raw form will no longer have the same original meaning.

Typically, learning algorithms expect input to be numeric, which requires that non-numeric features (called categorical variables) be converted. One popular way to convert categorical variables is by using the one-hot encoding scheme. One-hot encoding creates a "dummy" variable for each possible category of each non-numeric feature. For example, assume someFeature has three possible entries: A, B, or C.

## Results

Results are available [here](https://github.com/sylvesters911/finding_donors/blob/master/finding_donors.ipynb)

## Acknowledgements
Udacity [here](https://www.udacity.com/)
