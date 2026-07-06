---
title: "Blog 2"
date: 2026-07-05
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---


# Táº¡o tráº£i nghiá»‡m xÃ¡c thá»±c hiá»‡u quáº£ vá»›i Amazon Cognito vÃ  Authsignal

Trong cÃ¡c á»©ng dá»¥ng sá»‘ hiá»‡n nay, xÃ¡c thá»±c ngÆ°á»i dÃ¹ng lÃ  má»™t pháº§n ráº¥t quan trá»ng trong hÃ nh trÃ¬nh sá»­ dá»¥ng há»‡ thá»‘ng. XÃ¡c thá»±c giÃºp báº£o vá»‡ tÃ i khoáº£n ngÆ°á»i dÃ¹ng, thÃ´ng tin cÃ¡ nhÃ¢n, dá»¯ liá»‡u tÃ i chÃ­nh vÃ  cÃ¡c tÃ i nguyÃªn nháº¡y cáº£m khÃ¡c. Tuy nhiÃªn, báº£o máº­t máº¡nh Ä‘Ã´i khi láº¡i lÃ m tráº£i nghiá»‡m ngÆ°á»i dÃ¹ng trá»Ÿ nÃªn phá»©c táº¡p vÃ  khÃ³ chá»‹u.

Nhiá»u á»©ng dá»¥ng sá»­ dá»¥ng xÃ¡c thá»±c Ä‘a yáº¿u tá»‘, hay MFA, Ä‘á»ƒ tÄƒng cÆ°á»ng báº£o máº­t. MFA cÃ³ thá»ƒ bao gá»“m SMS OTP, email OTP, á»©ng dá»¥ng xÃ¡c thá»±c, sinh tráº¯c há»c, passkey hoáº·c khÃ³a báº£o máº­t pháº§n cá»©ng. Máº·c dÃ¹ MFA giÃºp tÄƒng má»©c Ä‘á»™ báº£o vá»‡, viá»‡c báº¯t buá»™c ngÆ°á»i dÃ¹ng xÃ¡c thá»±c nhiá»u lá»›p á»Ÿ má»i láº§n Ä‘Äƒng nháº­p hoáº·c má»i thao tÃ¡c cÃ³ thá»ƒ táº¡o ra tráº£i nghiá»‡m khÃ´ng tá»‘t.

BÃ i viáº¿t AWS **â€œCreating great authentication experiences with Amazon Cognito and Authsignalâ€** giáº£i thÃ­ch cÃ¡ch Amazon Cognito vÃ  Authsignal cÃ³ thá»ƒ káº¿t há»£p Ä‘á»ƒ táº¡o ra tráº£i nghiá»‡m xÃ¡c thá»±c tá»‘t hÆ¡n. Ã tÆ°á»Ÿng chÃ­nh lÃ  cÃ¢n báº±ng giá»¯a báº£o máº­t vÃ  tÃ­nh tiá»‡n lá»£i báº±ng cÃ¡ch sá»­ dá»¥ng xÃ¡c thá»±c thÃ­ch á»©ng, tÃ­n hiá»‡u rá»§i ro, xÃ¡c thá»±c liÃªn tá»¥c vÃ  cÃ¡c phÆ°Æ¡ng thá»©c xÃ¡c thá»±c linh hoáº¡t.

Thay vÃ¬ Ã¡p dá»¥ng cÃ¹ng má»™t yÃªu cáº§u xÃ¡c thá»±c cho má»i ngÆ°á»i dÃ¹ng vÃ  má»i tÃ¬nh huá»‘ng, há»‡ thá»‘ng cÃ³ thá»ƒ Ä‘Ã¡nh giÃ¡ rá»§i ro rá»“i Ã¡p dá»¥ng má»©c xÃ¡c thá»±c phÃ¹ há»£p vÃ o Ä‘Ãºng thá»i Ä‘iá»ƒm.

## 1. ThÃ¡ch thá»©c cá»§a tráº£i nghiá»‡m xÃ¡c thá»±c

XÃ¡c thá»±c cÃ³ hai má»¥c tiÃªu thÆ°á»ng cáº¡nh tranh vá»›i nhau:

- Báº£o vá»‡ á»©ng dá»¥ng khá»i truy cáº­p trÃ¡i phÃ©p.
- Giá»¯ tráº£i nghiá»‡m ngÆ°á»i dÃ¹ng Ä‘Æ¡n giáº£n vÃ  thuáº­n tiá»‡n.

Náº¿u xÃ¡c thá»±c quÃ¡ yáº¿u, káº» táº¥n cÃ´ng cÃ³ thá»ƒ truy cáº­p vÃ o tÃ i khoáº£n ngÆ°á»i dÃ¹ng. Náº¿u xÃ¡c thá»±c quÃ¡ nghiÃªm ngáº·t, ngÆ°á»i dÃ¹ng tháº­t cÃ³ thá»ƒ cáº£m tháº¥y phiá»n vÃ  rá»i bá» á»©ng dá»¥ng. VÃ­ dá»¥, náº¿u ngÆ°á»i dÃ¹ng pháº£i nháº­p OTP má»—i láº§n má»Ÿ á»©ng dá»¥ng, quy trÃ¬nh sáº½ trá»Ÿ nÃªn cháº­m vÃ  láº·p láº¡i quÃ¡ nhiá»u láº§n.

Váº¥n Ä‘á» nÃ y trá»Ÿ nÃªn rÃµ hÆ¡n khi á»©ng dá»¥ng má»Ÿ rá»™ng. Má»™t há»‡ thá»‘ng lá»›n cÃ³ thá»ƒ phá»¥c vá»¥ nhiá»u ngÆ°á»i dÃ¹ng trÃªn nhiá»u thiáº¿t bá»‹, vá»‹ trÃ­ vÃ  thÃ³i quen sá»­ dá»¥ng khÃ¡c nhau. Má»™t sá»‘ láº§n Ä‘Äƒng nháº­p cÃ³ rá»§i ro tháº¥p, trong khi má»™t sá»‘ láº§n khÃ¡c láº¡i Ä‘Ã¡ng nghi ngá». Náº¿u má»i láº§n Ä‘Äƒng nháº­p Ä‘á»u bá»‹ xem lÃ  rá»§i ro nhÆ° nhau, há»‡ thá»‘ng sáº½ táº¡o ra rÃ o cáº£n khÃ´ng cáº§n thiáº¿t.

