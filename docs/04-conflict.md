# Merge Conflict (Çakışma) Çözümü

Aynı dosyanın aynı fonksiyonunda farklı değişiklikler yaptığımızda Git çakışma (conflict) verebilir. Bu durumu mekanik bir süreçle, donanım mantığını gözeterek çözeriz.

**Çözüm Adımları:**
1. Çakışma anında kod editörümüz (VS Code) bize `<<<<<<< HEAD` (mevcut kod) ve `>>>>>>> branch_ismi` (gelen kod) şeklinde iki farklı blok sunar.
2. Sistemin bütünselliğini ve akış dinamiğini göz önüne alarak hangi kodun kalması gerektiğine takımca veya kodu yazan kişi olarak karar veririz.
3. Fazlalık olan işaretleri silip dosyayı temizleriz.
4. `git add .` ve `git commit -m "fix: haberleşme arayüzündeki merge conflict çözüldü"` diyerek krizi kapatırız.