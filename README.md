# BAGORA - Online Shopping Website

A modern and responsive online shopping website for bags, built using HTML, CSS, and JavaScript, and served using Nginx inside a Docker container.

## Project Structure

```text
BAGORA/
├── index.html
├── Dockerfile
└── README.md
```

## Requirements

Make sure you have the following installed on your Linux machine:

- Git
- Docker Engine

## Installation & Setup

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the Project Directory

```bash
cd BAGORA
```

### 3. Build the Docker Image

```bash
docker build -t bagora .
```

### 4. Run the Docker Container

```bash
docker run -d -p 8080:80 --name bagora-container bagora
```

### 5. Access the Website

Open your browser and visit:

```text
http://localhost:8080
```

Your website is now running using Nginx inside Docker.

## Updating the Website

If you want to modify the website:

1. Open `index.html` using your preferred code editor.
2. Make your changes and save the file.
3. Build a new Docker image:

```bash
docker build -t bagora .
```

4. Stop and remove the old container:

```bash
docker rm -f bagora-container
```

5. Run a new container:

```bash
docker run -d -p 8080:80 --name bagora-container bagora
```

Refresh your browser to see the updated website.

## Useful Docker Commands

Check running containers:

```bash
docker ps
```

View container logs:

```bash
docker logs bagora-container
```

Stop the container:

```bash
docker stop bagora-container
```

Start the container:

```bash
docker start bagora-container
```

Remove the container:

```bash
docker rm -f bagora-container
```

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Docker
- Nginx

## Notes

- Make sure Docker is running before executing Docker commands.
- If you get a permission error, use `sudo` before Docker commands.
- If port 8080 is already in use, you can change the host port, for example: `-p 8081:80`.
- Docker will automatically download the Nginx image if it is not available locally.

## Developer

BAGORA - Online Shopping Website
