+ <b>Author: Moole Muralidhara Reddy</b></br>
+ <b>Email:</b> telugudevopsguru@gmail.com</br>
+ <b>Website:</b> https://www.telugudevopsguru.com/</br>
+ <b>Mobile:</b>+91 7893121036</br>
+ <b>Description:</b>Setting up Customized VPC</br>

# Setting up Customized VPC.
![AWS Networking Workshop](https://github.com/telugudevopsguru/AWS-Networking-5-Days-Practical-Live-Workshop/blob/224a00b890f1b0d1cd8fd61b56a8f52362a37a1c/_Learn%20AWS%20Networking%20from%20Scratch%20in%20Telugu%20-%20Moole%20Muralidhara%20Reddy.pptx.png)

## Step 1: Create the AWS VPC
```xml
Name: Murali-VPC in US East (N. Virginia) us-east-1
CIDR : 10.100.0.0/16
```
## Step 2: Create a 2 public subnets with
```xml
CIDR :10.100.8.0/21
Name: murali-public-subnet-1a

CIDR :10.100.16.0/21
Name: murali-public-subnet-1b

```
## Step 3: Create a 2 private subnets with
```xml
CIDR :10.100.80.0/21
Name: murali-private-subnet-1a

CIDR :10.100.88.0/21
Name: murali-private-subnet-1b

```

## Step 4: Create a 2 app subnets with
```xml
CIDR :10.100.144.0/21
Name: murali-private-subnet-1a

CIDR :10.100.162.0/21
Name: murali-private-subnet-1b

```
## Step 4: Create a 2 data subnets with
```xml
CIDR :10.100.168.0/21
Name: murali-private-subnet-1a

CIDR :10.100.176.0/21
Name: murali-private-subnet-1b

```

## Step 5: Create an internet gateway and attach to Murali-VPC
```xml
Name: Murali-VPC-IGW
```
## Step 6: Create a route table and name it Murali-VPC-Public-RouteTable and attach the public subnets to this RouteTable.
```xml
Name: Murali-VPC-Public-RouteTable
```

## Step 7: Create a route table and name it Murali-VPC-Private-RouteTable and attach the private,app,data subnets to this RouteTable.

```xml
Name: Murali-VPC-Private-RouteTable
```

## Step 8: Add the Internet Gateway route to the Public RouteTable.

```xml
Route Entry

Destination : 0.0.0.0/0
Target : Internet Gateway ID
```

## Step 9: Launch the Linux EC2 instance in the Public Subnet.
## Step 10: Connect to the Linux EC2 instance through Putty or SSH command.

#### Congratulations! You have successfully set up the VPC.
