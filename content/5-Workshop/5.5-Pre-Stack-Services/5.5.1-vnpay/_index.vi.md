---
title : "Chuáº©n bá»‹ VNPay Sandbox"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.5.1. </b> "
---

#### Má»¥c tiÃªu

Chuáº©n bá»‹ thÃ´ng tin VNPay Sandbox trÆ°á»›c khi deploy payment backend.

#### CÃ¡ch A - VNPay Sandbox portal

1. ÄÄƒng kÃ½ hoáº·c yÃªu cáº§u tÃ i khoáº£n merchant VNPay Sandbox.
2. Láº¥y **TMN Code**.
3. Láº¥y **Hash Secret** vÃ  lÆ°u an toÃ n.
4. ChÆ°a cáº¥u hÃ¬nh IPN/Return URL á»Ÿ bÆ°á»›c nÃ y. CÃ¡c URL nÃ y chá»‰ cÃ³ sau khi CloudFront Ä‘Æ°á»£c táº¡o.

![ThÃ´ng tin VNPay](/TranKhanhTam_AWS_Template/images/5-Workshop/5.5-Pre-Stack-Services/5.5.1-vnpay/vnpay.png)

#### CÃ¡ch B - Biáº¿n mÃ´i trÆ°á»ng

```powershell
$env:VNPAY_PAYMENT_URL = "https://sandbox.vnpayment.vn/paymentv2/vpcpay.html"
$env:VNPAY_TMN_CODE = "YOUR_TMN_CODE"
$env:VNPAY_HASH_SECRET = "YOUR_HASH_SECRET"
```

#### Kiá»ƒm tra

TMN Code vÃ  Hash Secret pháº£i sáºµn sÃ ng trÆ°á»›c khi deploy application stack.

