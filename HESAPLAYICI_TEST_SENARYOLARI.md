# CNC maliyet hesaplayıcı — doğrulama senaryoları

Tarih: 2026-11-14. Bu kontrol, hesaplayıcıdaki JavaScript formüllerinin bağımsız Decimal aritmetiğiyle karşılaştırılmasıdır. Tarayıcı arayüzü veya canlı GitHub Pages uçtan uca testi değildir.

| Senaryo | Toplam | Fire | Çevrim (sn) | Tezgâh (TL/saat) | HM (TL/adet) | Diğer (TL) | Marj | Beklenen sağlam | Beklenen toplam TL | Beklenen birim TL | Beklenen satış TL |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Standart | 1000 | 30 | 45 | 900 | 12 | 0 | %20 | 970 | 23250,00 | 23,97 | 29,96 |
| Sıfır fire | 1000 | 0 | 45 | 900 | 12 | 0 | %20 | 1000 | 23250,00 | 23,25 | 29,06 |
| Yüksek fire | 100 | 99 | 36 | 360 | 5 | 50 | %25 | 1 | 910,00 | 910,00 | 1213,33 |
| Sıfır maliyet | 10 | 0 | 0 | 0 | 0 | 0 | %0 | 10 | 0,00 | 0,00 | 0,00 |

Formüller:
- Sağlam = toplam - fire
- Fire % = fire / toplam × 100
- Toplam maliyet = toplam × çevrim / 3600 × saatlik tezgâh maliyeti + toplam × HM birim maliyeti + diğer giderler
- Birim maliyet = toplam maliyet / sağlam
- Satış fiyatı = birim maliyet / (1 - marj/100)

**Sınırlar:** Fire adedi toplam adede eşit veya büyük olamaz. Negatif girdiler, boş alanlar, kesirli adetler ve marjın %100 veya üzeri olması reddedilmelidir. Satış fiyatı hesabı brüt kâr marjı yaklaşımıdır, maliyet üzerine kâr ekleme (markup) değildir. KDV ve finansman giderleri dahil değildir. Analiz girdilerin doğruluğuna bağlıdır.

**Henüz yapılmayan:** Canlı tarayıcı testi, mobil cihaz testi, kullanıcı deneyimi testi, otomatik regresyon testi.