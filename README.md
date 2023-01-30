# Machine Learning Model Training and Interaction with SageMaker Feature Store
This repo holds code for training a ML model and integrating it with SageMaker Feature Store for batch transformations and feature group updates. The model is trained using features from the Offline Feature Store and batch scoring is done using features in CSV and Parquet format from the same store. The labs also demonstrate how to etrieve records from the Online store for real-time and batch inference using single and multiple records.

## Requirements
- Amazon SageMaker
- Python 3.x
- AWS CLI
- AWS SDK for Python (Boto3)

## Data Ingestion
The data ingestion process involves extracting data from its source, cleaning and transforming it, and finally loading it into the SageMaker Feature Store. The data used in this project is stored in an S3 bucket.
![image](https://github.com/aws-samples/amazon-sagemaker-feature-store-end-to-end-workshop/raw/main/images/workshop.png)

## Model Training and Inferencing

### Leverage offline feature store for model training

- Training a model using feature sets derived from the Offline feature store
- Perform batch scoring using feature sets derived from Offline feature store in CSV and Parquet format
- Update customers Feature Group to add new feature, ingest data into the feature group and retrain XGBoost model using this data.

### Leveraging the online feature store for inference

- Get record from the online feature store during single inference.
- Use a feature set to retrieve features from multiple online feature groups in a single call from the endpoint.
- Use a SageMaker Inference Pipeline to allow feature retrieval to be clearly separated from model inference.
