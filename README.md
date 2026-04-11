# Getting started

### Quick Start (Simple Run)
To run the app locally without any external database requirement, simply run:
```bash
npm install
node src/index.js
```
The app will use a local SQLite database file (`todo.db`) and listen on port 3000.

---

- Our NodeJS App is dependent on v18.20.8, you need to install the similar version
- TCP Port 3000 is enabled in Security Group 

### Install NodeJS on EC2 Ubuntu instance
```jsx
# Be root user for all installation
sudo su

# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 18

# Install yarn
apt install cmdtest
```

### To install NodeJS on Windows / MacOS / Linux Distribution 
URL --> https://nodejs.org/en/download

### Verify the Node.js & npm version:
```jsx
node -v # Should print "v18.20.8".
nvm current # Should print "v18.20.8".
npm -v # Should print "10.8.2".
```

### Steps to deploy Locally or on DEV environment
1. Make sure we are root user
```jsx
sudo su
```

2. Clone the app
```jsx
git clone https://github.com/amigo-nishant/getting-started.git
```

3. Change the directory
```jsx
cd getting-started
```

4. Deploy the App
```jsx
npm install
node src/index.js
```

5. Test the App Frontend
```jsx
http://public-ip-ec2:3000/
```
