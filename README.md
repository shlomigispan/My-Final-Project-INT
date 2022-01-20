# **Final Project** 

## Module – 1 Git & python  
1. You can choose either github or gitlab   
2. Fork the code from : https://github.com/lidorg-dev/final-project.git  
3. Notice the python code ( python ver 3.2+)  
4. lock the master branch from commits  
5. create a new branch : dev  
6. create a new branch from dev: <yourname_sol>  
7. fix the code in yourname_sol branch  
8. commit your change  
9. test the new code in your Linux VM  
10. create a pull request to dev branch (attach your test screenshot to the pull request)– add the trainer as approval  
11. after trainer approved – merge the Pull Request (PR) to dev branch  
12. tag your code to 1.1  


### The solution for module 1 is in: https://github.com/shlomigispan/final-project/tree/dev  

## Module – 2 Git & JAVA-MAVEN  
1. First take the code from here https://github.com/lidorg-dev/spring-boot-examples -----from master branch  
2. The code in Github is written in Java  
3. Upload or fork it to your own repo in github  
4. Notice there is In pom.xml there is a version currently 0.0.1-SNAPSHOT  
5. now lock the master branch from commits  
6. make sure you make one approval in pull request/merge requests  
7. create a new branch : dev  
8. create a new branch from dev: <yourname_sol>  
9. fix the code in yourname_sol branch  
10. now try to build the code in linux VM -- make sure you have maven 3 installed and JDK 1.8 -- (the build command is: mvn compile) 
11. make sure to run that maven command in the pom folder  
12. if mvn passed then run mvn test command. ( it’s failing on the test) – fix it on your branch and increment the pom file to 0.0.2-SNAPSHOT  
13. do PR to trainer for approval with the screenshot of the fix  
14. after successful merge -> tag the release to 0.0.2  

### The solution for module 2 is in: https://github.com/shlomigispan/spring-boot-examples/tree/dev

## Module – 3 - Vagrant
1. launch Ubuntu 18.04 box with docker latest installed on it while it launches for the first time  
2. launch Centos 7 box with docker latest installed on it while it launches for the first time  
3. create a git repo name infra  
4. open 2 more branches from master branch  
5. commit the scripts and the vagrantfiles to your branch and pull request to dev branch – put the trainer as reviewer  

### The solution for module 3 is in: https://github.com/shlomigispan/infra/tree/dev


## module 4 – docker
1. write dockerfile to this maven project https://github.com/lidorg-dev/hello-world-war  
2. make sure you fork the repo  
3. build with maven the pom file  
4. build your docker file and run the container  
5. copy only the war file to docker container  
6. push the image to dokcer hub repo  
7. send me the repo details in slack  

### The solution for module 4 is in: https://hub.docker.com/r/shlomigis/final-project-module-4/tags

## module 5- docker compose
1. build docker compose file and deploy wordpress and mysql at the same time  
2. put the compose in your infra repo from module 3 and pull request to dev - and review to trainer  

### The solution for module 5 is in: https://github.com/shlomigispan/infra/tree/dev

## module 6- Jenkins
1. Setup Jenkins or use the one you already have  
2. Create a pipeline which :  
  A. checkout this code https://github.com/lidorg-dev/hello-world-war -> from branch dev  
  B. from your own repo – make sure to trigger the pipeline for each change in the code  
  C. build the maven war  
  D. run static code analysis (use sonarqube)  
  E. build the docker file using the dockerfile from module 4  
  F. tag it with build id  
  G. push the image with tag to Nexus private registry  
  H. notify slack (create a new channel ) the buid is successful ( make sure to notify if one the steps failed )  

### The solution for module 6 is in: https://github.com/shlomigispan/hello-world-war/tree/dev  


