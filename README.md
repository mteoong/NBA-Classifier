# NBA Win Prediction using Classification and Regression

## 1. Summary
- Developed an accurate predictor of an NBA team’s final win percentage and playoff status by combining traditional statistics, like rebounds per game, and advanced statistics, like true shooting percentage. 
- Compared the accuracy of the predictor after 10 games, 20 games, and 81 games. Achieved a Root Mean Squared Error of 3.3% for the regression and 94% accuracy for the classifier. 
- Surprisingly, after 10 games the predictor was already quite accurate, and after 20 games the increase in accuracy with more games dropped off significantly.
- Performed feature selection on over 60 statistics using the f_regression and SelectKBest functions to account for negative values (specifically for +/-, net rating, etc...).
- Compared the results of 6 classification models and 6 regression models such as linear regression, random forest, KNN, and SVM. 

## 2. Results Summary
![Screen Shot 2021-07-10 at 10 59 55 AM](https://user-images.githubusercontent.com/62133678/125149837-f8fdce80-e16d-11eb-956f-8a2765961b54.png)

## 3. Methodology
  #### 1. Data Scraping
  - Scraped data from the official NBA.com statistics database. Collected data from 2000 to 2021 (earliest available data was from 1997). 
  - Downloaded the data as a CSV and imported it into a jupyter notebook for analysis. 
  #### 2. Data Cleaning
  - Collected data from multiple pages (datasets on NBA.com were separated into multiple pages for traditional, advanced, and opponent statistics) and combined them into one table. Converted all the data into suitable formats for analysis. 
  #### 3. Feature Selection
  - Used three methods to determine which features to use out of the ~65 available metrics (from traditional, advanced, and opponent statistics).
    1. Used seaborn pairplot to create scatter plots of all the features and their correlation to win percentage. Also colored plots according to playoff status. 
    2. Applied the f_regression and SelectKBest class methods to extract the top features and compare their F statistics to help determine how many significant       features there were. 
    3. Plotted a correlation matrix with a heat map using the seaborn library. 
  #### 4. Classification and Regression Models
  - The following 6 classification models were applied and compared: Decision Trees, Logistic Regression, Support Vector Machines, K Nearest Neighbors, Random Forest, and Gradient Boost. 
  - The following 6 regression models were applied and compared: Linear Regression, Bayesian Ridge, Elastic Net, Logistic Regression, Gradient Boost, and Support Vector Regression. 
  #### 5. Evaluation
  - Classifier models were evaluated using their accuracy score and their confusion matrix. 
  - Regression models were evaluated using the root mean squared error. 

## 4. Feature Selection
#### Seaborn Pairplot
![Screen Shot 2021-07-10 at 11 49 16 AM](https://user-images.githubusercontent.com/62133678/125150769-efc43000-e174-11eb-91e1-a40b630c9f22.png)

#### F-Regression
![f-regression-81](https://user-images.githubusercontent.com/62133678/125149961-d91ada80-e16e-11eb-809b-caa2c9a251aa.png)

### Heat Map
![heat-map](https://user-images.githubusercontent.com/62133678/125149968-dddf8e80-e16e-11eb-9f0c-da46ba1f7f3c.png)


## 5. Results
![Screen Shot 2021-07-10 at 10 56 57 AM](https://user-images.githubusercontent.com/62133678/125149782-8f7dc000-e16d-11eb-8c6d-5f31108262e9.png)
![Screen Shot 2021-07-10 at 10 57 18 AM](https://user-images.githubusercontent.com/62133678/125149785-99072800-e16d-11eb-90a5-c09d283e6839.png)
![Screen Shot 2021-07-10 at 10 57 23 AM](https://user-images.githubusercontent.com/62133678/125149787-9c021880-e16d-11eb-859a-93e4e5a07d50.png)
![Screen Shot 2021-07-10 at 11 02 05 AM](https://user-images.githubusercontent.com/62133678/125149880-4712d200-e16e-11eb-874a-0affe46cf4d3.png)
