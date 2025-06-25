# 🐳 MongoDB with Docker & VS Code Integration

This guide helps you run MongoDB in a Docker container, connect it to VS Code, and execute MongoDB commands using a Playground.

---

## 📦 Prerequisites

- Docker installed ([Get Docker](https://www.docker.com/products/docker-desktop))
- Visual Studio Code installed ([Download VS Code](https://code.visualstudio.com/))
- MongoDB for VS Code extension

---

## 🚀 Step 1: Run MongoDB with Docker

Run the following command in your terminal (PowerShell, CMD, or Git Bash):

```bash
docker run -d --name mongodb \
  -p 27017:27017 \
  -e MONGO_INITDB_ROOT_USERNAME=admin \
  -e MONGO_INITDB_ROOT_PASSWORD=admin123 \
  mongo
```
This command:

- Starts a MongoDB container in the background

- Exposes it on localhost:27017

- Creates a root user: Username: admin and Password: admin123



## 🧩 Step 2: Install MongoDB Extension in VS Code

- Open Visual Studio Code

- Press Ctrl + Shift + X to open Extensions

- Search: MongoDB for VS Code

- Click Install on the official extension by MongoDB, Inc.


## 🌿 Step 3: Connect to MongoDB from VS Code
- Click the MongoDB icon in the sidebar (green leaf 🌿)

- Click + Connect

- Use the following connection string:

```
mongodb://admin:admin123@localhost:27017
```

## 🧪 Step 4: Create & Run a MongoDB Playground
Click + New Playground in the MongoDB extension

Paste the following code:
```
use("testdb");

db.users.insertOne({ name: "Mohammed", role: "Developer" });

db.users.find();

```