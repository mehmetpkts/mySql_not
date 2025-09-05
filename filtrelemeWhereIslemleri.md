# Filtreleme (WHERE) İşlemleri

- Filtreleme işlemi WHERE komutu ile yapılır. Bunu exceldeki filter'e benzetebiliriz.

```sql
SELECT city_id,city FROM city WHERE city_name = "London";  -- bu kod bize city tablosun içerisinde şehir adı London olan şehirlerin id ve şehir adını göre bir filtreleme işlemi yapar.
SELECT COUNT(film_id) FROM film WHERE rental_duration=6;  -- mesela bu kodda film tablosunda kiralama süresi 6 olanların id'lerini çekerek kaç tane olduğunu görebiliriz.
```

---

## Birazdaha zor örnekler

```sql
SELECT * FROM film WHERE length > 80;  -- uzunluğu 80den uzun olan filmler
SELECT * FROM film WHERE length >= 80;  -- uzunluğu 80e eşit ve 80den uzun olan filmler
SELECT * FROM film WHERE length <> 80;  -- uzunluğu 80den farklı olan filmler
SELECT * FROM film WHERE length <> 80;  -- uzunluğu 80den farklı olan filmler
```

## `ORDER BY` KULLANIMI

```sql
-- ASC komutu küçükten büyüğe sıralar.
SELECT * FROM film WHERE length > 80 ORDER BY length ASC;  -- uzunluğu 80den uzun olan filmler
SELECT * FROM film WHERE length >= 80 ORDER BY length ASC;  -- uzunluğu 80e eşit ve 80den uzun olan filmler
-- DESC komutu büyükten küçüğe sıralar
SELECT * FROM film WHERE length <> 80 ORDER BY length DESC;  -- uzunluğu 80den farklı olan filmler
SELECT * FROM film WHERE length != 80 ORDER BY length DESC;  -- uzunluğu 80den farklı olan filmler
```

## `BETWEEN` KULLANIMI

```sql
SELECT * FROM film WHERE length BETWEEN 80 AND 90;  -- seksen ile doksan arasındaki uzunluklları getirir.
```

## `LIKE` KULLANIMI

````sql
SELECT * FROM film WHERE title LIKE "AR%";  -- ar ile başlayan filmleri getirir.
SELECT * FROM film WHERE title LIKE "%AR";  -- ar ile biten filmleri getirir.
SELECT * FROM film WHERE title LIKE "%AR%";  -- içinde ar barındıran filmler.```
````
