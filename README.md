## Quantitative Analysis of Fundamentals by Machine Learning  

### Brief Introduction
1. Quantitative analysis of fundamentals in quarterly reports by Machine Learning.  
2. Preprocess data from raw data before model training.
2. Use 20 fundamental attributes to fit the model.  
3. Use 10 Machine Learning Models to do the training and prediction.  
4. After each model, do the result analysis.

### Data Details
1. Choose target stock: 600188.SH (兖州煤业).  
2. Time period: year 2003 - year 2019.  
3. Fundamentals are extracted from quarterly reports of target company (兖州煤业).
4. **Fundamental attributes**: gross revenue, revenue, total operating cost, selling expense, administration expense, financial expense, net investment income, operating profit, retained profit, net income attributable to parent company, basic EPS, total shares, total assets, current assets, total liabilities, current liabilities, minority equity, intangible assets, goodwill.
5. **Machine Learning Models**: AdaBoost Model, Decision Tree Model, Dummy Classifier Baseline Model, Gradient Boost Model, KNN Model, LogReg Model, Naive Bayes Model, Random Forest Model, SVM Model, XGBoost Model.  
6. Data source: *Wind*

### Algorithm Pipeline
1. **Data Preprocessing** 
- Do data preprocess, including data clean, replacing values with percent difference.   
- Export new data which have been preprocessed.
2. **Create Labels** 
- Create trade decisions in regard to percent change of high and low price. 
- There are 3 trade decisions: sell, buy, hold. These are labels for machine learning later.   
3. **Explore the data**
- Visualize the count of Buy, Hold, and Sell.
- Check for any correlation between the future price and the current quarter's features.
- Get and visualize feature importances using ExtraTreesClassifier.  
- Select top 10 features (respectively correlation and importance) and save into Excel files.
4. **Training and prediction of Machine Learning Model**
- Scale the Data.
- Split the Data.
- Plot confusion matrix.
- Fit and Train.
- Print out Evaluation Metrics.
- Tune model parameters.
- Show tuned results and choose optimal result.
- Model with the best parameters.
- Show results and confusion matrix from optimum parameters.
- Save the optimal model we trained into .m file.
5. **Classify new data using well-trained models**
- Extract trained classifier and new data for prediction.
- Preprocess data.
- Do prediction and analysis result of prediction.  

### Limitation and future work
- Since I get data from quarterly reports of one single firm, the amount of data is quite small for the training of Machine Learning. Therefore, the accuracy cannot be guaranteed much. 
- This whole project is more likely a very complete and good practice using Machine Learning Models to analyse fundamentals. Then, the project goes on to find trade decisions using trained classifiers.
- Maybe I will get more data (more firms) to train models to get higher accuracy.




