# End-to-End-Chest-Cancer-Classification-using-MLflow-DVC

This project is an **end-to-end pipeline** for predicting chest cancer using **deep learning (VGG16)** integrated with **MLOps practices** such as **DVC, MLflow, Docker, and CI/CD on AWS**.  

---

## 🚀 Features
- Chest X-ray data ingestion and versioning with **DVC**
- Preprocessing & augmentation for better generalization
- **Transfer Learning with VGG16** for cancer classification
- Experiment tracking using **MLflow**
- Automated CI/CD with **GitHub Actions**
- Model deployment on **AWS EC2/S3** with Docker + Flask/FastAPI

---
In the example below, a **normal chest X-ray** was uploaded to the model, and it correctly predicted the result as **Normal** ✅.
<h2>🎯 Sample Prediction</h2>

<p align="center">
  <img src="images/Screenshot (61).png" alt="Sample Prediction" width="500"/>
</p>


## 📂 Project Structure


## Workflows
1.	Update config.yaml
2.	Update secrets.yaml[Optional]
3.	Update params.yaml 
4.	Update the entity 
5.	Update the configuration manager in src config
6.	Update the components 
7.	Update the pipeline
8.	Update the main.py
9.	Update the dvc.yaml


### dagshub
MLFLOW_TRACKING_URI = "https://dagshub.com/Manashranjan/End-to-End-Chest-Cancer-Classification-using-MLflow-DVC.mlflow"
MLFLOW_TRACKING_USERNAME = "Manashranjan" 

MLFLOW_TRACKING_PASSWORD = "f4bf17c8688cb1ce18790ecb3c982f1fcfe449cc"

Run this to export as environment variable:
```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/Manashranjan/End-to-End-Chest-Cancer-Classification-using-MLflow-DVC.mlflow
export MLFLOW_TRACKING_USERNAME=Manashranjan
export MLFLOW_TRACKING_PASSWORD=f4bf17c8688cb1ce18790ecb3c982f1fcfe449cc
```

# End-to-End-Chest-Cancer-Classification-using-MLflow-DVC


## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml

### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


## About MLflow & DVC

MLflow

 - It is a Production Grade tool
 - Trace all of your expriements
 - Logging & taging your model


DVC 

 - Its very light weight for POC only
 - light weight expriements tracker
 - It can perform Orchestration (Creating Pipelines)



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 785202558418.dkr.ecr.eu-north-1.amazonaws.com/chest

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app


