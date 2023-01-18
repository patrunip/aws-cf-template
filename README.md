Welcome to VPC-EC2-Subnet Template Project.

Background:
This project has a reusable Cloudformation temlate. The template will create Singular VPC.
A public and private subnets will be created and A sample EC2 instance will be created in the public subnet. 
The EC2 will be accesible for a small modification on the subnet. This is to prevent unauthorized access to EC2 
A high level diagram for the architecture of this template is shown below.

This template is specifically useful when we want to create a quick EC2 instance a VPC configured with private and public subnet. 


![image](https://user-images.githubusercontent.com/46040062/211612100-e0ba5cec-4f2a-4fd9-8ea7-c31056d0fcb9.png)



To deploy all these services we can use both cli and AWS Console. 
From a best practices perspective, it is adivsable to use cli command with a specific user created for the same.
This will help us in limiting the actions the user can take on a specific environment.

Step-1: Install "aws cli". Very easy to install and make it up and running

Step-2: Configure AWS in your system by using the access key id and secret access key

Step-3: Please use below command to test the template creation yaml file

        aws cloudformation create-stack --stack-name samplestackname --template-body file://Single_VPC_Cloud_Formation.yaml

Step-4: Once the creation is successful, you will get respond with the stack id

Step-5: To delete the stack, please use the below command

        aws cloudformation delete-stack --stack-name samplestackname


Using this script you can always quickly spin up VPC, EC2 istances for testing out any simple applications.

