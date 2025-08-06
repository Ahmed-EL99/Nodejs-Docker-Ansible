# Node.js Deployment with Docker & Ansible 🚀

This repository showcases automated deployment of a basic Node.js application using **Docker** and **Ansible**.

---

## 🔧 Tech Stack

- **Node.js** (using `node:18-alpine` Docker base image)  
- **Docker** for containerization  
- **Ansible** for provisioning and automation  
- **Linux** target host (e.g., Ubuntu or local VM)

---

## 📂 Project Structure

├── ansible/
│ ├── nodejsdeploy.yml
│ └── hosts # Inventory file (not using .ini)
└── Dockerfile # Builds the Node.js container image
├── app/
| ├── package.json
| └── index.js # Simple dummy app entry point


---

## 🚀 What the Project Does

- Ansible connects to your target host (or `localhost`)
- Builds the Node.js Docker image defined in `Dockerfile`
- Runs the container on the host, exposing the app port
- Application is accessible via browser at `http://localhost:8080`

---

## 🧾 How to Run

1. Clone this repository
2. Edit `ansible/hosts` to include your target host (or leave as `localhost`)
3. Edit `ansible/nodejsdeploy` to include correct source and destinations for your nodejs app
4. Run:
   ```bash
   ansible-playbook -i ansible/hosts ansible/nodejsdeploy.yml

<img width="977" height="445" alt="nodejs output" src="https://github.com/user-attachments/assets/7fcf2228-453b-43c1-bfc1-778b8caebeec" />


Visit http://<host-IP-or-localhost>:8080 (or your configured port) to see your Node app running

<img width="947" height="116" alt="nodejs webpage" src="https://github.com/user-attachments/assets/ce70a8cc-55f0-4d76-8cac-269e5138f982" />
