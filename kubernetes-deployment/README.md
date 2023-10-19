# currency-service
This is Microservice-Demo project.

This service comprised of following microservices - 
1. currency-exchange : https://github.com/AnoopRahulChaudhary/currency-exchange-service/tree/kubernetes
2. currency-conversion : https://github.com/AnoopRahulChaudhary/currency-conversion-service/tree/kubernetes

Start the service in local system :
- Required software - git, docker, minikube, kubectl
- Make sure that you have installed the required software and then run the following commands.
1. Command to clone the project - `git clone https://github.com/AnoopRahulChaudhary/currency-service.git`
2. Command to Go inside the `currency-service/kubernetes-deployment` directory - `cd currency-service/kubernetes-deployment`
3. Commands to start installation of the service - 
    - `kubectl apply -f currency-exchange/deployment.yaml`
    - `kubectl apply -f currency-conversion/deployment.yaml`

