## Exploring Naive Bayes Classifiers using [SMS Spam Collection Set from UCI](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection#)

#### Objective:  Use a classifier to predict whether an SMS message is spam or not, using accuracy (% correct) as the metric.

This analysis was performed in a Jupyter notebook using algorithms from scikit-learn and nltk.  The analysis follows Chapter 4 of *Machine Learning with R* by Brett Lantz (though of course here we use Python, not R)

We were able to correctly classify about 98.4% of the test set by optimizing the parameters for a Naive Bayes Classifier.  This is slightly larger than the accuracy reported by Lantz ("almost 98%").

To arrive at the optimal classifier, we explored:

Different classification algorithms:
- Naive Bayes
- Linear Regression
- Support Vector Machine (with linear, polynomial, and RBF kernels)
- AdaBoost (on Naive Bayes)

Stemming algorithms:
- Original text
- Porter
- Snowball
- Lancaster

Vectorizers:
- Count (at both the char and word level)
- TF-IDF (at both the char and word level)

Regularization parameters:
- l2 vs l1 vs elastic
- alpha

The optimal parameter set was found to be:
- Naive Bayes, with alpha = 0.129
- Original text (no stemming)
- Count vectorizer (with 3- and 4-char n-grams)
