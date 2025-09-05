# Tablodan Sütun Getirme

- Bildiğimiz gibi tablonun tamamını getirmek için:

```sql
SELECT * FROM tablo;
```

şeklinde getirebiliyorduk. Şimdi ise bu tabloların sütunlarını nasıl getirebileceğimizi öğreneceğiz.

## Sütun Getirme

```sql
SELECT customer_id, first_name, last_name FROM customer;
```

- Bu kod ile customer tablosundaki customer_id, first_name, last_name'leri getirmiş olduk. Bütün sütunları değil (bütün sütunları * ifadesi ile getiriyorduk) sadece istediğimiz sütunları getirdik.

- İstersek bir tablo içerisinde istediğimiz sütunları tekrar getirebiliriz:

```sql
SELECT *, name FROM customer;
```

- Bu kod ile customer tablosundaki bütün sütunlar gelir ve ek olarak name sütunu tekrardan tablonun son sütununa eklenir.
