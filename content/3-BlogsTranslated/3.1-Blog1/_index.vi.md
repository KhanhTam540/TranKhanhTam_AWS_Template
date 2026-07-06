---
title: "Blog 1"
date: 2026-07-05
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---


# ÄÆ¡n giáº£n hÃ³a mÃ£ hÃ³a Ä‘a thuÃª má»¥c vá»›i chiáº¿n lÆ°á»£c AWS KMS Key tá»‘i Æ°u chi phÃ­

Trong cÃ¡c á»©ng dá»¥ng SaaS hiá»‡n Ä‘áº¡i, báº£o vá»‡ dá»¯ liá»‡u lÃ  má»™t trong nhá»¯ng yÃªu cáº§u kiáº¿n trÃºc quan trá»ng nháº¥t. Má»™t há»‡ thá»‘ng SaaS thÆ°á»ng phá»¥c vá»¥ nhiá»u khÃ¡ch hÃ ng cÃ¹ng lÃºc. Má»—i khÃ¡ch hÃ ng Ä‘Æ°á»£c xem lÃ  má»™t tenant riÃªng, vÃ  má»—i tenant Ä‘á»u yÃªu cáº§u dá»¯ liá»‡u cá»§a mÃ¬nh pháº£i Ä‘Æ°á»£c cÃ´ láº­p vá»›i cÃ¡c tenant khÃ¡c.

Äiá»u nÃ y cÃ³ nghÄ©a lÃ  máº·c dÃ¹ nhiá»u tenant cÃ³ thá»ƒ dÃ¹ng chung cÃ¹ng má»™t háº¡ táº§ng á»©ng dá»¥ng, dá»¯ liá»‡u cá»§a há» váº«n pháº£i Ä‘Æ°á»£c báº£o vá»‡ vÃ  phÃ¢n tÃ¡ch rÃµ rÃ ng. Äá»ƒ lÃ m Ä‘Æ°á»£c Ä‘iá»u Ä‘Ã³, mÃ£ hÃ³a thÆ°á»ng Ä‘Æ°á»£c sá»­ dá»¥ng nhÆ° má»™t lá»›p báº£o máº­t quan trá»ng. AWS Key Management Service, hay AWS KMS, giÃºp tá»• chá»©c táº¡o, quáº£n lÃ½ vÃ  kiá»ƒm soÃ¡t cÃ¡c khÃ³a mÃ£ hÃ³a cho workload trÃªn AWS.

Tuy nhiÃªn, thiáº¿t káº¿ mÃ£ hÃ³a cho há»‡ thá»‘ng Ä‘a thuÃª má»¥c khÃ´ng chá»‰ lÃ  bÃ i toÃ¡n báº£o máº­t. ÄÃ¢y cÃ²n lÃ  bÃ i toÃ¡n vá» chi phÃ­, kháº£ nÄƒng má»Ÿ rá»™ng vÃ  váº­n hÃ nh. Náº¿u thiáº¿t káº¿ khÃ´ng há»£p lÃ½, chi phÃ­ KMS vÃ  Ä‘á»™ phá»©c táº¡p quáº£n lÃ½ cÃ³ thá»ƒ tÄƒng ráº¥t nhanh khi sá»‘ lÆ°á»£ng tenant phÃ¡t triá»ƒn.

BÃ i viáº¿t AWS **â€œSimplify multi-tenant encryption with a cost-conscious AWS KMS key strategyâ€** trÃ¬nh bÃ y cÃ¡ch xÃ¢y dá»±ng mÃ´ hÃ¬nh mÃ£ hÃ³a Ä‘a thuÃª má»¥c hiá»‡u quáº£ hÆ¡n. Thay vÃ¬ cáº¥p má»™t KMS Customer Managed Key riÃªng cho má»i tenant, bÃ i viáº¿t Ä‘á» xuáº¥t cÃ¡ch tiáº¿p cáº­n cÃ¢n báº±ng hÆ¡n báº±ng cÃ¡ch káº¿t há»£p phÃ¢n táº§ng tenant, key dÃ¹ng chung, Encryption Context, chÃ­nh sÃ¡ch truy cáº­p Ä‘á»™ng, audit log vÃ  tá»‘i Æ°u chi phÃ­ lÆ°u trá»¯.

## 1. ThÃ¡ch thá»©c cá»§a mÃ£ hÃ³a Ä‘a thuÃª má»¥c

