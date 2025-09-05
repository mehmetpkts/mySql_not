# MySQL Workbench'te Kod Biçimlendirme (Beautify) Özelliği

- Bu özellik MySQL Workbench'te kullanılan bir kod biçimlendirme aracıdır.
- Sağ üst köşede bulunan fırça (brush) simgesi ile erişilebilir.
- Yazılan SQL kodlarını daha okunaklı ve düzenli hale getirir.
- Özellikle karmaşık sorgular için okunabilirliği büyük ölçüde artırır.

## Beautify Kullanmadan Önce

```sql
SELECT * FROM customer;
```

## Beautify Kullandıktan Sonra

```sql
SELECT
    *
FROM
    customer;
```

## Özellikler ve Avantajlar

1. **Otomatik Hizalama**: SQL anahtar kelimelerini ve ifadelerini otomatik olarak hizalar.
2. **Girinti Düzeni**: Mantıksal blokları daha iyi göstermek için uygun girintileme yapar.
3. **Satır Sonları**: Uzun satırları okunabilirlik için uygun noktalardan böler.
4. **Tutarlılık**: Tüm kod tabanında tutarlı bir biçimlendirme sağlar.
5. **Zaman Tasarrufu**: Manuel biçimlendirme yapmaya gerek kalmaz.

## Kullanım İpuçları

- Kısa ve basit sorgular için manuel yazım yeterli olabilir.
- Karmaşık sorgular, alt sorgular ve birleştirmeler için mutlaka kullanılmalıdır.
- Ekip çalışmalarında kod okunabilirliğini artırmak için önerilir.
- Klavye kısayolu genellikle `Ctrl+B` (Windows/Linux) veya `Cmd+B` (Mac) şeklindedir.