CÃ¡ch tiáº¿p cáº­n tá»‘t hÆ¡n lÃ  Ä‘Ã¡nh giÃ¡ theo ngá»¯ cáº£nh. Há»‡ thá»‘ng nÃªn Ä‘áº·t ra cÃ¡c cÃ¢u há»i:

- ÄÃ¢y cÃ³ pháº£i thiáº¿t bá»‹ quen thuá»™c khÃ´ng?
- Vá»‹ trÃ­ Ä‘Äƒng nháº­p cÃ³ bÃ¬nh thÆ°á»ng khÃ´ng?
- HÃ nh vi ngÆ°á»i dÃ¹ng cÃ³ quen thuá»™c khÃ´ng?
- HÃ nh Ä‘á»™ng nÃ y cÃ³ rá»§i ro tháº¥p hay cao?
- Sá»‘ tiá»n giao dá»‹ch cÃ³ báº¥t thÆ°á»ng khÃ´ng?
- NgÆ°á»i dÃ¹ng cÃ³ Ä‘ang truy cáº­p dá»¯ liá»‡u nháº¡y cáº£m khÃ´ng?

Dá»±a trÃªn cÃ¡c thÃ´ng tin nÃ y, há»‡ thá»‘ng cÃ³ thá»ƒ quyáº¿t Ä‘á»‹nh cho ngÆ°á»i dÃ¹ng tiáº¿p tá»¥c bÃ¬nh thÆ°á»ng hoáº·c yÃªu cáº§u thÃªm má»™t bÆ°á»›c xÃ¡c thá»±c.

## 2. XÃ¡c thá»±c thÃ­ch á»©ng lÃ  gÃ¬?

XÃ¡c thá»±c thÃ­ch á»©ng lÃ  chiáº¿n lÆ°á»£c xÃ¡c thá»±c thay Ä‘á»•i dá»±a trÃªn má»©c Ä‘á»™ rá»§i ro. Thay vÃ¬ yÃªu cáº§u cÃ¹ng má»™t bÆ°á»›c báº£o máº­t cho má»i tÃ¬nh huá»‘ng, há»‡ thá»‘ng phÃ¢n tÃ­ch ngá»¯ cáº£nh vÃ  quyáº¿t Ä‘á»‹nh má»©c xÃ¡c thá»±c cáº§n thiáº¿t.

VÃ­ dá»¥, náº¿u ngÆ°á»i dÃ¹ng Ä‘Äƒng nháº­p tá»« thiáº¿t bá»‹ quen thuá»™c, táº¡i vá»‹ trÃ­ thÆ°á»ng dÃ¹ng vÃ  vÃ o thá»i Ä‘iá»ƒm bÃ¬nh thÆ°á»ng, há»‡ thá»‘ng cÃ³ thá»ƒ cho phÃ©p Ä‘Äƒng nháº­p vá»›i Ã­t ma sÃ¡t hÆ¡n. NgÆ°á»£c láº¡i, náº¿u cÃ¹ng ngÆ°á»i dÃ¹ng Ä‘Ã³ Ä‘Äƒng nháº­p tá»« thiáº¿t bá»‹ má»›i, vá»‹ trÃ­ báº¥t thÆ°á»ng hoáº·c thá»i Ä‘iá»ƒm khÃ¡c thÆ°á»ng, há»‡ thá»‘ng cÃ³ thá»ƒ yÃªu cáº§u MFA.

VÃ­ dá»¥ Ä‘Æ¡n giáº£n:

```text
ÄÄƒng nháº­p rá»§i ro tháº¥p:
Thiáº¿t bá»‹ quen + vá»‹ trÃ­ thÆ°á»ng dÃ¹ng + hÃ nh vi bÃ¬nh thÆ°á»ng
â†’ Cho phÃ©p truy cáº­p vá»›i Ã­t rÃ o cáº£n

ÄÄƒng nháº­p rá»§i ro cao:
Thiáº¿t bá»‹ láº¡ + vá»‹ trÃ­ báº¥t thÆ°á»ng + hÃ nh vi khÃ´ng bÃ¬nh thÆ°á»ng
â†’ YÃªu cáº§u xÃ¡c thá»±c bá»• sung
```

CÃ¡ch tiáº¿p cáº­n nÃ y cáº£i thiá»‡n cáº£ báº£o máº­t vÃ  tráº£i nghiá»‡m ngÆ°á»i dÃ¹ng. NgÆ°á»i dÃ¹ng á»Ÿ tÃ¬nh huá»‘ng rá»§i ro tháº¥p khÃ´ng bá»‹ lÃ m phiá»n khÃ´ng cáº§n thiáº¿t, cÃ²n cÃ¡c tÃ¬nh huá»‘ng rá»§i ro cao sáº½ Ä‘Æ°á»£c báº£o vá»‡ máº¡nh hÆ¡n.

XÃ¡c thá»±c thÃ­ch á»©ng Ä‘áº·c biá»‡t há»¯u Ã­ch cho cÃ¡c á»©ng dá»¥ng cáº§n báº£o máº­t máº¡nh nhÆ°ng váº«n quan tÃ¢m Ä‘áº¿n tá»· lá»‡ chuyá»ƒn Ä‘á»•i, giá»¯ chÃ¢n ngÆ°á»i dÃ¹ng vÃ  sá»± hÃ i lÃ²ng khi sá»­ dá»¥ng.

