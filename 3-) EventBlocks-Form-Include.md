##### 🔔 Event-Block 
> Program akışını düzene sokmak için ve takibini yapmak için kullandığımız keyword'lerdir.
 + INITIALIZATION =>  Ekrana girilen user input parametrelerinden önce çalışmasını istediğimiz keywordleri yazdığımız yer
 + AT SELECTION-SCREEN => Ekran kullandığımız input parametrelerini özelleştirmemize yarayan yapı.
 + START-OF-SELECTION => Programı 'run' ettikten sonra çalışmasını istediğimiz kodları yazdığımzı yer.
 + END-OF-SELECTION => Formları kullanacağımız yapılar.
```
PARAMETERS: p_num  TYPE int4.

INITIALIZATION.
  p_num = 5.

AT SELECTION-SCREEN.
  p_num = p_num + 1.

START-OF-SELECTION.
  WRITE 'Start Of'.

END-OF-SELECTION.
  WRITE 'End Of'.
```
---
##### 🔔 Form 
> Yazılan bir kodu sürekli kullanmamıza olanak sağlayan yapılar.
+ Parametresiz form kullanımı
```
DATA: gv_num TYPE int4.

INITIALIZATION.

AT SELECTION-SCREEN.

START-OF-SELECTION.
  PERFORM sayiya_bir_ekle.
  WRITE: / 'Sonuc =', gv_num.

END-OF-SELECTION.
FORM sayiya_bir_ekle.
    gv_num = gv_num + 1.
ENDFORM.
```
+ Parametreli form kullanımı
```
INITIALIZATION.

AT SELECTION-SCREEN.

START-OF-SELECTION.

  PERFORM iki_sayinin_carpimi USING 3 4.

END-OF-SELECTION.
FORM iki_sayinin_carpimi USING p_num1 p_num2.
  DATA lv_sonuc TYPE int4.
  lv_sonuc = p_num1 * p_num2.
  WRITE: 'Sonuc', lv_sonuc.
ENDFORM.
```
