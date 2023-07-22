+ <b>Author: Moole Muralidhara Reddy</b></br>
+ <b>Email:</b> telugudevopsguru@gmail.com</br>
+ <b>Website:</b> https://www.telugudevopsguru.com/</br>
+ <b>Description:</b>Setting  Up AWS Site to Site VPN Connection</br>


# Setting Up AWS Site-to-Site VPN Connection:

You can follow the steps below to set up the AWS Site-to-Site VPN Connection.

##  Step 1: Launch the AWS EC2 instance for installing OpenSwan.
```xml
Name: OpenSwan-Server
```
### Install the openswan in AWs EC2 instance using below command
```xml
yum install openswan -y
ipsec --version
```
## Step 2: Create the AWS Customer Gateway.
```xml
Name: telugudevopsguru-CGW
```
## Step 3: Create the Virtual Private Gateway and attach it to the VPC.
```xml
Name: Murali-VPG
```
## Step 4: Create the Site-to-Site VPN Connection.
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

## Step 5: Download the Configuration of the Site-to-Site VPN Connection and configure it in OpenSwan.

## Step 6: Launch AWS EC2 instances in both VPCs.

## Step 7: Test the connection between the AWS VPC and the On-Premises VPC.

### Congratulations! You have successfully set up the AWS Site-to-Site VPN Connection.