## 3. CÃ¡c tÃ­n hiá»‡u rá»§i ro trong xÃ¡c thá»±c

TÃ­n hiá»‡u rá»§i ro lÃ  nhá»¯ng thÃ´ng tin theo ngá»¯ cáº£nh giÃºp há»‡ thá»‘ng hiá»ƒu má»™t láº§n xÃ¡c thá»±c lÃ  bÃ¬nh thÆ°á»ng hay Ä‘Ã¡ng nghi ngá». Nhá»¯ng tÃ­n hiá»‡u nÃ y cÃ³ thá»ƒ Ä‘áº¿n tá»« thiáº¿t bá»‹, máº¡ng, hÃ nh vi ngÆ°á»i dÃ¹ng, thÃ´ng tin giao dá»‹ch hoáº·c ngá»¯ cáº£nh á»©ng dá»¥ng.

CÃ¡c tÃ­n hiá»‡u rá»§i ro phá»• biáº¿n gá»“m:

### TÃ­n hiá»‡u thiáº¿t bá»‹

TÃ­n hiá»‡u thiáº¿t bá»‹ giÃºp xÃ¡c Ä‘á»‹nh ngÆ°á»i dÃ¹ng cÃ³ Ä‘ang dÃ¹ng thiáº¿t bá»‹ quen thuá»™c hay khÃ´ng. Há»‡ thá»‘ng cÃ³ thá»ƒ kiá»ƒm tra fingerprint cá»§a trÃ¬nh duyá»‡t, ID thiáº¿t bá»‹, há»‡ Ä‘iá»u hÃ nh, loáº¡i trÃ¬nh duyá»‡t hoáº·c lá»‹ch sá»­ sá»­ dá»¥ng thiáº¿t bá»‹.

Náº¿u ngÆ°á»i dÃ¹ng Ä‘Äƒng nháº­p tá»« thiáº¿t bá»‹ Ä‘Ã£ sá»­ dá»¥ng nhiá»u láº§n trÆ°á»›c Ä‘Ã³, rá»§i ro cÃ³ thá»ƒ tháº¥p hÆ¡n. Náº¿u ngÆ°á»i dÃ¹ng Ä‘Äƒng nháº­p tá»« thiáº¿t bá»‹ hoÃ n toÃ n má»›i, há»‡ thá»‘ng cÃ³ thá»ƒ xem request nÃ y lÃ  rá»§i ro cao hÆ¡n.

### TÃ­n hiá»‡u vá»‹ trÃ­

TÃ­n hiá»‡u vá»‹ trÃ­ giÃºp phÃ¡t hiá»‡n cÃ¡c máº«u truy cáº­p báº¥t thÆ°á»ng. VÃ­ dá»¥, náº¿u ngÆ°á»i dÃ¹ng vá»«a Ä‘Äƒng nháº­p á»Ÿ Viá»‡t Nam rá»“i vÃ i phÃºt sau láº¡i Ä‘Äƒng nháº­p á»Ÿ má»™t quá»‘c gia ráº¥t xa, há»‡ thá»‘ng cÃ³ thá»ƒ xem Ä‘Ã¢y lÃ  dáº¥u hiá»‡u Ä‘Ã¡ng ngá».

TrÆ°á»ng há»£p nÃ y thÆ°á»ng Ä‘Æ°á»£c gá»i lÃ  impossible travel. NÃ³ cho tháº¥y tÃ i khoáº£n cÃ³ thá»ƒ Ä‘Ã£ bá»‹ xÃ¢m nháº­p hoáº·c má»™t trong cÃ¡c láº§n Ä‘Äƒng nháº­p khÃ´ng thuá»™c vá» ngÆ°á»i dÃ¹ng tháº­t.

### TÃ­n hiá»‡u hÃ nh vi

TÃ­n hiá»‡u hÃ nh vi bao gá»“m tá»‘c Ä‘á»™ Ä‘Äƒng nháº­p, táº§n suáº¥t Ä‘Äƒng nháº­p, thá»i Ä‘iá»ƒm truy cáº­p, cÃ¡ch di chuyá»ƒn trong á»©ng dá»¥ng vÃ  cÃ¡c thÃ³i quen sá»­ dá»¥ng khÃ¡c. Náº¿u ngÆ°á»i dÃ¹ng thÆ°á»ng Ä‘Äƒng nháº­p trong giá» lÃ m viá»‡c nhÆ°ng Ä‘á»™t nhiÃªn Ä‘Äƒng nháº­p nhiá»u láº§n lÃºc ná»­a Ä‘Ãªm, há»‡ thá»‘ng cÃ³ thá»ƒ tÄƒng Ä‘iá»ƒm rá»§i ro.

PhÃ¢n tÃ­ch hÃ nh vi giÃºp há»‡ thá»‘ng xÃ¡c thá»±c thÃ´ng minh hÆ¡n vÃ¬ nÃ³ khÃ´ng chá»‰ kiá»ƒm tra danh tÃ­nh táº¡i má»™t thá»i Ä‘iá»ƒm. Há»‡ thá»‘ng cÃ²n quan sÃ¡t cÃ¡ch ngÆ°á»i dÃ¹ng thÆ°á»ng tÆ°Æ¡ng tÃ¡c vá»›i á»©ng dá»¥ng.

### TÃ­n hiá»‡u giao dá»‹ch

Má»™t sá»‘ hÃ nh Ä‘á»™ng cÃ³ má»©c rá»§i ro cao hÆ¡n cÃ¡c hÃ nh Ä‘á»™ng khÃ¡c. VÃ­ dá»¥, xem trang thÃ´ng tin cÃ´ng khai cÃ³ thá»ƒ lÃ  rá»§i ro tháº¥p, nhÆ°ng Ä‘á»•i máº­t kháº©u, thÃªm phÆ°Æ¡ng thá»©c thanh toÃ¡n má»›i hoáº·c thá»±c hiá»‡n giao dá»‹ch giÃ¡ trá»‹ lá»›n lÃ  hÃ nh Ä‘á»™ng rá»§i ro cao.

