# VM-vs-Docker
This repo contains some of differences and use cases for docker and VM

VM and docker both are virtualization technologies but there are some differences which makes them specific for use.

#### VM (Virtualization)
##### - VM provides hardware level virtualization for different OS which we called as Guest Operating Systems. All VMs that we created using any of the virtualization Tools like VirtualBox or Like VSphere or MSFT Hyper-V , Shares the Host OSs Hardware resources and this resources are isolated. (VMs are not share their resources among each other.)
##### - Whenever we want to run our applications on different OS flavours, at that time, we need VM. 
##### - Whenever our application is complicated (Likes requires lots of configurations like many network ports, some of network endpoints, requires high security configurations and so on)
##### - If we want to create IaaS scenarios by using VM management tool like Vagrant, then it will quite easy.
##### - VM takes more time to boot up as compared to docker
##### - A VM is more secure than a container. The main reason is that the VM has the advantage of having hardware isolation

--------------------------------------------------------------------------------------
#### Docker (Containerization)
##### - If we want to run multiple applications over a single OS kernal, then docker is best suite.
##### - Container provides OS level process isolation, that means containers shares OS kernal rather than Hardware.
##### - If we want to ship our applications and application data , then with docker , its quite simple.
##### - Container starts quickly as it has only required depedencies and libraries to run the application. That makes it faster.
##### - docker containers provides container level isolation but still shares the system kernal where one application interference to another sometimes cause serious issues.(there is a possibility that malicious code run within the container will affect other containers on this machine as well as the host operating system. This risk can be mitigated by adding built-in security checks to the container.)
##### - containerization mostly deal with quick application deployment in various scenarios like CICD.

##### As docker containers and virtual machines has its own cons and prons. but the best way to use these two technologies is combination of one. Where VM provides security and containers provides speed for our application deployments.
