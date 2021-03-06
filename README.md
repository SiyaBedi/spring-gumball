# CMPE 172 - Lab #10 Notes by Siya Bedi

## CI Workflow (Part 1)

### Navigated to "Actions" and created a new workflow:
![CI-1](images/CI-Workflow-2.png)

### I made a commit to the docker-compose.yaml to trigger the action
![CI-2](images/CI-workflow-1.png)

## CD Workflow (Part 2)

### GCP Service Accoucnt & JSON Service Account Key
![servicee-account](images/service-account.png)
![service-account-key](images/service-account-key.png)

### GitHub Action Secrets
![github-action-secrets](images/github-action-secrets.png)

## Trigger a CD Deployment by creating a new GitHub Release

### Created cluster
![cluster](images/create-cluster.png)

### Create Release
![release](images/create-release.png)

### Release success
![release-success](images/release-success.png)

### Workload
![workload](images/workloads.png)

### Services
![services](images/services.png)

### Creating Ingress
![create-ingress](images/creating-ingress.png)

### Successful Ingress
![successful-ingress](images/successful-ingress.png)

### Proof of success
![proof of success](images/proof-of-success.png)


### Issues faced:

I first uploaded the entire spring-gumball as a folder into the repo and the gradle.yaml would get created alongside the folder. This caused several build errors. Finally, I decided to upload all the contents of the folder into the repo and them create a workflow and that worked successfully. 

Another error that I faced was trying to figure out what kind of access to give to the service account to my project in the "Grant this service account access to project (optional)" section. I tried the "Owner" role and that seemed to give the service account sufficient access to my project to get things done ahead.

