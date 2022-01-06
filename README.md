# Final Project  

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

## Module – 3 - Vagrant
1. launch Ubuntu 18.04 box with docker latest installed on it while it launches for the first time  
2. launch Centos 7 box with docker latest installed on it while it launches for the first time  
3. create a git repo name infra  
4. open 2 more branches from master branch  
5. commit the scripts and the vagrantfiles to your branch and pull request to dev branch – put the trainer as reviewer  
## module 4 – docker
1. write dockerfile to this maven project https://github.com/lidorg-dev/hello-world-war  
2. make sure you fork the repo  
3. build with maven the pom file  
4. build your docker file and run the container  
5. copy only the war file to docker container  
6. push the image to dokcer hub repo  
7. send me the repo details in slack  
## module 5- docker compose
1. build docker compose file and deploy wordpress and mysql at the same time  
2. put the compose in your infra repo from module 3 and pull request to dev - and review to trainer  
## module 6- Jenkins
1. Setup Jenkins or use the one you already have  
2. Create a pipeline which :  
  a. checkout this code https://github.com/lidorg-dev/hello-world-war -> from branch dev  
  b. from your own repo – make sure to trigger the pipeline for each change in the code  
  c. build the maven war  
  d. run static code analysis (use sonarqube)  
  e. build the docker file using the dockerfile from module 4  
  f. tag it with build id  
  g. push the image with tag to Nexus private registry  
  h. notify slack (create a new channel ) the buid is successful ( make sure to notify if one the steps failed )  
## module 7- Jenkins- jobs
1. create 7 jobs -> downstream jobs and copy workspace from each other  
tip : use custom workspace plugin to make the same one for all the jobs  
job 1 -> checkout code from git using branch as parameter https://github.com/lidorgdev/aspnet4-sample.git so you can select them every time you trigger the job  
job 2 -> build using msbuild  
job 3 -> do static code analysis - > using sonar scanner  
job4 -> use mstest – to do test  
job 5-> package with nuget  
job 6 -> upload to nexus -> nuget repo  
job 7 – notify slack (use same channel as before )  
2. make a pipeline view for this jobs  
## module 8- Kubernetes
1. please create an automation deployment of K8s ( 1 master , 2 workers)
2. can be ( kops in aws , rancher, kubespray , kubeadm) using ansible or puppet or bash scripts
## module 9 – deploy Prometheus 
deploy Prometheus operator using Helm Chart and Grafana - > create a graph show metric of 
nodes and pods off all namespaces 
## module 10 – deploy app to k8s
deploy the app from module 6 ( hellow-world-war) -> write your own deployment yaml -> 
with replicas of 4 pods -> get the image from your nexus private registry
