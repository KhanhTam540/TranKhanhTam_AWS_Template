---
title : "Kiá»ƒm tra AMB ledger transaction"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.8.2. </b> "
---

#### Má»¥c tiÃªu

Kiá»ƒm tra AMB node pháº£n há»“i Ä‘Æ°á»£c vÃ  á»©ng dá»¥ng lÆ°u Ä‘Æ°á»£c ledger metadata.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ giao diá»‡n MedChain AI.
2. HoÃ n thÃ nh thao tÃ¡c há»“ sÆ¡ bá»‡nh Ã¡n cÃ³ ghi ledger metadata.
3. Má»Ÿ CloudWatch logs cá»§a ledger Lambda.
4. Kiá»ƒm tra `payloadHash` vÃ  `transactionHash`.

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
awscurl `
  --service managedblockchain `
  --region ap-southeast-1 `
  -X POST `
  -d {"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1} `
  "$env:AMB_ETHEREUM_ENDPOINT"
```

#### Kiá»ƒm tra

Káº¿t quáº£ cáº§n hiá»ƒn thá»‹ block number hoáº·c transaction hash.

