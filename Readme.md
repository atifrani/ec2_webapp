# Pre-Requisites
You must be having an AWS account to create infrastructure resources on AWS cloud.

# Pre-Deployment

You must have AWS CLI installed and configured on you laptop

# Deployment

Configure NACL allowing port 22 from custom IP source  ( Your IPV4 ) and port 80 from public.

Create Security Group (if not exist) allowing port 22 from custom IP source ( Your IPV4 ) and port 80 from public.

Create Key-Pair (if not exist) and download the private key.

Create t2.micro type EC2 instance using AMI (ami-01cae1550c0adea9c).


Connect to the EC2 instance using ssh and install this packages:
- apache httpd
- GIT

After installation, start the httpd service.

Use Git commands and clone the source code from github repository: https://github.com/atifrani/webapp1.git

Deploy the source code into EC2 instance in the folder: cd /var/www/html

Create S3 bucket with public access.

Check if all bucket objects have public read permission

Copy the images folder to the S3 bucket.

Update the source code to allow acces to the images folder

# Validation

Verify if you are able to access the web application from internet browser. ec2-ipv4/app/index.php
