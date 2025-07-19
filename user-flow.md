# 👣 Kullanıcı Akışı (User Flow)

Bu uygulama, bir üretim tesisinde görev rotalarındaki çakışmaları analiz ederek, daha verimli parça taşıma planı oluşturmayı hedefler. Kullanıcılar bu sistemi aşağıdaki adımlarla kullanır:

---

## 1. 🗂 Görev Verisi Yükleme
Kullanıcı (örneğin bir planlama uzmanı):

- Excel veya CSV formatında görev verisini sisteme yükler.
- Bu veri her görev için:
  - Başlangıç ve bitiş noktası (`from`, `to`)
  - Görevin yapılma zamanı (`start_time`, `end_time`)
  - Görev tekrar sayısı (`count`)
  gibi bilgileri içerir.

---

## 2. 🧠 Çakışma ve Yoğunluk Analizi Başlatma
Kullanıcı:

- "Analiz Et" butonuna tıklar.
- Sistem, NetworkX (veya benzeri) graf üzerinden:
  - Zaman bazlı koridor (edge) ve köşe (node) çakışmalarını tespit eder.
  - Görevlerin geçtiği yolların yoğunluğunu hesaplar.

---

## 3. 🧭 Tek Yön ve Alternatif Rota Önerileri
Sistem:

- En çok çakışan yollar için:
  - “Bu koridor sabah 08:00–10:00 arası tek yön sağa olabilir” gibi öneriler sunar.
- Alternatif olarak:
  - Görevlerin başlangıç saatini biraz kaydırarak çakışmasız bir plan önerir.

---

## 4. 📊 Görselleştirme ve Raporlama
Kullanıcı:

- Koridorlar renkli grafiklerle gösterilir:
  - Kırmızı: çok yoğun
  - Sarı: orta yoğunluk
  - Yeşil: uygun
- Sistem aynı zamanda önerilen düzenlemeleri ve etkilerini tablo halinde sunar:
  - % çakışma azalması
  - Ortalama taşıma süresinde azalma

---

## 5. 📤 Sonuçları İndir
Kullanıcı:

- Alternatif planları CSV/Excel olarak indirebilir
- Raporları yönetim ile paylaşmak üzere PDF olarak alabilir

---

## 🚦 Opsiyonel Genişlemeler
- Canlı görev akışı takibi (gerçek zamanlı analiz)
- Kamera/sensör destekli veri entegrasyonu
