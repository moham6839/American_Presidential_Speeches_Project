# American Presidential Speeches and Job Approval Ratings

## Overview

* Explore the relationship between Presidential Speeches and a President’s job approval ratings.
* Identify the frequency of words spoken in Presidential speeches.
* What constitutes a high and low job approval rating?
* Words associated with high and low job approval ratings.
* Similarities and differences between each President; does party affiliation make a difference in words spoken?

## Data Sources

* Presidential Speeches - Miller Center UVA
* Presidential Job Approval Ratings - Gallup

## Gallup

* Global analytics firm; began reporting on presidential job approval since 1938.
* Ratings data from Truman-Present.
* 1938-2008 - ratings based on reporting job approval ratings from discrete, multiday surveys.
* 2009 - 2017 - daily sampling and interviewing on tracking survey; 3-day rolling average.
* 2019 - reverted back to 1938-2008 methodology.

## Data Cleaning/EDA

* Ratings and Speeches - Clinton, Bush, Obama Trump.
* Speeches - Date, President, Political Party, Speech Title, Transcript.
* Job approval ratings - Start/End Date, Approve, Disapprove, Unsure.
* High job approval rating > 50%, low job approval ratings < 50%.
* Combine speeches dataset and job approval dataset based on month and year speech and rating were given.

## Initial Models Used

* K-Nearest Neighbors
* Bagging Tree
* Random Forest
* Naive Bayes
* Logistic Regression
* Decision Tree
* XG Boost

## Initial Model: K-Nearest Neighbors

![image](https://user-images.githubusercontent.com/77416319/152244088-9a7b6020-931c-494c-bbb4-f3ad84121e97.png)



## Initial Model: Decision Tree

![image](https://user-images.githubusercontent.com/77416319/152245698-d74fbb37-e0a0-4818-8900-52eac1a31133.png)



## Hyperparameter Tuning using GridSearch: KNN

![image](https://user-images.githubusercontent.com/77416319/152246424-1bfa39ce-79a9-4f54-9c9d-091f094e28ea.png)



## Hyperparameter Tuning using GridSearch: Decision Tree

![image](https://user-images.githubusercontent.com/77416319/152246569-2b39fb76-87de-4d82-b367-36c1938aa285.png)


## Word Associations

* Each President in combined dataset.
* Party affiliation (Democrat/Republican).
* High and low job approval ratings.

# Top 25 Words

## President Clinton Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152247999-a542d773-9ffc-4b17-944b-09b45d69b431.png)

![image](https://user-images.githubusercontent.com/77416319/152248103-5d8d4d0b-024e-4c6c-a9bd-42f8336480d8.png)

## President Bush Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152249352-c249a9bf-332f-4db7-8aa4-cafad655ddbf.png)

![image](https://user-images.githubusercontent.com/77416319/152250914-858924f4-5df4-4842-aec6-0a632b1a5237.png)

## President Obama Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152251490-f282ac11-aaa7-43f6-ae38-a8935c340cf2.png)

![image](https://user-images.githubusercontent.com/77416319/152251533-1fb3b07e-f99c-4a23-8d74-a7b2de42d196.png)

## President Trump Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152252155-6f903bcc-073d-4c67-bc4a-2baf71f7b270.png)

![image](https://user-images.githubusercontent.com/77416319/152252227-65cab19d-bcfb-48a6-9ccf-9ca6b79bd405.png)

## Democrat Word Frequency

## Republican Word Frequency

## High Job Approval Rating Word Frequency

## Low Job Approval Rating Word Frequency



















