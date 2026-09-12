# 1. GİT TEMELLERİ 
    Sıradan bir projede 'git add .' ve 'git commit -m "güncellendi"' yazıp geçebilirsiniz. Ancak büyük ekiplerde (örneğin otonom bir uçuş kontrol yazılımında), full-stack web projelerinde veya mikroservis mimarilerinde bu yaklaşım kod tarihçesini okunamaz hale getirir.

## Hazırlık bölgesi 
    **Durum** Otonom uçuş algoritması için `yolo_node.py` dosyasını güncellediniz ama aynı anda `README.md` dosyasındaki kurulum notlarını da değiştirdiniz. İkisini tek bir commit (paket) olarak birleştirmek, geçmişe dönük hata ayıklamayı zorlaştırır.

    **Çözüm** Tüm dosyaları (`git add .`) sepete atmak yerine, sadece ilgili dosyayı "Hazırlık Bölgesi"ne almalısınız.
    ```bash
    git add src/yolo_node.py

Not: 'git add' komutu kodu GitHub'a göndermez,sadece kargolanacak kutunun içine koyar. Eğer yanlış dosyayı eklerseniz, 'git restore --staged <dosya_adi>' ile kutudan geri çıkarabilirsiniz.
