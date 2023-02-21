# Web-Application
Multi Tier Web Application Setup Locally

**The objective of this project is to set up a web application stack locally to gain a baseline for upcoming projects and R & D **

TOOLS 
> HYPERVISOR - Oracle VM VirtualBox 
> AUTOMATION - VAGRANT 
> CLI        - Git Bash
> IDE        - Sublime

ARCHITECTURE OF PROJECT SERVICES
> NGINX
> TOMCAT
> RABBITMQ
> MEMCACHED
> MYSQL

We will be setting up a web application written by devs in Java. Nginx is going to do the work of load balancing, Nginx is a web service just like Apache, httpd and it's very commonly used to create the load balancing. So in one of our VM we will be having Nginx service and we'll configure it in a way as soon as the request comes, it is going to route the request to the Tomcat server, Apache Tomcat is a Java Web application service. Now here, there is also one more service called Rabbit MQ connected to Tomcat, Rabbit MQ is a message broker or also called a queuing agent to connect two applications together, in this project is not that functional but it's gonna be setup for training porpuse. So on our application the user needs to login, our application will run an SQL query to acces the user information stored in MySQL database, but before it goes to mysql, the request will got to MemcacheD and look for that information. MySQL Server will store the user information when the first time the request comes to the database, mysql it will be sent from the Mysql Server to the Tomcat and then it will be cache to the MemcacheD.

Vagrant will be used to automate the deploy of vms on VirtualBox and run the bash scrips for set up of all services.

