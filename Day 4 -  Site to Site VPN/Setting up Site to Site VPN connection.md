+ <b>Author: Moole Muralidhara Reddy</b></br>
+ <b>Email:</b> telugudevopsguru@gmail.com</br>
+ <b>Website:</b> https://www.telugudevopsguru.com/</br>
+ <b>Mobile:</b>+91 7893121036</br>
+ <b>Description:</b>Setting  Up AWS Site to Site VPN Connection</br>


# Setting Up AWS Site-to-Site VPN Connection:

You can follow the steps below to set up the AWS Site-to-Site VPN Connection.
## CIDR details for AWS and On-Premises.
```xml
AWS VPC CIDR : - 10.0.0.0/16
On-Premises VPC CIDR : - 192.168.0.0/16
```
##  Step 1: Launch the AWS EC2 instance for installing OpenSwan in On-Premises VPC.
```xml
Name: OpenSwan-Server
```
### Install the openswan in AWs EC2 instance using below command
```xml
yum install openswan -y
ipsec --version
```
## Step 2: Create the AWS Customer Gateway in AWS Side.
```xml
Name: telugudevopsguru-CGW
```
## Step 3: Create the Virtual Private Gateway and attach it to the VPC in AWS Side.
```xml
Name: Murali-VPG
```
## Step 4: Create the Site-to-Site VPN Connection in AWS Side.
```xml
Name: Murali-to-telugudevopsguru-site-to-site
```
### Static IP prefixes:
```xml
AWS CIDR - 10.0.0.0/16
On-Premises - 192.168.0.0/16
```
```xml
Local IPv4 network CIDR - 192.168.0.0/16 (On-Premises)
Remote IPv4 network CIDR - 10.0.0.0/16 (AWS CIDR)
```
## Step 5: Add the route table preparation for the Virtual Private Gateway in AWs Side.

## Step 6: Download the Configuration of the Site-to-Site VPN Connection and configure it in OpenSwan Server.
## Step 7: Add the OpenSwan instance id  route to the Public RouteTable.
```xml
Route Entry

Destination : 10.0.0.0/16
Target : OpenSwan instance ID
```
## Step 8: Launch AWS EC2 instances in both VPCs(AWS VPC and the On-Premises VPC.).

## Step 9: Test the connection between the AWS VPC and the On-Premises VPC.

### Congratulations! You have successfully set up the AWS Site-to-Site VPN Connection.