TÃ­n hiá»‡u giao dá»‹ch giÃºp há»‡ thá»‘ng quyáº¿t Ä‘á»‹nh cÃ³ cáº§n xÃ¡c thá»±c nÃ¢ng cáº¥p hay khÃ´ng. Má»™t giao dá»‹ch thÃ´ng thÆ°á»ng cÃ³ thá»ƒ tiáº¿p tá»¥c mÃ  khÃ´ng bá»‹ giÃ¡n Ä‘oáº¡n, cÃ²n giao dá»‹ch cÃ³ giÃ¡ trá»‹ cao hoáº·c báº¥t thÆ°á»ng cÃ³ thá»ƒ yÃªu cáº§u xÃ¡c minh bá»• sung.

## 4. XÃ¡c thá»±c liÃªn tá»¥c sau bÆ°á»›c Ä‘Äƒng nháº­p

Má»™t sai láº§m phá»• biáº¿n trong thiáº¿t káº¿ xÃ¡c thá»±c lÃ  chá»‰ kiá»ƒm tra danh tÃ­nh ngÆ°á»i dÃ¹ng táº¡i thá»i Ä‘iá»ƒm Ä‘Äƒng nháº­p. Sau khi ngÆ°á»i dÃ¹ng Ä‘Äƒng nháº­p thÃ nh cÃ´ng, há»‡ thá»‘ng cÃ³ thá»ƒ cho phÃ©p thá»±c hiá»‡n má»i hÃ nh Ä‘á»™ng mÃ  khÃ´ng cáº§n xÃ¡c minh thÃªm. Äiá»u nÃ y cÃ³ thá»ƒ gÃ¢y rá»§i ro.

BÃ i viáº¿t giáº£i thÃ­ch Ã½ tÆ°á»Ÿng xÃ¡c thá»±c liÃªn tá»¥c. Äiá»u nÃ y cÃ³ nghÄ©a lÃ  há»‡ thá»‘ng cÃ³ thá»ƒ Ä‘Ã¡nh giÃ¡ rá»§i ro trong suá»‘t phiÃªn lÃ m viá»‡c cá»§a ngÆ°á»i dÃ¹ng, khÃ´ng chá»‰ á»Ÿ lÃºc Ä‘Äƒng nháº­p.

Äá»‘i vá»›i hÃ nh Ä‘á»™ng rá»§i ro tháº¥p, ngÆ°á»i dÃ¹ng cÃ³ thá»ƒ tiáº¿p tá»¥c bÃ¬nh thÆ°á»ng. Äá»‘i vá»›i hÃ nh Ä‘á»™ng nháº¡y cáº£m hoáº·c rá»§i ro cao, há»‡ thá»‘ng cÃ³ thá»ƒ yÃªu cáº§u xÃ¡c thá»±c máº¡nh hÆ¡n.

VÃ­ dá»¥:

```text
Xem thÃ´ng tin tÃ i khoáº£n thÃ´ng thÆ°á»ng
â†’ KhÃ´ng cáº§n xÃ¡c thá»±c thÃªm

Äá»•i máº­t kháº©u
â†’ YÃªu cáº§u MFA hoáº·c passkey

ThÃªm phÆ°Æ¡ng thá»©c thanh toÃ¡n má»›i
â†’ YÃªu cáº§u xÃ¡c thá»±c bá»• sung

Truy cáº­p dá»¯ liá»‡u nháº¡y cáº£m
â†’ YÃªu cáº§u xÃ¡c thá»±c máº¡nh hÆ¡n

Thá»±c hiá»‡n giao dá»‹ch giÃ¡ trá»‹ cao
â†’ YÃªu cáº§u step-up authentication
```

MÃ´ hÃ¬nh nÃ y tÄƒng cÆ°á»ng báº£o máº­t vÃ¬ há»‡ thá»‘ng cÃ³ thá»ƒ báº£o vá»‡ cÃ¡c hÃ nh Ä‘á»™ng quan trá»ng ngay cáº£ khi ngÆ°á»i dÃ¹ng Ä‘Ã£ Ä‘Äƒng nháº­p. Äá»“ng thá»i, nÃ³ cÅ©ng cáº£i thiá»‡n tráº£i nghiá»‡m vÃ¬ ngÆ°á»i dÃ¹ng khÃ´ng bá»‹ yÃªu cáº§u xÃ¡c thá»±c thÃªm cho má»i thao tÃ¡c nhá».

## 5. Amazon Cognito lÃ  ná»n táº£ng Ä‘á»‹nh danh

Amazon Cognito Ä‘Æ°á»£c sá»­ dá»¥ng Ä‘á»ƒ quáº£n lÃ½ xÃ¡c thá»±c vÃ  Ä‘á»‹nh danh ngÆ°á»i dÃ¹ng trong á»©ng dá»¥ng. Dá»‹ch vá»¥ nÃ y cung cáº¥p user pool, Ä‘Äƒng kÃ½, Ä‘Äƒng nháº­p, xÃ¡c thá»±c báº±ng token vÃ  cÃ¡c kháº£ nÄƒng quáº£n lÃ½ ngÆ°á»i dÃ¹ng.

Trong kiáº¿n trÃºc xÃ¡c thá»±c, Cognito cÃ³ thá»ƒ Ä‘Ã³ng vai trÃ² lÃ  ná»n táº£ng Ä‘á»‹nh danh. NÃ³ lÆ°u trá»¯ vÃ  quáº£n lÃ½ tÃ i khoáº£n ngÆ°á»i dÃ¹ng, xá»­ lÃ½ quy trÃ¬nh Ä‘Äƒng nháº­p ban Ä‘áº§u vÃ  phÃ¡t hÃ nh token Ä‘á»ƒ á»©ng dá»¥ng sá»­ dá»¥ng trong cÃ¡c request.

