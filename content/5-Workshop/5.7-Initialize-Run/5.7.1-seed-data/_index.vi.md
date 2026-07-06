---
title : "Seed dá»¯ liá»‡u á»©ng dá»¥ng"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.7.1. </b> "
---

#### Má»¥c tiÃªu

Seed demo users vÃ  dá»¯ liá»‡u bá»‡nh viá»‡n sau khi Cognito vÃ  DynamoDB Ä‘Ã£ tá»“n táº¡i.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **DynamoDB** vÃ  thÃªm sample records thá»§ cÃ´ng náº¿u cáº§n.
2. Má»Ÿ **Cognito** vÃ  táº¡o demo users thá»§ cÃ´ng náº¿u cáº§n.
3. Kiá»ƒm tra roles vÃ  sample data Ä‘Ã£ cÃ³.

![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/dynamodb.png)
![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/cognito.png)
![Stack outputs](/TranKhanhTam_AWS_Template/images/5-Workshop/5.6-Deploy-Application/5.6.2-verify-resources/cognito_1.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$DatasetRoot = "D:\AWS\Project\Hospital_Dataset_Reset_V2_1"
$ProjectRoot = "D:\AWS\LabRuns\MedChainAI-CommandRun\Project_Hospital_AWS_P2TB"
cd $DatasetRoot
.\RESET_AND_SEED_DATASET.ps1 `
  -ProjectRoot $ProjectRoot `
  -Profile $Profile `
  -Region $Region `
  -StackName $StackName `
  -Mode Full `
  -Confirmation "RESET-HOSPITAL-DATA"
```

#### Kiá»ƒm tra

DynamoDB cáº§n cÃ³ demo patients, doctors, appointments vÃ  invoices.

