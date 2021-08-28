## ch05. 시스템 보안

### 01. 보안 책임
### 02. 소프트웨어 업데이트
### 03. IAM: AWS 계정 보안

#### 보안 = 인증( Authentication, Identity )            +   권한 ( Authorization, Access )
####       password, access key
####       계정(root) ,  사용자,   역할(자원)               정책(정책은 인증들 한테 정책을 부여한다.)
####                     그룹


### 04. 트레픽 제어 (3:23)
#### -> 네트워크와 네트워크 사이의 트래픽을 제어하는 것

### 05. VPC: 가상 사설 클라우드(네트워크)

### ex05.json 실행 방법
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/huckjuhwang/aws-practice/main/02/ch05/03/ex05.json --parameters ParameterKey=KeyName,ParameterValue=mykey ParameterKey=VPC,ParameterValue=vpc-3ca43a57 ParameterKey=InstanceType,ParameterValue=t2.micro --capabilities CAPABILITY_NAMED_IAM

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```