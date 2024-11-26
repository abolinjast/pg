# Docker PostgreSQL & pgAdmin Setup

This is a simple setup for running PostgreSQL and pgAdmin using Docker Compose. It allows you to manage your PostgreSQL database through a web interface provided by pgAdmin.

## Requirements

- Docker
- Docker Compose

## Services

1. **PostgreSQL**  
   A PostgreSQL database running in a container. It is configured with the following:
   - **Username:** `admin`
   - **Password:** `root`
   - **Database Name:** `users_db`

2. **pgAdmin**  
   A web-based administration tool for PostgreSQL. It provides an easy-to-use interface for managing PostgreSQL databases.  
   - Access pgAdmin on `http://localhost:5050`
   - Default login:
     - **Email:** `nick@raadgroup.com`
     - **Password:** `root`

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-project-directory>
```

### 2. Build and Start the Containers

Make sure you have Docker and Docker Compose installed. From your project directory, run:

```bash
docker-compose up -d
```

This will start both PostgreSQL and pgAdmin containers in the background.

### 3. Access PostgreSQL

You can connect to PostgreSQL using any SQL client on `localhost:5432` with the following credentials:
- **Username:** `admin`
- **Password:** `root`
- **Database:** `users_db`

### 4. Access pgAdmin

Open your browser and go to `http://localhost:5050`. Log in with the following credentials:
- **Email:** `nick@raadgroup.com`
- **Password:** `root`

You can now manage your PostgreSQL database through the pgAdmin interface.

### 5. Stopping the Containers

To stop the services, run:

```bash
docker-compose down -v
```

This will stop and remove the containers.
