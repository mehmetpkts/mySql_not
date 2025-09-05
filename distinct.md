# MySQL'de DISTINCT Kullanımı

- Bir kütüphanenin satış databasesi bizde olduğunu düşünelim. Burada farklı kişileri başka bir tabloda tutuyoruz ve payment tablosuna ise kişilerin id sütununu çekiyoruz.Bu durumda kaç tane tekil veri var bulmak istiyoruz. Bu durumda şu yapılır:

```sql
SELECT customer_id FROM payment;  -- Bu şekilde yapılırsa bir kişi birden fazla kitap alacağı için bir çok veri çıkar.
SELECT DISTINCT customer_id FROM payment; -- Böyle yapılırsa verileri tekilleştirmiş oluruz.
-- Eğer biz verileri görmek istemiyoruz, sadece kaçtane var onu öğrenmek istiyoruz dersek şöyle yaparız:
SELECT COUNT(DISTINCT customer_id) FROM payment; -- Bu şekilde toplamda kaç kişi kitap almış bulabiliriz.
SELECT COUNT(DISTINCT customer_id), COUNT(customer_id) FROM payment; -- bu ise bize hem kaçtane kitap alınmış onu gösterir hem de kaç kişi almış onu gösterir.
```

Peki eğer `DISTINCT` kodunu birden fazla kolonun önünde kullanmış olsaydık ne olurdu?

```sql
SELECT DISTINCT customer_id, store_id FROM customer;
```

- Bu kod ile customer tablosundaki customer_id ve store_id'lerininin kombinasyonlarını tekilleştirmiş oluruz.
