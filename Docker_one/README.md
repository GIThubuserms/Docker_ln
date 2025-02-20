🐳 Docker Cheat Sheet
Docker Basics
Image → A dependency package with commands to run a container.
Container → A running instance of an image (the result of executing an image).
📌 Creating an Image & Container
1️⃣ Pull an Image
sh
Copy
Edit
docker pull ubuntu
docker pull node
2️⃣ Create & Run a Container
sh
Copy
Edit
docker run -it ubuntu  # Run Ubuntu container interactively
docker run node         # Run Node.js container
3️⃣ Build a Custom Image (For VS Code)
sh
Copy
Edit
docker build -t mynodeimage .
4️⃣ Create a Named Container
sh
Copy
Edit
docker run -p 3002:3000 -t --name mynodeimage mynodeimage
🚀 Managing Containers
Run an Existing Container
sh
Copy
Edit
docker start mycon
Stop a Running Container
sh
Copy
Edit
docker stop mycon
List Images & Containers
sh
Copy
Edit
docker images  # List all available images
docker ps      # List running containers
docker ps -a   # List all containers (including stopped ones)
🏗️ Docker Compose
Docker Compose allows running multiple containers together with networking, ports, and environment variables.

Basic Commands
sh
Copy
Edit
docker compose up    # Start services
docker compose down  # Stop and remove services
Key Concepts in Docker Compose
Multiple Images → Define services in docker-compose.yml.
Port Mapping → Expose ports for communication.
Environment Variables → Pass necessary variables to services.
🌐 Docker Networking
Docker provides different networking modes for container communication.

1️⃣ Host Network
Uses the same IP and port as the host machine.
No need for port mapping.
Example:
sh
Copy
Edit
docker network create --driver host mynetwork
2️⃣ Bridge Network (Default)
Containers get an isolated network but can communicate via port mapping.
Example:
sh
Copy
Edit
docker network create --driver bridge mynetwork
📦 Docker Volume
Docker volumes store persistent data even after containers are removed.

Creating & Using a Volume
sh
Copy
Edit
docker volume create myvolume
docker run -v myvolume:/app/data myimage
🎯 Conclusion
This cheat sheet covers the essentials of Docker, including images, containers, Compose, networking, and volumes. 🚀 Keep experimenting and mastering Docker!