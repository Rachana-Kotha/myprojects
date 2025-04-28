Online Retail Data Clustering Project
Project Overview
This project focuses on designing and implementing a complete Machine Learning Solution for clustering online retail customer data.
The objective is to segment customers based on purchasing behavior using unsupervised learning techniques, while managing the end-to-end ML lifecycle through Azure Machine Learning (AML).

The project covers data exploration, model training, model evaluation, deployment preparation, and MLOps practices, using Azure services like Compute Instances, Data Assets, Pipelines, and MLflow for tracking.

Project Plan

Phase	Description
1. Workspace Management	Created and configured an Azure ML Workspace and connected GitHub for source control.
2. Data Management	Registered online retail datasets into AML using Azure Storage and created versioned data assets.
3. Compute Management	Set up compute targets: CPU compute instances, serverless Spark pools, and configured environments for scalable model training.
4. Data Exploration	Wrangled and preprocessed data using Spark compute; addressed missing values, outliers, and standardized features.
5. Model Training	Designed and trained clustering models using Azure ML Designer and Notebooks; implemented AutoML for model selection.
6. Model Evaluation	Evaluated clustering performance (e.g., silhouette score) and ensured responsible AI practices.
7. Deployment Preparation	Packaged and registered the final model; logged metrics via MLflow; created training pipelines with job configurations.
8. Deployment and MLOps	Deployed models to Azure online endpoints and batch endpoints; implemented retraining triggers using Azure DevOps and event-based pipelines.
Data Preparation
Source: Online Retail Transaction Dataset

Preprocessing Steps:

Removed null and duplicate entries.

Engineered features like TotalSpend, Frequency, Recency for RFM Analysis.

Normalized variables to improve clustering.

Created train/test datasets as AML data assets.

Modeling Approach
Algorithms Used:

KMeans Clustering

Hierarchical Clustering (exploratory)

DBSCAN (alternative approach for density-based clustering)

Tools:

Azure ML Designer for drag-and-drop model pipelines

Automated ML for model and hyperparameter optimization

Python SDK v2 for advanced custom training scripts

Tracking:

Used MLflow to log:

Clustering metrics

Hyperparameters

Model artifacts

Deployment Strategy
Model Registration:

Packaged the best model (KMeans) into the Azure ML Model Registry.

Online Deployment:

Created an Azure Online Endpoint for real-time scoring.

Batch Deployment:

Configured a Batch Endpoint to process large customer datasets periodically.

Retraining Strategy:

Scheduled model retraining based on new data arrival triggers.

Integrated retraining pipelines with Azure DevOps for CI/CD.

Observations
Cluster Insights:

Found meaningful customer segments such as:

High-value repeat customers

Infrequent but high-spending customers

Discount seekers

Performance:

Best model (KMeans) achieved a Silhouette Score of 0.65, indicating reasonable cluster separation.

Challenges:

Sparse transactional data required careful feature engineering.

Choosing the optimal number of clusters (k) involved using the elbow method and silhouette analysis.

Tech Stack
Language: R, Python

Cloud Platform: Azure Machine Learning

Compute: Azure Compute Instances, Serverless Spark Pools

Source Control: GitHub Integration

Tracking and Logging: MLflow

Pipelines: Azure ML Pipelines (Component-based architecture)

Deployment: Azure Online Endpoints and Batch Endpoints

How to Reproduce
Clone the Repository:

bash
Copy
Edit
git clone <repository_link>
Set Up Azure ML Workspace:

Create a new Azure ML Workspace.

Attach a Compute Instance and a Serverless Spark Pool.

Register Data Assets:

Upload and register the Online Retail Dataset as a data asset.

Run Training Pipelines:

Launch the pipeline from Azure ML Studio or use the provided notebooks to train models.

Model Evaluation:

View evaluation metrics logged through MLflow in Azure ML Studio.

Deploy the Model:

Deploy the trained model to an Online or Batch Endpoint.

Set Up Retraining:

Configure triggers for retraining through Azure DevOps Pipelines.
