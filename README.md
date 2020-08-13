# packer-cis-hardened-centos8
This repository illustrates one workflow for creating a hardened CentOS 8 AMI using Packer and Ansible.


## CI Pipeline

We are using CircleCI.  The config can be found in .circleci/config.yml.

### CircleCI Environment variables

| variable  | type  | description |
| --- | --- | --- |
| AWS_ACCESS_KEY_ID | string | Access Key for the AWS Account you wish to deploy the AMI to. |
| AWS_SECRET_ACCESS_KEY | string  | Secret Access Key for the AWS Account you wish to deploy the AMI to.|
| BUILD_VPC_ID | string | The VPC to build the temp EC2 instance |
| BUILD_SUBNET_ID | string | The Subnet to build the temp EC2 instance  |
| AWS_REGION | string | The AWS region to build the temp EC2 instance  |

## Other reading and inspirations

* We borrowed lightly in some places and heavily in others from these projects:
  * https://github.com/awslabs/ami-builder-packer
  * https://circleci.com/orbs/registry/orb/salaxander/packer
