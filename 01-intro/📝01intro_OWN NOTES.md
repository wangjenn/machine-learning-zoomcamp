---
Created: 09.08.2024
Tags: 
---
# 01intro_NOTES
```
This is the fallback Template.
Create your own template, see help!
```

## 📝 RULE-BASED SYSTEMS vs. ML

#ZETTLE

- **RULE-BASED --> HARD-CODED** RULES (so like stupid Hopelab and also Bookbub)
- **Machine Learning**: instead of using hard-coded rules, COLLECT DATA, DEFINE + CALCULATE FEATURES, TRAIN MODELS 
## Collect the data

Collecting the data while using the “SPAM” button of your mail system

## Define & calculate (extract) the features

**Creating the features** -> **start with the rules you would use in rule-based systems**

Features:

- Length of title > 10? true/false
- Length of body > 10? true/false
- Sender “promotions@online.com”? true/false
- Sender “hpYOSKmL@test.com”? true/false
- Sender domain “test.com”? true/false
- Description contains “deposit”? true/false

All of the six features here are binary features, so you can encode each mail as binary code like [1, 1, 0, 0, 1, 1]. Besides this every email has a label[1](https://knowmledge.com/2023/09/10/ml-zoomcamp-2023-introduction-to-machine-learning-part-2/#1f8cceb4-6b29-4628-b077-f7fa387d8e54) / target (spam = 1, no-spam = 0), which is the desired output.


## Training

This data is used to train the model. This process is often called as fitting a model.

In training, something happens that is similar to solving a very complex system of equations with many parameters. Here, the features are offset against each other in such a way that the correct classification is obtained at the end. Correct in this example means 1 for spam 0 for no spam. More precisely, we get a probability for the correct label. The trained model contains exactly the information that best solves the equation, namely the weights with which the individual features must be offset to get the correct result.[2](https://knowmledge.com/2023/09/10/ml-zoomcamp-2023-introduction-to-machine-learning-part-2/#85f88844-ac9c-4e81-afb8-7f6063e82037)

## Apply the model

If the model is now applied to unknown data sets, the result is a probability. **This probability indicates whether this is a spam mail or not.** To finally decide how to categorize the mail, a threshold is used (e.g. 0.5). Thus, everything greater than or equal to 0.5 is declared as spam.

![](https://knowmledge.com/wp-content/uploads/2023/09/image-6.png?w=300)

---

1. the term “label” is not used in this video [↩︎](https://knowmledge.com/2023/09/10/ml-zoomcamp-2023-introduction-to-machine-learning-part-2/#1f8cceb4-6b29-4628-b077-f7fa387d8e54-link)
2. this is not described in this video [↩︎](https://knowmledge.com/2023/09/10/ml-zoomcamp-2023-introduction-to-machine-learning-part-2/#85f88844-ac9c-4e81-afb8-7f6063e82037-link)

---

[NOTES FROM MEMBERS](https://knowmledge.com/2023/09/10/ml-zoomcamp-2023-introduction-to-machine-learning-part-2/)

The difference between ML and Rule-Based systems is explained with the example of a **spam filter**. Traditional Rule-Based systems are based on a set of **characteristics** (keywords, email length, etc.) that identify an email as spam or not. ==**As spam emails keep changing over time the system needs to be upgraded making the process untraceable due to the complexity of code maintenance as the system grows.**==

ML can be used to solve this problem with the following steps:



**1. Get data:** Emails from the user's spam folder and inbox give examples of spam and non-spam.

  

**2. Define and calculate features:** Rules/characteristics from rule-based systems can be used as a starting point to define features for the ML model. The value of the target variable for each email can be defined based on where the email was obtained from (spam folder or inbox).

  

Each email can be encoded (converted) to the values of its features and target.

  **3. Train and use the model:** A machine learning algorithm can then be applied to the encoded emails to build a model that can predict whether a new email is spam or not spam. The **predictions are probabilities**, and to make a decision it is necessary to define a threshold to classify emails as spam or not spam.
---