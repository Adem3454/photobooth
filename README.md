# Photobooth (PWA)

iPhone için, ana ekrana eklenerek kullanılan bir fotoğraf kabini uygulaması. Sunucu yok; her şey tarayıcıda çalışır, fotoğraflar telefonda kalır.

## Yayın için gereken dosyalar (sadece 5 tane)

`index.html`, `sw.js`, `manifest.webmanifest`, `icon-180.png`, `icon-512.png`

Hepsini GitHub'daki repoya yükle (**Add file > Upload files**, aynı adlı dosyaların üzerine yazılır). Başka dosya gerekmez. `index.html` içinde arayüz, stil ve kod birlikte durur.

## Güncelleme

Yeni sürüm geldiğinde sadece `index.html` ve `sw.js` değişir. Yükledikten 1-2 dakika sonra uygulamada "Yeni sürüm hazır · Yenile" bildirimi çıkar. Ayarlar'da sürüm numarasını ve "Yenilikler"i görebilirsin.

## Geri alma

GitHub'da dosyanın **History** sekmesinden eski sürümü bulup içeriğini geri yükleyebilirsin. Daha rahatı **GitHub Desktop** kullanmaktır: commit geçmişinden **Revert Changes in Commit** ile bozan sürüm geri alınır.

## Kaynak kod (isteğe bağlı)

`kaynak-2.2.0.zip` içinde kodun bölümlere ayrılmış hali (`src/`) ve paketleyici (`pack.py`) var. Kod değişikliği ihtiyacında bu klasör düzenlenir, `python pack.py` ile tek `index.html` ve `sw.js` üretilir. Sen bunlarla uğraşmak zorunda değilsin, sadece yedek olarak sakla.

## Gerçek cihaz test listesi (her sürümden sonra)

- [ ] İlk açılışta kamera açıklama ekranı çıkıyor, izin verince kamera açılıyor ve karşılama turu başlıyor
- [ ] Tur 5 adım gösteriyor, "Atla" çalışıyor, Ayarlar > "Turu göster" yeniden açıyor
- [ ] İlk şeritte sonuç ekranı ipucu kartı çıkıyor (bir kez)
- [ ] İzni reddedince "Tekrar dene" ve yönerge çıkıyor
- [ ] Çekim: geri sayım, flaş, kare düşüyor, şerit tepsiye iniyor, dokununca sonuç açılıyor
- [ ] Filtre ve çerçeve değişince şerit güncelleniyor, resim yerinde kalıyor
- [ ] Çerçeve kategorileri (10 adet) açılıyor, önizlemeler görünüyor, 🎲 Rastgele çalışıyor
- [ ] Her kategoriden 1-2 çerçeve seçip şeridin bozulmadığını gör (özellikle Türkiye, Sanat, Dijital)
- [ ] Hikaye / Kare / Baskı boyutları doğru
- [ ] Canlı fotoğraf (şeride dokun) ve Canlı video + paylaşım
- [ ] Şeridi yukarı kaydırınca paylaşım menüsü açılıyor
- [ ] Anı panosu: şerit kaydediliyor, açılıyor, siliniyor, "Panoyu temizle" çalışıyor
- [ ] Uzaktan çekim: iki telefon, farklı ağlarda; kamera donmuyor
- [ ] Deneysel: akıllı kare seçici, ışınlama (açıp kapat)
- [ ] Uçak modunda uygulama açılıyor (çevrimdışı)
- [ ] Ayarlar > Yenilikler ve sürüm numarası doğru
