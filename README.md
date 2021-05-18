# Setup AWS EC2 servers through Terraform
The script can be used to get create EC2 servers along with VPC, Subnets in AWS Cloud

## Requirements
Install terraform

## Steps

1. Create a copy of vars file inside env folder with name equals to the environment name

2. Now run the `deploy.sh` with appropriate command and the env name
    
    `deploy.sh create dev`
    
    `P.S: There should be dev.tfvars files available inside the env folder`

## Commands
A list of commands available:

1. `create` : This will create and configure a new EC2 servers along with VPC, subnets in AWS Cloud 
`example: ./deploy.sh create dev`

2. `update` : This will update the EC2 servers or subnet changes
`example: ./deploy.sh update dev`

## Tfvars Arguments:
Following arguments are available:

key_name (required): Name of the pem key file to use for instances

vpc_cidr (required): CIDR range need to specify to create vpc

environment (required): Name of the env where you are launching.

public_subnets_cidr (required): CIDR range need to specify to create public subnet

private_subnets_cidr (required): CIDR range need to specify to create private subnet

availability_zones (required): Avaibility zone to create subnet in specific zone. e.g us-east-1c

bucket(required): Name of s3 bucket to store the state

key(required): Name of the folder/state file. Example: terraform/tfstate
