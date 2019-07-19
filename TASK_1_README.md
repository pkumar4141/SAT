HI Team.

Below is my course of action to perform the task one .

TASK 1

Servers and tools used
1.Jenkins hosted on vm in my gcp account 35.185.116.170

2.Dev box on gcp with docker installed on it 

3.my Own gitlab repository to intigrated with jenkins.

4.Intigrated git and jenkins with creating webhook for specific project and using git credentials and api token for git and jenkins
communication 

5 .Created a pipeline job in jenkins which triggers for a push or merge req in git (configured in the git webhook)

6.Attached screen shot of webhook created and attached the jenkinsfile in the above repo

7 And i wrote docker file for creation of app containers which is in node-app and ngnix load balancer docker file in node-nginx which are attached in the above repo
Note : i used empty index.js which act as dummy here

8 Added the jenkins config.xml file and job file to pull the job 

incase of multiple branch we can create multtiple jobs in jennkins with webhooks for respective project in git and will trigger 
job when ever any merge happends to the master 

Kubernetes :

1.we can  update the docker image created for the app into docher hub

2. create a cluster from GKE or setup a master and worker node infrastructue .in any of the above case pull the app sever image from the docker hub and create a deployment along with replicasets binded labels and matchlabel modules and with a image pull polcy as Latest 

3.create a another stage in jenkins file which have node(jenkins slave)  as kubernetes master and 
commands as sh 'kubectl set image deployment.v1.apps/ nginx-deployment node-app=nginx:latest --record=true

we currently testing few of our applications on kubernetes 
