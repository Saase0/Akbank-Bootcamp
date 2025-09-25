# Görsel Veri Seti Sınıflandırma (CNNs)

##  Projenin Amacı
Bu proje, Akbank Derin Öğrenme Bootcamp kapsamında bir görsel veri setini sınıflandırmak için CNNs kullanılarak geliştirilmiştir. Amaç, verilen resimlerin doğru sınıfa atanmasını sağlayacak bir derin öğrenme modeli oluşturmaktır.

##  Veri Seti
-https://www.kaggle.com/datasets/ahmedelsany/car-brand-classification-dataset
- Eğitim, doğrulama ve test olarak ayrılmıştır.  
- Görseller 128x128 boyutuna ölçeklenmiştir.  
- Eğitim verisinde veri artırma teknikleri (color jitter) kullanılmıştır.  
- Toplam 33 sınıf bulunmaktadır.  

##  Kullanılan Yöntemler
PyTorch kütüphanesi ile CNN modeli geliştirilmiştir.
Model yapısı:
- 3 adet Conv2D + BatchNorm + MaxPool katmanı
- Fully Connected katmanlar (Dropout ile)
Optimizasyon:
- Adam optimizer
- CrossEntropyLoss
- Early Stopping
Hyperparameter tuning (Optuna) ile farklı öğrenme oranı, batch size ve dropout değerleri test edilmiştir. 

##  Sonuçlar  
- Eğitim ve doğrulama kayıpları takip edilerek overfitting engellenmiştir.  
- En iyi sonuçlara şu parametreler ile ulaşılmıştır:
  - Öğrenme oranı (lr): 0.001
  - Batch size: 32
  - Dropout: 0.3
  - Optimizer : adam
 
Kaggle link:
  - 
