We’re loading data about URLs, cleaning it up, and training two different models to predict which URLs might be phishing sites. We’re running this process multiple times to make sure our results are reliable.
By logging everything to W&B, we can easily track how well our models are doing, compare them, and see detailed performance metrics. This helps us decide which model is better for detecting phishing URLs.

STEPS TAKEN

Set Up the Environment:

Install W&B: This part makes sure we have the necessary tools to track our experiments.
Log in to W&B: Connects our code to our W&B account so we can log our experiment results.
Load and Inspect the Data:

Read the Data: We load a CSV file containing URL data.
Look at the Data: We take a quick look at the data to understand what it looks like and check for any missing or duplicated information.
Visualize the Data:

Histograms and Box Plots: These graphs help us see the distribution and spot any unusual data points.
Missing Values Heatmap: This shows us where data is missing, so we know how much of our data needs fixing.
Correlation Heatmap: Shows how different features of our data relate to each other.
Prepare the Data:

Convert Text to Numbers: Since machine learning models work with numbers, we convert any text data into numerical form.
Handle Missing Values: We fill in missing values to make sure our models can work with the data.
Train and Evaluate Models:

Repeat the Process: We run the experiment six times to ensure our results are reliable.
Split Data: We divide our data into training and testing sets.
Train Models: We build and train two types of models: Logistic Regression and Decision Tree.
Evaluate Models: We check how well each model performs by calculating their accuracy.
Log Results with W&B:

Log Metrics: We log the accuracy of each model for each run.
Log Predictions: We make predictions on a sample URL and log these predictions.
Detailed Reports: We log detailed performance reports, which include metrics like precision and recall.
This was the upload process using the commands
![image](https://github.com/user-attachments/assets/f90fb2ca-fe51-483e-aed7-087226af9d2d)

THE WEIGHTS AND BIASES RUNS
![image](https://github.com/user-attachments/assets/4bf13453-e565-4eb1-8a58-95d990414c1c)
![image](https://github.com/user-attachments/assets/f75d2320-2c47-498c-8aa8-37bbeb9a1deb)
![image](https://github.com/user-attachments/assets/39145d7b-9e4c-4a75-bc73-4dfcd54a6dc9)
![image](https://github.com/user-attachments/assets/a21d5596-a532-45a6-9d18-fcf57c93e737)



The Decision Tree model outperforms the Logistic Regression model with a higher accuracy of 95% compared to 75%. It shows better precision and recall, especially for the primary classes. Despite both models struggling with minor classes, the Decision Tree consistently provides more reliable predictions, making it the preferable choice for phishing URL detection.

By leveraging W&B for logging and visualization, we gained comprehensive insights into model performance, allowing for informed decision-making in selecting the best model for this task.
