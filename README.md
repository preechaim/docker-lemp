# docker-lemp
A docker-compose of LEMP stack, separated on multiple containers.

**L**inux + NGINX(**E**ngine-X) + MariaDB(**M**ySQL fork) + **P**HP7

1. Install Docker Compose.  
https://docs.docker.com/compose/install/  

2. Clone this repository.  
> $ git clone https://github.com/preechaim/docker-lemp.git  

3. Edit `docker-lemp/docker-compose.yml` to assign your MySQL root password and new user  

4. Start server for the first time.  
> $ cd docker-lemp  
> $ docker-compose up -d  

  Test the server by open your web browser to `http://localhost` or `http://YOUR_SERVER_IP`

6. Make the server to auto start at boot. (for Linux)  
  Open crontab file  
> $ crontab -e  

  Add a new line to the file.  
> @reboot cd ~/docker-lemp && /usr/local/bin/docker-compose up -d  

  Save, exit and reboot.  
> $ sudo reboot  
