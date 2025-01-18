# AKS-Wordpress

For secret use: <br>
echo -n 'your-password' | base64

Apply the Kubernetes Configurations <br>
Run the following commands to apply the configurations to your AKS cluster: <br>

kubectl apply -f mysql-secret.yaml <br>
kubectl apply -f mysql-deployment.yaml <br>
kubectl apply -f wordpress-pvc.yaml <br>
kubectl apply -f wordpress-deployment.yaml <br>
kubectl apply -f wordpress-service.yaml <br>

Access WordPress  <br>
Once the service is created, use the external IP assigned to the WordPress service to access it. To find the external IP, run:  <br>

kubectl get svc wordpress-service


