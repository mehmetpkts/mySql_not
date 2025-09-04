## Şema Yapısı (Tablolar arasındaki oklar- bağlantılar)

- MySql workbench kullanılıyorsa, yukardaki bardan database'ye tıklanır.
- Daha sonra reverse engineer'e tıklanır.
- Daha sonra next, next database seçilecek kısma kadar gelinir ve oradan databasemizi seçeriz.
- Daha sonra tekrardan next işlemleri yapılır ve en sonunda karşımıza birtane bağlantılı tablolar sayfası çıkar.

---

## MySql'de bazı kurallar

- MySql key sensitive değildir. Yani büyük harf küçük harf değildir.
- from gibi select gibi kelimeler mavi yazı ile gösterilir çünkü bunlar keyword'dür.
- Sql öğrenirken mysql'e ait olan çok güzel bir database var: sakila database.

---

## MySql workbench aktarımlar

- Eğer tablomuz seçiliyse bold bir şekilde gözükür ve sorgularımı ona göre yapabiliriz:

```sql
SELECT * FROM payment;
```

- Eğer tablolarımız bold değilse şu şekilde sorgularımızı yapabiliriz:

```sql
SELECT * FROM sakila.payment;
```

- Tablo üzerinde cursor'umuz getirdiğimizde logoların solunda info kısmı çıkar ve oradan da tablolarımıza bakabiliriz.
- Aynı yerden sağ tarafındaki tablo simgesine tıklarsak tablomuzu nasıl çektiğimizi görevibiliriz.
