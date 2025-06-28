# Server Baseline

**Server Baseline** is a boilerplate project combining NGINX and Django REST Framework (DRF), designed to help you quickly set up a new server project.  
It provides a structured environment with separate configurations for **development** and **deployment**, ensuring a smooth transition from local testing to production.

This project includes pre-configured `nginx.conf`, `Dockerfile`, and `docker-compose.yml` files.

---

## 📦 Features

- 🐳 Docker-Compose included
- 📧 Optional Celery + Redis integration for background tasks

---

## 📌 Getting Started

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

---

## 🗂 Project Structure

```text
├── nginx
│   ├── Dockerfile
│   └── nginx.conf
├── server (drf_baseline)
├── README.md
└── docker-compose.yml
```