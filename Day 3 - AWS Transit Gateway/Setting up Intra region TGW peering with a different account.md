+ <b>Author: Moole Muralidhara Reddy</b></br>
+ <b>Email:</b> telugudevopsguru@gmail.com</br>
+ <b>Website:</b> https://www.telugudevopsguru.com/</br>
+ <b>Description:</b>Setting up Intra region TGW peering with the different AWS account</br>

# Follow the steps below to set up Intra region TGW peering with the different AWS account.

## Step 1: Create the AWS VPC
Name: VPC-A in US East (N. Virginia) us-east-1
CIDR : 10.0.0.0/16

## Step 2: Create a public subnet with
CIDR 10.0.1.0/24
Name: VPC-A-Public-subnet-1a.

## Step 3: Create an internet gateway and attach to VPC-A
Name: VPC-A-IGW.

## Step 4: Create a route table and name it VPC-A-RouteTable and attach the public subnet to this RouteTable.

## Step 5: Create the AWS VPC different account
Name: VPC-B in US East (N. Virginia) us-east-1
CIDR : 192.168.0.0/16

## Step 6: Create a public subnet with
CIDR 192.168.1.0/24
Name: VPC-B-Public-subnet-1a

## Step 7: Create an internet gateway and attach to VPC-B
Name: VPC-B-IGW

## Step 8: Create a route table and name it VPC-B-RouteTable and attach the public subnet to this RouteTable.

## Step 9: Create the TGW

## Step 10: Create the TGW attachments for VPC-A.

## Step 11: Create the TGW route table and associate it with the TGW attachments of VPC-A.

## Step 12: Share the TGW with destination account using AWS RAM.

## Step 13: Accept the TGW in the AWS RAM destination account.

## Step 14: Create the TGW attachments for VPC-B and accept the request in source account

## Step 15: In TGW RouteTable associate it with the TGW attachments of VPC-B in source account.

## Step 16: Update the route tables in both VPCs to allow traffic to the other VPC.

+ In VPC-A route table, add a route for VPC-B's CIDR block to the TGW connection.
+ In VPC-B route table, add a route for VPC-A's CIDR block to the TGW connection.

## Step 17: Launch an EC2 instance in both VPC's public subnets.

## Step 18: Update the Security Group Inbound rules for both instances to allow ICMP traffic.

## Step 19: Test the connectivity between the instances using the ping command.

####  Congratulations, you have successfully set up Intra-region VPC peering with different accounts and tested connectivity between instances in the public subnets of each VPC..

### # Happy Learning
