# devops-interview
# tell me about yourself

# good morning im fine and thanks for asking , what about you.

# myself lakshmi , im having overall 4+ years of exp on devops tools , past 4+ years im working in new found infotech pvt ltd.as a devops engineer,
# well coming to my educational qualification  i have completed my post graduation from aknu kkd
# well coming to my skill set hands on exp on linux
Brown exp on git and build tool maven
im good at jenkins ang jenkins is automation tool for continuous integration and delivery 
hands on exp on shell script
and i have good knowledge on monitoring tools like prometheus and grafana
and hands on exp on creating EC2 instance in AWS cloud environment
and im good at docker it is virtualization  and containazation tool
# and coming to my ROLES AND RESPONSIBILITIES
I involved and resolving git related issues when developer had an issues designing creating maintaing git repositories as per client specifications  and im creating jobs in jenkins and jobs in jenkins and set up **global permissions** and scheduling jobs , building continuous integration environment in jenkins launching and configuration of amazon cloud services my using amis and configuing the servers for specified  applications and crreating **elastic ips** attaching and detaching  to instances as per client requirement and im experienced in writing Dockerfiles to build customized  image for creating containers, work with maven build  tool for continuous building Deployable Auto packs and i perform tasks such as check-in checkout and merging code from development branch to main branch and main branch to develpment branches and enabling sonar quality gates for the modules of the project to maintain code quality and simply this is my profile

# your exp in git right ?
rate your self 1-5
4 '
# 1. can you please explain uh which branching strategy you are using ?
3 we are using featuere branching strategy and in this master branch and integration branches or long lived branches  and master always points to the prod commits and the total code is available in integration and if i want to change feature i can create a branch from integration and while  developing for every commit we are developing CICD  and tracking whether the CICD is successful in development   or not but it is successful in development then the developer raising a PR request , when raising PR also we are putting some conditions to check whether the code is successful in development or not if it is success then  only i can raise PR and after raising PR everyone checking changes and approving to merge it so then the commits which are moved to integration or checked and tested  in all environmets like QA, PREPROD,performance so and if all these are successful then moving to the production deployment and also in production we are checking whether the code is success in development or not and also checking QA ,PREPROD and performance if it success then only CICD moving forward otherwise its stops there only and once it is success in prod master tip points to that commit , so we point the tip and tag it as v1 i mean V version 1.0 or something and in future we created version 2.0 i mean V2.0 so we can check ehether we 1.1 version 1.2,1.3, or develop which stage we can easily refer so and by doing this if we face any conflicts  and what are the conflicts i'll get i'll clear all those conflicts thaen i can  push back into integration branch and i can release a login or ign up model whatever for the client requirement .so thats it uh....

# 2. you said about git conflicts rights so what kind of conflicts you get and how you resolved it ?
in git two or more users make changes  to same file or lines of code and then try to match those changes together so it is in that case it is unable to automatically match the changes and requires the user to  maually resolve the conflilcts so to resolve this conflicts we uh first what should we do means which git status i mean which files we have the conflicts so after opening the files thte complex  located with a we have the complex markers there so uh we can edit the files and remove the conflicts marker and maually merge the changes as needed and i can save the file by using **git add file name** to mark the file as resolved so then once all these conflicts hasbeen resolved i can use git commit to commit the changes and one more important here is the uh conflicts can be complex right so it may requires the communicaton and collaboration with our teammates to resolve so therefore uh it should be important to have a good communication and collaboration practice when we're working with that grid so that is important is very neede in this im in this concern to resolve the conflicts.
#  jenkins scale up 1-5
4
# 3. can you pleae explain CICD ?
CICD is stads for on cont integration delivry and deployment it is a software development methedology that aims to automate the process of buildging > testing> deploying sotware changes and cont int is the practices of frequently and automatically emerging code changes from multiple developers into a single shared level whether it is a git or whatever the rrepository they are used and this allows the developers to catch and fix errors early in the development life  cycle and reducing the likelihood of conflicts and integration issues later on and cont in delivery  or deployment is the practice of automan=ting rhe deployment to make faster and more reliable and here this invludes the tasks such as **building ,testing and packaging** the software am
as well as deploying into prod environment and with CD developers can rapidly release new features and  debug fixes to users with a minimal downtime  and risk ,so simply as saying that CICD  creates a development uh i mean development pipeline and that can help the team to deliver high qualitty software faster and more frequently compared to recent ones 

# 4. do you have knowledge on writing jenkinsfile ?
can you share your screen and can you plz explain  
notepad
# ###############
**pipeline{
agent any
stages{
stage('Build'){
steps{
sh 'mvn clean install'
}
}
stage('Test'){
steps{
sh 'mvn test'
}
}
stage('Deploy'){
when{
branch 'master
}
steps{
sh'mvn deploy'
}
} am so 
}post{
always{
sh"echo pipeline succeeded"
}
failure{
sh"echo pipeline failed"
}
}
}**