Amazon Cognito há»¯u Ã­ch vÃ¬ cung cáº¥p cÃ¡c tÃ­nh nÄƒng Ä‘á»‹nh danh Ä‘Æ°á»£c quáº£n lÃ½ sáºµn, giÃºp Ä‘á»™i ngÅ© phÃ¡t triá»ƒn khÃ´ng cáº§n xÃ¢y dá»±ng toÃ n bá»™ há»‡ thá»‘ng xÃ¡c thá»±c tá»« Ä‘áº§u. á»¨ng dá»¥ng cÃ³ thá»ƒ tÃ­ch há»£p Cognito Ä‘á»ƒ xá»­ lÃ½ Ä‘Äƒng kÃ½, Ä‘Äƒng nháº­p, Ä‘áº·t láº¡i máº­t kháº©u vÃ  quáº£n lÃ½ phiÃªn Ä‘Äƒng nháº­p an toÃ n.

Tuy nhiÃªn, yÃªu cáº§u xÃ¡c thá»±c ngÃ y cÃ ng phá»©c táº¡p. Nhiá»u doanh nghiá»‡p cáº§n xÃ¡c thá»±c thÃ­ch á»©ng, quyáº¿t Ä‘á»‹nh dá»±a trÃªn rá»§i ro, step-up authentication vÃ  nhiá»u phÆ°Æ¡ng thá»©c xÃ¡c thá»±c khÃ¡c nhau. ÄÃ¢y lÃ  nÆ¡i Authsignal cÃ³ thá»ƒ má»Ÿ rá»™ng tráº£i nghiá»‡m xÃ¡c thá»±c.

## 6. Authsignal lÃ  bá»™ phÃ¢n tÃ­ch rá»§i ro vÃ  rules engine

Authsignal cung cáº¥p kháº£ nÄƒng Ä‘iá»u phá»‘i xÃ¡c thá»±c vÃ  há»— trá»£ quyáº¿t Ä‘á»‹nh dá»±a trÃªn rá»§i ro. Dá»‹ch vá»¥ nÃ y cÃ³ thá»ƒ káº¿t há»£p vá»›i Amazon Cognito Ä‘á»ƒ giÃºp á»©ng dá»¥ng táº¡o cÃ¡c luá»“ng xÃ¡c thá»±c thÃ­ch á»©ng vÃ  liÃªn tá»¥c.

Má»™t tÃ­nh nÄƒng quan trá»ng lÃ  rules engine. Rules engine cho phÃ©p quáº£n trá»‹ viÃªn cáº¥u hÃ¬nh cÃ¡c luáº­t báº£o máº­t dá»±a trÃªn ngá»¯ cáº£nh vÃ  yÃªu cáº§u kinh doanh. Thay vÃ¬ viáº¿t cá»©ng toÃ n bá»™ logic xÃ¡c thá»±c trong á»©ng dá»¥ng, tá»• chá»©c cÃ³ thá»ƒ Ä‘á»‹nh nghÄ©a rule linh hoáº¡t hÆ¡n.

VÃ­ dá»¥, quáº£n trá»‹ viÃªn cÃ³ thá»ƒ táº¡o cÃ¡c rule nhÆ°:

```text
Náº¿u ngÆ°á»i dÃ¹ng Ä‘Äƒng nháº­p tá»« thiáº¿t bá»‹ má»›i
â†’ YÃªu cáº§u MFA

Náº¿u sá»‘ tiá»n giao dá»‹ch vÆ°á»£t ngÆ°á»¡ng quy Ä‘á»‹nh
â†’ YÃªu cáº§u xÃ¡c thá»±c máº¡nh hÆ¡n

Náº¿u ngÆ°á»i dÃ¹ng Ä‘á»•i máº­t kháº©u
â†’ YÃªu cáº§u step-up authentication

Náº¿u ngÆ°á»i dÃ¹ng dÃ¹ng thiáº¿t bá»‹ tin cáº­y vÃ  vá»‹ trÃ­ rá»§i ro tháº¥p
â†’ Cho phÃ©p truy cáº­p vá»›i Ã­t rÃ o cáº£n
```

Äiá»u nÃ y giÃºp cÃ¡c nhÃ³m khÃ´ng chuyÃªn ká»¹ thuáº­t linh hoáº¡t hÆ¡n vÃ¬ há» cÃ³ thá»ƒ Ä‘iá»u chá»‰nh luáº­t báº£o máº­t mÃ  khÃ´ng cáº§n yÃªu cáº§u láº­p trÃ¬nh viÃªn sá»­a code má»—i láº§n.

Authsignal cÅ©ng há»— trá»£ nhiá»u phÆ°Æ¡ng thá»©c xÃ¡c thá»±c khÃ¡c nhau. TÃ¹y theo má»©c Ä‘á»™ rá»§i ro vÃ  ngá»¯ cáº£nh ngÆ°á»i dÃ¹ng, há»‡ thá»‘ng cÃ³ thá»ƒ chá»n OTP, passkey, sinh tráº¯c há»c hoáº·c cÃ¡c tÃ¹y chá»n xÃ¡c minh khÃ¡c.

## 7. Amazon Cognito vÃ  Authsignal phá»‘i há»£p nhÆ° tháº¿ nÃ o?

Sá»± káº¿t há»£p giá»¯a Amazon Cognito vÃ  Authsignal táº¡o ra má»™t kiáº¿n trÃºc xÃ¡c thá»±c máº¡nh vÃ  linh hoáº¡t hÆ¡n.

Má»™t luá»“ng Ä‘Æ¡n giáº£n cÃ³ thá»ƒ mÃ´ táº£ nhÆ° sau:

