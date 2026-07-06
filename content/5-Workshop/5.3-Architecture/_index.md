---
title : "Architecture and dependency order"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Architecture

The MedChain AI lab uses the following AWS services:

+ **CloudFront** to publish the website and forward `/api/*` requests.
+ **S3** to host frontend files and store medical documents.
+ **API Gateway** to expose backend APIs.
+ **Lambda** to run backend business logic.
+ **DynamoDB** to store application data.
+ **Cognito** to authenticate users and separate roles.
+ **Secrets Manager** to store integration configuration.
+ **Amazon Managed Blockchain Ethereum** to write real blockchain ledger proofs.
+ **CloudWatch** to monitor logs, metrics and errors.
+
+ **VNPay Sandbox** as the external payment gateway.

Users access the system through the CloudFront distribution domain.

![Sơ đồ kiến trúc](/images/5-Workshop/5.3-Architecture/architecture-0.png)

![Sơ đồ kiến trúc](/images/5-Workshop/5.3-Architecture/architecture-1.png)

#### Dependency order

The correct order is important because some resources depend on outputs from previous steps.

1. AWS account, budget, region and local profile.
2. CDK bootstrap resources.
3. VNPay Sandbox credentials.
4. AMB Ethereum node.
5. Secrets Manager configuration and environment variables.
6. CDK application stack.
7. DynamoDB, S3, Cognito, Lambda, API Gateway and CloudFront.
8. Dataset seed.
9. Frontend build and upload to S3.
10. CloudFront invalidation.
11. VNPay IPN and Return URL using CloudFront domain.
12. End-to-end testing and monitoring.
13. Cleanup in reverse order.

