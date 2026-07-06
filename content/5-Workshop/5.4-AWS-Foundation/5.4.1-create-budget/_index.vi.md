---
title : "Táº¡o budget vÃ  chá»n region"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.4.1. </b> "
---


#### Má»¥c tiÃªu

Táº¡o budget alert vÃ  xÃ¡c nháº­n region trÆ°á»›c khi táº¡o báº¥t ká»³ tÃ i nguyÃªn nÃ o.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **Billing and Cost Management**.
2. Chá»n **Budgets**.
3. Táº¡o monthly cost budget cho lab.
4. ThÃªm email notification.
5. Chá»n **ap-southeast-1** trong AWS region selector cho tÃ i nguyÃªn á»©ng dá»¥ng.

![Budget result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.1-create-budget/create-budgets-1.png)
![Budget result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.1-create-budget/create-budgets-2.png)
![Budget result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.4-AWS-Foundation/5.4.1-create-budget/create-budgets-3.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$Profile = "hospital-dev"
$Region = "ap-southeast-1"
$AccountId = aws sts get-caller-identity --profile $Profile --query Account --output text

aws budgets create-budget `
  --account-id $AccountId `
  --budget '{"BudgetName":"MedChainAI-Lab-Budget","BudgetLimit":{"Amount":"10","Unit":"USD"},"TimeUnit":"MONTHLY","BudgetType":"COST"}' `
  --profile $Profile
```


