# Billboard 100 Machine Learning Project 
![alt text](https://github.com/azagoren/Billboard100_MachineLearning/blob/master/bboard.png?raw=true)


## Project Overview

When given the opportunity to explore machine learning techniques on a topic of our choice, our team decided to predict music popularity. While we all enjoy exploring social issues through data research, we chose to embrace a more light-hearted topic and just have fun with data. With the rise of streaming platforms fundamentally altering music distribution, we were curious to predict which factors play an important role in predicting a song's popularity. Using the Million Song Dataset available [here](https://raw.githubusercontent.com/Vatshayan/Song-Classification/master/music.csv), and the Billboard 100 Weekly Charts Dataset available on [data.world](https://data.world/kcmillersean/billboard-hot-100-1958-2017) we developed classifying models to predict whether a song would make the Billboard Top 100, and examine which variables play important roles in determining this outcome. 

## Machine Learning Techniques 

We have listed below the four machine learning techniques implemented within this study: <br>
*(For more information regarding these techniques, please see our final report)*

* **Classification Tree:**

While our classification tree was able to correctly predict when a song would not make the charts 97.7% of the time, its low sensitivity values (16.7%) were a cause for concern. Since our project is more interested in predicting when a song will be successful, we chose to pursue other models in an effort to achieve better sensitivity results. 

* **Lasso Regression:**

Next, we turned to the Lasso regression, hoping to take best advatage of its feature selection capabilities and to determine if overfitting problem experienced with our decision tree results was attributable to overfitting. We faced similar challenges to its sensitivity as our classification trees and random forest. It had a specificity of 98%, sensitivity of 0% and accuracy of 97.9%, prompting us to look further into solutions for dealing with unbalanced data. 

* **Random Forest:**

The random forest yielded marginally improved specificity and accuracy values of 100% and 98% respectively. Sensitivity within this model however continued to decline, as our random forest predicted that no songs (0%) would ever make the Billboard 100. While not particularly insightful for our prediction objectives, this model yielded some valuable information regarding which factors play an important role in determining whether a song will become popular. It identified "artist.hotttnesss" and "familiarity" as relevant variables in determining a song's ability to top the charts. 

* **Random Forest using SMOTE sampling:** 

Observing how our unbalanced data was preventing our models from accurately predicting when a song would make it onto the Billboard charts, we elected to use SMOTE sampling with our model which performed best: random forest. With the SMOTE resampling, our sensitivity improved to 63.33% with a specificity of 89.6% and an accuracy of 89.1%. 

## Discussion: 

We found that the random forest model using SMOTE sampling provided the best predictions of whether a song would reach the Billboard Top 100 charts. This is largely due to the need for SMOTE sampling to deal with our unbalanced data. It remains completely plausible that a gradient boost or support vector machine using SMOTE sampling would yield superior results. While our random forest with SMOTE sampling has an accuracy that is slightly lower than our other models, it greatly outperforms them in its sensitivity measure, which is especially important as we're most interested in which factors will improve the likelihood of a song topping the charts. When examining which of these variables play important roles, we find that an artist’s popularity and familiarity are the most influential predictors of a song's likelihood to achieve widespread acclaim. This indicates that while streaming platforms offer users the ability to publish their music free of charge, songs released by acclaimed artists continue to have a much greater likelihood of popularity than their counterparts from lesser known musicians. 

## Contributors: 

* Anna Zagoren : azagoren@wesleyan.edu
* Erin Rose : erose@wesleyan.edu
* Emily Leff : eleff@wesleyan.edu
