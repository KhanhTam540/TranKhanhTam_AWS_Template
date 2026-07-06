---
title : "Äiá»u kiá»‡n chuáº©n bá»‹"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

#### Äiá»u kiá»‡n chuáº©n bá»‹

TrÆ°á»›c khi báº¯t Ä‘áº§u bÃ i lab, cáº§n chuáº©n bá»‹:

+ AWS account cÃ³ quyá»n billing.
+ AWS CLI Ä‘Ã£ cáº¥u hÃ¬nh trÃªn mÃ¡y local.
+ Node.js vÃ  npm.
+ AWS CDK CLI.
+ Git vÃ  PowerShell.
+ ThÃ´ng tin merchant VNPay Sandbox.
+ Quyá»n táº¡o Amazon Managed Blockchain Ethereum node.

Website vÃ  callback backend sáº½ dÃ¹ng CloudFront distribution domain.

#### Kiá»ƒm tra cÃ´ng cá»¥ local

```powershell
node --version
npm --version
aws --version
git --version
```

![CÃ´ng cá»¥ local](/TranKhanhTam_AWS_Template/images/5-Workshop/5.2-Prerequisites/local.png)

#### Ghi chÃº quyá»n IAM

Gáº¯n deploy policy vÃ o IAM user hoáº·c role dÃ¹ng Ä‘á»ƒ cháº¡y lab. Vá»›i bÃ i lab sinh viÃªn, deployer cáº§n quyá»n cho CloudFormation, S3, DynamoDB, Lambda, API Gateway, Cognito, CloudFront, Secrets Manager, CloudWatch, Managed Blockchain vÃ  IAM PassRole.

#### Táº¡o workspace lab má»›i

KhÃ´ng cháº¡y pháº§n command deployment trá»±c tiáº¿p trong project chÃ­nh. HÃ£y táº¡o thÆ° má»¥c riÃªng Ä‘á»ƒ cháº¡y lá»‡nh, chá»¥p hÃ¬nh vÃ  lÆ°u báº±ng chá»©ng.

```powershell
$LabRoot = "D:\AWS\LabRuns\MedChainAI-CommandRun"
New-Item -ItemType Directory -Path $LabRoot -Force | Out-Null
cd $LabRoot
```

![Region vÃ  budget AWS](/TranKhanhTam_AWS_Template/images/5-Workshop/5.2-Prerequisites/aws_region.png)
![Region vÃ  budget AWS](/TranKhanhTam_AWS_Template/images/5-Workshop/5.2-Prerequisites/iam.png)
![Region vÃ  budget AWS](/TranKhanhTam_AWS_Template/images/5-Workshop/5.2-Prerequisites/pttt.png)

