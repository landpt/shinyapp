---
title       : Iris Classification
subtitle    : Estimation of the type of iris plant
author      : landpt
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, quiz]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Iris database

1. This is perhaps the best known database to be found in the pattern recognition literature. Fisher's paper is a classic in the field and is referenced frequently to this day.
2. The data set contains 3 classes of 50 instances each, where each class refers to a type of iris plant.
3. It is our main task to try what type of iris plant is given four different attributes.


## Machine Learning

We opted to use Random Forest technique. In fact, it achieved an amazing score when using cross-validation Leave-one-out:


--- .class #id 

## Cross Validation 


```
## Confusion Matrix and Statistics
## 
##             Reference
## Prediction   setosa versicolor virginica
##   setosa         50          0         0
##   versicolor      0         50         0
##   virginica       0          0        50
## 
## Overall Statistics
##                                     
##                Accuracy : 1         
##                  95% CI : (0.976, 1)
##     No Information Rate : 0.333     
##     P-Value [Acc > NIR] : <2e-16    
##                                     
##                   Kappa : 1         
##  Mcnemar's Test P-Value : NA        
## 
## Statistics by Class:
## 
##                      Class: setosa Class: versicolor Class: virginica
## Sensitivity                  1.000             1.000            1.000
## Specificity                  1.000             1.000            1.000
## Pos Pred Value               1.000             1.000            1.000
## Neg Pred Value               1.000             1.000            1.000
## Prevalence                   0.333             0.333            0.333
## Detection Rate               0.333             0.333            0.333
## Detection Prevalence         0.333             0.333            0.333
## Balanced Accuracy            1.000             1.000            1.000
```

--- .class #id 

## ShinyApp

I built a ShinyApp available at:

http://landpt.shinyapps.io/IrisClassification

This allows the user to choose a set of attributes, and the app will estimate the type of iris plant.


--- .class #id 

## Example


For instance, if we have some plant that has 5.6 cm of sepal length in cm, 2.6 cm of sepal width, 4.7 cm of petal length and 1.4 cm petal width, this interactive app will estimate that we're have a versicolor plant.



```
## [1] versicolor
## Levels: setosa versicolor virginica
```


