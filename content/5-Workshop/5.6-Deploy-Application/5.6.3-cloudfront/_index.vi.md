---
title : "Táº¡o CloudFront distribution cho frontend"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.6.3. </b> "
---

#### Má»¥c tiÃªu

Táº¡o hoáº·c kiá»ƒm tra CloudFront distribution dÃ¹ng Ä‘á»ƒ phá»¥c vá»¥ frontend vÃ  chuyá»ƒn tiáº¿p request backend API. CloudFront distribution domain lÃ  URL public cá»§a á»©ng dá»¥ng.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **CloudFront** vÃ  kiá»ƒm tra distribution.
2. Kiá»ƒm tra default behavior trá» Ä‘áº¿n S3 frontend origin.
3. Kiá»ƒm tra behavior `/api/*` trá» Ä‘áº¿n API Gateway.
4. Copy CloudFront distribution domain, vÃ­ dá»¥ `dxxxxx.cloudfront.net`.

![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-s3-1.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-s3-2.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-s3-3.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-s3-4.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-s3-5.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-cloudfront-1.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-cloudfront-2.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-cloudfront-3.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-cloudfront-4.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/create-cloudfront-5.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/cloudfront-created.png)
![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/cloudfront-web.png)


#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$DistributionDomain = aws cloudformation describe-stacks `
  --stack-name $StackName `
  --region $Region `
  --profile $Profile `
  --query "Stacks[0].Outputs[?contains(OutputKey,'CloudFront')].OutputValue | [0]" `
  --output text

$DistributionDomain
```

#### Kiá»ƒm tra

CloudFront distribution pháº£i cÃ³ behavior cho frontend vÃ  behavior `/api/*` cho API. Website URL sáº½ lÃ  `https://<cloudfront-domain>`.

![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/cloudfront_code.png)