```text
NgÆ°á»i dÃ¹ng thao tÃ¡c
â†’ Amazon Cognito xá»­ lÃ½ Ä‘á»‹nh danh vÃ  phiÃªn ngÆ°á»i dÃ¹ng
â†’ Authsignal Ä‘Ã¡nh giÃ¡ rá»§i ro vÃ  luáº­t nghiá»‡p vá»¥
â†’ Há»‡ thá»‘ng quyáº¿t Ä‘á»‹nh phÆ°Æ¡ng thá»©c xÃ¡c thá»±c cáº§n thiáº¿t
â†’ NgÆ°á»i dÃ¹ng hoÃ n thÃ nh xÃ¡c minh náº¿u cáº§n
â†’ á»¨ng dá»¥ng cho phÃ©p hoáº·c tá»« chá»‘i hÃ nh Ä‘á»™ng
```

Amazon Cognito quáº£n lÃ½ lá»›p Ä‘á»‹nh danh ngÆ°á»i dÃ¹ng, cÃ²n Authsignal bá»• sung kháº£ nÄƒng ra quyáº¿t Ä‘á»‹nh thÃ­ch á»©ng vÃ  Ä‘iá»u phá»‘i xÃ¡c thá»±c. Nhá» Ä‘Ã³, há»‡ thá»‘ng cÃ³ thá»ƒ cÃ¢n báº±ng tá»‘t hÆ¡n giá»¯a báº£o máº­t tÃ i khoáº£n vÃ  sá»± tiá»‡n lá»£i cho ngÆ°á»i dÃ¹ng.

Sá»± káº¿t há»£p nÃ y há»¯u Ã­ch vÃ¬ khÃ´ng pháº£i má»i hÃ nh Ä‘á»™ng cá»§a ngÆ°á»i dÃ¹ng Ä‘á»u cáº§n cÃ¹ng má»™t má»©c báº£o máº­t. Há»‡ thá»‘ng cÃ³ thá»ƒ Ä‘Æ¡n giáº£n vá»›i cÃ¡c thao tÃ¡c rá»§i ro tháº¥p vÃ  nghiÃªm ngáº·t hÆ¡n vá»›i cÃ¡c thao tÃ¡c rá»§i ro cao.

## 8. PhÆ°Æ¡ng thá»©c xÃ¡c thá»±c vÃ  tráº£i nghiá»‡m ngÆ°á»i dÃ¹ng

Má»™t tráº£i nghiá»‡m xÃ¡c thá»±c tá»‘t nÃªn cung cáº¥p nhiá»u tÃ¹y chá»n xÃ¡c minh. NgÆ°á»i dÃ¹ng á»Ÿ cÃ¡c khu vá»±c khÃ¡c nhau hoáº·c nhÃ³m ngÆ°á»i dÃ¹ng khÃ¡c nhau cÃ³ thá»ƒ Æ°a thÃ­ch cÃ¡c phÆ°Æ¡ng thá»©c khÃ¡c nhau.

CÃ¡c phÆ°Æ¡ng thá»©c xÃ¡c thá»±c phá»• biáº¿n gá»“m:

- SMS OTP
- Email OTP
- á»¨ng dá»¥ng xÃ¡c thá»±c
- WhatsApp OTP
- Push notification
- Passkeys
- Sinh tráº¯c há»c
- KhÃ³a báº£o máº­t pháº§n cá»©ng
- Liveness detection

Má»—i phÆ°Æ¡ng thá»©c Ä‘á»u cÃ³ Æ°u vÃ  nhÆ°á»£c Ä‘iá»ƒm riÃªng. SMS OTP quen thuá»™c nhÆ°ng cÃ³ thá»ƒ bá»‹ áº£nh hÆ°á»Ÿng bá»Ÿi táº¥n cÃ´ng SIM swap. Email OTP dá»… sá»­ dá»¥ng nhÆ°ng phá»¥ thuá»™c vÃ o Ä‘á»™ an toÃ n cá»§a tÃ i khoáº£n email. Passkey vÃ  sinh tráº¯c há»c cÃ³ thá»ƒ mang láº¡i má»©c báº£o vá»‡ máº¡nh hÆ¡n vÃ  tráº£i nghiá»‡m mÆ°á»£t hÆ¡n, nhÆ°ng má»©c Ä‘á»™ Ã¡p dá»¥ng cÃ²n phá»¥ thuá»™c vÃ o thiáº¿t bá»‹ vÃ  thÃ³i quen ngÆ°á»i dÃ¹ng.

BÃ i viáº¿t nháº¥n máº¡nh ráº±ng xÃ¡c thá»±c khÃ´ng nÃªn lÃ  má»™t mÃ´ hÃ¬nh cá»‘ Ä‘á»‹nh. Tá»• chá»©c cáº§n cÃ³ kháº£ nÄƒng Ä‘iá»u chá»‰nh phÆ°Æ¡ng thá»©c xÃ¡c thá»±c dá»±a trÃªn rá»§i ro, chi phÃ­ vÃ  nhu cáº§u ngÆ°á»i dÃ¹ng.

VÃ­ dá»¥, doanh nghiá»‡p cÃ³ thá»ƒ chá»n WhatsApp OTP á»Ÿ má»™t sá»‘ khu vá»±c Ä‘á»ƒ giáº£m chi phÃ­ hoáº·c cáº£i thiá»‡n kháº£ nÄƒng gá»­i mÃ£. Äá»‘i vá»›i hÃ nh Ä‘á»™ng rá»§i ro cao, há»‡ thá»‘ng cÃ³ thá»ƒ yÃªu cáº§u phÆ°Æ¡ng thá»©c máº¡nh hÆ¡n nhÆ° passkey, sinh tráº¯c há»c hoáº·c khÃ³a báº£o máº­t pháº§n cá»©ng.

![Blog 2](/TranKhanhTam_AWS_Template/images/3-Blog/Blog-2.png)

## 9. Lá»£i Ã­ch cá»§a xÃ¡c thá»±c thÃ­ch á»©ng vÃ  xÃ¡c thá»±c liÃªn tá»¥c

