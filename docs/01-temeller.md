# 1. GİT TEMELLERİ 
    Sıradan bir projede 'git add .' ve 'git commit -m "güncellendi"' yazıp geçebiliriz. Ancak büyük ekiplerde (örneğin otonom bir uçuş kontrol yazılımında), full-stack web projelerinde veya mikroservis mimarilerinde bu yaklaşım kod tarihçesini okunamaz hale getirir.

## Hazırlık bölgesi 
    **Durum** Otonom uçuş algoritması için `yolo_node.py` dosyasını güncellediniz ama aynı anda `README.md` dosyasındaki kurulum notlarını da değiştirdiniz. İkisini tek bir commit (paket) olarak birleştirmek, geçmişe dönük hata ayıklamayı zorlaştırır.

    **Çözüm** Tüm dosyaları (`git add .`) sepete atmak yerine, sadece ilgili dosyayı "Hazırlık Bölgesi"ne almalısınız.
    ```bash
    git add src/yolo_node.py

Not: 'git add' komutu kodu GitHub'a göndermez,sadece kargolanacak kutunun içine koyar. Eğer yanlış dosyayı eklerseniz, 'git restore --staged <dosya_adi>' ile kutudan geri çıkarabilirsiniz.


# Git Temelleri: Kodun Güvenliğe Alınması

Git'i sadece bir yedekleme aracı olarak görmek en büyük yanılgıdır. Donanımla haberleşen algoritmalar geliştirirken her bir satır kodun versiyonlanması hayati önem taşır. Takım olarak yapılan işlerde tavsiye ettiğim temel döngü:

* `git status`: Arka planda nelerin değiştiğini kontrol ederiz. Test için yazılmış geçici bir scripti yanlışlıkla asıl koda dahil etmek istemeyiz.
* `git add .`: Değişiklikleri onaylayıp sahneye (staging area) alırız.
* `git commit -m "mesaj"`: Yaptığımız işi mühürleriz.

**Mühendislik Standardı:** 
Commit mesajlarını "hata düzeltildi", "yeni kod eklendi" gibi jenerik ifadelerle geçiştirmeyiz. Geriye dönüp bir hatayı aradığımızda uzun uğraşlar ve karmaşıklık arasında netlik hayat kurtarır.
*Doğru Kullanım:* `fix: kamera modülündeki FPS düşme sorunu bellek sızıntısı giderilerek çözüldü`