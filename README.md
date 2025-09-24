# Görsel Veri Seti Sınıflandırma (CNNs)

##  Projenin Amacı
Bu proje, **Akbank Derin Öğrenme Bootcamp** kapsamında bir görsel veri setini sınıflandırmak için Convolutional Neural Networks (CNNs) kullanılarak geliştirilmiştir. Amaç, verilen resimlerin doğru sınıfa atanmasını sağlayacak bir derin öğrenme modeli oluşturmaktır.

##  Veri Seti
- Eğitim, doğrulama ve test olarak ayrılmıştır.  
- Görseller 128x128 boyutuna ölçeklenmiştir.  
- Eğitim verisinde veri artırma teknikleri (rotation, horizontal flip, color jitter) kullanılmıştır.  
- Toplam 33 sınıf bulunmaktadır.  

##  Kullanılan Yöntemler
- PyTorch kütüphanesi ile CNN modeli geliştirilmiştir.  
- Model yapısı:
  - 3 adet Conv2D + BatchNorm + MaxPool katmanı
  - Fully Connected katmanlar (Dropout ile)
  *Adam optimizer, CrossEntropyLoss ve Early Stopping uygulanmıştır.  
- Hyperparameter tuning ile farklı öğrenme oranı, batch size ve dropout değerleri test edilmiştir.  

##  Sonuçlar
- Model, test veri setinde yüksek doğruluk oranı elde etmiştir.  
- Eğitim ve doğrulama kayıpları takip edilerek **overfitting engellenmiştir**.  
- En iyi sonuçlara şu parametreler ile ulaşılmıştır:
  - Öğrenme oranı (lr): `0.0005`  
  - Batch size: `64`  
  - Dropout: `0.3`
 
  - Kaggle link:
  - 
