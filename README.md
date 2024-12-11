# Christophineonyi_lita-project
This project documents how I launched an EC2 instance with Apache web server
Amazon EC2 instance is a web service that provides scalable computecapacity in the cloud
## Creation of security group
### I created my security group to protect my instance from unauthorized access and to prevent unwanted traffic from entering or leaving my instance
#### I navigated the side bar of the AWS console to locate the security group and clicked on the create security as seen in the image below
![security bar](/CreatingSG_1.png)
#### I put in my basic details with a name I can easily locate and description of the security group I am creating then I used the VPC created for the project 
![basic details](/CreatingSG_2.png)
#### I set my inbound rule which allows SSH port 22 using the IPv4 which allows you to remotely access your instance using an SSH client and also allows HTTP port 80 traffic using IPv4 which allows users to access the web server through the internet
![inbound rule](/CreatingSG_3.png)
#### I reviewed my security group setting and succesfully created my security group as seen below
![security group](/CreatingSG_4.png)
## Creation of keypair
### I created my keypair so that I can easily connect to my instance using SSH and also to ensure a secure connection between my local machine and my instance and to keep it encrypted
#### I navigated the side bar of the AWS console to locate the keypair and clicked on the create keypair as seen in the image below
![creatingkeypair](/CreatingKP_1.png)
#### I named the key pair and used the used the default keypair type and I selected the pem which is used in open SSH so that I can easily connect to my instance using my private key 
![creatingkeypair](/CreatingKP_2.png)
#### I reviewed my key pair setting and succesfully created my keypair as seen below
![creatingkeypair](/CreatingKP_3.png)
