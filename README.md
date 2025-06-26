# EC2-based-Web-Server - Configure Apache on an EC2 instance

In this project,you will deploy a webserver using Amazon EC2.You will launch an EC2 instance,install Apache and configure it to serve a basic website

Steps to Setup an EC2-based WebServer

# Step1:Launch an EC2 Instance

1.Go to the AWS Management Console-->EC2

2.Click Launch Instance

3.Configure the instance:

    Name:Mywebserver
    
    AMI:Choose Ubuntu
    
    Instance Type:t2.micro
    
    Key Pair:Create a new key pair or use an existing one
    
    Security Group:Allow SSH(port22) and HTTP(port 80)
    
4.Click Launch
# Step2:Connect to the EC2 Instance

Open a terminal and run:

ssh -i your-key.pem ec2-user@your-instance-public-ip

# Step3:Install Apache

For Apache
Update the package repository:
sudo apt update -y

Install Apache:
sudo apt install apache2 -y

Start and enable Apache:
sudo systemctl start apache2
sudo systemcl enable apache2

Verify Installation:
sudo systemctl status apache2

# Step4:Deploy a WebPage

Edit the default index file:

sudo echo "<h1>Welcome to My Web Server</h1>"> /var/www/html/html/index.html

# Step5:Access the Web Server

Open a browser and go to:
http://instanceip

You should be able to see "Welcome to My WebServer"

# Conclusion:

Successfully deployed an EC2-based webserver running Apache.This setup is commonly used for hosting websites,web applications,or acting as a reverse proxy.

