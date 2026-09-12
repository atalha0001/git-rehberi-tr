# Dallanma (Branch) Mimarisi

Geliştirme sürecindeki en katı kuralımız şudur: **Asla doğrudan main (ana) dala kod yazmayız.** Ana dal, sistemin en stabil, test edilmiş ve sahada çalışmaya hazır halidir. 

Yeni bir algoritma deneyeceğimiz veya mevcut bir sensör verisini filtreleyeceğimiz zaman her zaman yeni bir dal (branch) açarız. 

* `git branch`: Projedeki mevcut dalları listeleriz.
* `git checkout -b <yeni-dal-adi>`: Kendimize güvenli bir izole alan açıp oraya geçeriz.

Örneğin; hedef takip algoritmasına yeni bir PID kontrolcüsü ekleyeceğimiz zaman `git checkout -b feature/pid-optimizasyonu` diyerek çalışırız. Simülasyon testleri başarılı olursa, bu kodları kontrollü bir şekilde ana dala dahil ederiz.