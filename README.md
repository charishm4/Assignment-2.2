# AutomationWithAnsible
In this Assignment, I have to implement a simple python flask app and put it behind HAproxy, which will work as a load balancer.
The flask app answers the requests by replying with the time and hostname of the host that replied. 
The site consists of 5 hosts: HAproxy, devA, devB, devC, Bastion, and an internal site-local network. The HAproxy host acts as the entry point to the service and load balance between devA, devB, and devC.  
The dev servers use private addresses from the site-local network and do not have direct public access. The last host, Bastion, is acting as an SSH (Secure Shell) entry point to the internal network.
For this, I wrote an ansible-playbook site.yaml which deploys the HAproxy and flaskapp on appropriate existing hosts. And also I wrote the code to install SNMPd daemon onto the dev servers to monitor.

Run the playbook as:
ansible-playbook -i hosts site.yaml


 
