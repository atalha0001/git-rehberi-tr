# Takım Çalışması ve Kalite Kontrol

Kodları lokalden GitHub'a yollamak sürecin sadece bir adımıdır. Kod kalitesini korumak için uyguladığımız katı kurallar şunlardır:

* **Pull Request (PR) Kültürü:** Repoda tek kişi bile çalışsa doğrudan `main` dalına push atmayız. Önce PR açar, değişiklikleri dışarıdan bir gözle (Code Review) inceler, her şey içimize sinerse birleştiririz.
* **.gitignore Kullanımı:** Derleme yaparken oluşan geçici dosyaları (build, .o, __pycache__) veya API şifrelerini asla GitHub'a yollamayız. Güvenlik ilk işimizdir.
* **Tagging (Sürüm Etiketleme):** Kritik bir donanım testinden veya sahaya çıkmadan hemen önce, o anki stabil koda mutlaka bir etiket vururuz. (Örn: `git tag -a v1.2 -m "Saha testi stabil sürümü"`). Sahada bir şeyler ters giderse, dönüş noktamız bellidir.