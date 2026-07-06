---
title : "Táº¡o CDK bootstrap resources"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3. </b> "
---


#### Má»¥c tiÃªu

Táº¡o CDK bootstrap stack vÃ  artifact bucket trÆ°á»›c khi deploy application stack.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **CloudFormation**.
2. Kiá»ƒm tra `CDKToolkit` Ä‘Ã£ tá»“n táº¡i chÆ°a.
3. Má»Ÿ **S3** vÃ  kiá»ƒm tra CDK asset bucket sau khi bootstrap.

![CDKToolkit console](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.3-cdk-bootstrap/cdk.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$AccountId = aws sts get-caller-identity --profile $Profile --query Account --output text
npm install
npm --prefix web install
npx cdk bootstrap aws://$AccountId/$Region --profile $Profile
```

#### Kiá»ƒm tra

```powershell
aws cloudformation describe-stacks `
  --stack-name CDKToolkit `
  --region $Region `
  --profile $Profile `
  --query "Stacks[0].StackStatus" `
  --output text
```
![CDKToolkit console](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.3-cdk-bootstrap/cdk_1.png)
