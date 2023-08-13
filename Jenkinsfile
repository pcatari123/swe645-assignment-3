pipeline {
	
	agent any
	environment {
		DOCKERHUB_PASS = credentials('docker-cred')
	}
	stages {
		stage("Building web app image"){
				steps {
					script {
						checkout scm
						sh 'echo ${DOCKER_PWD}'
						sh 'echo ${DOCKER_TAG}'
						sh "docker login -u $DOCKERHUB_PASS_USR -p $DOCKERHUB_PASS_PSW"
						sh "docker build . -t srikar430/swe645-assignment-3:${BUILD_TIMESTAMP}"
					}
				}
			}
			stage("Pushing image to dockerhub"){
			  steps {
			    script {
			      sh 'docker push srikar430/swe645-assignment-3:${BUILD_TIMESTAMP}'
			    }
			  }
			}
	                stage("Deploying to Rancher as single pod") {
                        	
        		}
        		stage("Deploying to Rancher as load balancer"){
			}	
           		
		}
	}
