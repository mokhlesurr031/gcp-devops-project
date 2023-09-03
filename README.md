# GCP DevOps Project

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



















