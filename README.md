# detroit_housing_project

This ML classification project explores housing blight in Detroit, MI in an attempt to better understand evolving real estate trends in the city. The project consists of 3 parts:

1. Exploratory Data Analysis on housing-related data from the Detroit Open Portal website
2. Training and comparing model produced with this data to predict a home’s likelihood to have gotten *at least one* blighting citation in Detroit
3. A post-hoc analysis of the final model to better understand the problem and develop next steps


# 1. EDA
The charts below show a couple of findings confirm my two of my hypotheses:

## On blight trends as it relates to Detroiters:
!['blight chart'](https://github.com/rebecca-hh-rosen/detroit_housing_project/blob/master/blight_chart.png)

## And blight trends as it relates to homeowners vs rentals:
!['rentals chart'](https://github.com/rebecca-hh-rosen/detroit_housing_project/blob/master/rentals_chart.png)


The findings are further complicated by considering more about homeowners vs folks who put their homes up for rent. Future iterations of this project will include a more detailed breakdown about real estate trends for various demographics.



# 2. Modeling 

The final **Decision Tree** model does well at binary classfication, with metrics like the following:
- Accuracy : 94.69
- F1-Score : 0.60
- Precision Score : 0.589
- Recall Score : 0.621

Note: The majority of top indicators were features engineered from the raw data:
!['features chart'](https://github.com/rebecca-hh-rosen/detroit_housing_project/blob/master/features_chart.png)



# 3. Post-Hoc Analyses
However, feature importance evaluation, the total due per parcel (the most important feature at 0.534 importance) is too highly correlated with the target varialbe (total tickets) to provide an independent prediction. As such, the next iteration of this project apply the methods that mitigate this confluence.

These methods may include:

- Up and Down Sampling
- Various other modeling techniques such as grid search
- Look at a baseline model and null accuracy
- Deploy grid and random search to find optimal tree depth
- Observe evaluation metrics (including confusion matrix) for each class
- Try a more thorough EDA distribution of each feature again target and improve upon current visualizations
- Scale and normalize each variable more thoroughly
- Eventually try a multi-class target instead of binary, with categories of 0 tickets // 1-7 tickets // 8+ tickets


See full slides for this project's presentation at https://bit.ly/2MCz2Ob
All data can be found for free at Detroit's Open Data Portal https://data.detroitmi.gov/
