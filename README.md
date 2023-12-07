#Tools to install 

1. Turn on hyperv 
        Open the "Control Panel.", Go to "Programs" and then "Turn Windows features on or off."
        Find and check "Hyper-V.", Restart your computer.

2. Install Docker Desktop:
        Download and install Docker Desktop from the official Docker website.

3. Install kubernetes
        Install Kubernetes on Docker Desktop by enabling the feature in Docker Desktop settings.

4. Install Minikube:
        Install Minikube by downloading the installer from the official Minikube website and following the installation instructions.

5. Install kubectl  
        Install kubectl, the Kubernetes command-line tool, by downloading and adding it to your system's PATH.



#Deployment steps

1. Build Docker Image
          docker build -t cc-fraud:0.1 .
2. Start minikube 
          minikube start
3. Create Kubernetes deployment
          kubectl create --filename deployment.yaml
4. Create Kubernetes deployment
          kubectl create --filename service.yaml
5. Load local Docker image on Minikube cluster
          minikube image load cc-fraud:0.1
6. Check pods status
          kubectl get pods
7. Create a network tunnel between the host machine and the Minikube cluster 
          minikube tunnel
8. Retrieve the external IP address of your services
          kubectl get services
9. Send requests to application from external sources accessing the cluster.
          use <external-ip>:<port>






         #   f r a u d _ d e t e c t i o n _ d e p l o y m e n t _ u s i n g _ K u b e r n e t e s 
 
 
