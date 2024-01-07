# php-mysql-integration-ci-cd

Prerequiste :

1. AWS Acccount
2. IAM user with credentails
3. Idea about tools like git, jenkins, docker, DOckerhub.. etc
4. I'm using the Ubuntu server for this Project

# Refernece link : https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Tutorials.WebServerDB.CreateWebServer.html


# Steps :

1. Launch the Instance and install the required packages for the application
# commands
1. sudo su -
2. sudo apt install apache2-y
3. sudo apt update -y
4. sudo apt install php libapache2-mod-php php-mysql

# To check the connectiviy to RDS and Ec2 by installing the msql-client and fetech the db details
sudo apt install mysql-client

 mysql -u admin -h database-1.cey1degenukn.us-east-1.rds.amazonaws.com -p

 # Security Groups

- If your using the RDS out of vpc , you can provide with  custom level Range (Ex: 3306  port with instance level CIDR)
- Instance level SSH, HTTPS and HTTP must be enabled

# FYI 

code commit - Git/Github
code Build  - Jenkins 
code Deploy - Ansibel/Chef
code pipleine - jenkins pipeline
ECR - Docker     .. etc




- 