Trong há»‡ thá»‘ng SaaS Ä‘a thuÃª má»¥c, nhiá»u khÃ¡ch hÃ ng thÆ°á»ng dÃ¹ng chung háº¡ táº§ng nhÆ° API, database, storage vÃ  backend service. Tuy nhiÃªn, dÃ¹ háº¡ táº§ng Ä‘Æ°á»£c dÃ¹ng chung, dá»¯ liá»‡u khÃ¡ch hÃ ng khÃ´ng Ä‘Æ°á»£c phÃ©p dÃ¹ng chung. ÄÃ¢y lÃ  yÃªu cáº§u báº£o máº­t cá»‘t lÃµi: má»—i tenant chá»‰ Ä‘Æ°á»£c phÃ©p truy cáº­p dá»¯ liá»‡u cá»§a chÃ­nh mÃ¬nh.

Má»™t cÃ¡ch tiáº¿p cáº­n phá»• biáº¿n lÃ  táº¡o riÃªng má»™t AWS KMS Customer Managed Key cho tá»«ng tenant. CÃ¡ch nÃ y Ä‘em láº¡i má»©c cÃ´ láº­p cao vÃ¬ má»—i tenant cÃ³ má»™t khÃ³a mÃ£ hÃ³a riÃªng. Tuy nhiÃªn, khi sá»‘ lÆ°á»£ng tenant tÄƒng lÃªn, cÃ¡ch lÃ m nÃ y cÃ³ thá»ƒ trá»Ÿ nÃªn tá»‘n kÃ©m vÃ  khÃ³ quáº£n lÃ½.

VÃ­ dá»¥, náº¿u má»™t ná»n táº£ng SaaS chá»‰ cÃ³ vÃ i tenant, viá»‡c quáº£n lÃ½ má»™t KMS Key cho má»—i tenant cÃ³ thá»ƒ khÃ¡ Ä‘Æ¡n giáº£n. NhÆ°ng khi há»‡ thá»‘ng phÃ¡t triá»ƒn lÃªn hÃ ng trÄƒm hoáº·c hÃ ng nghÃ¬n tenant, sá»‘ lÆ°á»£ng key, policy, audit log vÃ  cÃ´ng viá»‡c váº­n hÃ nh cÅ©ng tÄƒng theo. Äiá»u nÃ y lÃ m tÄƒng chi phÃ­ cá»‘ Ä‘á»‹nh hÃ ng thÃ¡ng vÃ  táº¡o thÃªm gÃ¡nh náº·ng váº­n hÃ nh.

BÃ i viáº¿t nháº¥n máº¡nh ráº±ng má»™t chiáº¿n lÆ°á»£c mÃ£ hÃ³a tá»‘t cáº§n cÃ¢n báº±ng ba yáº¿u tá»‘ quan trá»ng:

- Báº£o máº­t vÃ  cÃ´ láº­p tenant
- Tá»‘i Æ°u chi phÃ­
- Kháº£ nÄƒng má»Ÿ rá»™ng trong váº­n hÃ nh

Äiá»u nÃ y cÃ³ nghÄ©a lÃ  há»‡ thá»‘ng khÃ´ng nÃªn Ã¡p dá»¥ng duy nháº¥t má»™t mÃ´ hÃ¬nh mÃ£ hÃ³a cho táº¥t cáº£ tenant. Thay vÃ o Ä‘Ã³, chiáº¿n lÆ°á»£c mÃ£ hÃ³a cáº§n Ä‘Æ°á»£c thiáº¿t káº¿ dá»±a trÃªn yÃªu cáº§u cá»§a tá»«ng nhÃ³m tenant, giÃ¡ trá»‹ kinh doanh, yÃªu cáº§u tuÃ¢n thá»§ vÃ  Ä‘á»™ nháº¡y cáº£m cá»§a dá»¯ liá»‡u.

## 2. Chiáº¿n lÆ°á»£c AWS KMS Key chÃº trá»ng chi phÃ­

Khuyáº¿n nghá»‹ chÃ­nh cá»§a bÃ i viáº¿t lÃ  sá»­ dá»¥ng **chiáº¿n lÆ°á»£c KMS Key chÃº trá»ng chi phÃ­**. Äiá»u nÃ y cÃ³ nghÄ©a lÃ  há»‡ thá»‘ng khÃ´ng nÃªn máº·c Ä‘á»‹nh táº¡o key riÃªng cho má»i tenant. Thay vÃ o Ä‘Ã³, tenant nÃªn Ä‘Æ°á»£c chia thÃ nh nhiá»u táº§ng dá»‹ch vá»¥ khÃ¡c nhau.

Äá»‘i vá»›i khÃ¡ch hÃ ng cÃ³ giÃ¡ trá»‹ cao nhÆ° Enterprise hoáº·c Premium, má»™t KMS Key riÃªng cÃ³ thá»ƒ lÃ  cáº§n thiáº¿t. Nhá»¯ng khÃ¡ch hÃ ng nÃ y cÃ³ thá»ƒ yÃªu cáº§u má»©c Ä‘á»™ cÃ´ láº­p dá»¯ liá»‡u cao hÆ¡n, tiÃªu chuáº©n tuÃ¢n thá»§ nghiÃªm ngáº·t hÆ¡n hoáº·c cÃ¡c thá»a thuáº­n báº£o máº­t riÃªng. KMS Key riÃªng giÃºp Ä‘Ã¡p á»©ng tá»‘t hÆ¡n nhá»¯ng yÃªu cáº§u Ä‘Ã³.

