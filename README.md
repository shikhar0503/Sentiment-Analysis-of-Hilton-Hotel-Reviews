# Sentiment-Analysis-of-Hilton-Hotel-Reviews
 
![Hotel_logo](https://user-images.githubusercontent.com/106606656/211645486-be0f3a74-dc83-4468-8bb6-4a80d7493887.jpg)

## Business Objectives :

Online Hilton Hotel reviews are currently found on tripadvisor, trustpilot, and expedia. The majority of reviewers gave a score between 3 and 5, so if a new customer browses online reviews on any of the previously mentioned review sites, they may consider booking a room at the Hilton.

Opinions are shared constantly on social media platforms, and are read by their followers. The knowledge, of what these followers think about our hotel, from reading these online posts, could help us better understand the general public's perception of our hotel.

So by using Sentiment Analysis on existing hotel reviews, I created a model that can quantify on a scale of 1-5, how the feels about the hotel, and as a result, also how the readers think about it. If a review classifies to be less than a score of 3, the review could be looked into, find out why they had a negative opinion, and in return seek recommendations and fix the problem.

## Data Collection :

The data was downloaded from Github.

The 5 Hilton hotels with the highest number of reviews were chosen to scrape data: London Gatwick Airport, London Metropole, London Euston, London Croydon, and London - West End. 

Between these 5 hotels there were 17538 reviews, from which a sample of 5000 reviews was scraped for analysis.

The root URL used was : www.tripadvisor.co.uk

## Modelling :

The following modelling approach was used in the project:

1. Cleaning the raw data
2. Applying pre-processing to extract relevant tokens.
3. Apply TF-IDF vectorization to predict the ratings using ML Models.
4. Apply ANNs
5. Applying LSTMs

The detailed analysis and model creation can be found in the .ipynb file. 

## Result :

Some of the test images are given below.

The results from Classical ML Models are as below:
![test](Snips/Result_1.JPG)

The Logistic Regression turns out to be the best model and the confusion matrix using it is as follows:
![test](Snips/CM_1.JPG)

The results from ANNs are as follows:
![test](Snips/Result_2.JPG)
![test](Snips/CM_2.JPG)

The results from LSTMs are as follows:
![test](Snips/Result_3.JPG)
![test](Snips/CM_3.JPG)


## Conclusions :

After testing various ML models, ANNs and LSTMS, the ANN model using the test data and achieved an accuracy of 0.54 which is better than the Logistic Regression model and Bidirectional LSTMs.

The error is more contained within adjacent scores with the ANN model. Almost zero confusion between extreme scores 1 and 5, and minimal confusion with scores 2 and 4. Although a score of 3 can be harder to predict, there is definitely an improvement from the Stacking model. Around 97% of the time the model predicts at least the adjacent score to the actual score.

### Future Scope :
  - Use a bigger training dataset
  - Try a deeper neural network
  - Reduce complexity of classification to binary classification
  - Implement other pre-made vectorisation methods — word2vec or GloVe
  - Using Transformers and Bert Models