XÃ¡c thá»±c thÃ­ch á»©ng vÃ  xÃ¡c thá»±c liÃªn tá»¥c Ä‘em láº¡i nhiá»u lá»£i Ã­ch quan trá»ng.

Thá»© nháº¥t, chÃºng giáº£m ma sÃ¡t cho ngÆ°á»i dÃ¹ng. NgÆ°á»i dÃ¹ng khÃ´ng bá»‹ Ã©p thá»±c hiá»‡n MFA cho má»i hÃ nh Ä‘á»™ng rá»§i ro tháº¥p. Äiá»u nÃ y giÃºp á»©ng dá»¥ng dá»… sá»­ dá»¥ng hÆ¡n vÃ  cáº£i thiá»‡n tráº£i nghiá»‡m tá»•ng thá»ƒ.

Thá»© hai, chÃºng tÄƒng cÆ°á»ng báº£o máº­t. Há»‡ thá»‘ng cÃ³ thá»ƒ yÃªu cáº§u xÃ¡c minh máº¡nh hÆ¡n khi rá»§i ro cao hÆ¡n. Nhá» Ä‘Ã³, má»©c báº£o máº­t Ä‘Æ°á»£c tÄƒng Ä‘Ãºng lÃºc cáº§n thiáº¿t.

Thá»© ba, chÃºng há»— trá»£ sá»± linh hoáº¡t trong kinh doanh. Rule cÃ³ thá»ƒ Ä‘Æ°á»£c Ä‘iá»u chá»‰nh dá»±a trÃªn máº«u gian láº­n, hÃ nh vi ngÆ°á»i dÃ¹ng, yÃªu cáº§u tuÃ¢n thá»§ hoáº·c chÃ­nh sÃ¡ch doanh nghiá»‡p.

Thá»© tÆ°, chÃºng cáº£i thiá»‡n kháº£ nÄƒng kiá»ƒm soÃ¡t váº­n hÃ nh. Vá»›i rules engine vÃ  authentication timeline, quáº£n trá»‹ viÃªn cÃ³ thá»ƒ theo dÃµi hoáº¡t Ä‘á»™ng xÃ¡c thá»±c vÃ  cáº­p nháº­t policy dá»±a trÃªn dá»¯ liá»‡u sá»­ dá»¥ng thá»±c táº¿.

Cuá»‘i cÃ¹ng, chÃºng há»— trá»£ phÃ²ng chá»‘ng gian láº­n tá»‘t hÆ¡n. CÃ¡c láº§n Ä‘Äƒng nháº­p Ä‘Ã¡ng ngá», thiáº¿t bá»‹ láº¡, vá»‹ trÃ­ báº¥t thÆ°á»ng vÃ  giao dá»‹ch rá»§i ro cao cÃ³ thá»ƒ tá»± Ä‘á»™ng kÃ­ch hoáº¡t xÃ¡c minh máº¡nh hÆ¡n.

## 10. BÃ i há»c chÃ­nh tá»« bÃ i viáº¿t

BÃ i há»c chÃ­nh tá»« bÃ i viáº¿t lÃ  xÃ¡c thá»±c khÃ´ng nÃªn Ä‘Æ°á»£c thiáº¿t káº¿ nhÆ° má»™t quy trÃ¬nh cá»‘ Ä‘á»‹nh vÃ  cá»©ng nháº¯c. Má»™t tráº£i nghiá»‡m xÃ¡c thá»±c tá»‘t cáº§n thay Ä‘á»•i dá»±a trÃªn ngá»¯ cáº£nh ngÆ°á»i dÃ¹ng, má»©c Ä‘á»™ rá»§i ro vÃ  yÃªu cáº§u kinh doanh.

CÃ¡c bÃ i há»c quan trá»ng gá»“m:

- Báº£o máº­t máº¡nh khÃ´ng pháº£i lÃºc nÃ o cÅ©ng Ä‘á»“ng nghÄ©a vá»›i nhiá»u rÃ o cáº£n.
- MFA nÃªn Ä‘Æ°á»£c Ã¡p dá»¥ng thÃ´ng minh, khÃ´ng nÃªn Ã¡p dá»¥ng mÃ¡y mÃ³c.
- Risk signals giÃºp há»‡ thá»‘ng quyáº¿t Ä‘á»‹nh khi nÃ o cáº§n yÃªu cáº§u xÃ¡c thá»±c thÃªm.
- XÃ¡c thá»±c nÃªn tiáº¿p tá»¥c sau Ä‘Äƒng nháº­p Ä‘á»‘i vá»›i cÃ¡c hÃ nh Ä‘á»™ng nháº¡y cáº£m.
- Amazon Cognito cÃ³ thá»ƒ cung cáº¥p ná»n táº£ng Ä‘á»‹nh danh.
- Authsignal cÃ³ thá»ƒ cung cáº¥p rule thÃ­ch á»©ng vÃ  Ä‘iá»u phá»‘i xÃ¡c thá»±c.
- CÃ¡c phÆ°Æ¡ng thá»©c xÃ¡c thá»±c khÃ¡c nhau nÃªn Ä‘Æ°á»£c chá»n theo rá»§i ro vÃ  nhu cáº§u ngÆ°á»i dÃ¹ng.
- Má»™t há»‡ thá»‘ng xÃ¡c thá»±c tá»‘t cáº§n cÃ¢n báº±ng báº£o máº­t, tráº£i nghiá»‡m, chi phÃ­ vÃ  tÃ­nh linh hoáº¡t.

## 11. á»¨ng dá»¥ng thá»±c táº¿

Nhá»¯ng Ã½ tÆ°á»Ÿng trong bÃ i viáº¿t cÃ³ thá»ƒ Ä‘Æ°á»£c Ã¡p dá»¥ng cho nhiá»u á»©ng dá»¥ng yÃªu cáº§u cáº£ báº£o máº­t máº¡nh vÃ  tráº£i nghiá»‡m ngÆ°á»i dÃ¹ng mÆ°á»£t mÃ . VÃ­ dá»¥ gá»“m á»©ng dá»¥ng y táº¿, ngÃ¢n hÃ ng, thÆ°Æ¡ng máº¡i Ä‘iá»‡n tá»­, ná»n táº£ng SaaS quáº£n trá»‹ vÃ  á»©ng dá»¥ng doanh nghiá»‡p.

