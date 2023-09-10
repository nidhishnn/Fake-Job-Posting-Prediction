# Marketing Campaign Prediction

## Problem Overview and Context from Kaggle
"Context - A superstore is planning for the year-end sale. They want to launch a new offer - gold membership, that gives a 20% discount on all purchases, for only $499 which is $999 on other days. It will be valid only for existing customers and the campaign through phone calls is currently being planned for them. The management feels that the best way to reduce the cost of the campaign is to make a predictive model which will classify customers who might purchase the offer. <br>

Objective - The superstore wants to predict the likelihood of the customer giving a positive response and wants to identify the different factors which affect the customer's response. You need to analyze the data provided to identify these factors and then build a prediction model to predict the probability of a customer will give a positive response." <br>

## Features and Target Variable Details from Kaggle
Response (target) - 1 if customer accepted the offer in the last campaign, 0 otherwise <br>
ID - Unique ID of each customer <br>
Year_Birth - Age of the customer <br>
Complain - 1 if the customer complained in the last 2 years <br>
Dt_Customer - date of customer's enrollment with the company <br>
Education - customer's level of education <br>
Marital - customer's marital status <br>
Kidhome - number of small children in customer's household <br>
Teenhome - number of teenagers in customer's household <br>
Income - customer's yearly household income <br>
MntFishProducts - the amount spent on fish products in the last 2 years <br>
MntMeatProducts - the amount spent on meat products in the last 2 years <br>
MntFruits - the amount spent on fruits products in the last 2 years <br>
MntSweetProducts - amount spent on sweet products in the last 2 years <br>
MntWines - the amount spent on wine products in the last 2 years <br>
MntGoldProds - the amount spent on gold products in the last 2 years <br>
NumDealsPurchases - number of purchases made with discount <br>
NumCatalogPurchases - number of purchases made using catalog (buying goods to be shipped through the mail) <br>
NumStorePurchases - number of purchases made directly in stores <br>
NumWebPurchases - number of purchases made through the company's website <br>
NumWebVisitsMonth - number of visits to company's website in the last month <br>
Recency - number of days since the last purchase <br>

## Conclusion
The supermarket intends to propose a new gold membership for customers which would give a 20% discount on all purchases for 499 dollars instead of the usual 999 dollars. The store needs information about which customers are likely to respond positively to its new marketing campaign, and factors which can help explain consumer behavior. The year in which an individual became a customer of the supermarket is the top predictor of whether he or she will respond favorably to the marketing campaign. Generally, if customers have been shopping at this particular supermarket for a long time, then it follows that they probably frequent this store over others and consequently prefer their assortment of goods and services. Additionally, the number of catalog purchases, which captures the number of purchased goods to be shipped in the mail, is the second leading predictor, suggesting consumers who have goods delivered may purchase more frequently and see value in an overall 20% discount on future purchases. The third leading predictor is for consumers with no teenage children, which is an interesting finding. Perhaps teenagers have greater influence on their parents as to which stores to visit than younger children, and either urge them to visit this supermarket or frequent a different store. After these three leading factors, the recency of visiting the supermarket, number of website visits in the last month, and the number of store purchases represent features with relatively high predictive power. <br>

The supervised learning machine learning models with the greatest overall performance were the RandomForest Classifier and XGBoost Classifier. Both achieved relatively high test accuracies of about 89%; however, in this problem, we are primarily interested in the minority class of whether individuals will respond positively to the new marketing campaign, so it will likely be more beneficial to evaluate the models' performance using precision and recall. For the positive class, the RandomForest model yielded a precision of 0.70 indicating that of the consumers predicted to respond positively, about 70% of them actually responded positively. The model's recall was low at 0.42 meaning of those who actually responded positively, only roughly 42% of them were predicted to respond positively. With the XGBoost model, the precision was 0.66 and recall was 0.49. The LogisticRegression model reached the highest recall of 0.79 but had one of the lowest precisions of 0.37 for the positive class. <br>

## Future Direction
In the future, it will be beneficial for the supermarket to collect more data about different consumers since there were only 2240 instances collected which may have made it difficult for the machine learning models to achieve higher performances. The supermarket may also want to provide specific features about the marketing campaign instead of just its consumers. There may be an issue with the marketing design, message, or content which affects customers' response to the campaign. Furthermore, I would try more advanced supervised learning techniques such as neural networks or deep learning given there is more data collected in the future. With the existing models, I would spend more time fine-tuning existing parameters to see if there would be a noticeable difference in perforamance, experiment with other novel features, and try new techniques to handle class imbalance, imputation, and standardization of the data. 
