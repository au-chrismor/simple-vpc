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

