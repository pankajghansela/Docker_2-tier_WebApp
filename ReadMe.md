# Building a 2-tier JS web app + DB with Docker and CI/CD with Jenkins

 The purpose is to simulate development of a 2-tier JS, MongoDB (+MongoExpress for DB) application in the local env. and continuously deploying the changes in the local env. of a testing server using Jenkins and deploying the containerized app in the testing env. using Docker 

 Overall Workflow: 
 (A schematic representation available in "Overall_Architecture.jpg") 

 1. Create the JS application
 2. Pull the MongoDB and MongoExpress Docker images and deploy in Docker containers to couple it with the app in a local environment
 3. Create a Dockerfile specifiying all the dependencies for the JS app
 4. Commit to the GitHub repo
 5. Jenkins initiates a build and creates a Docker image for the JS app every time a commit is made in the GitHub repo
 6. The Docker image is then pushed to a private repository in DockerHub by Jenkins, from where it can be pulled in the local testing environment
 7. The entire 2-tier app can be deployed in the local testing env. using the Docker compose to run in a containerized env.


 All the files and dependencies for the JS app resides inside "MyApp" directory

 Dockerfile to build an image of the JS app with all the necessary dependencies to run
 The image is pushed to my Docker Repository under /pankajghansela

 Docker-compose contains 3 services: JS app, MongoDB and MongoExpress

 The JS app listens on port 3000
 The MongoDB Express UI can be accessed via port 8081
