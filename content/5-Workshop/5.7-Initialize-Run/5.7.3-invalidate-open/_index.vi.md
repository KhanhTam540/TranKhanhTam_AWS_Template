---
title : "Invalidate CloudFront vÃ  má»Ÿ website"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.7.3. </b> "
---

#### Má»¥c tiÃªu

Refresh CloudFront cache vÃ  má»Ÿ website Ä‘Ã£ deploy.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **CloudFront**.
2. Chá»n distribution.
3. Táº¡o invalidation cho `/*`.
4. Má»Ÿ distribution domain.

![CloudFront behaviors](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.3-cloudfront/cloudfront-web.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$DistributionId = aws cloudformation describe-stacks --stack-name $StackName --region $Region --profile $Profile --query "Stacks[0].Outputs[?contains(OutputKey,'DistributionId')].OutputValue | [0]" --output text
$Invalidation = aws cloudfront create-invalidation --distribution-id $DistributionId --paths "/*" --profile $Profile | ConvertFrom-Json
aws cloudfront wait invalidation-completed --distribution-id $DistributionId --id $Invalidation.Invalidation.Id --profile $Profile
```

#### Kiá»ƒm tra

TrÃ¬nh duyá»‡t cáº§n hiá»ƒn thá»‹ trang chá»§ MedChain AI.

