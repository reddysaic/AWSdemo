README

Following things are required to be done.

1. Run this shell script from any Linux server which has access to internet

2. Run aws configure to connect to appropriate AWS account with role having permission to create resources on AWS

3. Ensure jq utility is installed, if not installed, please run yum -y install jq


Post above pre requ

Execute ./creatInfra.sh

IT will 
 - create the VPC
 - subnet in different regions
 - security group with access on port 22 and 80
 - create keypair
 - create couple of EC2 webservers in each subnet and region
 - Install Apache and start the service
 - Create the ELB 
 - Configure ELB by creating target group, listener and registering targets
 - Create RDS DB with some default settings


Entire automation is done using AWS CLI 

Please note, you need to enter yes, when asked by script, its used for first time connection to newly created EC2 instances.

This script is working fine, test and giving expected results.