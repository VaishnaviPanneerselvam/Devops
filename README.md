This repository contains a simple Flask application, contains  Docker and deployed on Kubernetes using Minikube.
Run the Docker Container Locally:
          docker run -p 5000:5000 flask-app
Set Up Minikube:
          minikube start
Use Minikube's Docker Daemon:
          & minikube -p minikube docker-env --shell powershell | Invoke-Expression
Load the Docker Image into Minikube:
         minikube image load flask-app:latest
Deploy to Kubernetes:
         kubectl apply -f deployment.yaml
         kubectl apply -f service.yaml
Access the Flask App:
         minikube service flask-app --url

