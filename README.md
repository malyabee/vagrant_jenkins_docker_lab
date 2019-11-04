## Vagrant Jenkins lab on Docker 
 A Vagrantfile to build a Jenkins   on docker  envirnment to learn Jenkins concepts.  
 
1. Docker Host  (centos/7)
    The docker node configured with docker software and ready to host containers. 
    

### Steps :  
  Step 1 :  Install virtual box (https://www.virtualbox.org)

  Step 2 :  Install vagrant  (https://www.vagrantup.com)

  Step 3 :  Download and  Vagrant file  
       git clone https://github.com/malyabee/vagrant_jenkins_docker_lab.git  

  Step 4  : starting virtual machines 

       $ cd vagrant_jenkins_docker_lab
 
       $ vagrant up
       # "vagrant up" might take a while for first time

### commands to login docker virtual machines
    

     vagrant ssh 
     
     
## Docker commands       
###  commands to verify docker version  and start docker daemon
      [vagrant@docker ~]$ docker version
       

       
       
   
   
#### Docker rommands to run jenkinsci/blueocean in a  container  
         [vagrant@docker ~]$  docker run -u root  --rm  -d -p 8080:8080 -p 50000:50000 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock jenkinsci/blueocean
         



#### Jenkins dashboard

Go to http://localhost:8080

### Host compatability :

    This Vagrant verified on Mac OS.


