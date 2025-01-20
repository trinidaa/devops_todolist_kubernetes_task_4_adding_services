## Deployment Steps

### Create a infrastructure:
   ```bash
   kubectl apply -k .\.infrastructure\
   ```
### how to access an app using a NodePort Service:
```bash
http://localhost:31111/
   ```
###  app using ports-forwarding:
```bash
kubectl port-forward todoapp-pod 8081:8080 -n todoapp
   ```
   You should look echo on your localhost. Open browser and enter  **Http://localhost:8081/**

### How to test the application using the:
```bash
kubectl exec -it busybox-pod -n todoapp -- curl http://todoapp:8000/api/readiness/
```
```bash
kubectl exec -it busybox-pod -n todoapp -- curl http://todoapp:8000/api/liveness/
```