# MLflow_starter

MLFLOW_TRACKING_URI=https://dagshub.com/swaroopyadav49/MLflow_starter.mlflow
MLFLOW_TRACKING_USERNAME=swaroopyadav49
MLFLOW_TRACKING_PASSWORD=a6b42b3aa2d3e12e2768fc2a50c86000eed68b72
python script.py


```cmd
add "MLFLOW_TRACKING_URI" ID in local Env
```

```cmd
add "MLFLOW_TRACKING_USERNAME" ID in local Env
```

```cmd
add "MLFLOW_TRACKING_PASSWORD" ID in local Env
```


## MLflow on AWS
# MLflow on AWS Setup:

1.Login to AWS console.
2.Create IAM user with AdministratorAccess
3.Export the credentials in your AWS CLI by running "aws configure"
4.Create a s3 bucket
5.Create EC2 machine (Ubuntu) & add Security groups 5000 port


## Run the following command on EC2 machine

```cmd

sudo apt update

sudo apt install python3-pip

sudo apt install pipenv

sudo apt install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell

```


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-buc49

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-34-227-148-52.compute-1.amazonaws.com:5000
