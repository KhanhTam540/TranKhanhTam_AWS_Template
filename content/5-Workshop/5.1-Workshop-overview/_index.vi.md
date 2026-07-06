---
title : "Tá»•ng quan workshop"
date : 2026-07-05
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---


#### TÃ¬nh huá»‘ng lab

Trong workshop nÃ y, báº¡n sáº½ triá»ƒn khai MedChain AI, má»™t á»©ng dá»¥ng quáº£n lÃ½ bá»‡nh viá»‡n sá»­ dá»¥ng AWS managed services cho frontend hosting, backend API, xÃ¡c thá»±c, database, thanh toÃ¡n, blockchain validation vÃ  monitoring.

Sau khi hoÃ n thÃ nh lab, á»©ng dá»¥ng cáº§n cÃ³:

+ Web frontend host trÃªn Amazon S3 vÃ  phÃ¢n phá»‘i báº±ng CloudFront.
+ Backend API má»Ÿ báº±ng API Gateway vÃ  xá»­ lÃ½ báº±ng Lambda.
+ ÄÄƒng nháº­p vÃ  phÃ¢n quyá»n báº±ng Cognito.
+ Dá»¯ liá»‡u bá»‡nh viá»‡n lÆ°u trong DynamoDB vÃ  tÃ i liá»‡u lÆ°u trong S3.
+ Luá»“ng thanh toÃ¡n hÃ³a Ä‘Æ¡n báº±ng VNPay Sandbox.
+ TÃ­ch há»£p AMB Ethereum node Ä‘á»ƒ lÆ°u metadata toÃ n váº¹n há»“ sÆ¡ bá»‡nh Ã¡n.
+ CloudWatch logs, metrics vÃ  alarms.

![Tá»•ng quan MedChain AI](/TranKhanhTam_AWS_Template/images/5-Workshop/5.1-Workshop-overview/mechain_ai.png)

#### CÃ¡ch viáº¿t lab

Má»—i bÆ°á»›c triá»ƒn khai Ä‘Æ°á»£c viáº¿t theo hai cÃ¡ch:

+ **CÃ¡ch A - AWS Console** dÃ nh cho ngÆ°á»i muá»‘n thao tÃ¡c trÃªn giao diá»‡n AWS vÃ  chá»¥p mÃ n hÃ¬nh.
+ **CÃ¡ch B - Lá»‡nh / code deployment** dÃ nh cho ngÆ°á»i muá»‘n triá»ƒn khai láº·p láº¡i báº±ng AWS CLI, CDK vÃ  PowerShell.

Sá»­ dá»¥ng stack name riÃªng cho lab:

```
MedChainAiLabStack
```

