# CICD

**complete corporate CICD Pipeline:**

Suppose we have one application which belongs to client and client wants to add some new features in that so client will generate one JIRA ticket and it will get assign to developer 

then developer will write a source code and then test the code, if source code is running fine then it will push the source code on github repository.

After this as a Devops Engineer we need to write the pipeline for that we use Jenkins,first step in jenkins  will do compilation this compilation is done to check if there is any syntax error or not,

after that we will run test cases to test the functionality of the code.

Next step is to perform sonarqube code quality check it will check if there is any vulnerabilities, bugs, issue inside the source code.

After that we are going to do vulnerability check is there any sensitive data and also this trivy tool will scan the dependencies of the application and it will generate a report.

After that we are going to build the applicatio or packaged the application to get the application artifact, now this application artifact and this artifact we are going to publish it on Nexus repository

so we can properly do release managemnet with different versions of artifact.

once the artifact is ready we will build a image docker image and it tag it properly (tagging is done to define different versions of docker image).

after that we are again going to use trivy to scan docker image to find the vulnerabilities inside the containers.Then we are going to push docker image to docker hub

Then we will deploy it using kubernetes, so before that we will use kubeaudit to check kubernetes clusters are secure or not.Then we will deploy the application.

after successfully deploying we need to monitor the application for monitoring we are using Prometheus and Grafana.

![image](https://github.com/Nachiketa-A/CICD/assets/157089767/b9e27bf6-e6cb-4be0-b9e2-bb1381720e53)
