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

## Güvenlik notu: bilinçli zafiyetler

Bu uygulama, Yavuzlar takımındaki Red Team çalışmaları sırasında **SQL Injection pratiği için bilinçli olarak zafiyetli** yazıldı.

| Zafiyet | Nerede | Güvenli hâli |
|---|---|---|
| SQL Injection | `login.php`, `register.php`, `insert.php`: kullanıcı girdisi doğrudan sorguya ekleniyor | Parametreli sorgu: `$DB->prepare("... WHERE eposta = ?")` + `execute([$eposta])` |
| Düz metin parola | `kullanicilar` tablosu | `password_hash()` ile saklama, `password_verify()` ile kontrol |

Yalnızca yerel ortamda, eğitim amacıyla çalıştırın. Canlı bir sunucuya koymayın.
