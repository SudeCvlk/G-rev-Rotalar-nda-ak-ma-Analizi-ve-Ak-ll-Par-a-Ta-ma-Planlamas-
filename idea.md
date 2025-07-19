# 📌 Problem Tanımı

Büyük ölçekli otomotiv üretim tesislerinde motor parçalarının üretim hücrelerine taşınması sırasında görevlerin rotaları genellikle sabit veya manuel planlamaya dayalıdır. Özellikle vardiya saatleri ve yoğun üretim dönemlerinde forklift, AGV ve operatörler aynı yolları kullanmakta ve bu durum:

- Rota çakışmalarına  
- Koridor tıkanıklıklarına  
- Görev gecikmelerine  
- İş güvenliği risklerine  

neden olmaktadır.

# 👤 Bu Problemi Yaşayan Kullanıcı Kimdir?

- Operasyonel Planlama Uzmanları  
- İç Lojistik Personeli  
- Malzeme Çekme Ekibi  
- Üretim Sorumluları

# 🤖 AI Bu Çözümde Nasıl Bir Rol Üstleniyor?
1. Görev ve Rota Analizi (Veri Girişi + Zamanlama)
Gerçekleştirilen taşıma görevlerinin kaynak–hedef (from → to) rotaları ve zaman aralıkları toplanır

Her görev bir zaman aralığında bir yol/köşe üzerinde bulunur

2. Çakışma Tespiti (Edge & Node Conflict Detection)
AI modeli, görevlerin zaman-mekân kesişimlerini analiz eder

Aynı anda aynı yolda olan görevleri tespit eder (koridor çakışması)

Aynı anda aynı kavşakta (dönüş noktası) bulunan görevleri belirler (köşe çakışması)

3. Yoğunluk ve Tek Yön Önerisi
Haftalık görev yoğunluğu ve yön analizi yapılır

4. Akıllı Parça Dağıtım Planı (Genişletilmiş)
AI, en az çakışmalı rotayı önererek görev zamanlamasını günceller

Görevler için alternatif zaman veya rota önerileri sunar

# 🚀 Neden Bu Proje?

Gerçek dünyada karşılaşılan, ölçülebilir bir problem. AI, grafik algoritmalar ve zaman analiziyle çözülebilir. Genişletilebilir ve sahadaki veriyle güçlendirilebilir.
Opsiyonel genişleme: Rota optimizasyonu, görselleştirme, öneri sistemleri
