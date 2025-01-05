# British-Airways-Job-Simulation-Project


Task 1:
Background information - 
British Airways (BA) is the flag carrier airline of the United Kingdom (UK). Every day, thousands of BA flights arrive to and depart from the UK, carrying customers across the world. Whether it’s for holidays, work or any other reason, the end-to-end process of scheduling, planning, boarding, fuelling, transporting, landing, and continuously running flights on time, efficiently and with top-class customer service is a huge task with many highly important responsibilities.

As a data scientist at BA, it will be your job to apply your analytical skills to influence real life multi-million-pound decisions from day one, making a tangible impact on the business as your recommendations, tools and models drive key business decisions, reduce costs and increase revenue.

Customers who book a flight with BA will experience many interaction points with the BA brand. Understanding a customer's feelings, needs, and feedback is crucial for any business, including BA.

This first task is focused on scraping and collecting customer feedback and reviewing data from a third-party source and analysing this data to present any insights you may uncover.

1. Scrape data from the webite called Skytrax
2. Analyse data
3. Present insights

Objective: Understanding customer reviews and identifying key themes and sentiments.


Methodology: Scrape data from Skytrax, preprocess it and use LDA for topic modeling and Vader for sentiment analysis.


Key Findings: 
• Overall Positive Experience: 54.9% positive reviews vs 30.9% negative
• Strong positive sentiment clustering (0.75-1.0 range)
• High focus on core service elements: seating, timing, and crew


![image](https://github.com/user-attachments/assets/3c34ac80-9285-4d13-85e0-cb853d730a42)
* This suggests that overall, customers are generally satisfied with British Airways services.


Task 2:

Explore and prepare the dataset, considering new features for a predictive model. Train a machine learning model to predict customer bookings, evaluating its performance and interpreting variable contributions.

* Random forest is chosen for its ability to handle various data types, provide feature importance, mitigate overfitting and can capture non-linear relationships.

Methodology: 
* An evident imbalance (8504 vs. 1496 samples) distorted the model’s preference for the majority class (0). Consequently, we employed SMOTE and SMOTEENN to enhance recall for the minority class, which is paramount for identifying holiday buyers and addressing class imbalance.
* To ensure the class distribution’s consistency across folds, we utilized StratifiedKFold.
* Furthermore, we adjusted the threshold for predicting class 1 (the minority class) based on the ROC curve to optimize recall and achieve a more balanced evaluation of metrics.

Key Findings:
 * Booking origin is the strongest predictor, accounting for ~21% of model decisions
 * Length of stay and total add-ons are the next most important features
 * Model shows good discrimination ability (AUC: 0.77) but has room for improvement
 * High false positive rate suggests opportunity to refine targeting criteria
 * Travel-related features (route, popularity) and customer preferences (baggage, meals) show moderate importance


![Slide1](https://github.com/user-attachments/assets/3c5ec185-c33b-404a-9a60-bd276d587d3a)


