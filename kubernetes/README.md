# Deploy n8n on Kubernetes

## Requirements

 - [K8s cluster](https://kubernetes.io/docs/tasks/tools/)

## Deploy manifest to Kubernetes server

Download manifest:
````
git clone https://github.com/davma-io-templates/n8n-template.git
cd n8n-template/kubernetes
````

Run the following command: 
````
kubectl apply -f n8n.yaml
````

Check that it worked by running the following: 
````
kubectl port-forward service/n8n-instance 5678:5678 -n default
````
Navigate to localhost:5678 in your browser. You should see a n8n login page.

Use admin for both the username and password to login.