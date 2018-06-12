# Risk_Lab
Data analysis on Dublin Science Gallery risk lab exhibitions

Completed as part MSG500 linear statistical models (Chalmers University of Technology)



Files (All in python notebook format): 
* __Scales_converter.ipynb:__ Conversion for scales (BIS,dospert)
* __Risk Taking predict smoking .ipynb:__ Predicting the number of cigarettes smoked per week from a measure of risk taking in a social context (DOSERT)
* __BIS Self Control Verse Car Crashes .ipynb:__ Predicting the number of car crashes from a measure of self control (BIS)
* __Model for Smoking.ipynb:__ Building a prediction model to predict if a participant in the dataset has smoked during their lifetime.
* __Model for drinking.ipynb:__ Building a prediction model to predict the age that a participant started drinking alcohol
 

Datasets:
* __RISKLAB_10_11_17.csv:__ Orginal uneditted dataset 
* __Risklab_2.4.csv__ Ready to use dataset 

## Summary 
#### Predicting the number of cigarettes smoked per week from a measure of risk taking in a social context (DOSERT)
- We divided cigarettes smoked per week (cspw) into seven levels, we then compared it against social risk taking. ANOVA and Kruskal-Wallis rank sum test suggested there was no statically significant mean difference between the seven groups. 
- We performed an regression holding the first level as base line, none of the levels where able to assist in the prediction of cspw. 
- We compared social risk taking against recreational risk taking by cspw group level. No statically significant result. 

#### Predicting the number of car crashes from a measure of self control
- We grouped car crashes dichotomously (no crash, or at least one crash). 
- Group 1, have a slightly lower self control mean then group 0, but neither ANOVA or Kruskal-Wallis rank sum test reported any difference in group means. 
- Applied a logistical regression model to the data, residuals plots suggested a number of assumption violations. We played around with transformations but it wasn't look good. 
- We concluded that it wasn't an easy prediction, and moved on. 

#### Building a prediction model to predict if a participant in the dataset has smoked during their lifetime.
  - Here we looked at building a prediction model for the variable "Ever smoked". We developed a logistical regression model with 12 other variables (Demographic,BIS,DOSERT)
  -  Backward selection and interaction search reduced our model down to Age ,BIS_Cog_Instability, BIS_self_Control, DOS_Fin_Investment, DOS_Fin_Gambling, DOS_Health Safety. 
  - Overall model stability looks acceptable. 
  - Evaluated the model on a test set, 99% prediction this... but this might be due to an issue with our R code. (Maybe should have tried Cross Validation)?? ## Maybe look back here. 
#### Building a prediction model to predict the age that a participant started drinking alcohol
  - Had to group age started drinking into four different levels. I haven't studied multinomial logistic regression yet so we put this model to bed! 
  
  
