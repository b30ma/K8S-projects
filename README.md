
# How to deploy an application on Kubernetes using Deployments and Services.

Scenario: Deploying a Web Application on Kubernetes

Step 1: Prepare the Application
Assume you have a simple web application, such as a frontend web server, that you want to deploy on Kubernetes. 
Prepare the necessary container image for your web application and push it to a container registry like Docker Hub or Amazon ECR.

Step 2: Create a Deployment
A Kubernetes Deployment is responsible for managing the desired state of your application's replicas. Create a YAML file, 
let's call it webapp-deployment.yaml, to define the Deployment.


Apply the Deployment to your Kubernetes cluster:

$ kubectl apply -f webapp-deployment.yaml

Step 3: Create a Service
A Kubernetes Service provides a stable IP and DNS name to access your application. Create another YAML file, 
let's call it webapp-service.yaml, to define the Service.

Apply the Service to your Kubernetes cluster:

$ kubectl apply -f webapp-service.yaml

Step 4: Verify the Deployment
Check if the Deployment and Service are running correctly:

$ kubectl get deployments
$ kubectl get pods
$ kubectl get services

Step 5: Access the Web Application
If you used type: LoadBalancer in the Service definition, Kubernetes should automatically 
provision a load balancer (in cloud environments) and assign an external IP to access your web application

$ kubectl get services

