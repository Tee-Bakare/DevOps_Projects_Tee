# Introduction to LoadBalancing and Nginx

Load balancing refers to efficiently distributing incoming network traffic across a group of backend servers, also known as a server farm or server pool.

Nginx, a popular web server software, can be configured as a simple yet powerful load balancer to improve your server's resource availability and efficiency. Nginx acts as a single entry point to a distributed web application working on multiple separate servers.

## Setting Up a Basic Load Balancer Using Ec2

### Step 1 - Launch EC2 instances with an Ubuntu AMI and use User Data to install the Apache Web Server.

Log in to your AWS Console and go to the EC2 dashboard.

Click on the “Launch Instance” button and select “Ubuntu Server “.

Refer to image:

![instance_launch](./img/01.instance_launch.png)


### Step 2 - Inboud Rule to Port 8000

Open port 8000. Server will run on port 8000 while load balancer will run on 80. To do this we add a rule to security group allowing traffic from anywhere. 

Refer to image:

![inbound_rule](./img/02.inbound_rule.png)

### Step 3 - Apache Webserver Installation

After opening necessary ports, we connect to webser and input command `sudo apt update -y &&  sudo apt install apache2 -y`, to install apache.

Refer to image:

![apache_installation](./img/03.apache_installation.png)

- Then verify apache is running by command `sudo systemctl status apache2`.

Refer to image:

![system_status](./img/04.system_status.png)

### Step 4 - Configure Apache to Server a Page Showing Public IP

We start by configuring Apache webser to serve content on port 8000. Then we create a new `index.html` file. Then override apache webserver's default html with new file.

- Using vi editor we opened file: `sudo vi /etc/apache2/ports.conf`, added a new `Listen` directive for port `8000`, then save.

Refer to image:

![port_8000](./img/05.port_8000.png)

- Next we opened file with command `sudo vi /etc/apache2/sites-available/000-default.conf`, change virtual host port 80 to 8000. Then restarted apache.

Refer to image:

![etc_apache_port80_to_port8000](./img/06.etc_apache_port80_to_port8000.png)



- Next we opened a new `index.html` file with command `sudo vi index.html`. Then pasted a placeholder text for IP address in html file.

Refer to image:

![index_code](./img/07.index_code.png)

- Overriding the default html file of Apache Webserver, we used command `sudo cp -f ./index.html /var/www/html/index.html` to replace it, then restarted webserver.


Refer to image:

![Override_default_html_file](./img/08.Override_default_html_file.png)

### RESULT:

![Welcome_to_EC2](./img/09.Welcome_to_EC2.png)


### Step 4 - Cofiguring Nginx as a Load Balancer

- Lunched a new EC2 instance to run on port 80.

Refer to image:

![New_Ec2_Instance](./img/10.New_Ec2_Instance.png)

![Port80_on_New-Instance](./img/11.Port80_on_New-Instance.png)


- Connect to webserver, install nginx, then verify status to check if running.

Refer to image:

![install_nginx_on_new_instance](./img/12.install_nginx_on_new_instance.png)

![system_status_nginx](./img/13.system_status_nginx.png)

- Opened Nginx configuration file with command `sudo vi /etc/nginx/conf.d/loadbalancer.conf`, then pasted configuration file edit and saved.

Refer to image:

![nginx_configuration](./img/14.nginx_configuration.png)

- Test configuration with `sudo nginx -t` 

![webserver2](./img/15.testing_configuration.png)


### RESULT:

![webserver2](./img/16.webserver2.png)



