Äá»‘i vá»›i khÃ¡ch hÃ ng Standard hoáº·c Free, mÃ´ hÃ¬nh dÃ¹ng chung KMS Key cÃ³ thá»ƒ phÃ¹ há»£p hÆ¡n. Nhá»¯ng tenant nÃ y cÃ³ thá»ƒ sá»­ dá»¥ng má»™t nhÃ³m KMS Key chung Ä‘á»ƒ giáº£m chi phÃ­ vÃ  Ä‘Æ¡n giáº£n hÃ³a quáº£n lÃ½. Há»‡ thá»‘ng váº«n cÃ³ thá»ƒ báº£o vá»‡ dá»¯ liá»‡u tenant báº±ng cÃ¡c cÆ¡ cháº¿ bá»• sung nhÆ° Encryption Context.

Chiáº¿n lÆ°á»£c phÃ¢n táº§ng nÃ y giÃºp nhÃ  cung cáº¥p SaaS trÃ¡nh chi phÃ­ khÃ´ng cáº§n thiáº¿t nhÆ°ng váº«n Ä‘áº£m báº£o má»©c báº£o vá»‡ cao cho nhá»¯ng khÃ¡ch hÃ ng cáº§n nÃ³. Äá»“ng thá»i, kiáº¿n trÃºc cÅ©ng dá»… má»Ÿ rá»™ng hÆ¡n vÃ¬ sá»‘ lÆ°á»£ng KMS Key khÃ´ng tÄƒng cÃ¹ng tá»‘c Ä‘á»™ vá»›i sá»‘ lÆ°á»£ng tenant.

MÃ´ hÃ¬nh Ä‘Æ¡n giáº£n cÃ³ thá»ƒ Ä‘Æ°á»£c mÃ´ táº£ nhÆ° sau:

```text
Enterprise Tier  â†’ KMS Key riÃªng cho tá»«ng tenant
Standard Tier    â†’ KMS Key dÃ¹ng chung káº¿t há»£p tenant-specific context
Free Tier        â†’ KMS Key dÃ¹ng chung káº¿t há»£p policy kiá»ƒm soÃ¡t truy cáº­p
```

CÃ¡ch tiáº¿p cáº­n nÃ y giÃºp há»‡ thá»‘ng linh hoáº¡t hÆ¡n. Thay vÃ¬ chá»‰ chá»n giá»¯a â€œmá»™t key cho táº¥t cáº£â€ hoáº·c â€œmá»™t key cho má»—i tenantâ€, kiáº¿n trÃºc cÃ³ thá»ƒ sá»­ dá»¥ng nhiá»u chiáº¿n lÆ°á»£c key khÃ¡c nhau cho tá»«ng nhÃ³m khÃ¡ch hÃ ng.

## 3. Sá»­ dá»¥ng Encryption Context Ä‘á»ƒ cÃ´ láº­p tenant

Khi nhiá»u tenant dÃ¹ng chung má»™t KMS Key, há»‡ thá»‘ng váº«n cáº§n ngÄƒn cháº·n truy cáº­p chÃ©o dá»¯ liá»‡u. ÄÃ¢y lÃ  lÃºc **Encryption Context** trá»Ÿ nÃªn ráº¥t quan trá»ng.

Encryption Context lÃ  metadata dáº¡ng key-value Ä‘Æ°á»£c gá»­i Ä‘áº¿n AWS KMS trong quÃ¡ trÃ¬nh mÃ£ hÃ³a vÃ  giáº£i mÃ£. VÃ­ dá»¥, khi mÃ£ hÃ³a dá»¯ liá»‡u cho má»™t tenant, á»©ng dá»¥ng cÃ³ thá»ƒ gá»­i kÃ¨m mÃ£ Ä‘á»‹nh danh tenant vÃ o context.

VÃ­ dá»¥:

```text
TenantID = tenant-a
```

Khi dá»¯ liá»‡u Ä‘Ã£ mÃ£ hÃ³a Ä‘Æ°á»£c giáº£i mÃ£ sau Ä‘Ã³, há»‡ thá»‘ng pháº£i cung cáº¥p Ä‘Ãºng Encryption Context tÆ°Æ¡ng á»©ng. Náº¿u request sá»­ dá»¥ng TenantID khÃ¡c, thao tÃ¡c cÃ³ thá»ƒ bá»‹ tá»« chá»‘i dá»±a trÃªn cÃ¡c Ä‘iá»u kiá»‡n policy.

