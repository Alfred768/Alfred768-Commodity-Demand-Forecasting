Commodity-Demand-Forecasting
=
Goals
-
* Compare the accuracy of various time series forecasting algorithms such as Prophet, and LightGBM<br>
* Find the best way to deal with seasonality? Compare the models separately by pooling them together. Does deep learning work better thantime series forecasting algorithms? <br>

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
### Mixture Modle
* Applied an innovative fusion methodology, calculating an optimal coefficient through reciprocal error analysis. <br>



This led to the development of the highly effective LightGBM-Prophet fusion model for demand prediction.

Conducted research on commodity demand forecasting using advanced machine learning techniques:
•	Analyzed actual product sales data in depth to predict future demand over a three-month period.
•	Implemented the time-sliding window technique for data processing, devising inventive strategies for feature engineering.
•	Engineered and fine-tuned prediction models such as Prophet and Light-GBM in the code named "demo", systematically evaluating and comparing their performance. Identified the Prophet algorithm as the standout performer, showcasing superior accuracy among single models.
•	Applied an innovative fusion methodology, calculating an optimal coefficient through reciprocal error analysis. This led to the development of the highly effective LightGBM-Prophet fusion model for demand prediction in the code named "main".
The output is the list named "ensemble" in excel.
