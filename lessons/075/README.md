# AWS SAM

[YouTube Tutorial]()

## 1. Install AWS SAM CLI
- [Instructions](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)

## 2. Setting up AWS credentials

- Create Admin user for AWS SAM
- Download Credentials
- Configure AWS Cli
```
aws configure
```

## 3. Create a sample app
- Created directory
```
mkdir ping-pong
```
- Change directory to `ping-pong`
```
cd ping-pong
```
- Initialize SAM project
```
sam iniit
```
- Select `1 - AWS Quick Start Templates`
- Select `2 - Image (artifact is an image uploaded to an ECR image repository)`
- Select `1 - amazon/nodejs14.x-base`
- Project name [sam-app]: `service-1`

- Change directory to service-1
```
cd service-1
```

- Build App
```
sam build
```
- Create ECR repository `service-1`
- Deploy
```
sam deploy --guided
```
- Stack Name [sam-app]: service-1
- AWS Region [us-east-1]:
- Image Repository for HelloWorldFunction: 424432388155.dkr.ecr.us-east-1.amazonaws.com/service-1
- Confirm changes before deploy [y/N]: y
- Allow SAM CLI IAM role creation [Y/n]: y
- HelloWorldFunction may not have authorization defined, Is this okay? [y/N]: y
- Save arguments to configuration file [Y/n]: y
- SAM configuration file [samconfig.toml]:
- SAM configuration environment [default]:

- Deploy this changeset? [y/N]: y

- Access Lambda
```
curl https://<id>.execute-api.us-east-1.amazonaws.com/Prod/hello/
```
> {"message":"hello world"}