Äiá»u nÃ y táº¡o thÃªm má»™t lá»›p cÃ´ láº­p logic. DÃ¹ nhiá»u tenant dÃ¹ng chung má»™t KMS Key, má»—i thao tÃ¡c mÃ£ hÃ³a vÃ  giáº£i mÃ£ váº«n cÃ³ thá»ƒ Ä‘Æ°á»£c gáº¯n vá»›i má»™t tenant cá»¥ thá»ƒ.

VÃ­ dá»¥ Ä‘Æ¡n giáº£n:

```text
Tenant A mÃ£ hÃ³a dá»¯ liá»‡u vá»›i:
TenantID = tenant-a

Tenant B cá»‘ gáº¯ng giáº£i mÃ£ cÃ¹ng dá»¯ liá»‡u Ä‘Ã³ vá»›i:
TenantID = tenant-b

Request bá»‹ tá»« chá»‘i vÃ¬ Encryption Context khÃ´ng khá»›p.
```

CÃ¡ch lÃ m nÃ y ráº¥t há»¯u Ã­ch trong cÃ¡c há»‡ thá»‘ng Ä‘a thuÃª má»¥c vÃ¬ nÃ³ giÃºp giáº£m nhu cáº§u táº¡o key riÃªng cho má»i tenant nhÆ°ng váº«n duy trÃ¬ kháº£ nÄƒng báº£o vá»‡ theo tá»«ng tenant.

Encryption Context cÅ©ng giÃºp tÄƒng kháº£ nÄƒng truy váº¿t. VÃ¬ thÃ´ng tin context cÃ³ thá»ƒ xuáº¥t hiá»‡n trong log, há»‡ thá»‘ng dá»… xÃ¡c Ä‘á»‹nh tenant nÃ o liÃªn quan Ä‘áº¿n má»™t request mÃ£ hÃ³a hoáº·c giáº£i mÃ£ cá»¥ thá»ƒ.

## 4. Giáº£m gÃ¡nh náº·ng váº­n hÃ nh báº±ng chÃ­nh sÃ¡ch truy cáº­p Ä‘á»™ng

Má»™t ná»n táº£ng SaaS lá»›n cÃ³ thá»ƒ cÃ³ ráº¥t nhiá»u tenant. Náº¿u quáº£n trá»‹ viÃªn pháº£i tá»± táº¡o policy thá»§ cÃ´ng cho tá»«ng tenant, há»‡ thá»‘ng sáº½ nhanh chÃ³ng trá»Ÿ nÃªn khÃ³ váº­n hÃ nh. Quáº£n lÃ½ policy thá»§ cÃ´ng cÅ©ng lÃ m tÄƒng nguy cÆ¡ sai sÃ³t do con ngÆ°á»i.

BÃ i viáº¿t giáº£i thÃ­ch ráº±ng **dynamic IAM policies** vÃ  policy variables cÃ³ thá»ƒ giÃºp giáº£m gÃ¡nh náº·ng nÃ y. Vá»›i policy Ä‘á»™ng, quyá»n truy cáº­p cÃ³ thá»ƒ Ä‘Æ°á»£c Ä‘Ã¡nh giÃ¡ dá»±a trÃªn cÃ¡c giÃ¡ trá»‹ táº¡i thá»i Ä‘iá»ƒm thá»±c thi, cháº³ng háº¡n nhÆ° mÃ£ Ä‘á»‹nh danh tenant. Äiá»u nÃ y cho phÃ©p há»‡ thá»‘ng táº¡o cÃ¡c quy táº¯c truy cáº­p linh hoáº¡t thay vÃ¬ duy trÃ¬ sá»‘ lÆ°á»£ng lá»›n policy tÄ©nh.

VÃ­ dá»¥, thay vÃ¬ táº¡o má»™t policy cho Tenant A, má»™t policy khÃ¡c cho Tenant B vÃ  má»™t policy khÃ¡c ná»¯a cho Tenant C, há»‡ thá»‘ng cÃ³ thá»ƒ Ä‘á»‹nh nghÄ©a má»™t máº«u policy tÃ¡i sá»­ dá»¥ng Ä‘á»ƒ kiá»ƒm tra request cÃ³ thuá»™c Ä‘Ãºng tenant hay khÃ´ng.

CÃ¡ch tiáº¿p cáº­n nÃ y Ä‘em láº¡i nhiá»u lá»£i Ã­ch:

- Giáº£m sá»‘ lÆ°á»£ng policy cáº§n quáº£n lÃ½
- Giáº£m nguy cÆ¡ lá»—i cáº¥u hÃ¬nh thá»§ cÃ´ng
- Dá»… onboard tenant má»›i
- Dá»… má»Ÿ rá»™ng khi sá»‘ lÆ°á»£ng tenant tÄƒng
- Quy táº¯c truy cáº­p nháº¥t quÃ¡n hÆ¡n

