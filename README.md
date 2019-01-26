# StackOverflow-Tag-Prediction
**Business Problem**<br>
Stack Overflow is something which every programmer use one way or another. Each month, over 50 million developers come to Stack Overflow to learn, share their knowledge, and build their careers. It features questions and answers on a wide range of topics in computer programming. The website serves as a platform for users to ask and answer questions, and, through membership and active participation, to vote questions and answers up or down and edit questions and answers in a fashion similar to a wiki or Digg. As of April 2014 Stack Overflow has over 4,000,000 registered users, and it exceeded 10,000,000 questions in late August 2015. Based on the type of tags assigned to questions, the top eight most discussed topics on the site are: Java, JavaScript, C#, PHP, Android, jQuery, Python and HTML<br/>

**Business Objective and Constraints:**<br/>
1. Predict as many tags as possible with high precision and recall.<br/>
2. Incorrect tags could impact customer experience on StackOverflow.<br/>
3. No strict latency constraints.<br/>

**Machine Learning Problem:**<br/>
Dataset contains 6,034,195 rows. The columns in the table are:<br/>
Id - Unique identifier for each question<br/>
Title - The question's title<br/>
Body - The body of the question<br/>
Tags - The tags associated with the question in a space-seperated format (all lowercase, should not contain tabs '\t' or ampersands '&')<br/>

**Mapping Business problem to Machine Learning Problem::**<br/>
It is a multi-label classification problem.Performance Metrics:<br/>
1. Mean F Score/Micro f1 score :  <br/>
 Calculate metrics globally by counting the total true positives, false negatives and false positives.orks good for imbalanced dataset.<br/>
2. Macro f1 score :  <br/>
Calculate metrics for each label, and find their unweighted mean. This does not take label imbalance into account.<br/>
3. Hamming loss :  <br/>
 Loss = (1/|D|)*Sum(xor(x,y)/|L|);where D = Number of datasamples and L is number of labels.This is sort of acuracy.<br/>
 
 **Sumaary:**
 
|        Model        |     precision     |        recall       |      f1-score      |
|---|---|---|---|
| Logistic Regression |     0.59668035    |      0.41897331     |    0.520994953     |
|     grid_TF_IDF     | 0.409867265539611 | 0.43365820541734745 | 0.4214272335643379 |
