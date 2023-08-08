# Optimizing Direct Marketing Strategies: Insights from Machine Learning Analysis on Term Deposit Subscriptions

## Introduction

In order to optimize our direct marketing efforts, we applied machine learning models to our customer data to understand the key factors influencing a client's decision to subscribe to a term deposit. We used Decision Tree, KNN and Logistic Regression models, well-known models for classification problems. This report presents the findings from these models, including the most influential factors, and provides recommendations on how we can improve our marketing efforts based on these insights.

## Key Findings

### Model metrics

Accuracy is the ratio of the total number of correct predictions to the total number of predictions made. All the models (including the Decision Tree model when limited to a maximum depth of 6) had a similar accuracy of approximately 90%, just above the baseline of 88%.

In imbalanced datasets like this one where one class significantly outnumbers the other, accuracy can be misleading. A model that simply predicts the majority class for all instances will have high accuracy but may be failing to correctly identify instances of the minority class. In such cases, metrics like precision, recall, and the F1 score are often more informative, as they provide more detailed insight into the model's performance for each class.

Precision is the ratio of true positive predictions to the total number of positive predictions made (including both true positives and false positives). In other words, it represents the fraction of positive predictions that were actually correct. Considering precision, the Logistic Regression model was 66% on both training and test datasets, the KNN model on the training dataset was 70%, falling to 52% on the test dataset, and the tuned Decision Tree model on the training dataset was 73%, falling to 67% on the test dataset.

Recall, also known as sensitivity or true positive rate, is the ratio of true positive predictions to the total number of actual positive instances (including both true positives and false negatives). In other words, it represents the fraction of actual positive instances that were correctly identified by the model. Considering recall, the Logistic Regression model was 22% on both training and test datasets, the KNN model on the training dataset was 38%, falling to 27% on the test dataset, and the tuned Decision Tree model was around 23% on both training and test datasets.

The F1 score is the harmonic mean of precision and recall, providing a single metric that balances the two. It is particularly useful when you want to balance precision and recall. Considering F1, the Logistic Regression model was 33% on both training and test datasets, the KNN model on the training dataset was 50%, falling to 36% on the test dataset, and the tuned Decision Tree model was around 35% on both training and test datasets.

In a direct marketing context, where both reaching potential subscribers and efficiency in resources are important, the F1 score might often be the most relevant metric. It ensures that the marketing campaign is neither too conservative (missing potential subscribers) nor too aggressive (wasting resources on unlikely subscribers).

### Important factors

Influential Factors: Considering the Logistic Regression and Decision Tree models, we found that the most influential factors include the number of employees (nr.employed), the outcome of the previous marketing campaign (poutcome_success), and the month of last contact being March (month_mar). These factors were most positively associated with a client's decision to subscribe to a term deposit.

Negative Factors: The Logistic Regression model also revealed factors that decreased the likelihood of a client subscribing to a term deposit. These include the employment variation rate (emp.var.rate), contact method being telephone (contact_telephone), and the month of last contact being June, November, or May (month_jun, month_nov, month_may).

##  Recommendations

Based on our findings, we recommend the following actions to improve our direct marketing campaigns:

Focus on Key Influential Factors: Emphasize clients with favorable values for the most influential factors, such as those who had a successful outcome in the previous marketing campaign, as they are more likely to subscribe to a term deposit.

Re-evaluate Contact Method and Timing: Our findings suggest that contacting clients by telephone and during certain months (June, November, and May) is less effective. We should re-evaluate our approach during these times and consider alternative contact methods.

Consider Economic Indicators: Keep an eye on economic indicators like the number of employees and the Euribor 3 month rate, as these were found to be influential in a client's decision to subscribe to a term deposit.

## Conclusion

Our analysis provides insight into the factors that influence a client's decision to subscribe to a term deposit. By focusing on the most influential factors and re-evaluating our approach for the negative factors, we can optimize our direct marketing efforts and improve the effectiveness of our campaigns.

Please find the full analysis in [analysis.ipynb](analysis.ipynb)