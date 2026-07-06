---
title : "Táº¡o AMB Ethereum node"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.5.2. </b> "
---

#### Má»¥c tiÃªu

Táº¡o AMB Ethereum node tháº­t trÆ°á»›c khi báº­t blockchain ledger validation.

#### CÃ¡ch A - AWS Console

1. Má»Ÿ **Amazon Managed Blockchain**.
2. Chá»n **Access Ethereum**.
3. Táº¡o dedicated Ethereum node.
4. Chá» tráº¡ng thÃ¡i **Available**.
5. Copy HTTP endpoint.

![AMB Ethereum node](/TranKhanhTam_AWS_Template/images/5-Workshop/5.5-Pre-Stack-Services/5.5.2-amb/amb_1.png)
![AMB Ethereum node](/TranKhanhTam_AWS_Template/images/5-Workshop/5.5-Pre-Stack-Services/5.5.2-amb/amb_2.png)
![AMB Ethereum node](/TranKhanhTam_AWS_Template/images/5-Workshop/5.5-Pre-Stack-Services/5.5.2-amb/amb_3.png)
![AMB Ethereum node](/TranKhanhTam_AWS_Template/images/5-Workshop/5.5-Pre-Stack-Services/5.5.2-amb/amb_4.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$env:AMB_ETHEREUM_ENDPOINT = "https://nd-xxxxx.ethereum.managedblockchain.ap-southeast-1.amazonaws.com/"
awscurl `
  --service managedblockchain `
  --region ap-southeast-1 `
  -X POST `
  -d {"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1} `
  "$env:AMB_ETHEREUM_ENDPOINT"
```

#### Kiá»ƒm tra

JSON-RPC response cáº§n tráº£ vá» block number result.

