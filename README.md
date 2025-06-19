🐳 Docker Cheat Sheet
📌 Docker Basics
What is Docker?
Image → A package containing dependencies and instructions to create a container.
Container → A running instance of an image (the execution result of an image).

🚀 Creating an Image & Container
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
docker run node        # Run Node.js container
3️⃣ Build a Custom Image (For VS Code)
sh
Copy
Edit
docker build -t mynodeimage .
4️⃣ Create a Named Container
sh
Copy
Edit
docker run -p 3002:3000 -t --name mynodecontainer mynodeimage
⚙️ Managing Containers
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
What is Docker Compose?
Docker Compose is a tool for defining and running multi-container Docker applications.

Basic Commands
sh
Copy
Edit
docker compose up    # Start services
docker compose down  # Stop and remove services
Key Concepts in Docker Compose
✅ Multiple Images → Define multiple services in docker-compose.yml.
✅ Port Mapping → Expose ports for external access.
✅ Environment Variables → Pass necessary configurations.

🌐 Docker Networking
Docker provides different networking modes to allow containers to communicate.

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
Docker volumes are used to store persistent data that remains even after containers are removed.

Creating & Using a Volume
sh
Copy
Edit
docker volume create myvolume
docker run -v myvolume:/app/data myimage
🎯 Conclusion
This cheat sheet covers the essential Docker commands, including images, containers, Compose, networking, and volumes. 🚀 Keep experimenting and mastering Docker!
