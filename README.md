> [!IMPORTANT]
> **Node.js Version Notice:**
> - This application is able to run **only on Node.js 26**.
> - Any references below mentioning Node.js **20.x** or **24.x** are kept **intentionally for demo purposes**.

---
# Getting started

A simple Node.js Todo application with SQLite / MySQL database support.

---

## Prerequisites

Before running the application, make sure you have **Git** and **Node.js** (with **npm**) installed on your system.

### 1. Install Git

- **Ubuntu / Debian:**
  ```bash
  sudo apt update
  sudo apt install -y git
  ```
- **Windows / macOS:**
  Download and install Git from [git-scm.com/install](https://git-scm.com/install/).
- **Verify Git Installation:**
  ```bash
  git --version
  ```

---

### 2. Install Node.js & npm

Node.js version **20.x** or **24.x LTS** is recommended.

#### Option A: Ubuntu / EC2 Linux (Recommended via NVM)
1. Update system packages and install prerequisites:
   ```bash
   sudo apt update && sudo apt upgrade -y
   sudo apt install -y curl ca-certificates gnupg
   ```

2. Install NVM (Node Version Manager):
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.8/install.sh | bash
   
   # Load nvm into the current shell session
   \. "$HOME/.nvm/nvm.sh"
   ```
   ```poweshell
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.8/install.sh | bash
   ```

3. Install Node.js (Version 24):
   ```bash
   nvm install 24
   nvm use 24
   ```

#### Option B: Windows / macOS
- Download the installer from the official website: [nodejs.org/en/download](https://nodejs.org/en/download)
- Run the installer and follow the on-screen instructions (npm is included automatically).

#### Verify Node.js and npm Installation
```bash
node -v   # Should print version (e.g. v24.x.x)
npm -v    # Should print npm version (e.g. 10.x.x / 11.x.x)
```

---

## Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/erchetansoni/getting-started-node.git
cd getting-started-node
```

### 2. Install Application Libraries & Dependencies
Install all required libraries and dependencies defined in `package.json` (such as Express, SQLite3, MySQL2, etc.):

```bash
npm install
```

> **Note:** If you encounter any permission warnings with sqlite3 or native build tools, make sure build essentials or python/gcc are available if compiling from source, or run `npm install` with standard user privileges.

---

## Running the Application

### Quick Start (Local Run with SQLite)
To run the app locally without any external database requirement:

```bash
# Start the application
node src/index.js

# Or start in development mode with nodemon auto-restart:
npm run dev
```

The app will initialize a local SQLite database (`todo.db`) and start the server.

- Open in your browser: [http://localhost:3000](http://localhost:3000)

---

## Deployment on EC2 / Ubuntu Server

1. **Switch to root user (or run with sudo):**
   ```bash
   sudo su
   ```

2. **Clone the repository:**
   ```bash
   git clone https://github.com/erchetansoni/getting-started-node.git
   cd getting-started-node
   ```

3. **Install dependencies:**
   ```bash
   npm install
   ```

4. **Start the application:**
   ```bash
   node src/index.js
   ```

5. **Access the application:**
   Open port 3000 in your EC2 Security Group inbound rules and visit:
   ```text
   http://<public-ip-ec2>:3000/
   ```
