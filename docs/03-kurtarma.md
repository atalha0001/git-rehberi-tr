# Kriz Anları ve Kod Kurtarma

Sistemi tamamen bozan bir kod yazdığımızda paniğe kapılmak yerine Git'in standart kurtarma protokollerini devreye sokarız.

* `git restore <dosya>`: Bir dosyada deneme yapıp işleri bozduğumuzda, değişiklikleri henüz commit'lemediysek bu komutla dosyayı anında bir önceki çalışan haline döndürürüz.
* `git revert <commit-id>`: Hatalı bir kodu commit'leyip sunucuya gönderdiysek geçmişi silmeyiz; takımın senkronunu bozmamak için `revert` kullanırız. Bu, hatalı işlemin tam tersini yapan yeni bir commit oluşturur. En güvenli geri alma yöntemidir.
* `git reset --hard HEAD~1`: Sadece lokal bilgisayarımızda çalışıyorsak ve son commit'in tamamen çöp olduğuna karar verdiysek, o commit'i tarihten silerek kodu bir önceki stabil haline çekeriz.