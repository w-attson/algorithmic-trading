![ml-alg-title](images/header-image.png)

# Machine Learning Trading 

The project analyse and improve existing trading algorithms through machine learning models and make adjustments accordingly.

Below outlines the steps taken in the project:

1. [Establish a Baseline Performance](establish-a-baseline-performance)
2. [Tune the Baseline Trading Algorithm](tune-the-baseline-trading-algorithm)
3. [Evaluate a New Baseline Learning Classifier](evaluate-new-baseline-learning-classifier)
4. [Create a Evaluation Report](create-a-evaluation-report)

## Establish a Baseline Performance
* Import the OHLCV dataset into a Pandas DataFrame.
* Generate trading signals using short- and long-window (Short Moving Average) SMA values.
* Split the data into training and testing datasets.
* Use the SVC classifier model from SKLearn's support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data.
* Generate and review the classification report associated with the SVC model predictions.
* Create a predictions DataFrame that contains columns for “Predicted” values, “Actual Returns”, and “Strategy Returns”.
* Create a cumulative return plot that shows the actual returns vs. the strategy returns.

### SVM Model

![svm-model](images/svm-model-4-100-3.png)
![svm-model-report](images/svm-model-4-100-3-report.png)

## Tune the Baseline Trading Algorithm
* Tune the model’s input features to find the parameters that result in the best trading outcomes. (You’ll choose the best by comparing the cumulative products of the strategy returns.) To do so, complete the following steps:
* Tune the training algorithm by adjusting the size of the training dataset.

## Evaluate a New Machine Learning Classifier
* Import a new classifier
* Using the original training data as the baseline model, fit another model with the new classifier.
* Backtest the new model to evaluate its performance.
* Answer the following questions: Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?

#### Logistic Regression Model
![lr-model](images/lr-model-4-100-3.png)
![lr-model-report](images/lr-model-4-100-3-report.png)

#### Decision Tree Model
![dt-model](images/dt-model-4-100-3.png)
![dt-model-report](images/dt-model-4-100-3-report.png)

#### AdaBoost Model
![boost-model](images/boost-model-4-100-3.png)
![boost-model-report](images/boost-model.png)


## Evaluation Report
### Tuning the Baseline Algorithm
* There are a few variables that were altered including:
    * short_window
    * long_window
    * DateOFfset

These alterations created scenarios that output plots to indicate if the changes create either a net positive or net negative change.

The following outputs are detailed accounts of the tests conducted:

* SVM Model (
    sma_short = 5
    sma_long = 100
    DataOffset = 3
)
![svm-model-5-100-3](images/svm-model-5-100-3.png)
![svm-model-5-100-3-report](images/svm-model-5-100-3-report.png)


* SVM Model (
    sma_short = 5
    sma_long = 80
    DataOffset = 3
)
![svm-model-5-100-3](images/svm-model-5-80-3.png)
![svm-model-5-100-3-report](images/svm-model-5-80-3-report.png)

* SVM Model (
    sma_short = 4
    sma_long = 100
    DataOffset = 6
)
![svm-model-5-100-3](images/svm-model-4-100-6.png)
![svm-model-5-100-3-report](images/svm-model-4-100-6-report.png)

* SVM Model (
    sma_short = 4
    sma_long = 100
    DataOffset = 10
)
![svm-model-5-100-3](images/svm-model-4-100-10.png)
![svm-model-5-100-3-report](images/svm-model-4-100-10-report.png)