[![CircleCI](https://dl.circleci.com/status-badge/img/gh/sirdesmond09/devops_project4/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/sirdesmond09/devops_project4/tree/master)

## Project Overview

This project deployes a Machine Learning Microservice API. 

I was given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms, highway access, and so on. More details about the data can be found on [the data source site](https://www.kaggle.com/c/boston-housing).
### Project Tasks

Here is a list of task that was performed:
* Test project code using linting
* Complete the Dockerfile to containerize the application
* Deploy the containerized application using Docker and make a prediction
* Improve the log statements in the source code
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested


---
### Short description of folders and files in the repo

* [.circleci](/devops_project4/.circleci): For the CircleCI build
* [model_data](/devops_project4/model_data) : this folder contains the pretrained `sklearn` model and housing csv files
* [output_txt_files](/devops_project4/output_txt_files): folder contains sample output logs from running `./run_docker.sh` and `./run_kubernetes.sh`
* [app.py](/devops_project4/app.py) : contains the flask app. Flask is a python web framework
* [Dockerfile](/devops_project4/app.py): contains instructions to containerize the application
* [Makefile](/devops_project4/Makefile) : contains instructions for environment setup and lint tests
* [requirements.txt](/devops_project4/requirements.txt): list of required dependencies
* [run_docker.sh](/devops_project4/run_docker.sh): bash script to build Docker image and run the application in a Docker container
* [upload_docker.sh](/devops_project4/upload_docker.sh): bash script to upload the built Docker image to Dockerhub
* [run_kubernetes.sh](/devops_project4/run_kubernetes.sh): bash script to run the application in a Kubernetes cluster
* [make_prediction.sh](/devops_project4/make_prediction.sh): bash script to make predictions against the Docker container and k8s cluster
* [README.md](/devops_project4/README.md): this README file

### Instructions
## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
