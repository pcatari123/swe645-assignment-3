#### Project Description
Backend for a Web Application that had a Welcome Page and Tabs which allowed prospective University students to fill out a Survey form with an acknowledgement. The Survey is a feedback about the campus visit. It also had an option to view all surveys filled out by the students till date. Used Intellij IDE to develop a RESTful Web service using Spring and integrated it with the MySQL AWS RDS service. The application was containerized using Docker and deployed on the container orchestration platform Kubernetes on AWS cloud. 

#### DOCKER
Dockerfile contains : Dependencies & Web application related docker definitions
DockerHub: [here](https://hub.docker.com/repository/docker/jinal0217/hw3_backend)

#### KUBERNETES
Deployment & Service Files Contains: container, kubernetes related deployment and execution definitions

#### Git: URL : [here](https://github.com/Jinal17/REST_WebService)


## Steps for Triggering the Build through Jenkins:

- **First Time User** Clone this Repo using: git clone https://github.com/Jinal17/REST_WebService
- Make necessary changes in java files for the Web service on your local system
- Modify the **DOCKER_TAG** version in Jenkinsfile. For example: Modify the **DOCKER_TAG** = ‘V8’ : to V9 (any version)
- $git status
- $git add -–all
- $git commit -m "Pushing Final Changes"
- $git push
- Once the above steps are executed successfully, the Jenkins build will get triggered and the web application with the new changes will get deployed on kubernetes cluster.
