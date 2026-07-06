---
title : "Cáº¥u hÃ¬nh VNPay IPN vÃ  Return URL"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.8.1. </b> "
---

#### Má»¥c tiÃªu

Cáº¥u hÃ¬nh VNPay callback URLs sau khi CloudFront domain Ä‘Ã£ sáºµn sÃ ng.

#### CÃ¡ch A - VNPay Sandbox portal

1. Má»Ÿ cáº¥u hÃ¬nh VNPay Sandbox.
2. Äáº·t Return URL lÃ  `https://<cloudfront-domain>/api/payment/vnpay-return`.
3. Äáº·t IPN URL lÃ  `https://<cloudfront-domain>/api/payment/vnpay-ipn`.
4. KhÃ´ng thÃªm dáº¥u `#` trÆ°á»›c URL.

![VNPay IPN](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.1-vnpay-url/vnpay.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$CloudFrontDomain = aws cloudformation describe-stacks `
  --stack-name $StackName `
  --region $Region `
  --profile $Profile `
  --query "Stacks[0].Outputs[?contains(OutputKey,'CloudFront')].OutputValue | [0]" `
  --output text

$AppBaseUrl = "https://$CloudFrontDomain"
$env:VNPAY_RETURN_URL = "$AppBaseUrl/api/payment/vnpay-return"
$env:VNPAY_IPN_URL = "$AppBaseUrl/api/payment/vnpay-ipn"

"Return: $env:VNPAY_RETURN_URL"
"IPN: $env:VNPAY_IPN_URL"
```

#### Kiá»ƒm tra

Táº¡o thanh toÃ¡n thá»­ vÃ  kiá»ƒm tra trang thanh toÃ¡n VNPay Sandbox má»Ÿ thÃ nh cÃ´ng.

