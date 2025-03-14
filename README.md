# Server Baseline

**Server Baseline** is a NGINX + Django REST Framework (DRF) boilerplate designed to help you quickly set up and start a new Server project.
  
It provides a structured environment with separate configurations for **development** and **deployment**, ensuring a smooth transition from local testing to production.

It includes pre-configured nginx.conf, Dockerfile and docker-compose.yml.

## 📌 How to Use

1. clone current project.
2. look README.md from drf_baseline for drf initialization
3. For HTTP
- In 'nginx/nginx.conf' and edit 'domain.yourdomain.com' to your down domain.
- docker compose up

3. For HTTP & HTTPS
- In 'nginx/nginx.conf' and remove '# HTTP' and unhash '# HTTPS'.
- In 'nginx/nginx.conf' and edit 'domain.yourdomain.com' to your down domain.
- In 'nginx/Dockerfile' unhash '# EXPOSE 443'
- In 'docker-compose.yml' unhash '# 443:443'  and '# /etc/letsencrypt:/etc/letsencrypt'
- Install letsencrypt on server computer and get SSL certificates.
- Following files could be missing in your server computer. Search web and download '/etc/letsencrypt/options-ssl-nginx.conf' 'ssl_dhparam /etc/letsencrypt/'ssl-dhparams.pem;
- docker compose up


## 📌 Server Baseline Structure

.

├── nginx
│   ├── Dockerfile
│   └── nginx.conf
├── server (drf_baseline)
│   ├── server
│   ├── .env
│   ├── README.md
│   ├── Dockerfile
│   └── manage.py
├── README.md
└── docker-compose.yml