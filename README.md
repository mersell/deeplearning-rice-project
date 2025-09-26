# deeplearning-rice-project
CNN tabanlı derin öğrenme modeli kullanarak 5 farklı pirinç türünü  (Arborio, Basmati, Ipsala, Jasmine, Karacadag) sınıflandıran proje. TensorFlow/Keras ile geliştirilmiş, data augmentation ve model değerlendirme içerir

## Giriş

Bu proje, Global AI Hub Bootcamp kapsamında geliştirilmiş bir pirinç görüntü sınıflandırma sistemidir. Rice Image Dataset üzerinde CNN tabanlı derin öğrenme modeli eğitilmiş ve model kararları Eigen-CAM ile görselleştirilmiştir.

###  Proje Amacı
- 5 farklı pirinç türünü yüksek doğrulukla sınıflandırmak
- Model interpretability için heatmap görselleştirmeleri oluşturmak
- Hiperparametre optimizasyonu ile optimal model performansına ulaşmak

### Veri Seti
- **Kaynak**: [Rice Image Dataset](https://www.kaggle.com/datasets/muratkokludataset/rice-image-dataset)
- **Sınıflar**: Arborio, Basmati, Ipsala, Jasmine, Karacadag (5 sınıf)
- **Görüntü Sayısı**: 15,000 adet (sınıf başına 3,000)
- **Split Oranı**: Train (%80), Validation (%10), Test (%10)

##  Metrikler



### Confusion Matrix  ve metrık Analizi
Confusion Matrix:
[[1496    0    2    2    0]
 [   0 1495    0    5    0]
 [   0    0 1500    0    0]
 [   4    2    3 1491    0]
 [  42    0    0    0 1458]]

Classification Report:
              precision    recall  f1-score   support

     Arborio       0.97      1.00      0.98      1500
     Basmati       1.00      1.00      1.00      1500
      Ipsala       1.00      1.00      1.00      1500
     Jasmine       1.00      0.99      0.99      1500
   Karacadag       1.00      0.97      0.99      1500

    accuracy                           0.99      7500
   macro avg       0.99      0.99      0.99      7500
weighted avg       0.99      0.99      0.99      7500


**Yorum**: Tüm sınıflarda dengeli ve yüksek performans gözlemlenmiştir.



## Kullanılan Teknolojiler
- **Deep Learning**: TensorFlow, Keras
- **Görüntü İşleme**: OpenCV
- **Hiperparametre Optimizasyonu**: Keras Tuner
- **Görselleştirme**: Matplotlib, Seaborn
- **Metrik Hesaplama**: Scikit-learn

### Proje Yapısı
rice-classification/
├── notebooks/
│ ├── 01_data_preprocessing.ipynb
│ ├── 02_cnn_model_training.ipynb
│ ├── 03_hyperparameter_tuning.ipynb
│ └── 04_eigen_cam_visualization.ipynb
├── models/
│ └── best_model.h5
├── utils/
│ ├── data_loader.py
│ └── visualization.py
└── README.md


##  Sonuç ve Gelecek Çalışmalar

###  Başarılar
- %99.20 basarı elde edildi
- Tüm sınıflarda dengeli performans sağlandı
- Model kararları görselleştirilebildi
- Hiperparametre optimizasyonu başarıyla uygulandı

### Yapılabilecek Gelecek Çalışmalar
- [ ] **Transfer Learning** ile model performansını iyileştirme
- [ ] **Real-time Classification** için web arayüzü geliştirme
- [ ] **Data Augmentation** çeşitliliğini artırma
