# A simple AWS VPC Environment

## Background
The best practice in the Amazon AWS world is to *not* use the default VPC and it's associated security groups.  This playbook sets up a clean environment based on a standard 3-tier layout.

## What do you need?
An AWS account with the ability to execute cloudfomation, aws cli tools and ansible installed.

## How do I use it?
Edit site.yml in the root to reflect your desired environment and then run:

ansible-playbook ./site.yml

Execution takes about 5 minutes to complete.

