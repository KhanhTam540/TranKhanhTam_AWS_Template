---
title: "Worklog Tuáº§n 6"
date: 2026-05-25
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---



### Má»¥c tiÃªu tuáº§n 6:

* Hiá»ƒu rÃµ lÃ½ thuyáº¿t ná»n táº£ng vÃ  cÃ¡ch sá»­ dá»¥ng cÆ¡ báº£n cÃ¡c dá»‹ch vá»¥ báº£o máº­t, quáº£n lÃ½ thÃ´ng tin máº­t vÃ  cáº¥u hÃ¬nh Ä‘á»‹nh danh ngÆ°á»i dÃ¹ng trÃªn AWS.

* NghiÃªn cá»©u luá»“ng nghiá»‡p vá»¥ cá»‘t lÃµi vÃ  tham gia phÃ¢n tÃ­ch thiáº¿t káº¿ cÆ¡ sá»Ÿ dá»¯ liá»‡u ban Ä‘áº§u cho dá»± Ã¡n.

### CÃ¡c cÃ´ng viá»‡c cáº§n triá»ƒn khai trong tuáº§n nÃ y:
| Thá»© | CÃ´ng viá»‡c                                                                                                                                                                                   | NgÃ y báº¯t Ä‘áº§u | NgÃ y hoÃ n thÃ nh | Nguá»“n tÃ i liá»‡u                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - TÃ¬m hiá»ƒu lÃ½ thuyáº¿t vÃ  thá»±c hÃ nh lÃ m quen cÆ¡ báº£n vá» MÃ£ hÃ³a dá»¯ liá»‡u vá»›i AWS KMS (Key Management Service).                                                                                       | 25/05/2026   | 25/05/2026      |<https://cloudjourney.awsstudygroup.com/>|
| 3   | - TÃ¬m hiá»ƒu lÃ½ thuyáº¿t vÃ  thá»±c hÃ nh lÃ m quen cÆ¡ báº£n vá» Quáº£n trá»‹ thÃ´ng tin máº­t vá»›i AWS Secrets Manager.                                     | 26/05/2026   | 26/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - TÃ¬m hiá»ƒu lÃ½ thuyáº¿t vÃ  thá»±c hÃ nh lÃ m quen cÆ¡ báº£n vá» XÃ¡c thá»±c ngÆ°á»i dÃ¹ng liÃªn miá»n vá»›i Amazon Cognito. | 27/05/2026   | 27/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - PhÃ¢n tÃ­ch Nghiá»‡p vá»¥: Táº­p trung nghiÃªn cá»©u tÃ i liá»‡u, phÃ¢n tÃ­ch cÃ¡c yÃªu cáº§u chá»©c nÄƒng vÃ  luá»“ng váº­n hÃ nh nghiá»‡p vá»¥ chi tiáº¿t cá»§a Ä‘á» tÃ i dá»± Ã¡n.               | 28/05/2026   | 28/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Thiáº¿t káº¿ CÆ¡ sá»Ÿ dá»¯ liá»‡u: Dá»±a trÃªn luá»“ng nghiá»‡p vá»¥ Ä‘Ã£ lÃ m rÃµ, tiáº¿n hÃ nh xÃ¢y dá»±ng sÆ¡ Ä‘á»“ thá»±c thá»ƒ má»‘i quan há»‡ (ERD) vÃ  thiáº¿t káº¿ cáº¥u trÃºc báº£ng dá»¯ liá»‡u ban Ä‘áº§u cho dá»± Ã¡n. <br> - Tá»•ng káº¿t tuáº§n: RÃ  soÃ¡t láº¡i toÃ n bá»™ ná»™i dung.                                                                                      | 29/05/2026   | 29/05/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Káº¿t quáº£ Ä‘áº¡t Ä‘Æ°á»£c tuáº§n 6:
* Náº¯m vá»¯ng kiáº¿n thá»©c ná»n táº£ng vÃ  cÆ¡ cháº¿ hoáº¡t Ä‘á»™ng cá»‘t lÃµi cá»§a cÃ¡c giáº£i phÃ¡p báº£o máº­t dá»¯ liá»‡u (KMS), quáº£n trá»‹ thÃ´ng tin nháº¡y cáº£m (Secrets Manager) vÃ  há»‡ thá»‘ng quáº£n lÃ½ Ä‘á»‹nh danh khÃ¡ch hÃ ng (Cognito).

* Äáº¡t kháº£ nÄƒng phá»‘i há»£p sá»­ dá»¥ng giao diá»‡n Web Console vÃ  CLI Ä‘á»ƒ cáº¥u hÃ¬nh, kiá»ƒm tra tráº¡ng thÃ¡i hoáº¡t Ä‘á»™ng cÆ¡ báº£n cá»§a cÃ¡c tÃ i nguyÃªn báº£o máº­t Ä‘Æ°á»£c há»c trong mÃ´i trÆ°á»ng thá»±c táº¿.

* LÃ m rÃµ toÃ n bá»™ luá»“ng nghiá»‡p vá»¥ vÃ  cÃ¡c quy táº¯c váº­n hÃ nh chÃ­nh cá»§a Ä‘á» tÃ i dá»± Ã¡n, táº¡o tiá»n Ä‘á» vá»¯ng cháº¯c cho cÃ¡c bÆ°á»›c phÃ¡t triá»ƒn tiáº¿p theo.

* HoÃ n thÃ nh báº£n thiáº¿t káº¿ sÆ¡ Ä‘á»“ thá»±c thá»ƒ dá»¯ liá»‡u (ERD) ban Ä‘áº§u, Ä‘á»‹nh hÃ¬nh rÃµ rÃ ng cáº¥u trÃºc cÃ¡c báº£ng vÃ  má»‘i quan há»‡ rÃ ng buá»™c dá»¯ liá»‡u phá»¥c vá»¥ cho dá»± Ã¡n.
