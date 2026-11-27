# Yavuzlar – PHP Web Görevleri

Siber Vatan **Yavuzlar** takımındaki haftalık web geliştirme görevlerim (2023).

| Klasör | Ne yapıyor |
|---|---|
| `Yavuzlar-Week-1` | HTML, CSS ve JavaScript ile yapılacaklar listesi; veriler tarayıcıda (localStorage) saklanıyor |
| `Yavuzlar-Week-3` | PHP ve MySQL ile üyelikli yapılacaklar listesi: kayıt, giriş/çıkış, oturum kontrolü, görev ekleme ve tamamlama |

## Kurulum (Week-3)

1. `db.sql` dosyasını MySQL'e aktarın.
2. `db.php` içindeki veritabanı bilgilerini kendi ortamınıza göre düzenleyin.
3. Klasörü yerel bir PHP sunucusunda (ör. XAMPP) çalıştırın.

## Güvenlik notu

Bu proje öğrenme amaçlı yazıldı ve bilinçli olarak düzeltilmemiş açıklar içeriyor:

- Giriş ve kayıt sorgularında kullanıcı girdisi doğrudan SQL'e ekleniyor → **SQL Injection** açığı var. Düzeltmesi: parametreli sorgular (`$DB->prepare("... WHERE eposta = ?")` + `execute([$eposta])`).
- Parolalar düz metin saklanıyor. Düzeltmesi: `password_hash()` ve `password_verify()`.

Canlı bir sunucuda kullanmayın.
