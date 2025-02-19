DOCKER 

Images --> A dependency and commands or instructians to run container

Container --> A running instance of a image  // The result of a image

How to create a image and conatainer using cmd ?

docker run -it ubuntu 

How to create a image ?

docker pull node
docker run node 

docker run node 

docker build -t mynodeimage .  // For Vs code


How to create a container ?

docker run -p 3002:3000 -t --name mynodeimage 


How to run a container?
docker start mycon
docker stop mycon

How to list images and container?

docker images
docker ps 
