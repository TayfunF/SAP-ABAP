#### Kullanıcı Veri Giriş Yöntemleri
---
##### 🔔 PARAMETERS
```
* // Üst Menüde GOTO ---> Text Element ---> Selection Text'te (?..) Yerine Yaşınız Yaz.

✔️ PARAMETERS p_num1 TYPE int4.
```
```
* // Tablonun DataElementini Kullanabiliyorum

PARAMETERS p_persad TYPE zbk_personelad_de.

✔️[PARAMETERS değişkenAdı TYPE tabloDataElementAdı.]
```
---
##### 🔔 SELECT-OPTIONS 
```
* Kullanım 1 : DATA oluşturup onu vermem lazım

DATA gv_persoy TYPE zbk_personelsoyad_de.
SELECT-OPTIONS: s_persoy FOR gv_persoy.

✔️[SELECT-OPTIONS: s_persoy FOR değişkenAdı.]
```
```
* Kullanım 2 : DATA Tanımlamadan Kullanma

TABLES: zbk_personel_t.
SELECT-OPTIONS: s_percin FOR zbk_personel_t-personel_cinsiyet.

✔️[SELECT-OPTIONS: s_percin FOR tabloAdi-tabloSütunAdı.]
```
---
##### 🔔 AS CHECKBOX 
```
✔️PARAMETERS p_num1 AS CHECKBOX.
```
---
##### 🔔 RADIOBUTTON GROUP
```
PARAMETERS: p_num2 RADIOBUTTON GROUP cins,
            p_num3 RADIOBUTTON GROUP cins,
            p_num5 RADIOBUTTON GROUP yas,
            p_num6 RADIOBUTTON GROUP yas,
            p_num7 RADIOBUTTON GROUP yas.
```
---
##### 🔔 SELECTION-SCREEN (Görselliği Güzelleştirme)
```
SELECTION-SCREEN BEGIN OF BLOCK bl1 WITH FRAME.

SELECTION-SCREEN END OF BLOCK bl1.
```
```
SELECTION-SCREEN BEGIN OF BLOCK bl1 WITH FRAME TITLE text-001.
PARAMETERS: p_num2 RADIOBUTTON GROUP cins,
            p_num3 RADIOBUTTON GROUP cins,
            p_num5 RADIOBUTTON GROUP yas,
            p_num6 RADIOBUTTON GROUP yas,
            p_num7 RADIOBUTTON GROUP yas.
SELECTION-SCREEN END OF BLOCK bl1.
```
