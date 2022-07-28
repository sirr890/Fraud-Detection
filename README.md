# Credit Card Fraud Detection

Anomaly detection is used to identify rare events, items, and observations suspicious of average or non-anomalous behavior or pattern. Such an approach has been developed for sevehis problem will be solved such that given x, the model will predict 1, corresponding to an anomaly or 0 to a normal example https://scikit-learn.org/stable/user_guide.html

My approach to solve this problem will be as follows. Given x, the model predicts 1, corresponding to an anomaly or 0 to a normal example. Then, I used three differents approches https://scikit-learn.org/stable/user_guide.html

**Isolation Forest**
  The Isolation Forest is an anomaly detection algorithm that identifies anomalies instead of profiling normal data points.
  
**Gaussian Mixture Models**
  A Gaussian Mixture model is a probabilistic model that assumes all the data points are generated from a mixture of a finite number of Gaussian distributions with unknown parameters.
  
**One Class SVM**
  The One Class SVM is an unsupervised algorithm that learns a decision function for novelty detection: classifying new data as similar or different to the training set.

The dataset is split into training, validation, and test sets. I used 60% of the non-anomalous or normal data is used for the training set. Besides, the other part of the non-anomalous and anomalous data is split equally in the validation and testing sets 20% for validation and 20% for testing.

The training set is used to fit the model. Then, the validation set is used to select the best model concerning a metric for different hyper-parameters. Since the data is very skewed, because y equals 0 is much more common, F-score would be a good evaluation metric.

$𝐹1=\frac{2∗𝑃∗𝑅}{𝑃+𝑅}$ 
where P and R are Precision and Recall.

𝑃=𝑇𝑃𝑇𝑃+𝐹𝑃  and  𝑅=𝑇𝑃𝑇𝑃+𝐹𝑁 
True Positive (TP): non-anomalous or normal items predicted as normal.
False Negative (FN): anomaly items indicated as normal. Also called a Type II error in statistics.
False Positive (FP): normal items predicted as anomalies. Also called a Type I error in statistics.
