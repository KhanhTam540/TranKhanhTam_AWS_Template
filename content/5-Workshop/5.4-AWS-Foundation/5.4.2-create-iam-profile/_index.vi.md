---
title : "Táº¡o IAM deployer vÃ  local profile"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.4.2. </b> "
---


#### Má»¥c tiÃªu

Táº¡o deploy identity vÃ  kiá»ƒm tra command line cÃ³ thá»ƒ truy cáº­p AWS.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **IAM**.
2. Táº¡o user hoáº·c role tÃªn `medchain-ai-lab-deployer`.
3. Gáº¯n lab deploy policy.
4. Táº¡o access key náº¿u dÃ¹ng AWS CLI.
5. KhÃ´ng chá»¥p secret access key.

![IAM deployer](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.2-create-iam-profile/iam_1.png)
![IAM deployer](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.2-create-iam-profile/iam_2.png)
![IAM deployer](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.2-create-iam-profile/iam_3.png)
![IAM deployer](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.2-create-iam-profile/iam_4.png)
![IAM deployer](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.2-create-iam-profile/iam_5.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
aws configure --profile hospital-dev
aws sts get-caller-identity --profile hospital-dev
```

![IAM deployer](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.2-create-iam-profile/iam_6.png)

#### Kiá»ƒm tra

Command pháº£i tráº£ vá» `Account`, `UserId` vÃ  `Arn`.

