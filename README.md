# Data Analytics & Science Portfolio

## Data Analytics Projects

### Tableau Visualisation on Superstore Dataset
I analysed the Superstore dataset, which contains data of the sales of a company in the USA. Some of the columns include Order ID, Order Date, Ship Mode, Item Category and Postal Code. With this data, I created an interactive dashboard on Tableau consisting of KPI indicators, a map and area graphs for sales profit analysis by city, customer segment and item category.

![Executive Summary Dashboard on Tableau](/tableau_ss_dashboard.png)

The interactive features can be viewed via this link: [Superstore Dashboard](https://public.tableau.com/app/profile/irfan.muzafar/viz/ExecutiveOverview_17296907596580/Dashboard1)

### Data Analysis (Excel) on Superstore Dataset
I analysed the dataset on Microsoft Excel using functions such as pivot tables and VLOOKUP. Thereafter, I produced insightful visualisations by answering various problem statements. 
Problem Statement 1: Is there a pattern/trend of the orders shipped over time? 

![Number of Orders by Year & Month](/excel_line.png) 

From the line graph, we observe that the busier months tend to be September and December. There could be a trend related to back to school or holiday season. We might need additional data in future analysis to confirm.

Problem Statement 2: Do some customer segments have more shipments by ship mode than others?
Customer Segment consists of Consumer, Corporate or Home Office. The ship modes are First Class, Same Day, Second Class and Standard Class.

![Number of Orders by Ship Mode & Customer Segment](/excel_stackedbar.png) 

From the stacked bar chart, we observe that Consumer and Corporate segments (blue & orange) look to have the bulk of the orders in Standard Class and Same Day. Also, Second Class and First Class are fairly equal between Corporate and Home Office (orange & grey). Lastly, regardless of ship mode, Consumer (blue) makes up the largest percentage compared to other customer segments.

### SQL Queries on Iowa Liquor Sales & WSDA Music Database
Worked on two databases that contain tables such as sales, customer, invoice and track. Queried multiple prompts by joining multiple tables, applying aggregate and date functions and subqueries on DB Browser for SQLite via LinkedIn Learning. For example, if we want as many customers as possible to spend between $7 and $15, we can create categories for the purchase type. We can use CASE function to create a new column which classifies the purchase type. The query can be seen in the image below.

![Using CASE to create new 'Purchase Type' column](/sql_create_column.png) 

Then it will return five columns, with 'Purchase Type' as the last column, indicating in each row either 'Baseline Purchase', 'Low Purchase', 'Target Purchase' or 'Top Performer'. It will also be ordered alphabetically by the billing city (A to Z).

## Data Science Projects @ General Assembly

### Accident Severity Image Multi Classifier
While analysing traffic accident fatalities and injuries data in Singapore, I found that the injury numbers are very high every year and there is an increasing trend in the number of fatalities and injuries from 2020. With that, I obtained an accident severity image dataset, classified into five accident severities: Fire, Minor, Moderate, No Accident and Severe, from Roboflow. 

![Severity Classes](/capstone.png) 

I built classifier models using a self-trained Convolutional Neural Network and three pre-trained models: MobileNetV2, VGG19 and EfficientNetB4. Considering their train/test accuracy scores and extent of overfitting, I chose MobileNetV2 model as our best model for hyperparameter tuning. Applying image augmentation on the images and regularisation methods on the model, I achieved an accuracy score of 0.834. As additional work, I explored using Zero-Shot Image Classification, which uses a large language model by OpenAI to predict an image via "candidate labels". Using our best model, I built a streamlit app for the multi classification. Inputting recent traffic accident images into our app, our app predicts each image to be in one of the five accident severity categories.

### Mild Stroke Detection
My group conducted research on stroke symptoms and numbers in USA. Since mild stroke symptoms can mimic other neurological symptoms, we decided to try and build a model that can detect a mild stroke based on a Kaggle dataset containing lifestyle factors of individuals. We conducted initial analysis on the dataset using visualisations to observe the distribution for BMI of the sample population, stroke occurence for each age group and high risk factors that can relate to stroke.

![Exploratory Data Analysis](/p4_eda_age.png) 

We first classified between Stroke and No Stroke, using Decision Tree, Random Forest, Bagging, Adaboost, Support Vector and Gradient Boost models for comparison. After hypertuning, we selected Gradient Boost as our best model, with an F1 score of 0.767. Then, we applied KMeans, Density-Based and Hierachical clustering to those wrongly classified to capture Mild Stroke cases.

![Clustering Algorithms](/p4.png) 

However, no clear clusters were found, partly due to the many binary features of the dataset. We also tried to use key features only, like high blood pressure and high cholesterol to relate to the presence of stroke, but we were still unable to find clear clusters.

### Delivery & Ride Hailing Classifier
Conducting sentiment analysis on each ride hailing app reviews in Singapore, my group compared each sentiment score with each app overall rating. We found that app overall ratings do not show the full picture of the app reviews. Thus, we decided to dive deeper into app reviews for Grab. Applying Natural Language Processing (webscraping and lemmatization) to uberEATS and uber subreddits, we built classifier models using Naive Bayes, K Nearest Neighbours and Logistic Regression. 

![Computational Intensity](/p3.png) 

We chose Naive Bayes model as our best model as it has the highest accuracy score of 0.775. Through our streamlit app, we then applied this model to Grab reviews on Google Play Store to classify between delivery reviews and ride hailing reviews. Our app is able to classify the reviews in a fast and accurate manner.

### HDB Price Predictor
While choosing a set of features that can affect the resale price of a HDB flat, my group built a price predictor model using linear regression. We also refined our model using regularisation methods like Ridge and Lasso to get a better R2 score of 0.87. Applying our model to our app, users can select a set of features and predict the price of a resale flat. 

![Flat Price](/p2.png) 

For example, a user can set the flat type to be a 4-room flat and the town to be Queenstown and predict the resale price. With our highly accurate model, sellers can avoid selling their flat at a price that is too low or too high.
