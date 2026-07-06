---
title : "Táº¡o application stack"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.6.1. </b> "
---

#### Má»¥c tiÃªu

Deploy main MedChain AI stack sau khi pre-stack services Ä‘Ã£ sáºµn sÃ ng.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **CloudFormation**.
2. Create stack tá»« synthesized template náº¿u deploy thá»§ cÃ´ng.
3. Nháº­p stack name `MedChainAiLabStack`.
4. Chá» **CREATE_COMPLETE**.

![Stack complete](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.1-deploy-stack/stack.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$env:ENABLE_API_ROUTES = "true"
$env:ENABLE_WEEK3_OPERATIONS = "true"
$env:RETAIN_DATA = "false"
$env:ENABLE_CLOUDFRONT = "true"
$env:USE_EXISTING_CLOUDFRONT = "false"
npx cdk synth $StackName --profile $Profile
npx cdk deploy $StackName --profile $Profile --require-approval never
```

#### Kiá»ƒm tra

CloudFormation stack pháº£i CREATE_COMPLETE vÃ  cÃ³ outputs.

![Stack complete](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.1-deploy-stack/stack_1.png)

