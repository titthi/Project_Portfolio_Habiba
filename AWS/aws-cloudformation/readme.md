# Create core AWS infrastructure

- VPC
- 2 subnets in 2 different AZs
- Internet Gateway (IGW)
- route tables

Command:

```bash
aws cloudformation create-stack --capabilities CAPABILITY_IAM --stack-name ecs-core-infrastructure --template-body file://./core-infrastructure-setup.yml
```


# Create ECS cluster based on EC2

Command to apply the CloudFormation template

Launchtype _EC2_:  

```bash
aws cloudformation create-stack --stack-name ecs-type-ec2 --capabilities CAPABILITY_IAM --template-body file://./ecs-ec2-with-cf.yml
```
