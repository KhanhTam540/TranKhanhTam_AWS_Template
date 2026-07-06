---
title : "Táº¡o vÃ  kiá»ƒm tra data, auth, API resources"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.6.2. </b> "
---

#### Má»¥c tiÃªu

Kiá»ƒm tra stack Ä‘Ã£ táº¡o DynamoDB, S3, Cognito, Lambda vÃ  API Gateway.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **DynamoDB** vÃ  kiá»ƒm tra table.
2. Má»Ÿ **S3** vÃ  kiá»ƒm tra buckets.
3. Má»Ÿ **Cognito** vÃ  kiá»ƒm tra user pool/groups.
4. Má»Ÿ **Lambda** vÃ  **API Gateway** Ä‘á»ƒ kiá»ƒm tra APIs.

![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/dynamodb.png)
![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/s3.png)
![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/cognito.png)
![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/cognito_1.png)
![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/lambda.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
aws cloudformation describe-stacks `
  --stack-name $StackName `
  --region $Region `
  --profile $Profile `
  --query "Stacks[0].Outputs[*].[OutputKey,OutputValue]" `
  --output table
```

#### Kiá»ƒm tra

Outputs cáº§n cÃ³ API endpoint, CloudFront domain, bucket names, table name vÃ  user pool ID.

![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/code.png)

