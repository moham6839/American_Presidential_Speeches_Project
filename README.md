# American Presidential Speeches and Job Approval Ratings

https://i.guim.co.uk/img/static/sys-images/Guardian/Pix/pictures/2009/01/20/crowdspeech460.jpg?width=465&quality=45&auto=format&fit=max&dpr=2&s=a3779e4f4b2cb9a7a7005f178f2815f2

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

* Training Accuracy: 79%
* Testing Accuracy: 72%

## Initial Model: Decision Tree

![image](https://user-images.githubusercontent.com/77416319/152245698-d74fbb37-e0a0-4818-8900-52eac1a31133.png)

* Training Accuracy: 100%
* Testing Accuracy: 69%

## Hyperparameter Tuning using GridSearch: KNN

![image](https://user-images.githubusercontent.com/77416319/152246424-1bfa39ce-79a9-4f54-9c9d-091f094e28ea.png)

* Training Accuracy: 73%
* Testing Accuracy: 76%

## Hyperparameter Tuning using GridSearch: Decision Tree

![image](https://user-images.githubusercontent.com/77416319/152246569-2b39fb76-87de-4d82-b367-36c1938aa285.png)

* Training Accuracy: 68%
* Testing Accuracy: 72%

# Final Model

* Based on the results from performing a GridSearch on the selected models, K-Nearest Neighbors produced the outcome when predicting high job approval ratings based on the speech transcripts. Its training accuracy is 73%, while its testing accuracy is 76%, which indicates that the model is appropriately fitted to the data. 

# Word Associations

* Each President in combined dataset.
* Party affiliation (Democrat/Republican).
* High and low job approval ratings.
* Note: the lemmatization of the word 'us' is 'u'. For statistical purposes 'u' has not been taken out of the bag of words because of its high frequency among the speeches in this dataset and its relevance among the other words.


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

![image](https://user-images.githubusercontent.com/77416319/152268337-4cf39516-2179-46c8-8686-df451f4b2889.png)

![image](https://user-images.githubusercontent.com/77416319/152268429-3a63a262-3ed1-4a95-abee-f9565f1cbce0.png)

## Republican Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152268477-f85bd096-e32c-4801-ab1e-acb354613c35.png)

![image](https://user-images.githubusercontent.com/77416319/152268533-1d75d9d9-fbf8-451c-87d9-4e1043b3e25c.png)

## High Job Approval Rating Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152268569-742adc80-abbd-4ea4-8351-dcbcf71b5835.png)

![image](https://user-images.githubusercontent.com/77416319/152268645-18993f49-ba59-4b88-8e8f-7061046d8a00.png)

## Low Job Approval Rating Word Frequency

![image](https://user-images.githubusercontent.com/77416319/152268709-38f35140-891e-495e-9edd-be3facfac8af.png)

![image](https://user-images.githubusercontent.com/77416319/152268793-8c38caff-d036-42c2-9f93-84fe94008e08.png)


## Conclusion

* KNN - best model to predict high approval ratings using speech transcripts.
* Most frequent words throughout speeches: People, American, America, Year; terms used to bring people together.
* Words that are more frequent in high than low job approval ratings in top 25: Must, Child. Life.
* Words that are more frequent in low than high job approval ratings: Country, Job, Us. 
* Emphasizing children and communicating urgency - leads to high job approval ratings.
* Terms associated with low job approval ratings - used to attempt to bring people together and emphasize the economy; not enough to gain favorable rating.


## Next Steps

* Explore previous presidents and their speech transcripts.
* Analyze Trump’s speeches towards end of his presidency.
* Has the pandemic affected what words are said by Trump/Biden?
* Look at bigrams and tri-grams to see if there are specific phrases presidents use.
* Look at other speeches given to see if there are similarities and/or differences.
* Analyze further how party affiliation impacts job approval ratings; similarities/differences?
* Relationship between speeches and the economy; frequency of words associated with high/low unemployment rates.




https://cdn.cnn.com/cnnnext/dam/assets/201211111910-01-barack-obama-2009-inauguration-01-20-2009-full-169.jpg










