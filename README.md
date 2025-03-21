[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)] 

This project sets up a CI/CD pipeline using GitHub Actions to ensure code quality and automate deployment of a Tech-Quiz application. The pipeline consists of two workflows:

1. Continuous Integration (CI): Runs Cypress component tests when a Pull Request is made to the develop branch.

2. Continuous Deployment (CD): Deploys the application to Render when code is merged from develop to main.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Deployment](#deployment)
- [Technologies Used](#technologies-used)
- [License](#license)


## Installation
If you'd like to run this application locally, follow these steps:

1. Clone the repository to your local machine:
   ```bash
   git clone git@github.com:TanyaH-create/cicd_deployment_challenge.git
   
2. Navigate to the project directory 
   ```bash
   cd cicd_deployment_challenge

3. Install required dependencies:
   ```bash
   npm install

4. Create a .env file in the server directory with a MongoDB URI:
   ```bash
   MONGODB_URI=your-mongo-url

5. Ensure MongoDB is installed and running on your local machine.
   
6. Build and Run the development application, there is an optional seed file included
   ~~~bash
   npm run build && npm run develop
   
## Usage
- Work on a feature branch and push changes
- Open a Pull Request to develop
- GitHub Actions will run Cypress tests
- Once tests pass, merge the pull request
- When the develop is merged into main, the applicatio will automatically deploy to Render.
- Branches used:
  - main - Production-ready code, merges trigger deployment
  - develop - Main integration branch. Pull requests from feature branches are merged here first
  - feature/* - Development branches for new features or fixes

![Screenshot 2025-03-20 224622](https://github.com/user-attachments/assets/b6cf0754-cb5a-46c1-9d55-5c3cb551423f)

![Screenshot 2025-03-20 224737](https://github.com/user-attachments/assets/ed3229e3-beba-446b-bd84-48f4da8687e3)

![Screenshot 2025-03-20 224816](https://github.com/user-attachments/assets/444ad45f-c135-44ba-b050-d79a4d67cbf5)

![Screenshot 2025-03-20 224838](https://github.com/user-attachments/assets/8e5197e0-b681-4fc6-8cba-f42e06286a0f)

## Deployment
This application is deployed on Render with a MongoDB database using MongoDB Atlas: 
   Live application [Tech Quiz](https://cicd-deployment-challenge.onrender.com) 

## GitHub Repository
The source code for this project can be found here [GitHub Repository](https://github.com/TanyaH-create/cicd_deployment_challenge).

## Technologies Used
 - GitHub Actions - Automates CI/CD processes
 - Cypress - End-to-end testing framework
 - Render - Hosting and deployment service
 - Node.js / Express.js - Backend server
 - MongoDB - Database for the application

## Contributing
Contributions are welcome! Please follow these steps:
1.	Fork the repository.
2.	Create a new branch for your feature or bug fix:
    ```bash
    git checkout -b feature-name
3.	Commit your changes:
    ```bash
    git commit -m "Add feature-name"
4.	Push your branch:
    ```bash
    git push origin feature-name
5.	Submit a pull request.
