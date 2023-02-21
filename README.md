# Multi Tier Web Application
Multi Tier Web Application Setup Locally

**The objective of this project is to set up a web application stack locally to gain a baseline for upcoming projects and R & D**

TOOLS 
- HYPERVISOR - Oracle VM VirtualBox 
- AUTOMATION - VAGRANT 
- CLI        - Git Bash
- IDE        - Sublime

ARCHITECTURE OF PROJECT SERVICES
- NGINX
- TOMCAT
- RABBITMQ
- MEMCACHED
- MYSQL

We will be setting up a web application written by devs in Java. Nginx is going to do the work of load balancing, Nginx is a web service just like Apache, httpd and it's very commonly used to create the load balancing. So in one of our VM we will be having Nginx service and we'll configure it in a way as soon as the request comes, it is going to route the request to the Tomcat server, Apache Tomcat is a Java Web application service. Now here, there is also one more service called Rabbit MQ connected to Tomcat, Rabbit MQ is a message broker or also called a queuing agent to connect two applications together, in this project is not that functional but it's gonna be setup for training porpuse. So on our application the user needs to login, our application will run an SQL query to acces the user information stored in MySQL database, but before it goes to mysql, the request will got to MemcacheD and look for that information. MySQL Server will store the user information when the first time the request comes to the database, mysql it will be sent from the Mysql Server to the Tomcat and then it will be cache to the MemcacheD.

Vagrant will be used to automate the deploy of vms on VirtualBox and run the bash scrips for set up of all services.


- Vagrantfile Vagrant file is the iac that defines vms, network, hostnames, machine resources and scripts to run 
- tomcat.sh script for instal dependencies and tomcat setup 
- rabbitmq.sh script for setup of rabbitmq service
- nginx.sh script for setup of nginx service
- mysql.sh script for setup of mariadb-server and database configuration
- memcached setup of memcached service
- application.properties this file contains the different configuration which is required to run the application in a different environment


<sub>THIS PROJECT WAS DEPLOYED MANUAL FOR TRAINING AND AUTOMATED, VALIDATION:</sub>

![Captura de tela 2023-02-20 214912](https://user-images.githubusercontent.com/95035624/220463475-f0b6d59c-2b8a-4300-9cb8-aa160eede3cb.png)

![Captura de tela 2023-02-20 215832](https://user-images.githubusercontent.com/95035624/220463489-10b7ba1a-e5cb-4966-80a0-7b96a45afe19.png)

![Captura de tela 2023-02-20 221345](https://user-images.githubusercontent.com/95035624/220463499-b51851ea-e56d-45ad-8d4a-3824f642fe48.png)

![Captura de tela 2023-02-20 221531](https://user-images.githubusercontent.com/95035624/220463506-e6840413-12b0-40af-9b84-8fa550804d18.png)
