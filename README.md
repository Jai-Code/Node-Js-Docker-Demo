# Docker Node MySQL Example

> Simple example of a dockerized Node/MySQL app

## Quick Start

```bash
# Build Mysql Image
docker build -t custom/mysql -f Dockerfile_mysql .

# Run Mysql in background
docker run -d --name mysql custom/mysql

# Build Nodejs Image
docker build -t custom/nodejs -f Dockerfile_nodejs .

# Run Nodejs in background
docker run -d --name nodejs --link mysql:mysql-db -p 3000:3000 custom/nodejs
# --link mysql:mysql-db (use mysql container in nodejs as the name of mysql-db)



