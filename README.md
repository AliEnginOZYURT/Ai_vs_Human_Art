AI vs Human Art Classifier (Yapay Zeka ve İnsan Sanatı Sınıflandırma Sistemi)
Bu proje, ResNet50 mimarisi ve Transfer Learning (Transfer Öğrenme) yöntemleri kullanılarak, bir görselin yapay zeka tarafından mı yoksa bir insan sanatçı tarafından mı üretildiğini tespit etmek amacıyla geliştirilmiştir.
+1

Dijital sanat platformlarında telif haklarının korunması ve içeriklerin doğru etiketlenmesi için yüksek doğruluklu bir çözüm sunar.

Proje Özeti

Amaç: Üretken yapay zeka (Generative AI) modelleri ile insan yapımı sanat eserlerini ayırt etmek.
Mimari: ImageNet üzerinde ön eğitimli ResNet50.
Yöntem: Transfer Learning & Fine-Tuning.
Başarı Oranı: %79.45 Test Doğruluğu (Accuracy).

Performans Metrikleri
Model, özellikle yapay zeka tarafından üretilen görselleri tespit etmede yüksek bir kesinlik oranına sahiptir.

Metrik	Değer	Açıklama
Genel Doğruluk (Accuracy)	%79.45	
Test seti genel başarısı.

Yapay Zeka Kesinliği (Precision)	%87.00	
AI görsellerini tespit etme başarısı.

Doğrulama Doğruluğu	%84.93	
Validation seti başarısı.

Kullanılan Teknolojiler
Dil: Python
Framework: PyTorch 
Model: ResNet50 (25M+ parametre) 
Optimizasyon: Adam Optimizer & CrossEntropyLoss 

Veri Seti ve İşleme
Proje verisi AiArtData ve RealArt olmak üzere iki ana sınıftan oluşur. Modelin ezberlemesini önlemek ve başarısını artırmak için şu teknikler uygulanmıştır:
Stratified Split: Veri seti dengeli bir şekilde Eğitim (%70), Test (%15) ve Doğrulama (%15) olarak ayrılmıştır.
Data Augmentation (Veri Artırma): Rastgele kırpma (RandomResizedCrop), yatay çevirme (RandomHorizontalFlip), döndürme ve renk titreşimi (ColorJitter) teknikleri ile modelin dayanıklılığı artırılmıştır.
