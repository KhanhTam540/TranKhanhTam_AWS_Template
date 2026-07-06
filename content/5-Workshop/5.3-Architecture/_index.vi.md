---
title : "Kiáº¿n trÃºc vÃ  thá»© tá»± phá»¥ thuá»™c"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Kiáº¿n trÃºc

BÃ i lab MedChain AI sá»­ dá»¥ng cÃ¡c dá»‹ch vá»¥ AWS sau:

+ **CloudFront** Ä‘á»ƒ publish website vÃ  chuyá»ƒn tiáº¿p request `/api/*`.
+ **S3** Ä‘á»ƒ host frontend vÃ  lÆ°u tÃ i liá»‡u y táº¿.
+ **API Gateway** Ä‘á»ƒ má»Ÿ API backend.
+ **Lambda** Ä‘á»ƒ cháº¡y logic nghiá»‡p vá»¥ backend.
+ **DynamoDB** Ä‘á»ƒ lÆ°u dá»¯ liá»‡u á»©ng dá»¥ng.
+ **Cognito** Ä‘á»ƒ xÃ¡c thá»±c ngÆ°á»i dÃ¹ng vÃ  phÃ¢n quyá»n vai trÃ².
+ **Secrets Manager** Ä‘á»ƒ lÆ°u cáº¥u hÃ¬nh tÃ­ch há»£p.
+ **Amazon Managed Blockchain Ethereum** Ä‘á»ƒ ghi báº±ng chá»©ng ledger blockchain tháº­t.
+ **CloudWatch** Ä‘á»ƒ giÃ¡m sÃ¡t logs, metrics vÃ  lá»—i.
+ **VNPay Sandbox** lÃ  cá»•ng thanh toÃ¡n bÃªn ngoÃ i.

NgÆ°á»i dÃ¹ng truy cáº­p há»‡ thá»‘ng báº±ng CloudFront distribution domain.

![SÆ¡ Ä‘á»“ kiáº¿n trÃºc](/TranKhanhTam_AWS_Template/images/5-Workshop/5.3-Architecture/architecture-0.png)

![SÆ¡ Ä‘á»“ kiáº¿n trÃºc](/TranKhanhTam_AWS_Template/images/5-Workshop/5.3-Architecture/architecture-1.png)
#### Thá»© tá»± phá»¥ thuá»™c

Thá»© tá»± triá»ƒn khai ráº¥t quan trá»ng vÃ¬ má»™t sá»‘ tÃ i nguyÃªn cáº§n output tá»« bÆ°á»›c trÆ°á»›c.

1. AWS account, budget, region vÃ  local profile.
2. CDK bootstrap resources.
3. VNPay Sandbox credentials.
4. AMB Ethereum node.
5. Secrets Manager configuration vÃ  environment variables.
6. CDK application stack.
7. DynamoDB, S3, Cognito, Lambda, API Gateway vÃ  CloudFront.
8. Seed dá»¯ liá»‡u máº«u.
9. Build frontend vÃ  upload lÃªn S3.
10. CloudFront invalidation.
11. VNPay IPN vÃ  Return URL dÃ¹ng CloudFront domain.
12. Kiá»ƒm thá»­ end-to-end vÃ  monitoring.
13. Cleanup theo thá»© tá»± ngÆ°á»£c láº¡i.


