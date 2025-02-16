# Run Notebook in the server
Datasets are not included here. Both the datasets are synthetically generated and are highly imbalanced

## 1. Install all the dependencies
```
pip install -r requirements.txt (
```
This may take a minute or two.
## Task 1: Credit Fraud Detection - System Training
PS4_task1_training.ipynb trains a random forest model on the testing credit fraud data - THIS IS ALREADY RAN
The model is exported as 'task_1_model.pkl'

## Task 1: Cred Fraud Detection - Prediction
prediction.ipynb uses the model to make label predictions (is_fraud, not_fraud)
Insert test path of dataset:  test_data_path = 'cct_train.csv'
Change file name to name of testf file.
Prints out the columns used for prediction and relevant metrics

## TASK 2: HUMAN ACTIVITY RECOGNITION

The model predicts the type of human activity (11 types of activities) based on different sensors' data.

## How to train the model

Run the file "PS4_task2_training.ipynb" entirely. It trains SVM and XGBoost models separately just to check the performance and then Voting Classifier is trained. Then the StandardScaler that is fit on the train data and the Voting Classifier are saved in the "pipeline_task2.pkl" file.
Also, the label encoder that is fit on the train data is saved in the "label_encoder_task2.pkl" file.

## How to test the model

In the file, "prediction.ipynb" Change the file name "har_train.csv" to the name of the test file being provided. Then run the code below. Model is loaded and metrics are reported on the given test data.
