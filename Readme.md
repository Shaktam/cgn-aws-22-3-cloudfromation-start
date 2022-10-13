## Cloudformation start

Set your credntials to setup your cli

Simple start template:
```
AWSTemplateFormatVersion: "2010-09-09"
Description: Vpc Stack
Resources:
  myVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/16
      Tags:
        - Key: Name
          Value: My Vpc
```

Create a new Stack:
```
aws cloudformation create-stack --stack-name vpcstack --template-body file://template.yml
```

Update a stack
```
aws cloudformation update-stack --stack-name vpcstack --template-body file://template.yml
```