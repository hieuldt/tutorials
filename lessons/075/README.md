# AWS SAM

[YouTube Tutorial]()

## 1. Install AWS SAM CLI
- [Instructions](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)
### macOS
```
brew tap aws/tap
```
```
brew install aws-sam-cli
```
```
sam --version
```

## 2. Setting up AWS credentials

- Create `admin` user for AWS SAM
- Download Credentials
- Configure AWS Cli
```
aws configure
```

## 3. Create AWS Lambda API Gateway Node JS
- Initialize SAM project
```
sam init
```
- Go over project structure
- Remove generated project
```
rm -rf sam
```
- Created directory
```
mkdir sam
```
- Change directory to `sam`
```
cd sam
```

## 4. Test Lambda Locally SAM
## 5. Test Lambda from Console
## Create AWS Lambda S3 File Upload NodeJS
## Create AWS Lambda SNS Python Example

sam local invoke
sam local invoke HelloFunction -e events/event.json

curl -d '{"name": "Anton"}' https://hzfn3mfbt3.execute-api.us-east-1.amazonaws.com/Prod/hello/

https://github.com/aws/serverless-application-model/issues/124

aws sns create-topic --name sns-topic-for-lambda

aws sns publish --message file://message.txt --subject Test \
--topic-arn arn:aws:sns:us-east-2:12345678901A:sns-topic-for-lambda \
--profile accountA


## Clen Up

 - Delete SNS topic `sns-topic-for-lambda`
 - Delete ECR repository `sns`
 - Delete all cloud watch log groups
 - Delete IAM User `aputra`
 - Delete AWS CLI `sam`
 ```
 brew remove aws-sam-cli
 ```
 - Delete all S3 buckets
 - Delete all CloudFormation Templates
