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
```

## Önemli Notlar

- `LIMIT` genellikle `ORDER BY` ile birlikte kullanılır, böylece hangi kayıtların döneceği öngörülebilir olur. `ORDER BY` komutunda daha sonra değinilecektir.
- Büyük veri kümelerinde performans için çok önemlidir.
- Sayfalama (pagination) yaparken sıkça kullanılır.
