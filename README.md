# Devops-task2
Devops internship

Node.js CI/CD Pipeline using Jenkins on AWS

This project demonstrates a basic CI/CD pipeline using Jenkins, Docker deployed on an AWS EC2 instance. The application is a simple Node.js Express server.

Tech Stack
- Node.js
- Express
- Docker
- Jenkins
- AWS EC2


Project Structure
.
├── app.js              # Node.js Express server
├── Dockerfile          # Docker configuration
├── Jenkinsfile         # Jenkins pipeline configuration
├── package.json        # Project metadata and dependencies
├── README.md           # You're here!


How It Works
1. Jenkins pulls the latest code from GitHub.
2. Runs npm install to install dependencies.
3. Builds a Docker  for the Node.js app.




Setup Guide


2. Install Dependencies
npm install

3. Run Locally (Optional)
node app.js

4. Open Browser
http://localhost:3000





