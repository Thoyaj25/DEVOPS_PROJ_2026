# DevOps Real-Time WebSocket Chat Application

## Project Overview

This is a production-style DevOps project that demonstrates deployment of a real-time WebSocket chat application using Docker, Nginx, and CI/CD on AWS EC2.

The system enables multiple users to communicate in real time using Socket.IO over WebSockets.

---

## Architecture
User Browser
↓
Nginx (Reverse Proxy - Port 80)
↓
Node.js + Express + Socket.IO (Port 3000)
↓
Real-Time WebSocket Communication

---

## Tech Stack

- Node.js
- Express.js
- Socket.IO
- Nginx
- Docker
- Docker Compose
- AWS EC2 (Deployment)

---

## How to Run the Project

```bash
git clone https://github.com/<your-username>/DEVOPS_PROJ_2026.git
cd DEVOPS_PROJ_2026
docker compose up -d --build
## Access Application
http://54.82.0.109
WebSocket Flow
Client connects via Socket.IO
Nginx forwards request to backend
Backend broadcasts messages to all connected clients
Real-time updates across multiple browser tabs
Docker Setup
Start containers
docker compose up -d --build
Stop containers
docker compose down -v
Architecture Diagram (Visual)
                 ┌────────────────────┐
                 │   User Browser     │
                 └─────────┬──────────┘
                           │
                           ▼
                 ┌────────────────────┐
                 │ Nginx (Port 80)    │
                 │ Reverse Proxy      │
                 └─────────┬──────────┘
                           │
        ┌──────────────────┴──────────────────┐
        ▼                                     ▼
HTTP Requests                        WebSocket Upgrade
        │                                     │
        └──────────────┬──────────────────────┘
                       ▼
        ┌──────────────────────────────────┐
        │ Node.js + Express + Socket.IO    │
        │ (Port 3000 inside Docker)        │
        └──────────────┬───────────────────┘
                       ▼
            Real-Time Chat System
1. Open application
http://54.82.0.109
Open 2 browser tabs
3. Send message
✔ Message should appear in both tabs instantly
Deployment Commands
docker compose down -v
docker compose up -d --build
Run:
```bash
git add README.md
git commit -m "Final submission ready README"
git push origin main
