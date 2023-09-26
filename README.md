# multi-container-deployment-k8s

The aim of this project is to build and deploy a simple (not production ready), multi-tier web application using Kubernetes and Docker. This example consists of the following components:

A single-instance Redis to store guestbook entries
Multiple web frontend instances

## Running the app (Local Deployment)
If you would be running the application locally, you can install minikube [here](https://minikube.sigs.k8s.io/docs/start/)



After the installation and configuration of minikube. Run **minkube status** to confirm. You should get a response like this

![Minikube running](/pictures/minikube.png)

Afterwards, you can apply all the files

    $ kubectl apply -f ./config

Start the app using port forwarding

    kubectl port-forward svc/frontend 8080:80

You can check that your application is running at http://localhost:8080. 

You should get a response like this

![Application running](/pictures/k8s%208.png)