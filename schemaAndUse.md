# MySQL'de Veritabanı ve Tablo Yönetimi

## Şema Yapısı (Tablolar Arasındaki İlişkiler)

- MySQL Workbench kullanılıyorsa, üst menüden "Database" seçeneğine tıklanır.
- Daha sonra "Reverse Engineer" seçeneğine tıklanır.
- "Next" butonlarına tıklayarak veritabanı seçim ekranına gelinir ve ilgili veritabanı seçilir.
- Tekrar "Next" işlemleri tamamlanır ve sonunda tablolar arasındaki ilişkileri gösteren bir şema görüntülenir.

---

## MySQL'de Bazı Kurallar

- MySQL, büyük/küçük harf duyarlı (case sensitive) değildir. Yani büyük harf-küçük harf ayrımı yapmaz.
- `SELECT`, `FROM` gibi SQL anahtar kelimeleri genellikle mavi renkle vurgulanır.
- MySQL öğrenirken kullanılabilecek örnek bir veritabanı: `sakila` veritabanı.

---

## MySQL Workbench Kullanımı

- Eğer bir veritabanı seçiliyse, o veritabanındaki tablolar kalın yazı tipinde görünür ve doğrudan sorgu yazılabilir:

```sql
SELECT * FROM payment;
```

- Eğer hiçbir veritabanı seçili değilse, sorguda veritabanı adını belirtmek gerekir:

```sql
SELECT * FROM sakila.payment;
```

- Tablolar üzerinde fare imleciyle üzerine gelindiğinde, sol tarafta bilgi ikonu çıkar. Buradan tablo detaylarına ulaşılabilir.
- Aynı bölümdeki tablo simgesine tıklanarak, tablonun nasıl oluşturulduğu görüntülenebilir.

## USE Komutu

- USE komutu ile aktif veritabanını değiştirebiliriz:

```sql
-- Sakila veritabanını kullanmak için:
USE sakila;

-- Artık veritabanı adı belirtmeden tablolara erişebiliriz:
SELECT * FROM payment;

-- Eğer farklı bir veritabanındaki tabloya erişmek istersek:
SELECT * FROM employees.departments;  -- employees veritabanındaki departments tablosu
```

- Önemli: USE komutu sadece o anki bağlantı için geçerlidir. Yeni bir bağlantıda tekrar kullanılması gerekir.
