# VPC_CORE

## What it does

vpc_core creates all the essential stuff you need for a three-tier VPC:

* The VPC itself

* Subnets based on site.yml vars

* Basic NACLs

* Internet Gateway and NAT

* Internal Security Group

* Endpoints for CloudFormation, KMS, DynamoDB and S3

* Private Route53 Zone

The CloudFormation is pretty basic, so you can easily enough customise it to suit your exact needs.

## What is the VPC Layout

There are 3 subnet groups (Public, Private and Restricted).
Public is intended for public-facing services, such as web servers and internet-facing load balancers.
Private is intended to host application services
Restricted is intended for more protected services such as databases.

NACLs are used to restrict traffic between these zones as shown:

Public <--> Private <--> Restricted

