# DevOps Real-Time WebSocket Chat Application

## Project Overview

This is a production-style DevOps project that demonstrates deployment of a real-time WebSocket chat application using Docker, Nginx, and CI/CD on AWS EC2.

The system enables multiple users to communicate in real time using Socket.IO over WebSockets.

---

## Tech Stack

- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **Socket.IO** - Real-time communication library
- **Nginx** - Reverse proxy & load balancer
- **Docker** - Containerization
- **Docker Compose** - Container orchestration
- **AWS EC2** - Cloud deployment

---

## Architecture

For detailed architecture diagram, see [arch.diagram](./arch.diagram)

**Communication Flow:**
- User Browser → Nginx (Reverse Proxy, Port 80) → Node.js + Express + Socket.IO (Port 3000) → Real-Time WebSocket Communication

---

## WebSocket Flow

1. Client connects via Socket.IO
2. Nginx forwards HTTP/WebSocket upgrade requests to backend
3. Backend broadcasts messages to all connected clients
4. Real-time updates across multiple browser tabs instantly

---

## Project Structure

```
DEVOPS_PROJ_2026/
├── Dockerfile              # Docker image configuration
├── docker-compose.yml       # Multi-container setup
├── server.js               # Node.js application
├── package.json            # Dependencies
├── README.md               # This file
├── arch.diagram            # Architecture diagram
└── nginx/
    └── default.conf        # Nginx configuration
```

---

## Setup & Deployment

### Prerequisites
- Docker & Docker Compose installed
- Git configured

### Local Development

```bash
# Clone repository
git clone https://github.com/<your-username>/DEVOPS_PROJ_2026.git
cd DEVOPS_PROJ_2026

# Start containers
docker compose up -d --build

# Access application
http://localhost
```

### Stop Containers

```bash
docker compose down -v
```

### AWS EC2 Deployment

```bash
# Deploy to EC2
docker compose up -d --build

# Access deployed application
http://54.82.0.109
```

---

## Testing the Application

1. Open application in browser: `http://localhost` (local) or `http://54.82.0.109` (deployed)
2. Open 2 browser tabs simultaneously
3. Send a message from one tab
4. ✅ Message should appear in both tabs instantly

---

## Deployment Commands

```bash
# Build and start
docker compose up -d --build

# View logs
docker compose logs -f

# Stop and clean up
docker compose down -v

# Commit changes
git add .
git commit -m "DevOps project submission"
git push origin main
```

---

## Key Features

- ✅ Real-time bidirectional communication
- ✅ Containerized architecture
- ✅ Reverse proxy configuration
- ✅ Production-ready deployment
- ✅ Multi-user support

---

## Author

DevOps Project 2026 - Submission Ready
