# Serverless_CICD_Pipelines
A fully serverless CI/CD pipeline on AWS that automates build, test, and deployment with CodePipeline, CodeBuild, Lambda, and API Gateway.
## Overview

This project demonstrates a fully automated Serverless CI/CD Pipeline using AWS services. The pipeline automates the build, test, and deployment process for AWS Lambda functions, enabling faster and more reliable releases.

## Architecture

GitHub Repository → AWS CodePipeline → AWS CodeBuild → AWS Lambda → API Gateway → CloudWatch

## Services Used

* AWS CodePipeline
* AWS CodeBuild
* AWS Lambda
* Amazon API Gateway
* Amazon CloudWatch
* AWS IAM
* GitHub

## Features

* Automated CI/CD pipeline for serverless applications
* Continuous integration using AWS CodeBuild
* Automated deployment to AWS Lambda
* API exposure through API Gateway
* Monitoring and logging with CloudWatch
* Infrastructure managed through AWS services

## Project Workflow

1. Developer pushes code to GitHub.
2. CodePipeline detects changes automatically.
3. CodeBuild builds and validates the application.
4. Lambda function is deployed automatically.
5. API Gateway exposes the Lambda endpoint.
6. CloudWatch collects logs and monitoring metrics.

## Prerequisites

* AWS Account
* GitHub Repository
* IAM Roles with required permissions
* AWS CLI configured
* Lambda Function
* API Gateway Endpoint

## Deployment Steps

### Clone Repository

```bash
git clone https://github.com/your-username/serverless-cicd-pipeline.git
cd serverless-cicd-pipeline
```

### Push Code

```bash
git add .
git commit -m "Initial Commit"
git push origin main
```

### Pipeline Execution

* CodePipeline automatically triggers on code changes.
* CodeBuild executes buildspec.yml.
* Lambda function gets updated.
* API Gateway serves the latest version.

## Monitoring

CloudWatch provides:

* Function execution logs
* Error tracking
* Performance metrics
* Pipeline monitoring

## Project Structure

```text
serverless-cicd-pipeline/
│
├── lambda_function.py
├── buildspec.yml
├── template.yaml
├── README.md
└── screenshots/
```

## Sample BuildSpec

```yaml
version: 0.2

phases:
  build:
    commands:
      - echo "Building Lambda Package"

artifacts:
  files:
    - '**/*'
```

## Benefits

* Faster deployments
* Reduced manual effort
* Improved reliability
* Scalable serverless architecture
* Continuous monitoring

## Author

Adhithya Sidharthan

## License

This project is for learning and demonstration purposes.
