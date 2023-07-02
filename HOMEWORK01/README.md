# HOMEWORK01

CBL0001.cbl dosyasındaki PRTLINE parametresini aşağıdaki şekilde değiştirerek yeni bir data set oluşturduk.

```
//PRTLINE   DD DSN=&SYSUID..OUTPUT,
//             DISP=(NEW,CATLG,DELETE),
//             UNIT=SYSDA,
//             SPACE=(TRK,(10,10),RLSE),
//             DCB=(RECFM=FB,LRECL=119,BLKSIZE=0)
```

**DISP=(NEW,CATLG,DELETE)** veri setinin işlem davranışını tanımlar. **NEW** Eğer veri seti henüz mevcut değilse, yeni bir veri seti oluşturulacağını belirtir, **CATLG** yeni oluşturulan veri setinin katalogda kaydedilmesini belirtir, **DELETE** işlem tamamlandıktan sonra veri setinin silinmesi gerektiğini belirtir.

**UNIT=SYSDA** veri kümesinin kullanacağı cihaz türünü belirtiyoruz.

**SPACE=(TRK,(10,10),RLSE)** veri kümesinin alan ihtiyacını belirtiyoruz. **RLSE** veri seti kapatılacağında kullanılmayan disk alanının serbest bırakılacağını ifade ediyor.  

**DCB=(RECFM=FB,LRECL=119,BLKSIZE=0)** veri setinin organizasyonel ve fiziksel özelliklerini tanımlar. **RECFM=FB** veri setinin kayıt formatını Fixed Block kullanılacağını gösterir. Bu kayıt formatında, her kayıt aynı uzunlukta olmalıdır. **LRECL=119** veri setindeki kayıtların maksimum uzunluğunu belirtiyor. **BLKSIZE=0** veri setinin blok boyutunu belirtir. 0 değeri, sistem tarafından otomatik olarak blok boyutunun belirleneceğini gösterir.