Äá»‘i vá»›i hÃ nh Ä‘á»™ng rá»§i ro tháº¥p, á»©ng dá»¥ng cÃ³ thá»ƒ cho phÃ©p ngÆ°á»i dÃ¹ng tiáº¿p tá»¥c mÃ  khÃ´ng cáº§n xÃ¡c minh thÃªm. Äá»‘i vá»›i hÃ nh Ä‘á»™ng rá»§i ro cao, á»©ng dá»¥ng cÃ³ thá»ƒ yÃªu cáº§u xÃ¡c thá»±c máº¡nh hÆ¡n. Äiá»u nÃ y táº¡o ra tráº£i nghiá»‡m cÃ¢n báº±ng hÆ¡n.

Thay vÃ¬ xem má»i ngÆ°á»i dÃ¹ng vÃ  má»i thao tÃ¡c lÃ  giá»‘ng nhau, xÃ¡c thá»±c thÃ­ch á»©ng cho phÃ©p há»‡ thá»‘ng Ä‘Æ°a ra quyáº¿t Ä‘á»‹nh thÃ´ng minh hÆ¡n. Äiá»u nÃ y giÃºp doanh nghiá»‡p giáº£m ma sÃ¡t nhÆ°ng váº«n báº£o vá»‡ cÃ¡c hÃ nh Ä‘á»™ng vÃ  dá»¯ liá»‡u nháº¡y cáº£m.

XÃ¡c thá»±c liÃªn tá»¥c cÅ©ng ráº¥t quan trá»ng vÃ¬ báº£o máº­t khÃ´ng nÃªn dá»«ng láº¡i sau khi Ä‘Äƒng nháº­p. Má»™t phiÃªn lÃ m viá»‡c cÃ³ thá»ƒ trá»Ÿ nÃªn rá»§i ro vá» sau, Ä‘áº·c biá»‡t khi ngÆ°á»i dÃ¹ng thá»±c hiá»‡n cÃ¡c hÃ nh Ä‘á»™ng nháº¡y cáº£m. Step-up authentication giÃºp báº£o vá»‡ nhá»¯ng thá»i Ä‘iá»ƒm quan trá»ng nÃ y.

## 12. Káº¿t luáº­n

BÃ i viáº¿t nÃ y há»¯u Ã­ch vÃ¬ cho tháº¥y thiáº¿t káº¿ xÃ¡c thá»±c khÃ´ng chá»‰ lÃ  thÃªm nhiá»u lá»›p báº£o máº­t. Äiá»u quan trá»ng lÃ  Ã¡p dá»¥ng Ä‘Ãºng lá»›p báº£o máº­t vÃ o Ä‘Ãºng thá»i Ä‘iá»ƒm.

Má»™t há»‡ thá»‘ng xÃ¡c thá»±c tá»‘t cáº§n báº£o vá»‡ tÃ i khoáº£n nhÆ°ng khÃ´ng lÃ m má»i tÆ°Æ¡ng tÃ¡c trá»Ÿ nÃªn khÃ³ khÄƒn. Amazon Cognito vÃ  Authsignal cÃ³ thá»ƒ phá»‘i há»£p Ä‘á»ƒ há»— trá»£ má»¥c tiÃªu nÃ y báº±ng cÃ¡ch káº¿t há»£p quáº£n lÃ½ Ä‘á»‹nh danh, Ä‘Ã¡nh giÃ¡ rá»§i ro, ra quyáº¿t Ä‘á»‹nh dá»±a trÃªn rule vÃ  cÃ¡c phÆ°Æ¡ng thá»©c xÃ¡c thá»±c linh hoáº¡t.

NhÃ¬n chung, bÃ i viáº¿t Ä‘Æ°a ra má»™t hÆ°á»›ng thiáº¿t káº¿ thá»±c táº¿ Ä‘á»ƒ xÃ¢y dá»±ng tráº£i nghiá»‡m xÃ¡c thá»±c tá»‘t hÆ¡n. NÃ³ cho tháº¥y tráº£i nghiá»‡m báº£o máº­t tá»‘t nháº¥t khÃ´ng pháº£i lÃºc nÃ o cÅ©ng lÃ  tráº£i nghiá»‡m nghiÃªm ngáº·t nháº¥t, mÃ  lÃ  tráº£i nghiá»‡m cÃ³ kháº£ nÄƒng thÃ­ch á»©ng vá»›i rá»§i ro, hÃ nh vi ngÆ°á»i dÃ¹ng vÃ  nhu cáº§u kinh doanh.

## Link bÃ i viáº¿t gá»‘c

AWS Partner Network Blog:  
**Creating great authentication experiences with Amazon Cognito and Authsignal**

https://aws.amazon.com/blogs/apn/creating-great-authentication-experiences-with-amazon-cognito-and-authsignal/

## CÃ¢u há»i tháº£o luáº­n

Báº¡n Ä‘Ã£ tá»«ng thiáº¿t káº¿ há»‡ thá»‘ng xÃ¡c thá»±c cÃ¢n báº±ng giá»¯a báº£o máº­t vÃ  tráº£i nghiá»‡m ngÆ°á»i dÃ¹ng chÆ°a? Theo báº¡n, pháº§n thÃ¡ch thá»©c nháº¥t lÃ  giáº£m rÃ o cáº£n Ä‘Äƒng nháº­p cho ngÆ°á»i dÃ¹ng bÃ¬nh thÆ°á»ng hay tÄƒng cÆ°á»ng báº£o vá»‡ cho cÃ¡c hÃ nh Ä‘á»™ng rá»§i ro cao?
