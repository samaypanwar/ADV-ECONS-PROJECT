# Advanced Econometrics

### Project Questions
    How to predict/explain inflation with google trends data with a lasso model

### To do List
    1. Create list of inflation queries ~ 50
    2. Query and clean data, concat with control variables
    3. Do we want to dd a PCA? --> might lead to inability to associate better accurarcy to predictions/defeats the 
       purpose of lasso
    4. Make baseline model with just control variables
    5. Make our model with google trends + control variables
    6. Add lags to the model for trends data
    7. Compare predictions with prediction intervals for each of the three types of models and conclude

### Model Structure
    Y. Inflation Monthly: yoy change
    
    X. 
        0. Lags? of Inflation? ADL
        1. TIPS Inflation
        2. Unemployment rate
        3. DXY
        4. SP500 Index
        5. Term spread
        6. 10Y Bond Yields
        7. Google Trends Data

### Methodology

    Do we add lags to our predictors --> would lead to forecast future rather than present
    
    nobs = (2023-2004) * 12 = 228

    5 fold cross validation and POOS nobs = 28
    
    training size = 180
    test size = 20

    On test samples, make t+1 predictions on an expanding window
    
    - Do this for all your folds to get a robust estimate of your model

### Tests
    1. Stationarity
    2. Normality
    3. VIF
    4. Granger causality for google trends
    5. BIC for inflation lag decision

Might be good to decide to do PCA on google trends to get results rather than values themselves


    

    