# ⚙️ Teknoloji Seçimi (Tech Stack)

Bu proje, bir otomotiv üretim tesisinde görev rotalarının çakışmalarını analiz etmek ve parçaların doğru araçlarla doğru sırayla taşınmasını optimize etmek amacıyla geliştirilmektedir. Proje, operasyonel planlama, malzeme taşıma ve iç lojistik süreçlerini yapay zekâ ile desteklemeyi hedefler.

---

## 🧱 1. Programlama Dili

### Python 3.10+
Python, geniş kütüphane desteği, veri analizi ve yapay zekâ alanındaki yetkinliği sayesinde projenin tamamında kullanılacaktır.

---

## 📚 2. Ana Python Kütüphaneleri

| Kategori | Kütüphane | Açıklama |
|----------|-----------|----------|
| **Veri Okuma/İşleme** | `pandas`, `numpy` | Excel ve CSV formatındaki görev ve parça verilerini yüklemek, işlem yapmak |
| **Grafik Yapısı ve Rota Analizi** | `networkx` | Görev yollarını graf olarak modellemek, koridor ve köşe çakışmalarını analiz etmek |
| **Zaman İşlemleri** | `datetime`, `timedelta`, `pytz` | Görevlerin başlangıç/bitiş zamanlarını karşılaştırmak |
| **Görselleştirme** | `matplotlib`, `seaborn`, `plotly` | Rota üzerindeki yoğunlukları, çakışmaları, güzergâhları renkli ve etkileşimli olarak göstermek |
| **UI / Arayüz** | `streamlit` | Kullanıcının dosya yüklemesi, analiz çalıştırması ve sonuçları görselleştirmesi için basit bir web arayüzü |
| **Veri Kaydetme** | `openpyxl`, `csv`, `json` | Sistem çıktılarının Excel, CSV veya JSON olarak dışa aktarılması |

---

## 🧠 3. AI & ML Modelleri (Zeka Katmanı)

Bu sistem doğrudan derin öğrenme kullanmasa da aşağıdaki AI bileşenleri entegre edilecektir:

### 🔸 Görev-Zaman Çakışma Tespiti (Custom Heuristic AI)
- Görevlerin zaman aralıklarını ve yollarını karşılaştırarak çakışma olup olmadığını belirleyen algoritmalar

### 🔸 Araç Eşleştirme Optimizasyonu
- Kapasite, hız, rota yoğunluğu gibi faktörlere göre taşıma görevlerini en uygun araçlara eşleştiren kural tabanlı AI

### 🔸 Opsiyonel: ML Tabanlı Teslim Süresi Tahmini
- Geçmiş taşıma görevlerine dayalı olarak parçaların teslim sürelerini tahmin edebilecek regresyon modelleri  
  (kütüphane: `scikit-learn`, `xgboost`)

---

## 🌐 4. Açık Kaynak AI Modelleri (Opsiyonel Entegrasyon)

| Model | Amaç | Nereden |
|-------|------|---------|
| **GPT-4 / GPT-3.5** | Doğal dil üzerinden rota durumu sorgulama, plan özeti oluşturma | `openai` API |
| **Mistral / LLaMA 3** | Yerel çalıştırma seçeneği ile doğal dil analizleri | `ollama`, HuggingFace |
| **RAG sistemi** | Kullanıcı tarafından yüklenen PDF veya prosedür dökümanlarından bilgi çekme | FAISS / ChromaDB |

---

## 🔁 5. Otomasyon & Agent Mimarisi

| Bileşen | Açıklama |
|---------|----------|
| **LangChain / AutoGen** | Görevleri planlayan, öneriler sunan ya da planları karşılaştıran görev ajanları oluşturmak için |
| **agents/** | AI ajanlarının görev dağılımı yapacağı yapı klasörü |
| **automation.md** | Bu sistemin nasıl otomatik kararlar aldığı açıklanır |

---

## 📦 6. Dosya ve Veri Formatları

| Veri Tipi | Format | Açıklama |
|-----------|--------|----------|
| Görev Verisi | `.xlsx`, `.csv` | from → to, saat, tekrar sayısı, görev tipi |
| Parça Listesi | `.xlsx` | Üretim planına göre ihtiyaç duyulan parçalar |
| Araç Bilgisi | `.csv` | Kapasite, tipi, güzergâhı, hızı |
| Grafik Haritası | `.json`, `.py` | Tesis layout’unda node-edge tanımlamaları |

---

## 📈 7. Veri Tabanı / Hafıza Yönetimi

Küçük veri boyutu nedeniyle klasik veritabanına ihtiyaç duyulmaz. Ancak:

- **Streamlit session_state** → kullanıcı etkileşimleri için
- **JSON dosyaları** → ara sonuçların kaydedilmesi için
- **FAISS/Chroma** → (opsiyonel) metin içeriği ile sorgulama yapılacaksa

---

## 💻 8. Geliştirme Ortamı

| Araç | Amaç |
|------|------|
| **VSCode** | Geliştirme ve test ortamı |
| **Jupyter Notebook** | Veri analizi prototiplerini hızlı test etmek |
| **GitHub** | Versiyon kontrolü, paylaşım |
| **Streamlit Cloud (opsiyonel)** | Demo yayını ve kullanıcı testleri |
| **Docker (opsiyonel)** | Kurulumların taşınabilir hâle getirilmesi |

---

## 🧪 9. Test Süreci

- Görev verileri ve güzergâhlar üzerinden test senaryoları oluşturulacak
- Çakışma tespiti algoritmaları manuel doğrulama ile test edilecek
- Streamlit üzerinden test formu sunulacak
- Araç rotası planlamaları öncesi/sonrası kıyaslama yapılacak

---

## 🚀 10. Gelecek Genişleme Fikirleri

- Gerçek zamanlı taşıma görevlerinin canlı takibi
- Kamera/sensör verisinin sisteme entegrasyonu
- İş güvenliği açısından tehlikeli çakışmaları önceden tespit eden sistem
- Tam otomatik plan üretimi + LLM destekli doğal dil sorgu motoru

