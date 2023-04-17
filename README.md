# Brain Stroke Prediction
This is basically a classification problem. The aim of this study is to check how well it can be predicted if patient will have barin stroke based on the available health data such as glucose level, age, gender etc.

We checked the [data](https://github.com/muscak/Brain-Stroke-Prediction/tree/main/Data) and performed some explanotary data analysis first, then processed the data as needed. Fortunately there was no Null values in any of the features. One of the major challenges that we faced was that the data was imbalaced. The ratio of the people who had no stroke was 96.30% and the people who had stroke was 3.70%. The gap between these two classes was huge. 
<p>
  <img src='images/imbalanced.png' align='center' height=300>
</p>


After removing the outliers and checking the distribution of the numerical features, we used `RandomUnderSampler` function of `imblearn` library with 0.5 `sampling_strategy` to make the labels more balanced. We checked the performance of Support Vector Classifier, Decision Tree Classifier, $k$-Nearest Neighbor, Linear Discrimenant Analyses and Gaussian Naive Bayes algorthims with the given dataset.

<p>
  <img src='images/under_sampling_perf.png' align='center' height=300>
</p>


After preparing the data, we'll evaluate the performance of different algorithms and tune the hyperparameters of the one which is the most promissing. Finally we'll perform a prediction on the test data to check the overall performance of the chosen algorithm.
