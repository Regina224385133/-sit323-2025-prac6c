### Step 1: Pull up item 6.1

### Step 2: Deploying to a Kubernetes Cluster
   ```
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
   ```

### Step 3: Using Minikube
Start Minikube
```
minikube start
```
```
kubectl cluster-info
```

### Step 4:  Check that Pods and Services are running properly
```
kubectl get pods
kubectl get services
```
At this point, you can see that the Pod status is Running, and the CLUSTER-IP and port of the service are normal.
### Step 5: Port forwarding and access to the application in the browser
Use port forwarding to locally access the service:
```
kubectl port-forward service/nodejs-service 8080:3000
```
Then access it in your browser:
```
http://localhost:8080/
```
### Step 6: Submit Code and Dockerfile

1. **Push code to GitHub**:
   initialize a Git repository in project folder:
     ```bash
     git init
     git add .
     git commit -m "Initial commit"
     ```

2. **Create a GitHub repository**:
   - Go to GitHub and create a new repository called `sit323-2025-prac6c`.

3. **Push code to GitHub**:
   - Add the remote repository and push code:
     ```bash
     git remote add origin https://github.com/username/sit323-2025-prac6c.git
     git push -u origin main
     ```

