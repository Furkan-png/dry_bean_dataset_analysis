# Dry Bean Dataset Analysis


### Dataset: [Link](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset)

---

I analyzed this dataset with --. I also used some preprocess functions.

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
  
  ---
  
  ### Experiment - 1 - XGBoostClassifier

> This experiment made with XGBoostClassifier algorithm to get better metric values. The prepocess and train test split transactions I used same methods as previous experiments. Experiment - 1 includes just LabelEncoder and StandardScaler. In next experiments I will add more methods to get better values.

- *Confusion Matrix*

  **[[238   0  21   0   3   4   5]<br />
 [  0 104   0   0   0   0   0]<br />
 [  6   0 320   0   1   2   7]<br />
 [  0   0   0 651   1   6  39]<br />
 [  0   0   6   2 353   0   9]<br />
 [  3   0   0  16   0 398  10]<br />
 [  2   0   0  47   8   2 459]]**
  
- *Accuracy Score* 
  
  **0.9265515975027543**
  
- *Macro F1 Score* 
  
  **0.936949897623269**

- *get_support()*

  [ True  True  True  True False False  True False False False  True  True
  True False False False]
  
- *get_rankings_*
  
  [1 1 1 1 3 9 1 8 6 5 1 1 1 2 7 4]
   
### Experiment - 2

> In this experiment I used RandomOverSampler to imbalance classes. Other methods are same with previous experiment. Feature selection results may vary but I will give them in anyway.

- *Confusion Matrix*

  **[[672   0  17   0   3   1  12]<br />
 [  0 729   0   0   0   0   0]]<br />
 [  8   0 682   0   7   0   5]]<br />
 [  0   0   0 636   2  12  36]]<br />
 [  4   0   3   6 715   0  17]]<br />
 [  0   0   0   9   0 679  11]]<br />
 [  2   0   0  60   4   3 630]]**
  
- *Accuracy Score* 
  
  **0.9552870090634441**
  
- *Macro F1 Score* 
  
  **0.9549815177220005**

- *get_support()*

  [ True  True False  True False False  True False False False  True  True
  True  True False False]
  
- *get_rankings_*
  
  [1 1 2 1 5 9 1 8 6 4 1 1 1 1 7 3]

### Experiment - 3

> Experiment 3 involves FeatureSelection features unlike the previous experiments. Also in this experiment features which are selected by RFE algorithm badly affected the results. 

- *Confusion Matrix*

  **[[632   0  49   0   6   6  12]< /br>
 [  1 728   0   0   0   0   0]< /br>
 [ 22   0 659   0  13   3   5]< /br>
 [  0   0   0 629   2  15  40]< /br>
 [  4   0   9   7 712   0  13]< /br>
 [  1   0   0  12   0 670  16]< /br>
 [  1   0   0  79   5  17 597]]**
  
- *Accuracy Score* 
  
  **0.9319234642497483**
  
- *Macro F1 Score* 
  
  **0.9311865965143975**

- *get_support()*

  [False False  True False False  True False  True  True  True False]
  
- *get_rankings_*
  
  [3 4 1 5 7 1 2 1 1 1 6]

### Experiment - 1 - Support Vector Classifier (SVC from SVM)

> Today I am analyzing again same dataset. Today's algorithm is Support Vector Classifier from SVM. I am not going to use feature selection for beginning. In this experiment I tried training without scaling and it's made massive difference than the previous models.

- *Confusion Matrix*

  **[[ 12   0 187   0  60   0  12]<br />
 [  0 104   0   0   0   0   0]]<br />
 [ 10   0 297   0  26   0   3]]<br />
 [  0   0   0 606   0  71  20]]<br />
 [  8   0  25   8 188  15 126]]<br />
 [  0   0   0 145  15 103 164]]<br />
 [  0   0   0  24  35  51 408]]**
  
- *Accuracy Score* 
  
  **0.6309217774513405**
  
- *Macro F1 Score* 
  
  **0.5863603166078509**

### Experiment - 2

> Unlike the previous experiment I used Scaling and see the difference on metrics. 

- *Confusion Matrix*

  **[[214   0  40   0   2   4  11]<br />
 [  0 104   0   0   0   0   0]<br />
 [  6   0 320   0   3   2   5]<br />
 [  0   0   0 643   1   7  46]<br />
 [  0   0   5   3 353   0   9]<br />
 [  2   0   0  13   0 386  26]<br />
 [  0   0   1  49   6   5 457]]**
  
- *Accuracy Score* 
  
  **0.9096584649283878**
  
- *Macro F1 Score* 
  
  **0.9196135603363059**

### Experiment - 3

> For the last experiment I used Over Sampler for imbalance classes. DERMASON and BOMBAY classes are that imbalance classes. I used ROS (Random Over Sampler) from imblearn library.

- *Confusion Matrix*

  **[[603   1  62   0   4   6  29]<br/>
 [  0 729   0   0   0   0   0]<br/>
 [ 27   0 649   0  11   2  13]<br/>
 [  0   0   0 619   2  16  49]<br/>
 [  1   0  10   9 702   0  23]<br/>
 [  2   0   0  10   0 665  22]<br/>
 [  1   0   1  48   4  16 629]]**
  
- *Accuracy Score* 
  
  **0.9256797583081571**
  
- *Macro F1 Score* 
  
  **0.9252603274877432**

### Experiment - 1 - KNeighbors Classifier

> In this experiment I used KNegihbors Classifier for Dry Beans Dataset. I am tried to get more accuracy in every experiment. In first experiment I didn't use scaling method 

- *Confusion Matrix*

  **[[133   0 107   0  18   0  13]<br />
 [  0 104   0   0   0   0   0]<br />
 [ 39   1 284   0   8   1   3]<br />
 [  0   0   0 648   0   9  40]<br />
 [ 10   0  23  13 282   0  42]<br />
 [  1   0   0  31   2 331  62]<br />
 [  1   0   0  59  11   6 441]]**
  
- *Accuracy Score* 
  
  **0.8163789937568858**
  
- *Macro F1 Score* 
  
  **0.8131287082670368**

### Experiment - 2

> Unlike the previous experiment I used Scaling and see the difference on metrics. 

- *Confusion Matrix*

  **[[214   0  40   0   2   4  11]<br />
 [  0 104   0   0   0   0   0]<br />
 [  6   0 320   0   3   2   5]<br />
 [  0   0   0 643   1   7  46]<br />
 [  0   0   5   3 353   0   9]<br />
 [  2   0   0  13   0 386  26]<br />
 [  0   0   1  49   6   5 457]]**
  
- *Accuracy Score* 
  
  **0.9096584649283878**
  
- *Macro F1 Score* 
  
  **0.9196135603363059**
