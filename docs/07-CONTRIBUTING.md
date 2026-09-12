# Katkıda Bulunma Rehberi (Contributing)

Bu Git ve GitHub rehberini büyütmek, eksik komutları tamamlamak veya dokümantasyon hatalarını düzeltmek için yapacağınız katkıları memnuniyetle karşılıyoruz. Dokümantasyonun mühendislik standartlarını korumak adına, yapılacak eklemelerde aşağıdaki kurallara uyulması zorunludur.

## 1. Dallanma (Branch) Stratejisi
Asla doğrudan `main` dalına içerik yüklemesi (push) yapılamaz. Yeni eklemeler veya format düzeltmeleri için amacına uygun isimlendirilmiş bir dal açmalısınız:
* **Yeni İçerikler/Belgeler:** `feature/konu-adi` (Örn: `feature/stash-kullanimi`)
* **Yazım/Format Düzeltmeleri:** `bugfix/hata-adi` (Örn: `bugfix/kirik-link-cozumu`)

## 2. Commit Mesajı Standartları
Geçmişe dönük takip yapabilmek için Conventional Commits standardını kullanıyoruz. Mesajlarınız yapılan işlemin türünü net bir şekilde belirtmelidir:
* `feat:` Yeni bir rehber başlığı veya alt bölüm eklendiğinde.
* `fix:` Yazım hatası, kırık link veya Markdown format hatası düzeltildiğinde.
* `refactor:` Mevcut bir belgenin anlatım dili veya yapısı iyileştirildiğinde.
* *Örnek:* `feat: rebase ve merge farklarını anlatan doküman eklendi`

## 3. İçerik ve Anlatım Standartları
Rehberin bütünselliğini korumak için yazım dilinde şunlara dikkat edilmelidir:
* **Biz Dili:** Anlatımlarda kişisel bir dil yerine, takım çalışmasını ve profesyonelliği vurgulayan kapsayıcı "biz" dili kullanılmalıdır.
* **Senaryo Odaklılık:** Komutlar sadece teknik tanımlarla verilmemeli, donanım projeleri veya yazılım takımlarında karşılaşılan gerçekçi senaryolarla desteklenmelidir.

## 4. Pull Request (PR) Süreci
Eklemelerinizi tamamladıktan sonra `main` dalına bir Pull Request açmalısınız. İçeriğinizin ana dokümantasyona dahil edilmesi için şu şartları sağlaması gerekir:
* **Linter Kontrolü:** Projeye entegre edilmiş CI/CD (Markdown Linter) testleri başarıyla tamamlanmalı ve yeşil tik almalıdır. Belgenizde Markdown yapı hataları bulunmamalıdır.
* **Açıklama:** PR açıklaması, hangi rehber eksikliğinin giderildiğini net bir şekilde özetlemelidir.