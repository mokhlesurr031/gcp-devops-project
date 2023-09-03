# GCP DevOps Project


### GCP services used:
1. GKE - Kubernetes Engine.
2. Cloud Build - The CI/CD tool responsible for deploying something to GCP from out github is called cloud build. 
3. GCP Artifact Registry - For storing docker images and others. 
4. Secret Manager API


Sprint: A set period of time during which specific work has to be completed and made ready for review. 

Steps of sprint:
1. Backlog Grooming - Curated list of tasks to be worked on. 
2. Sprint Planning - Tasks can be picked based on team capacity. 
3. Sprint - Work time allocated to complete the tasks (1 week or 2 weeks)
4. Sprint Review - Review of the work completed. 


## Sprint - 01 

Sprint Goals: 
1. Creating a github repository. 
2. Setup the repository according to the company's best practice. 
3. Write the code for a sample docker image. 
4. Testing the code locally. 
5. Pushing the code to the github repository. 


## Sprint - 02 

Sprint Goals:
1. Creating a GCP account. 
2. Understand the fundamentals of GKE in GCP. 
3. Setup the GKE cluster. 

Note: While practicing on GCP, it is always better to delete everything after practicing lab session in a personal account, otherwise it may charge. 

### Setting up Billing Alerts in GCP.

We want to setup an alert so that if we exceed the threshold, it gives us alert. 

1. Login to the account. 
2. Search for Billing.
3. In left panel, there's an option called Budget & Alerts. Click on it and go for creating a budget. 
4. Put a name for budget, ex: learning_budget. Click Next. 
5. Set a budget on montly or yearly basis. Click Next. 
6. You can set budget alert schedule. Click Finish if done. 

Note: You can create multiple budget here on various parameter like amount, resource level and others. 


Creating GKE cluster:
1. Search for GKE and select Kubernetes Engine. 
2. Click Enable, it may take some time to enable. 
3. Two options available for GKE:
    a. Autopilot - Most of the things that we do to maintain a GKE cluster, is taken care by GCP itself.
    b. Standard - You will have to do some kind of maintainance activity. 

4. Click create and we will go do standard cluster. 
5. You can select image clicking in node pools option.

Node Pool: Is a bunch of machines that are put together, and they will be attached as the on pool of the machine in the GKE cluster. 

CLI installation: https://www.educative.io/answers/how-to-install-google-cloud-cli-on-debian-ubuntu
Connect Plugin: sudo apt-get install google-cloud-sdk-gke-gcloud-auth-plugin



## Sprint - 03

Spring Goals:

Deployment Design Things

1. CI/CD Desing process.
2. Deploying CI/CD process.
    a. Automated way to build the docker image.
    b. Store the docker image in an artifactory. 
    c. Write deployment/service yaml in k8s for deployment. 
    d. Setup CD to deploy this code to GKE using the docker image stored in artifactory. 



## Sprint - 04 

Cloud Build: CI/CD tool to build the softwares. 

Why:
1. Build software quickly across all programming languages, including go, java, nodejs and more. 
2. Chose from 15 machine types and run hundreds of concurrent build per pool. 
3. Deploy across multiple environments such as VMs, serverless, k8s or Firebase. 
4. Access cloud-hosted, fully managed CI/CD workflows within your private network. 
5. Keep your data at rest within a geographical region or specific location with data residency. 

Cloud Build connects to github using tool named Cloud Build Trigger.

Connecting your github repo to cloud build:

1. Search for cloud build and enable it. 
2. Select 2nd gen, clink on link repository. 
3. It may ask to enable Secret Manager API, enable it. 
4. Authenticate github repo. 
5. Write code in cloudbuild.yaml for CI process. If it runs properly. go to artifact registry and click on container registry. The built image should be there. 



## Sprint - 05

Extending the CI/CD process to deploy our Docker image on GKE cluster. 

Steps:
1. Creating a namespace in GKE cluster.
    a. Using cloud shell or terminal. 
    b. kubectl create namespace <name>
2. Creating a deployment file. 
    - in code
3. Update the Cloud Build code for deployment.
    - in code
4. Validating the deployment. 



## Sprint - 06

Exposing our Application. 


















