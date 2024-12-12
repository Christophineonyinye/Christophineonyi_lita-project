# Christophineonyi_lita-project
### This project documents how I launched an EC2 instance with Apache web server
###  Amazon EC2 instance is a web service that provides scalable compute capacity in the cloud

## Creation of security group
### I created my security group to protect my instance from unauthorized access and to prevent unwanted traffic from entering or leaving my instance

I navigated the side bar of the AWS console to locate the security group and clicked on the create security as seen in the image below
![security bar](/CreatingSG_1.png)

 I put in my basic details with a name I can easily locate and description of the security group I am creating then I used the VPC created for the project 
![basic details](/CreatingSG_2.png)

I set my inbound rule which allows SSH port 22 using the IPv4 which allows you to remotely access your instance using an SSH client and also allows HTTP port 80 traffic using IPv4 which allows users to access the web server through the internet

![inbound rule](/CreatingSG_3.png)

I reviewed my security group setting and succesfully created my security group as seen below

![security group](/CreatingSG_4.png)


## Creation of keypair
### I created my keypair so that I can easily connect to my instance using SSH and also to ensure a secure connection between my local machine and my instance and to keep it encrypted

I navigated the side bar of the AWS console to locate the keypair and clicked on the create keypair as seen in the image below

![creatingkeypair](/CreatingKP_1.png)

I named the key pair and used the used the default keypair type and I selected the pem which is used in open SSH so that I can easily connect to my instance using my private key 
![creatingkeypair](/CreatingKP_2.png)

I reviewed my key pair setting and succesfully created my keypair as seen below

![creatingkeypair](/CreatingKP_3.png)


## launching my EC2 instance
I navigated the side bar of the AWS console to locate the instance and clicked on the launch instance as seen in the image below

![launchinginstance](/Launchinginstance_1.png)

I named my instance and I selected Amazon linux 2 kernel which is a popular choice for webservers eg apachhe webservers. it is also secure and cost effective and can easily be deployed on an EC2 instance

![launchinginstance](/Launchinginstance_2.png)
![launchinginstance](/Launchinginstance_3.png)

I selected the t2 micro instance type because it is cost effective and suitable for small scale applications and development environment and it is scalable
  
I selected the keypair I created

![launchinginstance](/Launchinginstance_4.png)

I edited my security group by selecting the vpc created for the project

I put my subnet in the public subnet

I enabled auto assign public IP

I selected the security group I created

![launchinginstance](/Launchinginstance_5.png)
![launchinginstance](/Launchinginstance_6.png)

I reviewed my instance configurations and i launched my instance successfully. I allowed the instance to successfully pass the status check

![launchinginstance](/Launchinginstance_7.png)
![launchinginstance](/Launchinginstance_8.png)


## Installing apache web server

After i successfully launched my instance, I connected to it so as to install my apache web server using my SSH client

I opened my gitbash terminal on the part of my file where my keypair was downloaded

I Used the following codes to get the updated version of the amazon linux and to install my apache web server I went further to start apache and to enable it to start automatically on boot

sudo yum update -y

sudo yum install httpd -y

sudo systemctl start httpd

sudo systemctl enable httpd

### These images shows how I successfully installed my Apache web server using my EC2 instance
![Installingwebserver](/Apacheweb_1.png)
![Installingwebserver](/Apacheweb_2.png)
![Installingwebserver](/Apacheweb_3.png)

### Confirmation of apache installation
I copied my public IP address from my instance and pasted it on my microsoft browser to confirm if my apache was running 

The image below confirms i successfully installed my apache web server

![Installingwebserver](/Apacheweb_4.png)











