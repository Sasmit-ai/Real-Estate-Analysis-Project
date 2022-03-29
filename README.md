# Sydney-Real-Estate-Data-Analysis-Project

The motivation for this project came for my concerns for like-minded Young Aussie looking to purchase a new home in a market deemed to be a housing bubble. I was curious to see what various macroeconomic events such as the covid-19 pandemic had on the rigidity of pricing and determined the factors that when into the pricing of these properties. My implementation looked at normalising and developing new features to predict real estate pricing and predict the implications of various macroeconomic effects such as the pandemic.








## Methodology

A Real-time Data Analysis Project that looks to take data from realestate.com using a custom data pipeline and perform various analysis on pricing of the market. The project begins with an ETL to improve the quality of the dataset. This is followed up with an EDA to observe valuable insights in consumer behaviour and the distribution of properties on the current market. Initially, the dataset was fit and trained on various ML algorithms that are the best suit for the dataset. Initial validation testing saw a model that was able to predict test data at 61%. Implementing feature engineering by parsing JSON description data fields I was able to implement a sentiment feature into the model. This feature was developed using a one hot encoding approach to capture key phrases in the description attributing value to bespoke offerings by the real estate such as "waterfront views" or "near school". Normalisation of other attributes with a MinMaxScaler i was able to implement the dataset across multiple ML regression model including SVM, Ridge and Random Tree. However, after searching some interesting approaches to asset pricing in industry I found that the LightGBM Regression Model (with hyper parameter tuning using RandomizedSearchCV) was the most effective to optimise the model to this unique dataset. Finally testing yielded an accuracy rate of 93% across the test dataset, allowing to predict Sydney housing prices based on listing information.

A second analysis looked at seasonality changes in pricing for real estate.  By implementing linear regressor models such as ARIMA, SARIMA and FBProphet I was able to remodel the past 5 years and see the implication of a COVID world on the housing prices, with strong implication of volatility in the market. The FBProphet algorithm provides the best recreation of the non-covid market.
