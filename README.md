# Christophineonyi_lita-project
This project documents how I launched an EC2 instance with Apache web server
Amazon EC2 instance is a web service that provides scalable computecapacity in the cloud
### creation of security group
#### I navigated the side bar of the AWS console to locate the security group and clicked on the create security as seen in the image below
![security bar](/CreatingSG_1.png)
#### I put in my basic details with a name I can easily locate and description of the security group I am creating then I used the VPC created for the project 
![basic details](/CreatingSG_2.png)
#### I set my inbound rule which allows SSH port 22 using the IPv4 which allows you to remotely access your instance using an SSH client and also allows HTTP port 80 traffic using IPv4 which allows users to access the web server through the internet
![inbound rule](/CreatingSG_3.png)
#### I reviewed my security group setting and succesfully created my security group as seen below
![security group](/CreatingSG_4.png)

