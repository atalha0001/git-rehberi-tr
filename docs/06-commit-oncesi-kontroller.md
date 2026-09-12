# Commit Öncesi Otomatik Kontroller (Pre-commit)

Derlenmeyen, bellek sızıntısı riski taşıyan veya standart dışı bir kodu GitHub'a yollamak büyük bir zaman ve güvenlik kaybıdır. Bu süreci insan inisiyatifine bırakmayız.

Git'in `pre-commit hook` mekanizmasını kullanarak arka planda çalışan otomatik bir denetim ağı kurarız. 

**Mekanizma Nasıl Çalışır?**
Kodu commit'lemeye çalıştığımız an sistem devreye girer:
* Kodu güvenlik ve formatlama (Linter) standartlarına göre tarar.
* Kullanılmayan tehlikeli değişkenler veya yapısal hatalar arar.

Eğer bu testlerden biri bile başarısız olursa, Git commit işlemini iptal ederek bizi kodumuzu düzeltmeye zorlar. Böylece ana repoya sadece temiz, çalışır ve test edilmiş kodların girmesini donanımsal bir filtre gibi garanti altına almış oluruz.