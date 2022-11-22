# Dry Bean Dataset Analysis


### Dataset: [Link](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset)

---

I analyzed this dataset with DecisionTreeClassifier. I also used some preprocess functions.

I am going to give 2 experiment about this analysis for the first time. I am going to add other experiments when I try them.


### Experiment - 1 - Decision Tree Classifier

> In this experiment I used RandomOverSampler for imbalanced classes. I used LabelEncoder for 'y's cathegorical values. I split my data to train and test set. While I was doing this I determined test size as 0.20. For scaling I used StandardScaler which is effect not that much to metrics for this model. Finally, I used SequentialFeatureSelector for feature selection. I am going to give it's rankings and support values under the metrics. 

- *Confusion Matrix*

  **[[669   0  22   0   1   5   8] <br />
   [  4 725   0   0   0   0   0]<br />
   [ 18   0 666   0  12   2   4]<br />
   [  0   0   0 616   3  16  51]<br />
   [  8   0   9   3 704   0  21]<br />
   [  2   0   1  14   0 670  12]<br />
   [  5   0   1  75  15  18 585]]**
  
- *Accuracy Score* 
  
  **0.9335347432024169**
  
- *Macro F1 Score* 
  
  **0.9327973979258182**

- *get_support()*

  [False  True  True False False False False False False  True  True False
  True  True  True  True]
  
- *get_rankings_*
  
  [9 1 1 5 8 7 6 4 2 1 1 3 1 1 1 1]
   
   
### Experiment - 2

> Unlike the previous experiment, I used features which is given in SequentialFeatureSelector.
Also for the new feature selection process I used RFE method.
- *Confusion Matrix*

  **[[671   0  13   0   5   4  12]<br />
 [  1 728   0   0   0   0   0]<br />
 [ 17   0 670   0  10   1   4]<br />
 [  0   0   0 615   4  15  52]<br />
 [  4   0  10   4 716   0  11]<br />
 [  3   0   5  14   0 668   9]<br />
 [  8   0   0  74   8   7 602]]**
  
- *Accuracy Score* 
  
  **0.9405840886203424**
  
- *Macro F1 Score* 
  
  **0.9399229686676708**

- *get_support()*

  [ True  True False False False  True  True  True False False False]
  
- *get_rankings_*
  
  [1 1 6 5 4 1 1 1 7 2 3]

---

I hope this can be enlightening for the people who interested in with data science.

And please do not step back to warn me if I have mistakes, if I miss something about model, preprocess or even for github because I am trying to get used to it.

Thank you for your time.

---

### Experiment - 1 - Random Forest Classifier

> This experiment made with RandomForestClassifier algorithm to get better metric values. The prepocess and train test split transactions I used same methods as previous experiments. In this model, Experiment - 2 will be model with features which is given by RFE feature selection method.

- *Confusion Matrix*

  **[[669   0  22   0   1   5   8] <br />
   [  4 725   0   0   0   0   0]<br />
   [ 18   0 666   0  12   2   4]<br />
   [  0   0   0 616   3  16  51]<br />
   [  8   0   9   3 704   0  21]<br />
   [  2   0   1  14   0 670  12]<br />
   [  5   0   1  75  15  18 585]]**
  
- *Accuracy Score* 
  
  **0.9335347432024169**
  
- *Macro F1 Score* 
  
  **0.9327973979258182**

- *get_support()*

  [False  True  True False False False False False False  True  True False
  True  True  True  True]
  
- *get_rankings_*
  
  [9 1 1 5 8 7 6 4 2 1 1 3 1 1 1 1]
   
### Experiment - 2

- *Confusion Matrix*

  **[[633   0  50   0   4   6  12]<br />
 [  0 729   0   0   0   0   0]<br />
 [ 37   0 647   0  13   0   5]<br />
 [  0   0   0 633   3  15  35]<br />
 [  4   0  11   8 705   0  17]<br />
 [  1   0   0  14   0 668  16]<br />
 [  7   0   1  67   5  16 603]]**
  
- *Accuracy Score* 
  
  **0.9301107754279959**
  
- *Macro F1 Score* 
  
  **0.9294272637358352**

- *get_support()*

  [ True  True  True False False False False False  True False  True]
  
- *get_rankings_*
  
  [1 1 1 6 4 5 3 2 1 7 1]
