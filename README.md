Commodity-Demand-Forecasting
=
Goals
-
* Compare the accuracy of various time series forecasting algorithms such as Prophet, LightGBM and Mixture Model<br>
* Analyzed actual product sales data in depth to predict future demand over a three-month period.Find the best way to deal with seasonality, and Compare the models separately by pooling them together. Does deep learning work better thantime series forecasting algorithms? <br>

Requirements
-
*The dataset can be downloaded from [this Kaggle competition](https://www.kaggle.com/competitions/demand-forecasting-kernels-only).<br>
*In addition to the [Anaconda](https://www.anaconda.com/) libraries, you need to install `numpy`, `pandas`, `lightgbm`, `statsmodels.api`, `matplotlib.pyplot`, `seaborn`and`SelectFromModel`.<br>

Datasets and Evaluation
-
* This thesis aims to forecast monthly sales for the next 3 months based on sales over the last 5 years' daily sales of 1 items of one store.<br>
* Data includes (i) date, (ii) daily sales quantity, and (iii) store and item's ID.<br>
* Evaluation is done through Symmetric Mean Absolute Percentage Error. <br>

Algorithms
-
### Litght-gbm Model
* Implemented the time-sliding window technique for data processing, devising inventive strategies for feature engineering.<br>
* Based on the historical sales records of the enterprise, EDA technology is used to analyze the sales data.<br>
<img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/2.png" width="700px"><img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/3.png" width="700px"><br>
 * On this basis, the date-related features are divided, and the mean, standard deviation, maximum value, minimum value, and Statistics such as sums. Secondly, in view of the time series in the data, the lagged characteristics of sales are constructed, including moving average, exponentially weighted moving average and statistical information of commodity sales records. The addition of these features can improve the accuracy of predictions and help machine learning algorithms learn the temporal characteristics of data.<br>
 <img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/4.png" width="500px"><br>
* Finally, a total of 127 model features were constructed. Feature importance characteristics are used for feature screening, and time series segmentation is used to reasonably divide the data set.<br>
* The sales forecast for day D+1 was used recursively to predict the sales volume for day D+2 through feature engineering, and through this iterative process, 28-day test set performance was measured.<br>
 *In the figures below, the actual sales (bule lines), the predictions (yellow dotted lines).<br>
<img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/6.png" width="300px"><br>

### Prophet Model
* Prophet can incorporate forward-looking related time series into the model, so additional features were created with holiday and event information.<br>
* In the figures below, the actual sales (black dots), the point predictions and confidence intervals (blue lines and bands), and the test period are shown.<br>
  <img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/5.png" width="500px"><br>
•	Engineered and fine-tuned prediction models such as Prophet and Light-GBM, systematically evaluating and comparing their performance. Identified the Prophet algorithm as the standout performer, showcasing superior accuracy among single models.<br>
### Mixture Model
* Applied an innovative fusion methodology, calculating an optimal coefficient through reciprocal error analysis. <br>
<img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/1.png" width="400px"><br>
 * Apply the reciprocal error method shown above to calculate weights. This method assigns greater weights to models with smaller average relative errors to reduce the average relative error of the entire hybrid model and obtain more accurate prediction results. This led to the development of the highly effective LightGBM-Prophet fusion model for demand prediction.<br>

Algorithms Performance Summary
-
* The prediction of product sales in next three months among several models.<br>
<img src="https://github.com/Alfred768/Alfred768-Commodity-Demand-Forecasting/raw/master/photos/7.png" width="700px"><br>
* As a result, through comparison, it can be found that the prediction accuracy of the Mixture Model is better than that of a single model. <br>

| Algorithm | sMAPE |
| :-----: | :-----: |
| LightGBM | 10.06% |
| Prophet | 5.20% |
|Mixture Model | 2.35% |
|Moving Average | 23.64%| <br>

* In practice, retail stores can adopt the method in this article to predict future demand for goods, thereby optimizing inventory management and formulating purchasing plans, and improving business efficiency and profitability.

