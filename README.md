# End-to-End-Chest-Cancer-using-MLflow-DVC

# Workflows

 1.Update config.yaml <br>
 2.Update secrets.yaml [Optional] <br>
 3.Update params.yaml <br>
 4.Update the entity <br>
 5.Update the configuration manager in src config <br>
 6.Update the components <br>
 7.Update the pipeline <br>
 8.Update the main.py <br>
 9.Update the dvc.yaml (dvc/data version control-  for pipeline tracking) <br>


## MLflow
- [Documentation](https://mlflow.org/docs/latest/index.html)


- MLflow learning

cmd

- mlflow ui

## dagshub

- [dagshub](https://dagshub.com/dashboard)

```cmd
MLFLOW_TRACKING_URI=https://dagshub.com/swaroopyadav/chest-Disease-Classification-MLflow-DVC.mlflow
MLFLOW_TRACKING_USERNAME=swaroopyadav
MLFLOW_TRACKING_PASSWORD=6824692c47a4545eac5b10041d5c8edbcef0
python script.py
```


# Add MLFlow credientials to your local_machine env variables: <br>

- Open env and add <br>

MLFLOW_TRACKING_URI=https://dagshub.com/swaroopyadav/chest-Disease-Classification-MLflow-DVC.mlflow

MLFLOW_TRACKING_USERNAME=swaroopyadav

MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9353c5b10041d5c8edbcef0


## DVC (data version control - Pipeline Tracking)
1) dvc init <br>
2) dvc repro <br>
3) dvc dag  <br>


## About MLflow & DVC (summary)
MLflow

- Its Production Grade
- Trace all of your expriements
- Logging & taging your model

DVC

- Its very lite weight for POC only
- lite weight expriements tracker
- It can perform Orchestration (Creating Pipelines)


## AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console. <br>
## 2. Create IAM user for deployment <br>

- with specific access
```cmd
 (Key-Points)
 
1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2


#Policy:
Note: (while creating in IAM user add these policies)

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```
## 3. Create ECR repo to store/save docker image
```cmd
- Save the URI: 443370711849.dkr.ecr.us-east-1.amazonaws.com/chest
```
## 4. Create EC2 machine (Ubuntu)
## 5. Open EC2 and Install docker in EC2 Machine:
```cmd
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```
- Additional After succesfull installation,
```cmd
Note: If wanted to verify docker is running,
docker --version
```

## 6. Configure EC2 as self-hosted runner: (Note: In GitHub)
```cmd 
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```
## 7. Setup github secrets: (Under Secrets and variables>actions)
```cmd
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = Mentain Repository name which you have given
```
