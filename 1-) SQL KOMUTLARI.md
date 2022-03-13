### ZBK_PERSONEL_T Adında Tablo
![ZBK_PERSONEL_T](https://i.hizliresim.com/ecvvwe2.jpg)

---
### ZBK_PERSONEL_T İÇİNDEKİ KAYITLAR
![ZBK_PERSONEL_T VERİLER](https://i.hizliresim.com/5kbnqu7.jpg)
---
##### ✅ Tablo Verileri Tanımlama (se38 => Executable Program ile)
```
DATA: gv_personelid       TYPE zbk_personelid_de,
      gv_personelad       TYPE zbk_personelad_de,
      gv_personelsoyad    TYPE zbk_personelsoyad_de,
      gv_personelcinsiyet TYPE zbk_personelcinsiyet_de,
      gs_personelt        TYPE zbk_personel_t,
      gt_personelt        TYPE zbk_personel_t.
```
---
##### ✅ SELECT KULLANIMI (se38 => Executable Program ile)
```
* // TABLODAKİ VERİLERİ ÇEKME => Tüm tablodaki verileri çekme
SELECT * FROM zbk_personel_t INTO TABLE gt_personel_t.

* // STRUCTURE DAKİ VERİLERİ ÇEKME => Tek bir satırdaki verileri çekme
SELECT SINGLE * FROM zbk_personel_t INTO gs_personelt.

* // VARIABLE DAKİ VERİLERİ ÇEKME => Tek bir veriyi çekme
SELECT SINGLE personel_id INTO gv_personelid.

* // Tablodaki Verilerden ID si 1 Olanı Çek (se38 => Executable Program ile)
SELECT * FROM zbk_personel_t INTO TABLE gt_personel_t WHERE personel_id EQ 1.
```
---

##### ✅ UPDATE KULLANIMI (se38 => Executable Program ile)
```
* TABLODAKİ Personel Id 'si 1 Olanın Adını Tufan Yap  
UPDATE ZBK_PERSONEL_T SET personel_ad = 'Tufan' where personel_id eq 1.


```
