# MySQL Notlarım

Bu notlar [Youtube'daki MySQL Eğitim Serisi](https://youtube.com/playlist?list=PLrGQS8Gq-kkLdkdSaycy19hQJzwouvPTZ&si=Z7ohltzKK89MdNJw) izlenerek hazırlanmıştır.

---

#### DBMS (Database Management System)

- **Veritabanı Yönetim Sistemi** anlamına gelir.
- Veritabanı ile etkileşim kurmak için bir arayüz sağlar.

## DBMS Türleri

İki tane DBMS türleri vardır. Bunlar:

- İlişkilsel veri tabanı (RDBMS).
- İlişkisel olmayan veri tabanı.

Bizim ilgileneceğimiz kısım _İlişkisel Veritabanlarıdır._

## SQL (Structured Query Language)

- SQL, yapılandırılmış sorgu dilidir.
- Veritabanı ile iletişim kurmak için kullanılan standart bir dildir.
- Her SQL sorgusu noktalı virgül (;) ile sonlandırılır.

## MySQL

- MySQL, popüler bir açık kaynak ilişkisel veritabanı yönetim sistemidir.
- Bu eğitimde MySQL kullanarak SQL öğreneceğiz.

## Temel SQL Sorgu Örnekleri

### Tüm Verileri Getirme

```sql
SELECT * FROM users;
```

- `users` tablosundaki tüm verileri getirir.

### Koşullu Sorgulama

```sql
SELECT * FROM users WHERE ad = 'ali';
```

- `users` tablosunda `ad` sütunu 'ali' olan kayıtları getirir.

### Çoklu Koşul ile Sorgulama

```sql
SELECT * FROM users WHERE ad = 'ali' AND soyad = 'veli';
```

- `users` tablosunda hem `ad` sütunu 'ali' hem de `soyad` sütunu 'veli' olan kayıtları getirir.

### Joker Karakter ile Arama

```sql
SELECT * FROM dersler WHERE ad LIKE 'Mat%';
```

- `dersler` tablosunda `ad` sütunu 'Mat' ile başlayan kayıtları getirir.

### Joker Karakter Kullanımı

- `%` : Herhangi bir karakter dizisini temsil eder.
  - `'Mat%'` : 'Mat' ile başlayanlar
  - `'%mat'` : 'mat' ile bitenler
  - `'%mat%'` : içinde 'mat' geçenler