Thiáº¿t káº¿ policy Ä‘á»™ng Ä‘áº·c biá»‡t quan trá»ng vá»›i há»‡ thá»‘ng SaaS vÃ¬ tenant cÃ³ thá»ƒ Ä‘Æ°á»£c táº¡o, cáº­p nháº­t hoáº·c xÃ³a thÆ°á»ng xuyÃªn. Tá»± Ä‘á»™ng hÃ³a giÃºp mÃ´ hÃ¬nh báº£o máº­t phÃ¡t triá»ƒn cÃ¹ng vá»›i á»©ng dá»¥ng.

## 5. Audit vÃ  minh báº¡ch vá»›i AWS CloudTrail

MÃ£ hÃ³a thÃ´i lÃ  chÆ°a Ä‘á»§ cho má»™t kiáº¿n trÃºc an toÃ n. Há»‡ thá»‘ng cÅ©ng cáº§n kháº£ nÄƒng quan sÃ¡t cÃ¡ch cÃ¡c khÃ³a mÃ£ hÃ³a Ä‘Æ°á»£c sá»­ dá»¥ng. AWS CloudTrail giÃºp cung cáº¥p kháº£ nÄƒng quan sÃ¡t nÃ y báº±ng cÃ¡ch ghi láº¡i cÃ¡c hÃ nh Ä‘á»™ng quan trá»ng liÃªn quan Ä‘áº¿n AWS KMS.

CloudTrail cÃ³ thá»ƒ ghi log cÃ¡c hoáº¡t Ä‘á»™ng nhÆ°:

- Táº¡o key
- Sá»­ dá»¥ng key
- Request mÃ£ hÃ³a
- Request giáº£i mÃ£
- Thay Ä‘á»•i policy
- Sá»± kiá»‡n bá»‹ tá»« chá»‘i truy cáº­p

Nhá»¯ng log nÃ y ráº¥t quan trá»ng cho kiá»ƒm toÃ¡n báº£o máº­t vÃ  tuÃ¢n thá»§. ChÃºng giÃºp quáº£n trá»‹ viÃªn tráº£ lá»i cÃ¡c cÃ¢u há»i nhÆ°:

- Ai Ä‘Ã£ sá»­ dá»¥ng má»™t KMS Key cá»¥ thá»ƒ?
- Dá»¯ liá»‡u Ä‘Æ°á»£c mÃ£ hÃ³a hoáº·c giáº£i mÃ£ khi nÃ o?
- Tenant nÃ o liÃªn quan Ä‘áº¿n request Ä‘Ã³?
- Request thÃ nh cÃ´ng hay bá»‹ tá»« chá»‘i?
- CÃ³ máº«u truy cáº­p báº¥t thÆ°á»ng nÃ o khÃ´ng?

Äá»‘i vá»›i nhÃ  cung cáº¥p SaaS, CloudTrail logs cÅ©ng cÃ³ thá»ƒ há»— trá»£ chargeback hoáº·c phÃ¢n bá»• chi phÃ­. Náº¿u há»‡ thá»‘ng ghi nháº­n context liÃªn quan Ä‘áº¿n tenant, doanh nghiá»‡p cÃ³ thá»ƒ hiá»ƒu cÃ¡ch tá»«ng tenant sá»­ dá»¥ng tÃ i nguyÃªn vÃ  phÃ¢n bá»• chi phÃ­ chÃ­nh xÃ¡c hÆ¡n.

Äiá»u nÃ y giÃºp tÄƒng tÃ­nh minh báº¡ch vÃ  há»— trá»£ doanh nghiá»‡p Ä‘Æ°a ra quyáº¿t Ä‘á»‹nh váº­n hÃ nh tá»‘t hÆ¡n.

## 6. Tá»‘i Æ°u hiá»‡u nÄƒng vÃ  chi phÃ­ vá»›i Amazon EBS gp3

BÃ i viáº¿t cÅ©ng Ä‘á» cáº­p Ä‘áº¿n Amazon EBS gp3 nhÆ° má»™t pháº§n trong chiáº¿n lÆ°á»£c tá»‘i Æ°u hiá»‡u nÄƒng vÃ  chi phÃ­. Trong má»™t sá»‘ workload, lÆ°u trá»¯ mÃ£ hÃ³a cáº§n cung cáº¥p hiá»‡u nÄƒng cao. Tuy nhiÃªn, viá»‡c chá»n sai loáº¡i lÆ°u trá»¯ hoáº·c cáº¥p phÃ¡t dÆ° dung lÆ°á»£ng cÃ³ thá»ƒ lÃ m tÄƒng chi phÃ­.

