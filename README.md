This project has a CloudFormation Template which will create a Single VPC with 1 Public and 1 Private Subnet
A sample EC2 instance will be created in the public subnet. The EC2 will be accsible for a small modification on the subnet. This is to prevent unathorized access to EC2 

To deploy all these services we can use aws cli.
If "aws cli" is already configured in your system, please use below command to test the template creation yaml file
aws cloudformation create-stack --stack-name samplestackname --template-body file://Single_VPC_Cloud_Formation.yaml

To delete the stack
aws cloudformation delete-stack --stack-name samplestackname

