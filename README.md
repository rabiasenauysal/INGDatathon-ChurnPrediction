# ING Hubs Türkiye Datathon 2025 - ML Model

Bu repository, ING Hubs Türkiye Datathon 2024 için geliştirilmiş makine öğrenimi modelini ve submission dosyasını içerir. Model, yarışma verilerini kullanarak churn olasılıklarını tahmin etmek için geliştirilmiştir.

---

## 🚀 Datathon Hakkında

ING Hubs Türkiye, yapay zekâ ve teknoloji projeleriyle ING’nin global dijitalleşme yolculuğuna katkı sunan bir merkezdir.  

Bu yarışmanın amacı:
- Yenilikçilik ve iş birliğini teşvik etmek
- Gerçek iş etkisi yaratacak veri odaklı çözümler geliştirmek

---

## 🎯 Yarışma Değerlendirme

Yarışma metriği, üç temel ölçüt üzerinden ağırlıklı olarak hesaplanır:

| Metrik | Ağırlık | Baseline Değeri |
|--------|--------|----------------|
| Gini | 40% | 0.38515 |
| Recall@10% | 30% | 0.18469 |
| Lift@10% | 30% | 1.84715 |

- Gini, ROC AUC’ye göre ölçeklenmiş bir skor: `Gini = 2 x ROC AUC - 1`
- Recall@10% ve Lift@10% tahminlerin en üst %10’luk dilimi üzerinden hesaplanır.
- Özel metrik hesaplama fonksiyonu notebook içinde örneklenmiştir.

---

## 📁 Dosya Yapısı

INGHubsDatathon-MLModel/
│
├─ notebooks/
│ └─ model_training.ipynb # Colab notebook
│
├─ submissions/
│ └─ submission.csv # Yarışmaya gönderilen tahminler
│
├─ README.md
└─ .gitignore # Opsiyonel

---

## 🛠️ Kullanılan Teknolojiler

- Python 3.10  
- Pandas, NumPy, Scikit-learn  
- Matplotlib / Seaborn (veri görselleştirme)  
- Google Colab (model geliştirme ortamı)  

---

## 🚀 Kurulum ve Çalıştırma

1. Repository’yi klonlayın:
git clone <repo-url>
cd INGHubsDatathon-MLModel
Gerekli kütüphaneleri yükleyin:

pip install -r requirements.txt
Notebook’u Colab’da açın ve çalıştırın.

Submission dosyası submissions/submission.csv içinde yer almaktadır.

📌 Özel Metrik Hesaplama
Notebook içinde aşağıdaki özel metrikler hesaplanmıştır:

from sklearn.metrics import roc_auc_score
import numpy as np

# recall_at_k, lift_at_k, convert_auc_to_gini ve ing_hubs_datathon_metric fonksiyonları
Model skorları Gini, Recall@10% ve Lift@10% metriklerine göre ağırlıklandırılır.

Bu metrikler baseline model performansına göre normalize edilmiştir.

✅ Proje Durumu
Model eğitilmiş ve submission dosyası üretilmiştir.

Notebook içinde veri ön işleme, özellik mühendisliği, model eğitim ve değerlendirme adımları yer almaktadır.
