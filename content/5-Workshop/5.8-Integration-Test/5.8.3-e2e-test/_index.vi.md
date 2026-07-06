---
title : "Cháº¡y kiá»ƒm thá»­ end-to-end"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.8.3. </b> "
---

#### Má»¥c tiÃªu

Cháº¡y toÃ n bá»™ luá»“ng bá»‡nh viá»‡n sau khi Ä‘Ã£ cáº¥u hÃ¬nh cÃ¡c tÃ­ch há»£p.

#### CÃ¡ch A - AWS Console

1. Bá»‡nh nhÃ¢n Ä‘Äƒng nháº­p vÃ  Ä‘áº·t lá»‹ch.
2. NhÃ¢n viÃªn xÃ¡c nháº­n lá»‹ch.
3. BÃ¡c sÄ© táº¡o phiáº¿u khÃ¡m.
4. HÃ³a Ä‘Æ¡n Ä‘Æ°á»£c táº¡o.
5. Bá»‡nh nhÃ¢n thanh toÃ¡n báº±ng VNPay Sandbox.
6. Metadata ledger cá»§a há»“ sÆ¡ bá»‡nh Ã¡n Ä‘Æ°á»£c sinh ra.

![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/dk.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/dkl_completed.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/lk.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/ttlk.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/pk.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/pk_completed.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/dt.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/dt_completed.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/hsba.png)
![End-to-end result](/TranKhanhTam_AWS_Template/images/5-Workshop/5.8-Integration-Test/5.8.3-e2e-test/hsba_1.png)

#### CÃ¡ch B - Lá»‡nh / code deployment

```powershell
$AppDomain = "https://<cloudfront-domain>"
Invoke-WebRequest $AppDomain -UseBasicParsing
```

#### Kiá»ƒm tra

á»¨ng dá»¥ng cáº§n hoÃ n thÃ nh luá»“ng mÃ  khÃ´ng cÃ³ lá»—i backend.

