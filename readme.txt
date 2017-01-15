
To install this application you need an Ubuntu 16.04.1. Within it, run the following commands:

1) This command will install ansible on your machine. 
   $sudo apt-get install ansible 

2) Now you have to edit ansible's hosts file. To do so, run:
   $ sudo nano /etc/ansible/hosts
   And add this at the bottom (where your_ip is the public ip of your machine):
    [servers]
    your_ip

3) Now run:
   $ sudo apt-get install sshpass

4) So far you have installed everythin needed to run ansible. Now, copy and paste the vars.yml and deploy.yml found in this repository at
   /ormuco_challenge/ansible in your machine.

5) $ ansible all -m ping

6) $ ansible all -m ping -s -k -u root

7) $ ansible-playbook deploy.yml -u root
   Here the playbook run will "freeze" at the "script" task wich is the one that runs the server.
   
8) Now you're able to go tu http://your_ip:8000/ormuco and use the ormuco challenge app.
