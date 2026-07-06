---
title : "Monitoring, báº£o máº­t, chi phÃ­ vÃ  cleanup"
date : 2024-01-01
weight : 9
chapter : false
pre : " <b> 5.9. </b> "
---

#### Monitoring

Sau khi á»©ng dá»¥ng cÃ³ traffic, má»Ÿ CloudWatch Ä‘á»ƒ kiá»ƒm tra logs vÃ  metrics.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **CloudWatch**.
2. Má»Ÿ **Log groups**.
3. Kiá»ƒm tra cÃ¡c Lambda log groups.
4. Má»Ÿ **Metrics** vÃ  kiá»ƒm tra Lambda errors, duration vÃ  throttles.

![CloudWatch logs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.9-Monitoring-Cleanup/log_group.png)
![CloudWatch logs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.9-Monitoring-Cleanup/metric.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
aws logs describe-log-groups `
  --region $Region `
  --profile $Profile `
  --log-group-name-prefix "/aws/lambda" `
  --output table
```

#### Kiá»ƒm tra báº£o máº­t vÃ  chi phÃ­

Kiá»ƒm tra cÃ¡c má»¥c sau:

+ Secrets Ä‘Æ°á»£c lÆ°u trong Secrets Manager hoáº·c environment variables, khÃ´ng hard-code trong frontend files.
+ S3 data bucket khÃ´ng public.
+ API routes Ä‘Æ°á»£c báº£o vá»‡ báº±ng Cognito khi cáº§n.
+ AMB node Ä‘Æ°á»£c xÃ³a sau khi Ä‘Ã£ chá»¥p báº±ng chá»©ng blockchain náº¿u khÃ´ng cÃ²n dÃ¹ng lab.
+ Billing dashboard Ä‘Æ°á»£c kiá»ƒm tra sau khi deploy.

![Cost review](/TranKhanhTam_AWS_Template/images/5-Workshop/5.9-Monitoring-Cleanup/cost-review.png)

#### Thá»© tá»± cleanup

Cleanup pháº£i thá»±c hiá»‡n theo thá»© tá»± ngÆ°á»£c:

1. Ngá»«ng sá»­ dá»¥ng web application.
2. XÃ³a AMB Ethereum node.
3. Gá»¡ VNPay Sandbox IPN/Return URL náº¿u cáº§n.
4. Disable vÃ  xÃ³a CloudFront distribution.
5. Empty cÃ¡c S3 buckets.
6. Destroy CDK stack hoáº·c xÃ³a CloudFormation stack.
7. XÃ³a Secrets Manager secrets cÃ²n láº¡i náº¿u bá»‹ retain.
8. Kiá»ƒm tra Billing vÃ  Cost Explorer.

```powershell
npx cdk destroy $StackName `
  --profile $Profile `
  --force
```

![Delete stack](/TranKhanhTam_AWS_Template/images/5-Workshop/5.9-Monitoring-Cleanup/delete-stack.png)