Amazon EBS gp3 cho phÃ©p cáº¥u hÃ¬nh dung lÆ°á»£ng lÆ°u trá»¯ vÃ  hiá»‡u nÄƒng má»™t cÃ¡ch Ä‘á»™c láº­p. Äiá»u nÃ y cÃ³ nghÄ©a lÃ  ngÆ°á»i dÃ¹ng cÃ³ thá»ƒ chá»n dung lÆ°á»£ng lÆ°u trá»¯ cáº§n thiáº¿t vÃ  cáº¥u hÃ¬nh riÃªng cÃ¡c thÃ´ng sá»‘ hiá»‡u nÄƒng nhÆ° IOPS vÃ  throughput.

Äiá»u nÃ y há»¯u Ã­ch vÃ¬ cÃ³ nhá»¯ng há»‡ thá»‘ng cáº§n hiá»‡u nÄƒng cao nhÆ°ng khÃ´ng nháº¥t thiáº¿t cáº§n dung lÆ°á»£ng lÆ°u trá»¯ lá»›n. Vá»›i gp3, tá»• chá»©c cÃ³ thá»ƒ trÃ¡nh tráº£ tiá»n cho dung lÆ°á»£ng khÃ´ng cáº§n thiáº¿t chá»‰ Ä‘á»ƒ Ä‘áº¡t hiá»‡u nÄƒng tá»‘t hÆ¡n.

Ã chÃ­nh á»Ÿ Ä‘Ã¢y lÃ  chiáº¿n lÆ°á»£c mÃ£ hÃ³a khÃ´ng nÃªn Ä‘Æ°á»£c thiáº¿t káº¿ tÃ¡ch rá»i khá»i chi phÃ­ háº¡ táº§ng. Storage, key management, audit logs vÃ  access control nÃªn Ä‘Æ°á»£c xem xÃ©t cÃ¹ng nhau khi thiáº¿t káº¿ kiáº¿n trÃºc SaaS vá»«a an toÃ n vá»«a tá»‘i Æ°u chi phÃ­.

![Blog 1](/TranKhanhTam_AWS_Template/images/3-Blog/Blog-1.png)

## 7. BÃ i há»c chÃ­nh tá»« bÃ i viáº¿t

BÃ i há»c quan trá»ng nháº¥t tá»« bÃ i viáº¿t lÃ  mÃ£ hÃ³a Ä‘a thuÃª má»¥c cáº§n má»™t thiáº¿t káº¿ cÃ¢n báº±ng. Báº£o máº­t lÃ  quan trá»ng, nhÆ°ng chi phÃ­ vÃ  váº­n hÃ nh cÅ©ng quan trá»ng khÃ´ng kÃ©m.

Náº¿u má»—i tenant Ä‘á»u cÃ³ KMS Key riÃªng, há»‡ thá»‘ng cÃ³ thá»ƒ trá»Ÿ nÃªn Ä‘áº¯t Ä‘á» vÃ  khÃ³ quáº£n lÃ½. Náº¿u táº¥t cáº£ tenant dÃ¹ng chung má»™t key mÃ  khÃ´ng cÃ³ lá»›p kiá»ƒm soÃ¡t bá»• sung, há»‡ thá»‘ng cÃ³ thá»ƒ khÃ´ng Ä‘á»§ kháº£ nÄƒng cÃ´ láº­p dá»¯ liá»‡u. VÃ¬ váº­y, cÃ¡ch tiáº¿p cáº­n tá»‘t nháº¥t lÃ  káº¿t há»£p nhiá»u ká»¹ thuáº­t khÃ¡c nhau.

CÃ¡c ká»¹ thuáº­t quan trá»ng gá»“m:

- Chia tenant thÃ nh cÃ¡c táº§ng dá»‹ch vá»¥
- Sá»­ dá»¥ng KMS Key riÃªng cho tenant Enterprise
- Sá»­ dá»¥ng KMS Key dÃ¹ng chung cho tenant Standard hoáº·c Free
- Ãp dá»¥ng Encryption Context Ä‘á»ƒ báº£o vá»‡ theo tenant
- DÃ¹ng policy Ä‘á»™ng Ä‘á»ƒ giáº£m thao tÃ¡c thá»§ cÃ´ng
- Ghi nháº­n hoáº¡t Ä‘á»™ng KMS báº±ng CloudTrail
- Tá»‘i Æ°u hiá»‡u nÄƒng vÃ  chi phÃ­ lÆ°u trá»¯ báº±ng lá»±a chá»n lÆ°u trá»¯ phÃ¹ há»£p

