# 🏠 My HomeLab Setup

A centralized, Docker-based infrastructure for managing my NAS, services, and monitoring.

## 🛠 The Stack

| Service | Purpose | Port |
| :--- | :--- | :--- |
| **Homepage** | Main Dashboard | `3000` |
| **FileBrowser** | Web-based NAS Manager | `8080` |
| **Uptime Kuma** | Service Monitoring | `3001` |
| **Nginx** | Reverse Proxy | `80` |

## 🚀 Getting Started

1. **Clone the Repo**
   ```bash
   git clone [https://github.com/kimzam30/my-homelab-setup.git](https://github.com/kimzam30/my-homelab-setup.git)
   cd my-homelab-setup

    Configure Environment Duplicate the example file and fill in your secrets:
    Bash

cp .env.example .env

Edit .env with your PUID, PGID, and NAS_ROOT path.

Deploy
Bash

    docker-compose up -d

📂 Configuration

    Homepage: configs located in config/homepage/

    Nginx: rules located in config/nginx/nginx.conf

    FileBrowser: settings in config/filebrowser/

🔒 Security

This repository uses "dummy" config files. Sensitive data (databases, .env files) are gitignored.


---

### 6. How to Push This (The Renaming)

Since you are changing the identity of the repo, I recommend renaming it on GitHub first, then pushing this fresh code.

1.  **Go to GitHub:** Settings > General > Rename repository to `my-homelab-setup`.
2.  **On your PC (in the new folder you just made):**
    ```bash
    git init
    git add .
    git commit -m "Initial commit: Rebuild homelab setup from scratch"
    
    # Link it to your renamed repo
    git remote add origin https://github.com/kimzam30/my-homelab-setup.git
    
    # Force push to overwrite the old docker-setup history
    git push -u origin master --force
    ```

This gives you a clean slate, professional structure, and zero security risks. Ready to execute?