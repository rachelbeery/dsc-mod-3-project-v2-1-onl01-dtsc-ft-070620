![seattlepolice](https://downtownseattle.org/app/uploads/2020/07/Seattle-police-cruiser-4x3-v1-1280x0-c-default.jpg)

# Module 3 Final Project Rachel Beery

## Introduction

Hello there, welcome to this Readme! Using a dataset of police officer stops and arrests for traffic violations, we will be creating a binary classification machine learning algorithm to see if arrests were made at a Terry Stop. 

## Background

Terry Stops are stops made of suspicious drivers. In Terry v. Ohio (https://www.oyez.org/cases/1967/67), a landmark Supreme Court case in 1967-8, the court found that a police officer was not in violation of the "unreasonable search and seizure" clause of the Fourth Amendment, even though he stopped and frisked a couple of suspects only because their behavior was suspicious. Thus was born the notion of "reasonable suspicion", according to which an agent of the police may e.g. temporarily detain a person, even in the absence of clearer evidence that would be required for full-blown arrests etc. 

## Objectives

I will be building a classifier to predict whether an arrest was made after a Terry Stop.

## Approach

The OSEUMiN data science workflow is utilized to effectively build a classifier to predict whether an arrest was made after a Terry Stop, given information about the presence of weapons, the time of day of the call, etc. Note that this is a binary classification problem. We will also be analyzing whether race (of officer or of subject) plays a role in whether or not an arrest is made.

## Data

In my project I will be utilizing the Terry Traffic Stops dataset that was provided by Flatiron School. The data set can be downloaded from the following website: https://catalog.data.gov/dataset/terry-stops
 
## Questions

- What officer demographics influence policing including arrests?
- Is there a difference in demographics among the different call types?
- Does gender have an influence on certain arrests/stops?
- Using a machine learning model can we find what feature has the most influence on an arrest?
- Does carrying a weapon affect subject arrested?

# EDA

## 1. What officer and subject demographics influence policing including arrests?

![offrace](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/offdemos.png?raw=true)

**There is a notably large amount of white officers compared to any other race group. We know that this may have some affects on policing and dynamics of the police department.** 

![subjectrace](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/offrace.png?raw=true)

**The demographics of subject pereceived race are diverse, but still with a majority of white subjects.**

![offracearrest](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/offracearrest.png?raw=true)

**White officers are by far seen from this image below to be the most likely race group to arrest rather than not arrest their subjects.**

![subracearrest](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/subracearrest.png?raw=true)

**The white and African-American or Black race group have the highest number of arrests. What is to note here is that in Seattle there is just over 7% of the population. This indicated that there are more black people arrested proportionately compared to any other race group. This is an occurance that should be investigated to understand why this is happening.** 


## 2. Is there a difference in demographics among the different call types?

![calltypes](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/calldemos.png?raw=true)

**Call type as we will see soon is an important feature in predicting an arrest. 911 is the largest feature group for arrests being made. This image additionally shows us that white subject again are the largest race group for all the call type categories. Black or African American is still proportionally larger than any other race group in all categories including 911 and Onview, and other.** 


## 3. Does gender have an influence on certain arrests/stops?

![genderoffrace](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/genderoffrace.png?raw=true)

**As seen from these images there is a great disparity of female police officers in the Seattle police departments. As in most cities around the world half the population is women. This increased male workforce may increase or decrease certain aspects of a stop or arrest.**

![officergender](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/officergender.png?raw=true)


## 4. Does carrying a weapon affect subject arrested?

![weaponarrest](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/weaponarrest.png?raw=true)

![weaponfrisk](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/weapontypefrisk.png?raw=true)


## 5. Using a machine learning model can we find what feature has the most influence on an arrest?

![xgboostmodel](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/xgboosttuning.png?raw=true)

### Our most successful model is our XGBoost mode
This confusion matrix shows us the results of our model. Our resulting accuracy and recall score are as follows: Train Accuracy: 0.589, Test Accuracy: 0.597, and the Cross Validation Recall 0.744. 

## Feature Importance

![featureimp](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/featureimportance.png?raw=true)

## Conclusions

### - Our XGBoost Model worked the best. We used this model to see what features had the greatest importance to our target of arrest flag. 

### - The top features were Weapon Type_None, Precinct_South, Call Type 911, Precinct_West, Subject Perceived Gender, Subject Perceived Race_White. This tells us that possessing a weapon was by far the strongest feature of importance. 

### - In second was precint south and west This may show us that this area may need to be evaluated for their practices and/or research needs to be done to understand why this area has such a high level of arrest. 

### - The third feature importance was subject perceived gender. In our EDA we explored this and also found that there is a clear difference in gender. This may show that women are seen as less of a threat to the officers that are evaluating whether to stop them and/or arrest these subjects.

### - The last feature of importance is seen to be subject perceived race as white. This can indicate that there is also biases happening so that those who are pulled over and white subjects are less likely to be arrested. 

# Further Recommendations

## If given more time and resources I would suggest the following
### * Recruitment of a more diverse officer workforce in Seattle
###       * There is a lack of female officers
###       * There is a lack of officers of other races other than white
### * Better record keeping
###       * There was a consistent 12,776 rows of missing values or nulls
### * Research into why certain precincts have more frisks and arrests
###       * Precinct South and West