Äiá»u nÃ y cho tháº¥y kiáº¿n trÃºc mÃ£ hÃ³a cáº§n Ä‘Æ°á»£c thiáº¿t káº¿ dá»±a trÃªn yÃªu cáº§u kinh doanh thá»±c táº¿. KhÃ´ng pháº£i khÃ¡ch hÃ ng nÃ o cÅ©ng cáº§n cÃ¹ng má»™t mÃ´ hÃ¬nh báº£o máº­t, vÃ  khÃ´ng pháº£i workload nÃ o cÅ©ng cáº§n cÃ¹ng má»™t má»©c Ä‘á»™ cÃ´ láº­p.

## 8. á»¨ng dá»¥ng thá»±c táº¿

Nhá»¯ng Ã½ tÆ°á»Ÿng trong bÃ i viáº¿t cÃ³ thá»ƒ Ä‘Æ°á»£c Ã¡p dá»¥ng cho nhiá»u há»‡ thá»‘ng SaaS cáº§n báº£o vá»‡ dá»¯ liá»‡u khÃ¡ch hÃ ng á»Ÿ quy mÃ´ lá»›n. Má»™t doanh nghiá»‡p cung cáº¥p ná»n táº£ng SaaS cÃ³ thá»ƒ phá»¥c vá»¥ nhiá»u nhÃ³m khÃ¡ch hÃ ng khÃ¡c nhau, tá»« doanh nghiá»‡p nhá» Ä‘áº¿n cÃ¡c tá»• chá»©c Enterprise lá»›n. Má»—i nhÃ³m khÃ¡ch hÃ ng cÃ³ thá»ƒ cÃ³ yÃªu cáº§u khÃ¡c nhau vá» báº£o máº­t, tuÃ¢n thá»§ vÃ  chi phÃ­.

Äá»‘i vá»›i khÃ¡ch hÃ ng Enterprise, viá»‡c sá»­ dá»¥ng KMS Key riÃªng cÃ³ thá»ƒ giÃºp tÄƒng kháº£ nÄƒng cÃ´ láº­p dá»¯ liá»‡u vÃ  há»— trá»£ tá»‘t hÆ¡n cho cÃ¡c yÃªu cáº§u tuÃ¢n thá»§. Äá»‘i vá»›i khÃ¡ch hÃ ng Standard, viá»‡c dÃ¹ng chung KMS Key káº¿t há»£p vá»›i Encryption Context váº«n cÃ³ thá»ƒ Ä‘áº£m báº£o phÃ¢n tÃ¡ch dá»¯ liá»‡u vá» máº·t logic nhÆ°ng giÃºp giáº£m chi phÃ­.

Äiá»u nÃ y cho tháº¥y thiáº¿t káº¿ mÃ£ hÃ³a khÃ´ng nÃªn Ã¡p dá»¥ng má»™t mÃ´ hÃ¬nh cá»‘ Ä‘á»‹nh cho táº¥t cáº£ khÃ¡ch hÃ ng, mÃ  cáº§n linh hoáº¡t theo nhu cáº§u kinh doanh, yÃªu cáº§u cá»§a tenant vÃ  Ä‘á»™ nháº¡y cáº£m cá»§a dá»¯ liá»‡u.

Encryption Context cÅ©ng lÃ  má»™t ká»¹ thuáº­t quan trá»ng vÃ¬ nÃ³ cho phÃ©p gáº¯n metadata theo tá»«ng tenant vÃ o cÃ¡c thao tÃ¡c mÃ£ hÃ³a vÃ  giáº£i mÃ£. Nhá» Ä‘Ã³, ngay cáº£ khi nhiá»u tenant dÃ¹ng chung má»™t KMS Key, dá»¯ liá»‡u cá»§a há» váº«n cÃ³ thá»ƒ Ä‘Æ°á»£c phÃ¢n tÃ¡ch vá» máº·t logic.

Khi káº¿t há»£p vá»›i CloudTrail logs, há»‡ thá»‘ng cÃ³ thá»ƒ tÄƒng tÃ­nh minh báº¡ch, há»— trá»£ audit vÃ  nÃ¢ng cao kháº£ nÄƒng truy váº¿t. Äiá»u nÃ y ráº¥t quan trá»ng vá»›i cÃ¡c tá»• chá»©c cáº§n chá»©ng minh ráº±ng dá»¯ liá»‡u khÃ¡ch hÃ ng Ä‘Æ°á»£c báº£o vá»‡ vÃ  truy cáº­p Ä‘Æ°á»£c giÃ¡m sÃ¡t Ä‘Ãºng cÃ¡ch.

