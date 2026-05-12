# Fullstack Dockerized Architecture

This repository contains Docker configurations to simulate a fullstack environment consisting of:

- Frontend (Next.js)
- Backend (Express.js)
- Database (PostgreSQL)
- Nginx (Reverse Proxy)

---

/tourid-next-project → Frontend repository (Next.js)
/tourid-express-typesript → Backend repository (Express.js)
/tourid-docker-config → Docker configurations

---

## Docker Configurations

The `tourid-docker-config` folder contains:

- `docker-compose-development.yml` → local development simulation  
- `docker-compose-staging.yml` → staging environment simulation  
- `docker-compose-nginx.yml` → reverse proxy (Nginx) simulation  

Each compose file defines services for:
- frontend
- backend
- database (PostgreSQL)
- nginx (optional depending on environment)

---

## Source Repositories

- Frontend: [https://github.com/januardlg/tourid-next-FE/tree/docker-main-containerized]
- Backend: [https://github.com/januardlg/tourid-express-typescript/tree/docker-main-containerized]

---

## How to Run

### Development
```bash
docker compose -f docker-compose-development.yml up --build
```

### Staging
```bash
docker compose -f docker-compose-staging.yml up --build
```

### Nginx
```bash
docker compose -f docker-compose-nginx.yml up --build
```

##  Note
- Services communicate using Docker network (service name resolution)
- Nginx acts as a reverse proxy entry point
- This setup simulates a production-like architecture locally


## References
- Docker Documentation: https://docs.docker.com/
- Docker Compose: https://docs.docker.com/compose/
- Nginx Reverse Proxy: https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/

## Purpose
#### This setup is built for learning and simulating:
- containerized fullstack architecture
- service isolation
- reverse proxy routing
- production-like deployment flow