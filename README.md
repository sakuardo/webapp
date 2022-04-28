Hi,  

Thanks for giving me this opportunity, it was an interesting challenge. Unfortunately, I had no time left for configuring the rest. 

Important: 

    Host computer needs to have vagrant installed with VirtualBox provider 

    Host computer should not have any service running on port 8080 

    Modern web browsers try to use https instead of http so be careful when writing the addresses (There are still some problems with the reverse proxy + port forwarding using Vagrant on port 8080) I tested this without Vagrant and the reverse proxy works perfectly 

    Grafana user and password: admin:admin 
    

What is working? 

    Vagrant will deploy a Centos 8 image 

    Vagrant will forward the port 80 on guest to 8080 on host 

    Vagrant will forward the port 3000 on guest to 3000 on host 

    Vagrant will run a boot script 

    Vagrant will install Ansible 

    Ansible will do hardening based on STIG using a public role that I modified to make it work on Centos 8. You can find it here ->  https://docs.openstack.org/ansible-hardening/latest/ 

    Ansible will add repos for Grafana 

    Ansible will configure Grafana  

    Ansible will install Nginx 

    Ansible will configure Nginx as reverse proxy to serve Grafana 

    Ansible will allow the webserver with SELinux enabled 
    

How does it work? 

    Clone the repository:  

    https://github.com/sakuardo/webapp.git 

    Execute command inside cloned directory: 

    vagrant up 

    Access web applications: 

    http://localhost:8080 

    http://localhost:8080/grafana/ 

 

 

 

