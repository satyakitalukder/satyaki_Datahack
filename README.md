# satyaki_Datahack

This is a project based on a Hackathon conducted by IIT Guwahati in collaboration with Geeks for Geeks

DESCRIPTION OF THE PROJECT :
    Our goal is to predict how likely individuals are to receive their 'xyz' and 'seasonal' flu vaccines. Specifically, we'll predict two probabilities(and not binary class): one for 'xyz_vaccine' and another for       'seasonal_vaccine'.
    ---> The two target variables are :
        ● xyz_vaccine - Whether the respondent received xyz flu vaccine.
        ● seasonal_vaccine - Whether the respondent received seasonal flu vaccine.
        Both are binary variables: 0 = No; 1 = Yes. Some respondents didn't get either vaccine, others got only one, and some got both. This is formulated as a multilabel(and not multiclass) problem.

STEPS 
---> Performing some exploratory data analysis and feature transformations to clean up the data 👌
---> Using the 'Correlation Matrix' to find relative feature importance and correlation among various features to tweak the feature columns as required 🕵️
---> Using the 'Seaborn Heatmap' to locate and eliminate some of the empty values in the feature columns, and using some basic intuition to select the most important features for modelling 😎
---> I have used the 'Histogram Gradient Boosting' Algorithm, which has many specialities but here's why I used it in this particular case...
    🎈The Histogram Gradient Boosting Classifier is used because it’s efficient with large training datasets(like ours), handles categorical features well, and deals with missing values effectively. It can handle 
     non-linear relationships in data, making it a powerful tool for classification tasks.
    🎈Since our Test dataset had many missing values and some belonged to the important feature columns, this model is used. (ps: I wouldn't just drop thousands of entries(people in our case) just because their 
     'health insurance' data is somehow missing, and I wouldn't fill them with any statistical replacements(mean, mode, median) because it would cause much bias, because the missing values are numerous)
    🎈This classifier model gave the highest mean ROC-AUC score for this dataset, which was the main evaluation metric for the project(model).
---> The last part contains a comparison with the 'Support Vector Machine' Algorithm with the 'Linear' kernel, which performed well too, in this dataset, but the accuracy metric and ROC-AUC score were still 
     better for the 'Histogram Gradient Boosting' Algorithm. 👍

     (-- The Python code of the model can be found in this repo. It is named 'satyakitalukder_Datahack.ipynb')
     (-- The final prediction of the model on the test set can be found in the same, in the name 'final.csv')
     (-- Other related doccuments can be found on the repo itself)
