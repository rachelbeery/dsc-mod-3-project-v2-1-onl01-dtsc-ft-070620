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
- Does gender have an influence on certain arrests/stops?
- Using a machine learning model can we find what feature has the most influence on an arrest?

# EDA

## 1. How does officer and subject race affect stop, frisk, and arrest?

![]()

## 2. Is there a difference in demographics among the different call types?

![]()


## 3. How does gender influence stop and arrest?

![]()

## 4. Does carrying a weapon affect subject arrested?

![]()

## Final Model using XGBoost and hypertuning features


## Feature Importance


![featureimp](https://github.com/rachelbeery/dsc-mod-3-project-v2-1-onl01-dtsc-ft-070620/blob/master/images/featureimportance.png?raw=true)
