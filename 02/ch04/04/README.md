## ex0X 실행 방법 ( AWS에 stack 생성하기 )

### ex03.json 
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/aws-bitacademy/aws-practices/main/02/ch04/04/ex03.json --parameters ParameterKey=KeyName,ParameterValue=mykey ParameterKey=VPC,ParameterValue=vpc-3ca43a57 ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```

### ex04.json 
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/huckjuhwang/aws-practice/main/02/ch04/04/ex04.json --parameters ParameterKey=KeyName,ParameterValue=mykey ParameterKey=VPC,ParameterValue=vpc-3ca43a57 ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```