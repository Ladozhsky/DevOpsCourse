# Quick Start: Notes App on GCP VM

Follow these steps in your GCP VM SSH terminal.

---

1. **SSH into your VM**  
   ```bash
   gcloud compute ssh <VM_NAME> --zone=<ZONE>

2. **Create project folder**

bash
mkdir -p ~/notes-app
cd ~/notes-app

3. **Add docker-compose.yml**

Create ~/notes-app/docker-compose.yml with:

version: '3.8'
services:
  backend:
    image: ladozhsky/notes-backend:latest
    volumes:
      - ./notes.json:/app/notes.json
    expose:
      - "5000"
    restart: unless-stopped

  frontend:
    image: ladozhsky/notes-frontend:latest
    ports:
      - "80:80"
    depends_on:
      - backend
    restart: unless-stopped

4. **Add notes.json**
Create ~/notes-app/notes.json

5. **docker login**

6. **Pull images & start containers**

docker-compose pull
docker-compose up -d