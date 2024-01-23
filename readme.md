# Nginx application Deployment through helm chart

Steps for deploying the nginx application in Minikube/local cluster.

- Start the minikube cluster or local cluster.
- create namespace in the cluster "kubectl create ns nginx"
- Clone the repository https://github.com/vijkr/Nginxapp.git
- Navigate to the charts/nginxapp directory.
- Run the following command to install Nginx "**helm install nginx . -f .\values.yaml -n nginx**"
- Once deployed, run "**kubectl get all -n nginx**" to confirm that all resources have been deployed.
- Use "**kubectl -n nginx port-forward svc/nginx-service 80:80**" to initiate a port-forward in order to access the application
- Finally, check your browser for the webpage, **127.0.0.1:80**.