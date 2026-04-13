# DevOps WebSocket Chat Application

## Overview
Real-time chat application built using Node.js, Socket.IO, Docker, and Nginx reverse proxy.  
Deployed on AWS EC2 with full containerized architecture.

---

## Architecture

User Browser  
→ Nginx (Port 80)  
→ Node.js App (Port 3000)  
→ Socket.IO WebSocket Connection  

---

## Tech Stack
- Node.js
- Express
- Socket.IO
- Nginx
- Docker
- Docker Compose
- AWS EC2

---

## How to Run

```bash
docker compose up -d --build
Then open:
http://54.82.0.109
