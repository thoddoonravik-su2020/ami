# AMI

Creating an AMI using Hashicorp Packer
Circle CI Environment Variables

ami_users
aws_access_key
aws_region
aws_secret_key
source_ami
ssh_username
subnet_id

# 1 To Generate Ami locally:-

=> Packer Template name : ami.json

"aws_region": "Region where the AMI would be created",
"aws_access_key": "AWS Access key of user",
"aws_secret_key": "AWS Secret key of user",
"subnet_id": "Leave it blank for default VPC else provide the id",
"source_ami": "Source AMI as base",
"ami_users": "User if with whom this new AMI will be shared"

=> Validate the Packer using the command :- 
./packer validate ami.json

=> Output - AMI image is created.

# 2 To Generate Ami using circleci:-

=> Validate the packer with the above steps and push the code in git hub and raise a pull request. 
=> All the pre-requisite applications in the EC2 instance should already be mentioned in the ami.json file as commands.
=> Using the confif.yml file the ami is generated automatically
=> Connect to the application using server ip address