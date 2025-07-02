# 🚀 Setting Up Docker Inside GitHub Codespaces: A Complete Beginner’s Guide

> *“Imagine coding in the cloud, version-controlling with Git, and containerizing with Docker — all in one place. That’s GitHub Codespaces + Docker for you.”*

---

## 🧠 What You’ll Learn

This guide walks you through setting up and running Docker inside a GitHub Codespace. You’ll learn:

* What Docker and Codespaces are
* Why they work great together
* How to install and use Docker in a Codespace
* How to create and run a basic Dockerized app
* Bonus tips to level up your dev workflow

Let’s go from zero to Dockerized! 🐳

---

## 🛠️ Prerequisites

Make sure you:

✅ Have a **GitHub account**
✅ Have access to **GitHub Codespaces** (available in Pro, Team, or Enterprise plans)
✅ Have basic knowledge of Git and terminal commands

---

## ⚙️ Step 1: Create a GitHub Repository

Let’s start by creating a playground for Docker.

1. Head to [github.com/new](https://github.com/new)
2. Name your repo something like `docker-in-codespaces`
3. Add a README and `.gitignore` (Node, Python, or blank)
4. Click **"Create repository"**

---

## 💻 Step 2: Open in GitHub Codespaces

1. Click the green **"Code"** button in your new repo.
2. Select **"Codespaces" → "Create codespace on main"**
3. Wait for a few seconds — GitHub spins up a full VS Code dev environment in the cloud!

You’re now inside a remote, containerized dev machine. Pretty cool, right?

---

## 🐳 Step 3: Install Docker CLI in Codespaces

> GitHub Codespaces already runs in a container behind the scenes. But to build and run your *own* Docker containers inside it, we’ll set up Docker manually.

### 🧰 Update and Install Docker

Run the following inside your Codespaces terminal:

```bash
sudo apt-get update
sudo apt-get install -y docker.io
```

Then start and enable Docker:

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

Check if it works:

```bash
docker --version
```

✅ You should see something like: `Docker version 24.x.x`

---

## 🧪 Step 4: Test Docker with a Hello World App

Let’s test Docker with a simple “Hello World” Node.js script.

### 1. Create a new file:

```bash
echo 'console.log("Hello from Docker inside Codespaces!")' > app.js
```

### 2. Create a Dockerfile:

```Dockerfile
# Use an official Node base image
FROM node:18

# Set the working directory
WORKDIR /app

# Copy files
COPY . .

# Run the app
CMD ["node", "app.js"]
```

### 3. Build and run your Docker image:

```bash
docker build -t my-docker-app .
docker run my-docker-app
```

🎉 Output:

```
Hello from Docker inside Codespaces!
```

Boom! You just built and ran your first Docker container **inside GitHub Codespaces**. 👏

---

## 🌐 Step 5: Build a Web App in Docker (Optional)

Let’s make it more real by spinning up a basic Express web server.

### 1. Initialize Node project

```bash
npm init -y
npm install express
```

### 2. Create `server.js`:

```js
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => res.send("Hello from Express + Docker in Codespaces!"));

app.listen(port, () => console.log(`Server running on port ${port}`));
```

### 3. Update your Dockerfile:

```Dockerfile
FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "server.js"]
```

### 4. Rebuild and run:

```bash
docker build -t express-docker-app .
docker run -p 3000:3000 express-docker-app
```

Now click **“Ports”** tab at the bottom of your Codespace and **forward port 3000** to preview the app.

---

## 🧹 Bonus: Use a `.devcontainer` for Automation

Want Docker and other dev tools preinstalled every time you open a Codespace?

Add a `.devcontainer/devcontainer.json` file:

```json
{
  "name": "Docker Dev",
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    "docker-in-docker": "latest"
  },
  "postCreateCommand": "sudo apt-get update && sudo apt-get install -y docker.io"
}
```

This automates your environment setup. No more typing `apt-get` manually!

---

## 🪄 Pro Tips

* Use Git to version control your Dockerfiles.
* Use GitHub Actions to build/push Docker images automatically.
* Use Docker Compose for multi-container projects (like backend + database).
