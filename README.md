# Methamphetamine Use Classification
Project investigates underlying risk factors for meth usage to combat increase in overdoes related deaths.
Data obtained from 2020 U.S. Department of Health and Human Services published annual National Survey on Drug use and Health (NSDUH).
# Solution Strategy
Utilizing Data From Survey, Tree based Ensemble ML models were used to classify meth usage. Data ETL processing done using Pandas and EDA done to identify key drivers to use as features for model.
Classification was heavily imbalanced so different sampling methods (Under, Over, SMOTE) were utilized to re-balance labels for modelling. 
Models evaluated based on routine classification metrics but due to imbalance, Accuracy was of lower importance, instead metrics such as AUPRC, F1-Score and Recall were selected as key evaluation criteria.
# Result
Three (3) star models chosen from best model on 3 sampling techniques:
1. Random Forest Classifier - Undersampling
2. Gradient Boosted Classifier - Oversampling
3. Light GBM Classifier - SMOTE sampling.

Out of these 3 models, the GBC performed the best when a balanced comparion of the 3 key metrics are done. Using the GBC model, an attempt was made to formulate some simple rules to guide meth usage prediction - thus allowing a better understanding of risk factors.
![image](https://github.com/davidpcg01/methUseClassification/assets/88422385/84dd570d-ed06-4e59-9698-e94fe8e6e4be)

For some more intuitive rules, the following were proposed:
1. A person with early first Marijuana usage (<18 years), Adult Cocaine usage and Hallucinogen use within the past year and has arrest history is more likely to delve into meth usages in their mid-30’s to late 40’s
2. A person with no history of cocaine or hallucinogen usage and adult usage of marijuana with no prior arrests or bookings less likely to delve into meth usage

See full report and notebook for detailed analysis and conclusions.

