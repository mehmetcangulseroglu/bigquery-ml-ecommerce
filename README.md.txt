# 🛒 Predicting Visitor Purchases with BigQuery ML

## 📌 Proje Özeti
Bu proje, **Google Merchandise Store**'un gerçek e-ticaret verilerini kullanarak, web sitesini ziyaret eden kullanıcıların **geri gelip satın alma ihtimallerini** tahmin eden bir makine öğrenimi modelidir.

**Google Cloud BigQuery ML** kullanılarak geliştirilen bu proje, pazarlama bütçesinin (ROI) verimliliğini artırmayı hedefler.

## 🎯 İş Problemi ve Çözüm
E-ticaret sitelerinde ziyaretçilerin sadece çok küçük bir kısmı (%2.69) satın alım yapar. Reklam bütçesini rastgele harcamak yerine, satın alma potansiyeli yüksek kullanıcıları önceden tespit etmek gerekir.

* **Hedef:** İlk ziyaret verilerine bakarak kullanıcının gelecekteki satın alma ihtimalini (Propensity Scoring) hesaplamak.
* **Sonuç:** Geliştirilen model, satın alma ihtimali en yüksek %6'lık kitleyi başarıyla tespit etmiştir. Bu kitleye odaklanıldığında pazarlama **ROI (Yatırım Getirisi) 9 katına çıkmaktadır.**

## 📊 Başarı Metrikleri (ROC AUC)
Modelin performans değerlendirmesi sonucunda **0.91 ROC AUC** skoruna ulaşılmıştır. Bu, modelin "satın alacak" ve "almayacak" kullanıcıları çok yüksek doğrulukla ayırabildiğini gösterir.

### Başarı Skoru ve ROC Eğrisi
![Evaluation Score](evaluation_score.png)
![ROC Curve](roc_curve_graph.png)

## 🛠️ Kullanılan Teknolojiler
* **Platform:** Google Cloud Platform (GCP)
* **Araç:** BigQuery ML (SQL tabanlı Makine Öğrenimi)
* **Dil:** Standard SQL
* **Model:** Logistic Regression (Binary Classification)

## 📂 Dosya İçeriği
* `project_queries.sql`: Veri temizleme, özellik mühendisliği ve model eğitimi için kullanılan tüm SQL kodları.
* `prediction_data.csv`: Modelin ürettiği örnek tahmin sonuçları (CSV formatında).
* `prediction_results.png`: Tahmin çıktısının ekran görüntüsü.

### Örnek Tahmin Çıktısı
Aşağıdaki görselde, modelin her bir ziyaretçi için atadığı satın alma olasılıkları (`predicted_will_buy_on_return_visit_probs`) görülmektedir:

![Prediction Results](prediction_results.png)

---
*Bu proje Google Cloud Skills Boost laboratuvarı kapsamında geliştirilmiştir.*