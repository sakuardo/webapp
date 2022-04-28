Hi,  

Thanks for giving me this opportunity, it was an interesting challenge. Unfortunately, I had no time left for configuring the rest. 

What is working? 

    Vagrant will deploy a Centos 8 image 

    Vagrant will forward the port 80 on guest to 8080 on host 

    Vagrant will run a boot script 

    Vagrant will install Ansible 

    Ansible will do hardening 

    Ansible will add repos for Grafana 

    Ansible will configure Grafana  

    Ansible will install Nginx 

    Ansible will configure Nginx as reverse proxy to serve Grafana 

    Ansible will allow the webserver with SELinux  

 

How does it work? 

    Clone the repository:  

    https://github.com/sakuardo/webapp.git 

    Execute command inside cloned directory: 

    vagrant up 

    Access web applications: 

    http://localhost:8080 

    http://localhost:8080/grafana/ 

     

