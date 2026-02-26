Winning the Space Race with Data Science
Predicting SpaceX Falcon 9 First-Stage Landing Success
Kimberley Usher | IBM Data Science Professional Certificate - Capstone Project
________________________________________
Overview
SpaceX disrupted the launch industry by recovering and reusing the Falcon 9's first-stage booster, cutting launch costs to approximately $62M compared to competitors charging $165M or more. Whether that booster lands successfully is therefore a critical cost driver.
This project uses publicly available SpaceX launch data to predict first-stage landing outcomes as a binary classification problem. It covers the full data science pipeline - from API data collection and web scraping, through exploratory analysis and interactive visualisation, to machine learning classification.
Key result: A Decision Tree classifier achieved 94.4% test accuracy, correctly identifying all 12 successful landings in the test set.
________________________________________
Project Pipeline
#	Stage	File
1	Data Collection - SpaceX REST API	01_data_collection_api.ipynb
2	Data Wrangling	02_data_wrangling.ipynb
3	EDA with Data Visualisation	03_eda_visualization.ipynb
4	Interactive Dashboard with Plotly Dash	spacex_dashboard.py
5	Predictive Analysis - Classification Models	05_machine_learning_classification.ipynb
________________________________________
Data
Launch data was collected from the SpaceX REST API (v4) and supplemented with historical Falcon 9 launch records from Wikipedia, merged into a unified dataset of 90 Falcon 9 launches.
Key features: Flight Number, Date, Booster Version, Payload Mass (kg), Orbit, Launch Site, Landing Outcome, Mission Outcome.
________________________________________
Key Findings
Exploratory Analysis
•	KSC LC-39A had the highest landing success rate (~76.9%) and the most successful launches overall (41.7% of all successes across sites)
•	Landing success improved markedly over time - from 0% in 2010–2013 to consistently above 80% from 2017 onwards
•	Orbit type is a strong predictor: ES-L1, GEO, HEO, and SSO all achieved 100% success; GTO had the lowest rate (~52%)
•	Heavier payloads (5,000 -10,000 kg) in later years showed near-perfect success rates, reflecting SpaceX's maturity with the B5 booster
Predictive Modelling
Model	Validation Accuracy	Test Accuracy
Logistic Regression	84.6%	83.3%
SVM	84.8%	83.3%
Decision Tree	88.8%	94.4% ✅
KNN	84.8%	83.3%
Best Decision Tree hyperparameters: criterion=gini, max_depth=4, splitter=random
Precision: 92.3% | Recall: 100% | F1-score: 96.0%
________________________________________
Tools & Technologies
Python Pandas NumPy Scikit-learn Matplotlib Seaborn Folium Plotly Dash BeautifulSoup SQLite Jupyter Notebook
________________________________________
Presentation
The full project report and slide deck is available here.

