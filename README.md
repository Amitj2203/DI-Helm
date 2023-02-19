# DI-Helm
Solution set using Helm

# DI-Helm
Recruitment Case Solution Using HelmChart

This repository contains the files for Recruitment case solution, it deploys Very simple python flask application as a http endpoint. This application is containerized using Docker and deployed on a minikube cluster and exposed to Internet using Helm.

# Assumptions
- Docker is installed on the machine where this code will be executed.
- Minikube is installed where this code will be executed.

# Prerequisites
- kubectl installed
- helm installed

# Clone the repository
git clone https://github.com/Amitj2203/DI-Helm.git

# Execute the script(install.sh)
./install.sh

Above script will perform the below actions

- Create a docker image with base python alpine image and containerized the python flask application.
- Make image available to minikube cluster so that it can be pulled locally.
- Helm will deploy a release containing the Pod and LoadBalancer service to expose the http endpoint using the Helm Chart supplied in chart folder.
- Expose the above pod with a service of type NodePort.
- Allow port forwarding to allow incoming traffic.  
