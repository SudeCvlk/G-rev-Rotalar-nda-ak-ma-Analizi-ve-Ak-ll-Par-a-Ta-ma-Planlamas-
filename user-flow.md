# 👣 Kullanıcı Akışı (User Flow)

Bu uygulama, bir üretim tesisinde görev rotalarındaki çakışmaları analiz ederek ve taşıma ihtiyaçlarını üretim planına göre değerlendirerek **akıllı parça taşıma ve araç atama planı** oluşturur. Kullanıcılar bu sistemi aşağıdaki adımlarla kullanır:

---

## 1. 🗂 Görev ve Parça Verilerini Yükleme
Kullanıcı:
- Üretim planına dayalı malzeme ihtiyaç verisini yükler (örneğin: motor tipi, üretim istasyonu, parça tipi, hedef nokta, teslim saati).
- Görev geçmişi veya gerçek zamanlı görev verilerini sisteme yükler:
  - Kaynak → Hedef (rota)
  - Görev saati ve süresi
  - Parça miktarı
  - Görev tekrarı (frekans)
- Araç envanteri (forklift, AGV) bilgilerini girer:
  - Araç tipi, kapasitesi, hız bilgisi

---

## 2. 🧠 AI Tabanlı Görev-Rota-Çakışma Analizi
Sistem:
- Görevlerin zaman-mekân analizini yapar
- Koridor (edge) ve köşe (node) çakışmalarını tespit eder
- Hangi yollarda hangi saatlerde yoğunluk olduğu belirlenir
- Araç güzergâhlarına göre trafik haritası çıkarılır

---

## 3. 🚚 Akıllı Parça Dağıtım ve Araç Atama
Sistem:
- Her parçanın hedef üretim hücresine ne zaman ulaşması gerektiğine göre:
  - Hangi araçla taşınmalı?
  - Hangi sırayla yüklenmeli?
  - Hangi rotadan gitmeli?
  - Ne zaman yola çıkmalı?
- Teslimat süresine göre öncelik verir
- Araçların yük kapasitelerini aşmadan optimum dağılım yapar

---

## 4. 🔁 Alternatif Planlama ve Rota Önerileri
Kullanıcı:
- Sistemden gelen önerileri inceler:
  - Alternatif rotalar (çakışmasız yollar)
  - Farklı araç atamaları
  - Görevlerin zamanının değiştirilmesi (± dakikalık kaydırmalar)
- Gerekirse “çakışmaları azalt” veya “öncelikli teslimata göre sırala” gibi modları seçer

---

## 5. 📊 Raporlama ve Görselleştirme
- Grafik üzerinde:
  - Araç rotaları
  - Yoğunluk seviyeleri (renkli)
  - Çakışma bölgeleri
- Tablolarda:
  - Her parçanın taşıma planı
  - Araç başına görev listesi
  - Gecikme riski taşıyan parçalar
- Karşılaştırma: “AI planı” vs “Mevcut manuel plan”

---

## 6. 📥 Planları Dışa Aktarma
Kullanıcı:
- Araçlara atanmış görev listelerini Excel/PDF olarak indirir
- Raporları yönetimle paylaşır
- Gelişmiş kullanıcılar Streamlit panel üzerinden canlı senaryoları simüle edebilir

---

## 🚦 Opsiyonel Genişlemeler
- Gerçek zamanlı konum/sensör verisiyle canlı trafik analizi
- ML tabanlı gecikme tahmini (parça bazlı)
- LLM destekli doğal dil sorgulama:  
  > “Bugün saat 13:00’te N7-N9 arası yoğun mu?”  
  > “A101 parçası en geç kaçta yüklenmeli?”
