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

nano docker-compose.yml

<img width="287" height="272" alt="image" src="https://github.com/user-attachments/assets/cca693bd-52e1-489d-a0d8-e308d29c4fd9" />


4. **Add notes.json**
Create ~/notes-app/notes.json

5. **docker login**

6. **Pull images & start containers**

docker-compose pull
docker-compose up -d


Screenshots:
docker compose ps
<img width="913" height="47" alt="image" src="https://github.com/user-attachments/assets/9da90fc8-9581-4af5-923b-29b202a9b3e2" />

Running app in GCP:

<img width="407" height="106" alt="image" src="https://github.com/user-attachments/assets/01059049-7064-46d2-b844-fc2769236dfd" />

<img width="380" height="177" alt="image" src="https://github.com/user-attachments/assets/2ffdfa9d-7438-439b-af3d-f71ca068952a" />

