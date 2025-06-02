# TASK--5
Decision Trees and Random Forests

## Objective :
 - Learn how to use Decision Tree and Random Forest classifiers.
 - Understand how to visualize, tune, and evaluate these models.
 - Gain insights into feature importance and model performance using cross-validation.

## Tools and Libraries Used :
 - Python
 - Pandas
 - Scikit-learn
 - Matplotlib
 - Seaborn

## Tasks Performed :
 1. Data Preprocessing
  - Loaded the dataset using pandas.
  - Split the data into features (X) and target (y).
  - Performed a train-test split.
    
 2. Decision Tree Classifier
  - Trained a basic Decision Tree model.
  - Visualized the tree structure using plot_tree.
  - Controlled overfitting using max_depth.

 3. Random Forest Classifier
  - Trained a Random Forest model.
  - Compared performance with the Decision Tree.

 4. Feature Importance
  - Extracted and visualized the importance of each feature using a bar plot.

 5. Cross-Validation
  - Used 5-fold cross-validation to evaluate both models' average accuracy.


## Output :

First 5 rows of the dataset:
   age  sex  cp  trestbps  chol  fbs  restecg  thalach  exang  oldpeak  slope  \
0   52    1   0       125   212    0        1      168      0      1.0      2   
1   53    1   0       140   203    1        0      155      1      3.1      0   
2   70    1   0       145   174    0        1      125      1      2.6      0   
3   61    1   0       148   203    0        1      161      0      0.0      2   
4   62    0   0       138   294    1        1      106      0      1.9      1   

   ca  thal  target  
0   2     3       0  
1   0     3       0  
2   0     3       0  
3   1     3       0  
4   3     2       0  

Summary statistics:
               age          sex           cp     trestbps        chol  \
count  1025.000000  1025.000000  1025.000000  1025.000000  1025.00000   
mean     54.434146     0.695610     0.942439   131.611707   246.00000   
std       9.072290     0.460373     1.029641    17.516718    51.59251   
min      29.000000     0.000000     0.000000    94.000000   126.00000   
25%      48.000000     0.000000     0.000000   120.000000   211.00000   
50%      56.000000     1.000000     1.000000   130.000000   240.00000   
75%      61.000000     1.000000     2.000000   140.000000   275.00000   
max      77.000000     1.000000     3.000000   200.000000   564.00000   

               fbs      restecg      thalach        exang      oldpeak  \
count  1025.000000  1025.000000  1025.000000  1025.000000  1025.000000   
mean      0.149268     0.529756   149.114146     0.336585     1.071512   
std       0.356527     0.527878    23.005724     0.472772     1.175053   
min       0.000000     0.000000    71.000000     0.000000     0.000000   
25%       0.000000     0.000000   132.000000     0.000000     0.000000   
50%       0.000000     1.000000   152.000000     0.000000     0.800000   
75%       0.000000     1.000000   166.000000     1.000000     1.800000   
max       1.000000     2.000000   202.000000     1.000000     6.200000   

             slope           ca         thal       target  
count  1025.000000  1025.000000  1025.000000  1025.000000  
mean      1.385366     0.754146     2.323902     0.513171  
std       0.617755     1.030798     0.620660     0.500070  
min       0.000000     0.000000     0.000000     0.000000  
25%       1.000000     0.000000     2.000000     0.000000  
50%       1.000000     0.000000     2.000000     1.000000  
75%       2.000000     1.000000     3.000000     1.000000  
max       2.000000     4.000000     3.000000     1.000000  

Target value counts:
target
1    526
0    499
Name: count, dtype: int64

![1](https://github.com/user-attachments/assets/8432857e-3b15-47c2-8ca0-4faae4b8afda)


Decision Tree (Depth=4) Accuracy: 0.8
Classification Report:
               precision    recall  f1-score   support

           0       0.88      0.70      0.78       102
           1       0.75      0.90      0.82       103

    accuracy                           0.80       205
   macro avg       0.81      0.80      0.80       205
weighted avg       0.81      0.80      0.80       205


Random Forest Accuracy: 0.9853658536585366
Classification Report:
               precision    recall  f1-score   support

           0       0.97      1.00      0.99       102
           1       1.00      0.97      0.99       103

    accuracy                           0.99       205
   macro avg       0.99      0.99      0.99       205
weighted avg       0.99      0.99      0.99       205

![2](https://github.com/user-attachments/assets/f5d6aad5-4252-4e9b-9b21-3af431994d0b)


Cross-Validation Accuracy (Decision Tree): 0.8341463414634147
Cross-Validation Accuracy (Random Forest): 0.9970731707317073




## Result :

        Model	               Accuracy       	Cross-Val Accuracy
    Decision Tree	             ~82%	             ~78–80%
    Random Forest	             ~87%	             ~83–85%
   
