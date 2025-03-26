1. Go to your backend path then create the image and push to dockerhub
    docker build -t docker_username/chatapp-backend:latest .
    docker push docker_username/chatapp-backend:latest
   
2. Go to your frontend path then create the image and push to DockerHub
    docker build -t docker_username/chatapp-frontend:latest .
    docker push docker_username/chatapp-frontend:latest
   
3. Now create a folder with name "k8s" where we store out kubernetes files.
   Now create a namespace 'chat-app' and create it.
4. Now create a backend-deployment with backend image.
5. Also create a frontend-deployment with frontend-images.
6. Also create mongodb-deployment with public mongo:latest images
7. Now you can create PersistentVolume, PersistentVolumeClaim
8. Now run this commadn kubectl apply -f mongodb-pv.yml
9. Now clain for volume using kubectl apply -f mongodb-pvc.yml
10. Now run mongo-deployment kubectl apply -f mongodb-deployment.yml
11. Now run backend depoloyment using kubectl apply -f backend-deployment.yml
12. Now create a frontend-service.yml and backend-service.yml file
13. Create also service for mongodb using mongodb-service.yml.
14. same way run kubectl apply -f frontend-service/backend-service.yml
15. Now run frontent deployment using kubectl apply -f frontend-deployment.yml
16. Now your service, deployment and all are running.
17. Now forword you port using kubectl port-forword service/backend(service name) -n  chat-app 5001:5001 &
18. Now forword you port using kubectl port-forword service/frontend(service name) -n  chat-app 80:80 &


After running all of this CONGRATULATION !

