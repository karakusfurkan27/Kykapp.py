# KYK Yurt Sistemi Uygulaması

Bu uygulama, KYK yurtlarında öğrenci yönetimini ve yemekhane bilgilerini takip etmeyi amaçlayan bir sistemdir. SQLite veritabanı kullanılarak öğrenci ve yemek bilgileri saklanır. Kullanıcılar, öğrenci ekleyebilir, silebilir, güncelleyebilir ve listeleyebilir; ayrıca yemek ekleyebilir ve yemekhane listesine göz atabilirler.

## Özellikler

- **Öğrenci Yönetimi**: Öğrenciler sisteme eklenebilir, silinebilir ve güncellenebilir.
- **Yemek Yönetimi**: Yemekler eklenebilir ve öğün bazında listelemeler yapılabilir.
- **SQLite Veritabanı**: Tüm veriler SQLite veritabanında saklanır ve işlenir.

## Kullanılan Teknolojiler

- **Python**: Uygulamanın yazılım dili.
- **SQLite**: Veritabanı yönetim sistemi.
- **SQLite3 Modülü**: Python ile SQLite veritabanı bağlantısını sağlar.

## Kurulum

1. Python yüklü değilse, [Python resmi web sitesinden](https://www.python.org/) Python'u indirip yükleyin.
2. Bu uygulama için ek bir paket yüklemeye gerek yoktur çünkü SQLite3, Python ile birlikte gelir.
3. Uygulamayı çalıştırmak için aşağıdaki komutu kullanabilirsiniz:
   ```bash
   python kyk_yurt_sistemi.py
   ```

## Kullanım

Program, aşağıdaki işlemleri gerçekleştirmenize olanak tanır:

1. **Öğrenci Ekle**: Sisteme yeni bir öğrenci ekler.
2. **Öğrenci Sil**: Sistemdeki bir öğrenciyi siler.
3. **Öğrenci Güncelle**: Sistemdeki bir öğrencinin bilgilerini günceller.
4. **Öğrenci Listesi**: Sistemdeki tüm öğrencileri listeler.
5. **Yemek Ekle**: Yemek bilgilerini sisteme ekler.
6. **Yemek Listesi**: Sistemdeki tüm yemekleri listeler.
7. **Çıkış**: Programdan çıkış yapar.

## Örnek Komutlar

- **Öğrenci Ekleme**: 
   - Ad: Ahmet
   - Soyad: Yılmaz
   - Oda No: 101
- **Öğrenci Silme**: ID 1 olan öğrenciyi silmek.
- **Yemek Ekleme**: 
   - Yemek Adı: Tavuklu Pilav
   - Öğün: Akşam
   - Tarih: 2024-12-24

## Veritabanı Yapısı

### `ogrenciler` Tablosu

| Kolon Adı  | Tür           | Açıklama             |
|------------|---------------|----------------------|
| id         | INTEGER       | Öğrenci ID (Primary Key) |
| ad         | TEXT          | Öğrencinin adı       |
| soyad      | TEXT          | Öğrencinin soyadı    |
| oda_no     | INTEGER       | Öğrencinin oda numarası |

### `yemekhane` Tablosu

| Kolon Adı  | Tür           | Açıklama              |
|------------|---------------|-----------------------|
| id         | INTEGER       | Yemek ID (Primary Key)|
| yemek_adi  | TEXT          | Yemeğin adı           |
| ogun       | TEXT          | Öğün (Sabah/Öğle/Akşam) |
| tarih      | DATE          | Yemek tarihi          |

## Katkılar

- Uygulama geliştirilmeye açık bir projedir. İhtiyaçlarınıza göre eklemeler yapabilirsiniz.

## Lisans

Bu proje, [MIT Lisansı](https://opensource.org/licenses/MIT) ile lisanslanmıştır.
