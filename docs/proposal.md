# CS 4641 Proposal

### Introduction and Background

The stock market's fluctuations are influenced by multiple factors including “political events, economic conditions, and investor psychology [6]”. Recent trends show an increased use of machine learning (ML) techniques to improve market forecast accuracy and efficiency. Strader [2] categorizes recent ML research into four main approaches for stock prediction: artificial neural networks, support vector machines, genetic algorithms combined with other techniques, and hybrid of multiple algorithms. These methods aim to enhance the precision of stock market forecasts. We will be using the first three approaches for our project.

The dataset is New York Stock Exchange data from 2010 to 2016, which includes the daily prices, prices adjusted for stock split, company descriptions, and underlying metrics drawn from the annual SEC 10K filing.



### Problem Definition

1. Problem

    Traditionally, market trends were learned through experience, but now, this is impractical due to the market's size and speed. Basic statistical analysis alone is insufficient for making informed decisions in a fast-trending market.
2. Motivation

    We aim to identify the most accurate market prediction machine learning algorithms that will offer consumers analyses of real-time financial and economic data for making decisions.




### Methods

For our first model, we chose to implement linear regression. This type of model typically performs very well when there is a need to predict trends and movements in data where outcomes are continuous. Linear regression is a relatively simple algorithm as well, which serves as an excellent starting point for the problem that allows us to determine how to proceed with future implementations.

Data preprocessing was done by calculating rolling averages. For stock prices, rolling averages are typically very well-suited to predicting market trends, both short and long-term [1]. These rolling averages were treated as features in the model. In total, we used 6 different features to predict the stock’s closing price: open price, low, high, volume, and the rolling average price over both 5 and 10 days. If there was an invalid value in any point in a row, that row was removed from the data. Because of the high number of rows and low amount of missing data, we do not expect a point’s removal to have too high of an impact on the overall data.

Model validation was done by using k-fold validation using 5 and 10 folds, and evaluated using performance metrics including Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) to measure prediction accuracy, R² to gauge the model's explanatory power, and Precision and Recall for classification accuracy. The goal is to minimize MAE and RMSE for close-to-actual predictions, maximize R² for high predictive relevance, and achieve high Precision and Recall for reliable classification. Achieving the goals for these metrics will indicate that the model is capable of making accurate and reliable stock market predictions.

For the rest of the project, we plan on using the following libraries and algorithms:
1. Preprocessing Methods

    1. Pandas Library

        Enables dataset loading and handling missing data by dropping or filling them.

    2. Matplotlib

        Useful for plotting stock closing prices over time, comparing stocks, or visualizing trade volumes.

	3. Numpy Library

        Aids in data standardization, centering by mean removal, and scaling by standard deviation.



2. ML Algorithms

    1. Neural network algorithm

        Neural networks use historical stock data (like open and close prices, trading volume) to predict future prices, employing techniques like Genetic Algorithm - Artificial Neural Network and Harmony Search - Artificial Neural Network for stock market forecasting.

    2. Support vector Machine algorithm (Supervised)

        SVM is a supervised learning algorithm used for classification or regression, including predicting stock market price directions.

	3. LSTM algorithm

        LSTM's ability to remember patterns for long periods makes it effective for predicting stock prices using historical data. Nabipour found that deep LSTM with an embedded layer performed better than LSTM with automatic encoding [5].

    4. Random Forest Algorithm

        Random Forest is an ensemble method combining weak models into a strong one, capable of managing large, complex data sets. It's useful for analyzing vast stock price data to identify key variables for classification.

	5. Radial Basis Function

        A Radial Basis Function (RBF) is a mathematical function that computes the similarity between data points in a multidimensional space. It's often used in machine learning for tasks such as interpolation, approximation, and classification [4].




### (Potential) Results and Discussion
![image info](./pictures/image.png)
The performance metrics include Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) to measure prediction accuracy, R<sup>2  to gauge the model's explanatory power, and Precision and Recall for classification accuracy. The goal is to minimize MAE and RMSE for close-to-actual predictions, maximize R<sup>2  for high predictive relevance, and achieve high Precision and Recall for reliable classification. Achieving the goals for these metrics will indicate that the model is capable of making accurate and reliable stock market predictions.

### Reference


[1] T. J. Strader et al, &#34;Machine Learning Stock Market Prediction Studies: Review and Research Directions,&#34; Journal of International Technology and Information Management, vol. 28, (4), pp. 63-83, 2019. Available: https://www.proquest.com/scholarly-journals/machine-learning-stock-market-prediction-studies/docview/2419750880/se-2.

[2] D. Sheth and M. Shah, &#34;Predicting stock market using machine learning: best and accurate way to know future stock prices,&#34; International Journal of Systems Assurance Engineering and Management, vol. 14, no. 1, pp. 1-18, Jan. 2023, doi: 10.1007/s13198-022-01811-1.


[3] A. Khan et al., &#34;A performance comparison of machine learning models for stock market prediction with novel investment strategy,&#34; PLOS ONE, vol. 18, no. 9, p. e0286362, Sep. 2023, doi: 10.1371/journal.pone.0286362.

[4] K. S. R. Vanukuru, &#34;Stock Market Prediction Using Machine Learning,&#34; International Research Journal of Engineering and Technology (IRJET), vol. 05, no. 10, pp. 1032, Nov. 2018, DOI: 10.13140/RG.2.2.12300.77448.

[5] Nabipour, M.; Nayyeri, P.; Jabani, H.; Mosavi, A.; Salwana, E.; S., S. Deep Learning for Stock Market Prediction. Entropy 2020, 22, 840. https://doi.org/10.3390/e22080840
https://ieeexplore.ieee.org/abstract/document/7783235
https://scholarworks.lib.csusb.edu/jitim/vol28/iss4/3/


## Gantt Chart

https://docs.google.com/spreadsheets/d/1gdDA0MfhDgKv55N_eectzp0srOznWuNAZxiQP6nlWtM/edit?usp=sharing
