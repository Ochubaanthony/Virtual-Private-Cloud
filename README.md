# Virtual-Private-Cloud

VPC.    RANGE IS 10.0.0.0/16

AWS REGION IN EUROPE ( N.Virginia REGION)


SUBNET 1			SUBNET 2		SUBNET 3 				INTERNET GATEWAY
USA-EAST-1A			USA-EAST-1B		USA-EAST-1C

10.0.1.0/24			10.0.2.0/24		10.0.3.0/24

STEP 1 TO CREATE VPC
Search
Name tag - Three_tire
IPv4 CIDR  should be this range = 10.0.0.0/16.   And should be in Private Network only
Click on create  vpc


STEP 2
AFTER CREATE THE VPC > Click on Actions > Edith VPC Settings
Make sure you enable DNS hostnames
SAVE
Note if you did not do it no public access


STEPS 3
SUBNET
CREATE A SUBNTE FOR THE VPC YOU CREATED
Click on Create a subnet
Select from the drop-down the vpc create (three_tire)
Create a tag “name” Called it “App_Servers”
Availability Zone is  selected from the drop-down USA-EAST-1A
IPv4 VPC CIDR block 10.0.0.0/16
IPv4 subnet CIDR block is 10.0.1.0/24
Click on create subnet

REPEAT AGAIN
CREATE A SUBNTE FOR THE VPC YOU CREATED
Click on Create a subnet
Select from the drop-down the vpc create (three_tire)
Create a tag “name” Called it “Web_Servers”
Availability Zone is  selected from the drop-down USA--EAST-1B
IPv4 VPC CIDR block 10.0.0.0/16
IPv4 subnet CIDR block is 10.0.2.0/24
Click on create subnet

REPEAT AGAIN
CREATE A SUBNTE FOR THE VPC YOU CREATED
Click on Create a subnet
Select from the drop-down the vpc create (three_tire)
Create a tag “name” Called it “DB_Servers”
Availability Zone is  selected from the drop-down USA--EAST-1C
IPv4 VPC CIDR block 10.0.0.0/16
IPv4 subnet CIDR block is 10.0.3.0/24
Click on create subnet



STEP 4
INTERNET GATEWAY

Create internet Gateway
Create tag name “Three_tire_IGW
Click on create internet gateway

ONCE IT CREATE THE YOU HAVE TO 
Click on Actions
Click on Attach to VPC
Select from drop-down the attach gateway

STEP 5
ROUTE TABLES

Create route tables
Create a tag name “Three_tire_RT”
Select from VPC Drop-down “three_tire”
Click on create route table
Click on edit routes
Click on Add route  enter 0.0.0.0/0 
From the drop down select the internet gateway 
This pop-up the Internet Gatewat(three_tire_IGW)
Click Add Save changes

ONCE THIS ARE DONE
CLICK ON Subnet Associations
Click on edit subnet associations
Click all the 3 subnet and save associations 






