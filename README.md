# Financial-Statement-Fraud-Detection
The project's aim was to flag fraudulent financial statements from companies that have been issued a guarantee from an insurance company. The purpose is to ensure the financial information used in the credit risk modelling process is sound.



The deliverables were:

- A solution that can handle new incoming data and flag the fraudulent financial statements.
- Analysis of the predicted fraud across different features.
- Comparison of the prediction models used.


In the course of the project, my team was given a dataset containing financial statements from companies spanning across different industries like construction, logistics etc. and we were tasked to use features like EBITA, Revenue, Default Status etc. to find patterns between similar statements in the dataset. Since there was no ground truth given in the dataset (no labels) as to whether a financial statement was fraudulent or not, We applied an ensemble of 3 unsupervised machine learning techniques, these techniques include; Isolation forest model, Auto-Encoders and Ratio Analysis, After obtaining classifications from each of the models, an ensemble model was formed in the following pattern:

1. If all the models indicates a statement is not fraudulent, we classify that as “Not Fraudulent” with a Fraud Probability of 0

2. If 1 out of the 3 models indicates a statement is fraudulent, we classify that as “Unlikely Fraudulent” with a Fraud Probability of 1/3 or 0.33

3. If 2 out of the 3 models indicates a statement is fraudulent, we classify that as “Likely Fraudulent” with a Fraud Probability of 2/3 or 0.67

4. If all 3 models indicates a statement is fraudulent, we classify that as “Fraudulent” with a Fraud Probability of 3/3 or 1.

After this model was developed, we launched the solution in form of a streamlit application and deployed on AWS EC2, where a user an upload their financial statement and get the classification in real time.

## NOTE: 
The Dataset used for this project contains sensitive information, Hence I'm unable to share the code.However I have added a demonstration of our solution; a streamlit web app that classifies financial statement and gives a result of the analysis in a downloadable csv format.



https://github.com/nuel000/Financial-Statement-Fraud-Detection/assets/102439386/33cf55a7-e893-48c3-be48-2b52de715dde




