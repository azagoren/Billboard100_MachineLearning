# Billboard 100 Machine Learning Project 

## Project Overview

When given the opportunity to explore machine learning techniques on a topic of our choice, our team decided upon predicting music popularity. While we all enjoy exploring social issues through data research, we're not afraid to embrace a more light-hearted topic and just have fun with the data. With the rise of streaming platforms fundamentally altering music distribution, we were curious to predict what factors to play an important role in predicting a song's popularity. Using the Million Song Dataset available here (insert link), and the Billboard 100 Weekly Charts Dataset available on data.world (insert link) we developed classifying models predicting whether or not a song would make the Billboard Top 100 and examining which variables played important roles in determining this outcome. 

## Machine Learning Techniques 

We have listed below the four machine learning techniques implemented within this study: 
*(For more information regarding these techniques, please see our final report)*

* **Classification Tree:**

While our classification tree was able to correctly predict when a song would not make the charts 97.7% of the time, its low sensitivity values (16.7%) were a cause for concern. Since our project was more interested in prediciting when a song would be successful, we chose to pursue other models in hopes that they would yield better sensitivity results. 

* **Random Forest:**

The random forest most yielded mariginally improved specificity and accuracy values of 100% and 98% respectively. Sensitivity within this model however continued to decline, as our random forest predicted that no songs (0%) would ever make the Billboard 100. This model also yielded some valuable information on which factors play and important role in identifying whether a song will achieve popularity. It identified "artist.hottness" and "familiarity" as relevant variables in determining a song's ability to top the charts. 

* **Lasso Regression:**

The Lasso regression faced similar challenges to its sensitivity as our classification trees and random forest. It had a specificity of 100%, sensitivity of 0% and accuracy of 97.9%, prompting us to look further into solutions for dealing with unbalanced data. 

* **Random Forest using SMOTE sampling:** 

Observing how our unbalanced data prevent our models from accurately predicting when a song would make it onto the Billboard charts, we elected to use SMOTE sampling on our model which performed best: random forest. With the SMOTE resampling our sensitivity improved to 63.33% with a specificity of 89.6% and an accuracy of 89.1%. 

## Discussion: 

We found the the random forest model using SMOTE sampling to provide the best results when predicting whether a song would eng up on the Billboard Top 100 charts. This is partially due to the unbalanced nature of our data, which required SMOTE sampling to yield acceptable results given the unbalanced nature of our data. While its accuracy is slightly lower than our other models, it greatly outperforms them in its sensitivity measure, which is especially important as we're most interested in which factors will improve the likelihood of a song topping the charts. When examining which of these variables play important roles, we find that an artists popularity and familiarity are the most influental predictors of a song's liklihood to achieve widespread acclaim. This indicates that while streaming platforms offer users the ability to publish their music without charge, songs released by acclaimed artists continue to have a much greater likelihood of popularity than their counterparts from lesser known musicians. 

## Contributors: 

* Anna Zagoren : azagoren@wesleyan.edu
* Erin Rose : erose@wesleyan.edu
* Emily Leff : eleff@wesleyan.edu
