# MySQL'de LIMIT Kullanımı

- Sorgu sonuçlarında dönen kayıt sayısını sınırlamak için `LIMIT` anahtar kelimesi kullanılır.
- Bu işlem iki şekilde yapılabilir:
  1. MySQL Workbench arayüzündeki grafiksel araçları kullanarak
  2. Doğrudan SQL kodu yazarak

## Temel Kullanım

```sql
SELECT * FROM tablo_adi LIMIT 10;
```

Bu sorgu, belirtilen tablodan en fazla 10 kayıt döndürür.

## Başlangıç Noktası Belirterek Kullanım

```sql
-- İlk 10 kaydı atlayıp sonraki 5 kaydı getirir
SELECT * FROM tablo_adi LIMIT 10, 5;

-- Veya daha modern sözdizimi ile:
SELECT * FROM tablo_adi LIMIT 5 OFFSET 10;
```

## Örnekler

```sql
-- İlk 5 müşteriyi getir
SELECT * FROM customers LIMIT 5;

-- 6. müşteriden itibaren 10 müşteri getir
SELECT * FROM customers LIMIT 5, 10;

-- En pahalı 5 ürünü getir
SELECT * FROM products ORDER BY price DESC LIMIT 5;
```

## Önemli Notlar

- `LIMIT` genellikle `ORDER BY` ile birlikte kullanılır, böylece hangi kayıtların döneceği öngörülebilir olur.
- Büyük veri kümelerinde performans için çok önemlidir.
- Sayfalama (pagination) yaparken sıkça kullanılır.
