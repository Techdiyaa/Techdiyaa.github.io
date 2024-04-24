Title: Docker Three Tier Architecture 
---

# Three-Tier Application Deployment using Dockerfile


## Prerequisites

Before you begin, ensure that you have the following installed:

- [Docker](https://www.docker.com/get-started)
  
## Project Structure

- backend: Node.js application serving as the backend.
- frontend: React.js application for the frontend.
- mysql: Dockerfile and configurations for the MySQL database.

## Dockerfile(Database)
![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/db%20dockerfile.png)


## Dockerfile(Frontend - Backend)
![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/frontend%20bacend%20dockerfile.png)

## Deployment Steps
0. Create Network
   - Navigate to the project directory
   - bash
     docker network create my-network
     
     ![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/1.jpg)
     
1. MongoDb Database:   - Navigate to the Mongodb directory.
   - Build the Mongodb Docker image:
     bash
     docker build -t 21bcp454d_db_img .
     
     
     ![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/4.jpg)

     
   - Run the MongoDB container:
 
     ![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/5.jpg)
  
2. Frontend - Backend Application:

   - Navigate to its directory.
   - Build the backend Docker image:
     bash
     docker build -t 21bcp454d_frontend_backend_img .
     
     ![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/2.jpg)
   - Run the frontend-backend container:
     bash
     
     ![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/3.jpg)

3. Access the Application:

   Open your favorite browser and visit [http://localhost:3000](http://localhost:3000). Enjoy exploring the pplication!
   ![Alt Text](https://raw.githubusercontent.com/Techdiyaa/Techdiyaa.github.io/master/images/6op.jpg)

    
