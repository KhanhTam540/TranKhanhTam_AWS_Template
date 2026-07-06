---
title : "Build vÃ  upload web frontend"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.7.2. </b> "
---

#### Má»¥c tiÃªu

Build frontend vÃ  upload files sinh ra lÃªn frontend S3 bucket.

#### CÃ¡ch A - AWS Console

1. Build frontend trÃªn mÃ¡y local.
2. Má»Ÿ **S3** vÃ  chá»n frontend bucket.
3. Upload files tá»« `web/dist`.
4. Kiá»ƒm tra cÃ³ `index.html` vÃ  `assets/`.

![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-s3-5.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/cloudfront-created.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/cloudfront-web.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
cd "D:\AWS\LabRuns\MedChainAI-CommandRun\Project_Hospital_AWS_P2TB"
npm --prefix web run build
$FrontendBucket = aws cloudformation describe-stacks --stack-name $StackName --region $Region --profile $Profile --query "Stacks[0].Outputs[?contains(OutputKey,'FrontendBucket')].OutputValue | [0]" --output text
aws s3 sync .\web\dist "s3://$FrontendBucket" --profile $Profile
```

#### Kiá»ƒm tra

S3 frontend bucket cáº§n cÃ³ `index.html` vÃ  assets Ä‘Ã£ build.

