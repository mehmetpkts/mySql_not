# MySQL'de Aritmatik İşlemler

- MySQL'de artimatik işlemleri `SELECT` ile yapabiliyoruz.

```sql
SELECT 2 + 2  -- buranın çıktısı 4 olur.
```

Tablolar üzerinden örenk veilmesi gerekirse:

```sql
SELECT amount, amount+1 FROM payment;  -- Bu ise bize payment tablosundaki amount sütununun değerini ve onun 1 fazlasını gösterir.
```

## `AS` komutu ile isim değiştirme:

- `AS` komutu ile tablomuzun sütunlarının adını değiştirebiliriz.

```sql
SELECT amount, (amount+1) AS "BIR FAZLA" FROM payment;  -- istersek "" ile gösteririz ve türkçe olarak yazabiliriz. "" ile göstermek istemiyorsak _ tarzı karakterler kullanabiliriz(altta verilen örnek gibi).
SELECT amount, amount+1 AS BIR_FAZLA FROM payment;
```

```sql
SELECT amount, amount+1 FROM payment;
SELECT amount AS "ilk fiyat", amount + amount*0.5 AS "zamlı fiyat" FROM payment;  -- burada ise ilk fiyat ve zamlı fiyat gösterilmiş oldu.
```
