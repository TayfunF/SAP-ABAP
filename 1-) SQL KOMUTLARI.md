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
      gt_personelt        TYPE TABLE OF zbk_personel_t.
```
---
##### ✅ SELECT KULLANIMI (se38 => Executable Program ile)
```
* // TABLODAKİ VERİLERİ ÇEKME => Tüm tablodaki verileri çekme
SELECT * FROM zbk_personel_t INTO TABLE gt_personelt.

* // STRUCTURE DAKİ VERİLERİ ÇEKME => Tek bir satırdaki verileri çekme
SELECT SINGLE * FROM zbk_personel_t INTO gs_personelt.

* // VARIABLE DAKİ VERİLERİ ÇEKME => Tek bir veriyi çekme
SELECT SINGLE personel_id INTO gv_personelid.

* // Tablodaki Verilerden ID si 1 Olanı Çek (se38 => Executable Program ile)
SELECT * FROM zbk_personel_t INTO TABLE gt_personelt WHERE personel_id EQ 1.
```
---
##### ✅ UPDATE KULLANIMI (se38 => Executable Program ile)
```
* // TABLODAKİ Personel Id 'si 1 Olanın Adını Tayfun Yap  
UPDATE zbk_personel_t set personel_ad = 'Tayfun' where personel_id eq 1.
```
---
##### ✅ INSERT KULLANIMI (se38 => Executable Program ile)
```
* // İlk olarak personel için bilgileri dolduruyorum. Sonra ekleme yapıyorum.
gs_personelt-personel_id = 5.
gs_personelt-personel_ad = 'Ahmet'.
gs_personelt-personel_soyad = 'Mehmet'.
gs_personelt-personel_cinsiyet = 'E'.
INSERT zbk_personel_t FROM gs_personelt.
```
---
##### ✅ DELETE KULLANIMI (se38 => Executable Program ile)
```
* // Personel Id 'si 5 olanı sil.
DELETE FROM zbk_personel_t WHERE personel_id EQ 5.
```
---
##### ✅ MODIFY KULLANIMI (se38 => Executable Program ile)
```
* // Personel Bilgileri Tabloda Varsa Güncelle Yoksa Ekle
* // Yani Varsa => UPDATE , Yoksa => INSERT Mantığı ile çalışıyor
gs_personelt-personel_id = 5.
gs_personelt-personel_ad = 'Ahmet'.
gs_personelt-personel_soyad = 'Hasan'.
gs_personelt-personel_cinsiyet = 'E'.
MODIFY zbk_personel_t FROM gs_personelt.
```
