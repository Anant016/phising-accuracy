## Phishing Website Dataset

In this tutorial, we use a dataset of phishing website publicly
available on the [machine learning repository](https://archive.ics.uci.edu/ml/datasets/Phishing+Websites)
provided by UCI. You don't have to download the dataset yourself
as it is included directly in this repository (`dataset.csv` file) and
was downloaded on your machine when you cloned this repository.

The dataset was collected by analyzing a collection of `2456` websites
among which some were used for phishing and others not. For each website
included in the dataset, `30` attributes are given. You can find a list
[here](https://github.com/npapernot/phishing-detection/blob/master/features.md).
The list includes for instance the URL length, whether the website
uses pop-up windows or Iframes, or how old the domain registration is.

Each website in the dataset is labeled by `-1` if it is not a phishing
website and by `1` if it is a website used for phishing.

## Training the decision tree to detect phishing website

You can find the code that trains the decision tree in the
[`decision_tree.py`](https://github.com/npapernot/phishing-detection/blob/master/decision_tree.py)
file. To run the code, simply execute it in a terminal:

```
python decision_tree.py
```

This will first train the decision tree on `2,000` websites, then use
the trained model to predict whether `456` websites are used for
phishing or not (these websites were not analyzed during training).
The model should make predictions that are about 90.5% correct, i.e. the
accuracy of the model on the testing data should be 90.5%. Here is a
dump of the output made by the script.

```
Tutorial: Training a decision tree to detect phishing websites
Training data loaded.
Decision tree classifier created.
Beginning model training.
Model training completed.
Predictions on testing data computed.
The accuracy of your decision tree on testing data is: 0.906129210381
```

To understand how this was done, you can read the line by line comments
in the [`decision_tree.py`](https://github.com/npapernot/phishing-detection/blob/master/decision_tree.py) file.
