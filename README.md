# CMPE 172 - Lab #10 Notes by Siya Bedi

## CI Workflow (Part 1)

Navigated to "Actions" and created a new workflow:
![CI-1](images/CI-Workflow-2.png)

I made a commit to the docker-compose.yaml to trigger the action
![CI-2](images/CI-Workflow-1.png)

## CD Workflow (Part 2)

1. Create a new "Build and Deploy to GKE" workflow:
![pre create CD, home page of new workflow](images/github-preCreateCD.png)

2. Setup GKE by creating an IAM & Admin Service Account with Owner permissions:
![create IAM & Admin Service Account (SA)](images/gke-createSA.png)

3. Create a JSON Service Account Key. Then for macOS view the key using a base64 encoding:
![Create JSON SA Key](images/gke-createSAKey.png)
![Contents of key](images/gke-keyInfo.png)
![base 64 encoding](images/github-SAKEYBase64.png)

4. Set the Project ID as GKE_PROJECT and base64 encoded key as GKE_SA_KEY:
![show secrets](images/github-showSecrets.png)

5. Create a GKE Cluster:
![create cluster](images/gke-createCluster.png)

6. Trigger a CD by creating a release: 
![create release](images/github-createRelease.png)
![trigger home](images/github-releaseTrigger.png)
![trigger overview](images/github-releaseTriggerOverview.png)
![trigger start](images/github-releaseTriggerStart.png)
![trigger end](images/github-releaseTriggerEnd.png)

7. Verify the CD was successful by checking GKE Workload and Service:
![gke workload](images/gke-workload.png)
![gke service](images/gke-service.png)

8. Create a Load Balancer Ingress:
![gke create ingress](images/gke-createIngress.png)
![gke ingress created](images/gke-ingressCreated.png)

9. Check that the app works:
![check app works](images/gke-proofOfSuccess.png)
