# Optimizing Direct Marketing Strategies: Insights from Machine Learning Analysis on Term Deposit Subscriptions

## Introduction
In order to optimize our direct marketing efforts, we applied machine learning models to our customer data to understand the key factors influencing a client's decision to subscribe to a term deposit. We used Decision Tree, KNN and Logistic Regression models, well-known models for classification problems. This report presents the findings from these models, including the most influential factors, and provides recommendations on how we can improve our marketing efforts based on these insights.

## Key Findings

Model Performance: The Logistic Regression and KNN model showed good generalizability, with an accuracy of approximately 90% on both the training and test datasets. The Decision Tree model, when limited to a maximum depth of 6, also showed good performance with a similar accuracy of approximately 90%.

Influential Factors: Consider the Logistic Regression and Decision Tree models, we found that the most influential factors include the number of employees (nr.employed), the outcome of the previous marketing campaign (poutcome_success), and the month of last contact being March (month_mar). These factors were most positively associated with a client's decision to subscribe to a term deposit.

Negative Factors: The Logistic Regression model also revealed factors that decreased the likelihood of a client subscribing to a term deposit. These include the employment variation rate (emp.var.rate), contact method being telephone (contact_telephone), and the month of last contact being June, November, or May (month_jun, month_nov, month_may).

##  Recommendations

Based on our findings, we recommend the following actions to improve our direct marketing campaigns:

Focus on Key Influential Factors: Emphasize clients with favorable values for the most influential factors, such as those who had a successful outcome in the previous marketing campaign, as they are more likely to subscribe to a term deposit.

Re-evaluate Contact Method and Timing: Our findings suggest that contacting clients by telephone and during certain months (June, November, and May) is less effective. We should re-evaluate our approach during these times and consider alternative contact methods.

Consider Economic Indicators: Keep an eye on economic indicators like the number of employees and the Euribor 3 month rate, as these were found to be influential in a client's decision to subscribe to a term deposit.

## Conclusion

Our analysis provides insight into the factors that influence a client's decision to subscribe to a term deposit. By focusing on the most influential factors and re-evaluating our approach for the negative factors, we can optimize our direct marketing efforts and improve the effectiveness of our campaigns.

Please find the full analysis in [analysis.ipynb](analysis.ipynb)