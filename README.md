![Project diagram](https://github.com/sugalvojau/js-docker-multi-container-application/blob/master/README-diagram.png)  

![Project example](https://github.com/sugalvojau/js-docker-multi-container-application/blob/master/README-example.png)  


# Wake up the application with docker-compose  
`docker-compose down && docker-compose up --build`  
http://localhost:3050/  


# Various container-specific alternatives to docker-compose

Test worker:

`cd worker/`  
`node index.js`  

`docker build -f Dockerfile.dev .`  
`docker run 71088f27a8f5` (take worker's container id)    


Test server:  

`cd server/`  
`node index.js`  

`docker build -f Dockerfile.dev .`  
`docker run 71088f27a8f6` (take server's container id)    

Build client:  
  
`docker build -f Dockerfile.dev .`  
`docker run 71088f27a8f7` (take client's container id)    
