🚀 DevOps Internship Assignment – Docker + NGINX Reverse Proxy
This project demonstrates a Docker Compose setup involving two backend services — a Golang API and a Python Flask API — with an NGINX reverse proxy handling routing based on URL paths.

📦 Services Overview
URL Path	Service	Internal Port
/service1/hello	Golang Service	8001
/service2/hello	Python Flask	8002

✅ All traffic is exposed via the NGINX container at:
http://localhost:8080

📁 Folder Structure
css
Copy
Edit
Assignment/
├── docker-compose.yml
├── nginx/
│   ├── nginx.conf
│   └── Dockerfile
├── service_1/
│   ├── main.go
│   └── Dockerfile
├── service_2/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
🐳 Tech Stack
Docker & Docker Compose

Golang for Service 1

Python Flask for Service 2

NGINX as a reverse proxy

▶️ How to Run
In the root folder, run:

bash
Copy
Edit
docker-compose up --build
This will:

Build both services (service_1 and service_2)

Build the NGINX reverse proxy image

Route requests through NGINX at localhost:8080

🌐 Routing Features (NGINX)
/service1 → routed to the Go backend

/service2 → routed to the Python Flask backend

Uses bridge networking (not host mode)

Logs all incoming requests with timestamp and path

🧪 Test Endpoints
You can test the services using browser or curl:

http://localhost:8080/service1/hello

http://localhost:8080/service2/hello

📸 Screenshots

✅ Golang service running in Docker
![Screenshot (124)](https://github.com/user-attachments/assets/254bd1f3-7d27-407b-93e2-7d8c8d91dd78)

✅ Python Flask service running in Docker
![Screenshot (125)](https://github.com/user-attachments/assets/b0bff0da-f123-48b3-a370-00e3ae33b5c3)

✅ Docker Compose booting all services
![Screenshot (121)](https://github.com/user-attachments/assets/f3577405-d38b-4029-a16d-f191431606f2)
![Screenshot (122)](https://github.com/user-attachments/assets/736e46ce-2461-4e9b-9369-bdc67f36ec1d)

✅ Testing routing through localhost:8080 service_1
![Screenshot (119)](https://github.com/user-attachments/assets/a4da3d99-7cda-46d8-af1b-b1fe2f79840b)

✅ Testing routing through localhost:8080 service_2
![Screenshot (120)](https://github.com/user-attachments/assets/feac5c6a-c21f-4146-bbf5-68861ad91bf3)
