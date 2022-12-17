# Building an App + DB with Docker and CI/CD with Jenkins

 The purpose is to simulate development of a JS, Nodejs application to execute a CI/CD pipeline using Jenkins and connect the app with MongoDB (combined with MongoExpress) for database using Docker container 

 Overall Workflow:

 1. Create Docker container for the JS application 
 2. Deploy MongoDB and MongoExpress containers with Docker and couple it with the app in a local environment
 3. Commit to the GitHub repo
 4. Jenkins triggers a build for the JS app and creates Docker image every time a commit is made in the GitHub repo
 5. The Docker image is pushed to a private repository in DockerHub, from where it can be pulled in the local testing environment


