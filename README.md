# CI-CD-with-Dockers-and-Jenkins

For details on how to use the repo refer to our blog: https://blog.avmconsulting.net/posts/2019-04-07-automated-ci-cd-with-docker-and-jenkins/


Goal is to ensure our pipeline works well after each code being pushed. The processes we want to auto-manage:

Just One commit and the application is deployed in Docker Container

Code checkout
Run tests
Compile the code
Run Sonarqube analysis on the code
Create Docker image
Push the image to Docker Hub
Pull and run the image
First step, running up the services

Since one of the goals is to obtain the Sonarqube report of our project, we should be able to access sonarqube from the jenkins service. Docker compose is a best choice to run services working together.