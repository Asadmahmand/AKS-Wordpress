# AKS-Wordpress

For secret use:
echo -n 'your-password' | base64

Apply the Kubernetes Configurations
Run the following commands to apply the configurations to your AKS cluster:
bash
CopyEdit
kubectl apply -f mysql-secret.yaml
kubectl apply -f mysql-deployment.yaml
kubectl apply -f wordpress-pvc.yaml
kubectl apply -f wordpress-deployment.yaml
kubectl apply -f wordpress-service.yaml

Access WordPress
Once the service is created, use the external IP assigned to the WordPress service to access it. To find the external IP, run:

bash
Copy
Edit
kubectl get svc wordpress-service


