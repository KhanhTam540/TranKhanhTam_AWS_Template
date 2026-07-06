---
title : "Táº¡o Secrets Manager configuration"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.5.3. </b> "
---

#### Má»¥c tiÃªu

LÆ°u cáº¥u hÃ¬nh tÃ­ch há»£p trÆ°á»›c khi application stack Ä‘á»c cÃ¡c giÃ¡ trá»‹ nÃ y.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **Secrets Manager**.
2. Store a new secret.
3. ThÃªm key-value cho VNPay vÃ  AMB.
4. Äáº·t tÃªn `medchain-ai/lab/integrations`.

![Secrets created](/TranKhanhTam_AWS_Template/images/5-Workshop/5.5-Pre-Stack-Services/5.5.3-secrets/secrets.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$SecretValue = @{ VNPAY_PAYMENT_URL=$env:VNPAY_PAYMENT_URL; VNPAY_TMN_CODE=$env:VNPAY_TMN_CODE; VNPAY_HASH_SECRET=$env:VNPAY_HASH_SECRET; AMB_ETHEREUM_ENDPOINT=$env:AMB_ETHEREUM_ENDPOINT } | ConvertTo-Json -Compress
aws secretsmanager create-secret `
  --name "medchain-ai/lab/integrations" `
  --secret-string $SecretValue `
  --region $Region `
  --profile $Profile
```

#### Kiá»ƒm tra

Describe secret nhÆ°ng khÃ´ng in ra giÃ¡ trá»‹ nháº¡y cáº£m.