Má»™t Ä‘iá»ƒm thá»±c táº¿ khÃ¡c lÃ  chi phÃ­ cloud cáº§n Ä‘Æ°á»£c cÃ¢n nháº¯c ngay tá»« giai Ä‘oáº¡n thiáº¿t káº¿ kiáº¿n trÃºc. Náº¿u má»—i tenant Ä‘á»u Ä‘Æ°á»£c cáº¥p má»™t KMS Key riÃªng mÃ  khÃ´ng cÃ³ chiáº¿n lÆ°á»£c rÃµ rÃ ng, chi phÃ­ hÃ ng thÃ¡ng vÃ  Ä‘á»™ phá»©c táº¡p váº­n hÃ nh cÃ³ thá»ƒ tÄƒng ráº¥t nhanh. Chiáº¿n lÆ°á»£c quáº£n lÃ½ key chÃº trá»ng chi phÃ­ giÃºp há»‡ thá»‘ng má»Ÿ rá»™ng hiá»‡u quáº£ hÆ¡n.

## 9. Káº¿t luáº­n

BÃ i viáº¿t nÃ y há»¯u Ã­ch vÃ¬ giáº£i thÃ­ch ráº±ng mÃ£ hÃ³a Ä‘a thuÃª má»¥c khÃ´ng chá»‰ lÃ  váº¥n Ä‘á» báº£o vá»‡ dá»¯ liá»‡u. ÄÃ¢y cÃ²n lÃ  bÃ i toÃ¡n thiáº¿t káº¿ kiáº¿n trÃºc an toÃ n, cÃ³ kháº£ nÄƒng má»Ÿ rá»™ng vÃ  tá»‘i Æ°u chi phÃ­.

BÃ i há»c quan trá»ng nháº¥t lÃ  cÃ¡c tenant khÃ¡c nhau cÃ³ thá»ƒ cáº§n cÃ¡c má»©c báº£o vá»‡ khÃ¡c nhau. Chiáº¿n lÆ°á»£c phÃ¢n táº§ng key giÃºp há»‡ thá»‘ng cung cáº¥p má»©c cÃ´ láº­p cao hÆ¡n cho khÃ¡ch hÃ ng Premium, Ä‘á»“ng thá»i giáº£m chi phÃ­ khÃ´ng cáº§n thiáº¿t cho nhÃ³m khÃ¡ch hÃ ng Standard.

Encryption Context, policy Ä‘á»™ng, CloudTrail audit vÃ  thiáº¿t káº¿ lÆ°u trá»¯ chÃº trá»ng chi phÃ­ lÃ  nhá»¯ng ká»¹ thuáº­t quan trá»ng Ä‘á»ƒ xÃ¢y dá»±ng mÃ´ hÃ¬nh mÃ£ hÃ³a Ä‘a thuÃª má»¥c hiá»‡u quáº£ hÆ¡n. Khi káº¿t há»£p cÃ¡c ká»¹ thuáº­t nÃ y, há»‡ thá»‘ng cÃ³ thá»ƒ tÄƒng cÆ°á»ng báº£o máº­t, giáº£m táº£i váº­n hÃ nh vÃ  kiá»ƒm soÃ¡t chi phÃ­ AWS KMS tá»‘t hÆ¡n.

NhÃ¬n chung, bÃ i viáº¿t Ä‘Æ°a ra má»™t hÆ°á»›ng thiáº¿t káº¿ thá»±c táº¿ cho mÃ£ hÃ³a Ä‘a thuÃª má»¥c trÃªn AWS. NÃ³ cho tháº¥y má»™t kiáº¿n trÃºc cloud tá»‘t cáº§n cÃ¢n báº±ng giá»¯a báº£o máº­t, chi phÃ­, kháº£ nÄƒng má»Ÿ rá»™ng vÃ  sá»± Ä‘Æ¡n giáº£n trong váº­n hÃ nh.

## Link bÃ i viáº¿t gá»‘c

AWS Architecture Blog:  
**Simplify multi-tenant encryption with a cost-conscious AWS KMS key strategy**

https://aws.amazon.com/vi/blogs/architecture/simplify-multi-tenant-encryption-with-a-cost-conscious-aws-kms-key-strategy/

## CÃ¢u há»i tháº£o luáº­n

Báº¡n Ä‘Ã£ tá»«ng thiáº¿t káº¿ há»‡ thá»‘ng lÆ°u trá»¯ mÃ£ hÃ³a cho á»©ng dá»¥ng SaaS Ä‘a thuÃª má»¥c trÃªn AWS chÆ°a? Theo báº¡n, pháº§n thÃ¡ch thá»©c nháº¥t lÃ  Ä‘Ã¡p á»©ng tiÃªu chuáº©n cÃ´ láº­p dá»¯ liá»‡u cá»§a khÃ¡ch hÃ ng Enterprise hay lÃ  tá»‘i Æ°u hÃ³a hÃ³a Ä‘Æ¡n AWS KMS hÃ ng thÃ¡ng?