# #############
HERE PIPELINE== MEANS ITS DEFINES ENTIRE JENKINSFILE 
agent=== any means it will available for any agent in jenkins
stages ==defines diff stages of pipeline 
steps== once build is done it installmvn install 
steps ==test to run the unit project test 
stage deployment == there is any changes in master branch then only the deployment  will proceed 
steps== sh mvn deploy 
and here i had included the steps like um post actions right so here post means uh this can deploy the post build actions to be executed after the pipeline is completed 
# always in the sense means 
it gives wheteger theh pieline is success or failed 
# 5. how to schedule builds in jenkins?
so in jenkins what the build want triggers i will go to build confgi and set checkbox  **build periodically**  under that i can use the scheduled text field and entering the schedule for the build and the schedule should uh i included in the crontab format like we have five wheels separated by space and sstrips like minutes as day of the month and day of week ...
# everyday at 9 
so will use * 9 * * * like this i configured and based on this i will check build triggers .
# 6. have exp on docker ? what is docker ?
docker is a tool that enables a developers to package their applications and all of it depends into single container mkaing it easier to run cosistently across a different environments and it helps to resolve the problems of application dependencies and makeit easier to build it and run applications 
# 7.what is diff b/w ADD AND COPY ?
Are used to copy the files or directories from the host machine to the container file system while they may similar there may be the some difference b/w these two cmds 
ADD== NOT ONLY COPYING THE FILE OR DIRECTORES  butb also it can download the files from URL's
and extract or archives as well as it is uh it has a more versatile functionality than copy however this personality also comes with some cavities i mean such as potentially security reasons 
eg:
 if you add the URL that points your file that contains malicious code and it will executing during the build process while you use the add and coming to copy it is a similar uh command that canonly copyfiles and directories from the host to the container system so my suggestion is it is safe option what file you exactly want to copy
 use copy ,if need aditional then only you can use ADD 
 # 8. DIFF BETWEEN ENTRYPOINT AND CMD ?
 Both are used in docker file that is run when the container is started and entry point is for exectable run well CMD specify the default arguements for that executable .
 # 9. what is the dockerfile ?
 Docker file is a text file which is used for set of instructions to build a docker image so it is a simple and reproducable way to build docker images which can thenbe used to v=create containers and in the docker files also it includes the commands like specify base image to build open and copy files from directories from the host machine to the conatainer file syatem and we can use the run command inside the container such as installing packages or config int the software and also exporse ports to allow the communication with the container and we can define entrypoint or default command to run whether the contianer starts so simply uh using Docker  plush developers can define and automate the process of building a Docker image .
 # 10.write a dockerfile exp it ?
 # ##########
 FROM alpine:latest              ( base image)
 RUN apk add --update nodejs.npm ( install npm nodejs on base image )
 WORKDIR /app                    ( set as path for wrkd)
 COPY ./app                      (copy content into the current app dir )
 RUN npm install                  ( app depencies using npm)
 EXPOSE 3000                      ( exp my port on 3000 comm with ouside world )
 CMD ["npm","start"]               ( specifies cont start )
 # ##########
# 11. how should we go into a running container ?
# ****doecker exec -it <cid> bash  # you will get id by using PS  command 

# 12. exp on k8s ? explain k8s architecture ?
# masternode >>>>>>>>>
# apiserver====== central management of the k8s clusters so it allows users and othersto interact with cluster 
# etcd ===== distributed key value that stores the configuration data for the cluster and it is used to store the state of the cluster inlcuding information about the** nodes ****services** and ****pods ****
# controller manager == manages desired state of cluster it inclueds controller of the nodes ,replication, endpoints and services and apart from that we have in a scheduler 
# scheduler=== resposible for deployment of app and the noddes in the cluster
# node =============== worker machine in cluster that runs the containerized workloads annd each node has the container runtime such as docker by running the containers a well as kubernetes agent 
kubectl== that comm with master node 
pod == smallest deployment unit in k8s and its represent a singke instance of a running process in the cluster .
and a pod can contain one or more containers that shares the same network and storage resources 
kubectl
service : accesing ports 
volume: way of store data
# 13. diff b/w k8s and dockerswarm terms ?
docker warm for smaller deployment 
# 14. which cloud you are using  scale 3.5/5? is it possible to recover last private key 
get by only backup or copy of the file so it is recommended to always keep a backup of your prvkey in a secure location i mean such as  a password protected USB drive or a hardware valley
and also some key management   system also offer recover mechanism that can help to recover lost scrheme but these systems requires prior setup and conclusion ...
so if i dont have backup i will generate new key 

# creating new ec2 instance and attching EBS volume of other instance
# conn pub ip with prv ip by using bastion host== creating bastyion host in public subnet \and i connect through SSH
# LINUX  ?305/5
# TYPES OF PERMISSIONS WHAT IS chmod ?
r== READ PERMISSIONS ==4
w=== WRITE PERMISSIONS ==2
x=== EXECUTABLE PERMISSSIONS ==1

U
O
G
# EG: chmod 644 mytext.txt
owner== r+w (O)
=========r (g)
==========r (u)
# checking running process ?
ps command
other than that TOP command we have  cpu memory
# RAM USES
free command 
free -m megbyte 
free -g megabyte 
free -h humanreadable 
free -k kilobytes 

# shell script 3/5
# ansible and terraform  ?
i dont have knowledge on that but if i gert chance i will definenetly work on that .






