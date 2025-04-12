# System Requirements & Setup

The microservice runs on Node.js and requires npm to install dependencies. It uses Express.js for backend routing and basic HTML/JavaScript for the frontend interface. To use the service, simply start the Node.js server, access the HTML page in a browser, and perform calculations. The system is lightweight and can be deployed on any server.

1) Download Node.js (LTS version) from https://nodejs.org/ and install it.

2) Open a terminal and navigate to your preferred directory.

3) Initialize a Node.js project through terminal:
   ```sh
   npm init -y
   ```

4) Enable Kubernetes in docker desktop
5) Create docker image (it is already created in previous task so using the same)
6) create two yaml file i.e. deployment.yaml and service.yaml
7) Run these commmands
   kubectl apply -f deployment.yaml  #Creates your app pods
   kubectl apply -f service.yaml    #Makes your app reachable
8) Check the services running in kuber cluster
   kubectl get service web-app-service
9) Run the project
    kubectl port-forward pod/web-app-deployment-7f78585f69-9thvn 8080:3000

