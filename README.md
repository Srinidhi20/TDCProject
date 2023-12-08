# Financial Fraud Detection using Kubernetes

### Tools

**1. Turn on hyperv**  
                Open "Control Panel", Go to "Programs" and then "Turn Windows features on or off"  
                Find and check "Hyper-V", Restart your computer.

**2. Docker Desktop**  
                Download and install Docker Desktop from the official Docker website.

**3. kubernetes**  
                Install Kubernetes on Docker Desktop by enabling the feature in Docker Desktop settings.

**4. Minikube**  
                Install Minikube by downloading the installer from the official Minikube website and following the installation instructions.

**5. kubectl**   
                Install kubectl, the Kubernetes command-line tool, by downloading and adding it to your system's PATH.



### Deployment steps

1. Build Docker Image  
                  `docker build -t cc-fraud:0.1 .`
2. Start minikube   
                  `minikube start`
3. Create Kubernetes deployment  
                  `kubectl create --filename deployment.yaml`
4. Create Kubernetes deployment  
                  `kubectl create --filename service.yaml`
5. Load local Docker image on Minikube cluster  
                  `minikube image load cc-fraud:0.1`
7. Check pods status  
                  `kubectl get pods`
8. Create a network tunnel between the host machine and the Minikube cluster   
                  `minikube tunnel`
9. Retrieve the external IP address of your services  
                  `kubectl get services`
10. Send requests to application from external sources accessing the cluster.  
                  use `<external-ip>:<port>`

CreditCard Fraud detection dataset used from :  [kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).

