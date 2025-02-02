1. docker build -t docker_username/chatapp-backend:latest .
2. docker push docker_username/chatapp-backend:latest
3. docker build -t docker_username/chatapp-frontend:latest .
4. docker push docker_username/chatapp-frontend:latest
5. Now create a namespace chat-app and create it. 
6. Now create Deployment for backend
7. create a service for backend as well as for frontend
7. kubectl apply -f mongodb-pv.yml
8. kubectl apply -f mongodb-pvc.yml
9. kubectl apply -f mongodb-deployment.yml


After running all of this 

