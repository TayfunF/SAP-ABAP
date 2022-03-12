# SAP-ABAP

+ se38 => Program Oluşturma (Proje İsimleri ZBK_ ile başlar)
+ 

*&---------------------------------------------------------------------*  
*& Report ZBK_LESSON_2  
*&---------------------------------------------------------------------*  
*&  
*&---------------------------------------------------------------------*  
REPORT zbk_lesson_2.  
  
* ### DEĞİŞKEN TANIMLAMA SYNTAX  
```
DATA gv_a TYPE int4.  
DATA gv_b TYPE int4.  
DATA gv_c TYPE int4.  
gv_a = 100.  
gv_b = 50.  
gv_c = gv_a + gv_b.  
WRITE gv_c.  
  ```
  ---
* ### 4 İŞLEM SYNTAX  
 ```
DATA: gv_degisken1 TYPE i,gv_degisken2 TYPE i, gv_sonuc TYPE i.  
gv_degisken1 = 10.  
gv_degisken2 = 5.  
WRITE : gv_degisken1 , / gv_degisken2.  
gv_sonuc = gv_degisken1 + gv_degisken2.  
WRITE: 'Toplam =', gv_sonuc.  
  ```
  ---
* ### IF KOŞULU SYNTAX  
 ```
DATA: gv_sayi TYPE i, gv_sayi2 TYPE i.  
gv_sayi = 5.  
gv_sayi2 = 6.  
IF gv_sayi > gv_sayi2.  
WRITE '1. Sayı Daha Büyüktür'.  
ELSEIF gv_sayi < gv_sayi2.  
WRITE '2. Sayı Daha Büyüktür.'.  
ELSE.  
WRITE 'İki Sayı Birbirine Eşit'.  
ENDIF.  
  ```
  ---
* ### IF-elseIF KOŞULU SYNTAX  
```
DATA gv_degisken TYPE i.  
gv_degisken = 1.  
IF gv_degisken = 1.  
WRITE 'Değişken değeri 1.'.  
ELSEIF gv_degisken = 2.  
WRITE 'Değişken değeri 2.'.  
ELSEIF gv_degisken = 3.  
WRITE 'Değişken değeri 3.'.  
ELSEIF gv_degisken = 4.  
WRITE 'Değişken değeri 4.'.  
ELSEIF gv_degisken = 5.  
WRITE 'Değişken değeri 5.'.  
ELSE .  
WRITE 'Hiçbir değere eşit değil'.  
ENDIF.  
  ```
  ---
* ### CASE SYNTAX  
```
DATA gv_degisken TYPE i.  
gv_degisken = 1.  
CASE gv_degisken.  
WHEN 1.  
WRITE 'Değişken degeri 1.'.  
WHEN 2.  
WRITE 'Değişken degeri 2.'.  
WHEN 3.  
WRITE 'Değişken degeri 3.'.  
WHEN 4.  
WRITE 'Değişken degeri 4.'.  
WHEN 5.  
WRITE 'Değişken degeri 5.'.  
WHEN OTHERS.  
WRITE 'Hiçbir değere eşit değil.'.  
ENDCASE.  
  ```
  ---
* ### DO SYNTAX  
 ```
DO 10 TIMES.  
WRITE / 'Do Döngüsünü öğreniyorum'.  
ENDDO.  
DATA gv_degisken TYPE i.  
gv_degisken = 1.  
DO 5 TIMES.  
WRITE / gv_degisken.  
gv_degisken = gv_degisken + 1.  
ENDDO.  
 ``` 
 ---
* ### WHILE SYNTAX  
```
DATA gv_degisken TYPE i.  
gv_degisken = 1.  
WHILE gv_degisken <= 5.  
WRITE / gv_degisken.  
gv_degisken = gv_degisken + 1.  
ENDWHILE.
```
