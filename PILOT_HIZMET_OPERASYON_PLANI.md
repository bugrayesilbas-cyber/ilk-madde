# İLK MADDE — Pilot Hizmet Operasyon Akışı
Sürüm: 1.0 | 14.11.2026

## 1. Talep ve ön değerlendirme
- Talep kaynağı: `[ana-sayfa]`, `[hesaplayici]`, `[hizmet-kapsami]`, `[dogrudan]`.
- Kayıt alanları: talep tarihi, firma/iletişim, iletişim adresi, üretim türü, talep konusu, aşama, son iletişim, sonraki aksiyon.
- Gizli müşteri çizimleri ve ticari sırlar ön görüşmede talep edilmez.
- Ön görüşmede tek parça/tek senaryo sınırı, gerekli veri ve teslim formatı doğrulanır.

## 2. Teklif ve sipariş onayı
- Tanıtım bedeli: 1.490 TL / tek parça, tek üretim senaryosu.
- Vergi/fatura, ödeme yöntemi, teslim tarihi, revizyon kapsamı ve veri gizliliği şartları karşılıklı yazılı netleştirilmeden ücretli çalışma başlamaz.
- Ödeme tahsilatı ve fatura düzenleme için yasal/ticari altyapı ayrıca doğrulanır. Sitede ödeme alınmaz.
- Müşteriye taslak rapor değil, kapsamı onaylanmış teslimat sözü verilir.

## 3. Veri kabul kontrolü
- Toplam üretim > 0; 0 ≤ fire < toplam; adetler tam sayı.
- Çevrim süresi, saatlik tezgâh gideri, hammadde birim gideri, diğer parti giderleri ≥ 0.
- Para birimi ve dönem, verinin kaynağı ve varsayımlar kayda geçirilir.
- Tezgâh saat maliyetinin hangi giderleri içerdiği teyit edilir; çift sayım riski incelenir.
- Yeniden işleme, hurda geri kazanımı, hazırlık süresi ve dış operasyon gibi kalemlerin kapsam dışı olup olmadığı açıklanır.

## 4. Hesap ve mühendislik kontrolü
- Parti maliyeti = toplam × çevrim/3600 × saat maliyeti + toplam × hammadde + diğer giderler.
- Sağlam birim maliyet = parti maliyeti / (toplam − fire).
- Hedef fire senaryosu aynı parti maliyeti varsayımıyla karşılaştırmadır; gerçekleşmiş tasarruf değildir.
- Hesaplama sonucu, girdi kaynakları ve müşteri varsayımları ayrı gözden geçirilir.
- Mühendislik önerileri veriyle desteklenmiyorsa kesin kök neden olarak sunulmaz.

## 5. Rapor ve teslimat
- `rapor-olusturucu.html` ile rapor taslağı hazırlanır.
- Rapor numarası, parça tanımı, veriler, hesap yöntemi, karşılaştırma, öneriler ve sınırlamalar kontrol edilir.
- PDF çıktısı alınır, okunabilirlik ve sayfa düzeni kontrol edilir.
- Onaylanan PDF müşteriye gönderilir; teslim tarihi ve geri bildirim kayda alınır.

## 6. Satış hunisi ve ölçümler
Aşamalar: Yeni aday → İletişime geçildi → Yanıt geldi → Ön görüşme → Teklif → Onay → Analiz → Teslim → Tamamlandı; ayrıca Yanıtsız ve Kaybedildi.

Haftalık metrikler: temas edilen firma sayısı, yanıt sayısı, görüşme sayısı, teklif sayısı, kabul sayısı, tahsil edilen gelir (kanıtlı), teslim edilen rapor sayısı.

**Dönüşüm:** Onaylanan teklif / gönderilen teklif. Yalnızca doğrulanmış kayıtlarla hesaplanır.

## 7. Kalite kontrol listesi
- [ ] Firma ve veri paylaşımı yetkisi teyit edildi
- [ ] Kapsam/bedel/fatura/teslim tarihi yazılı onaylandı
- [ ] Girdi bütünlüğü ve çift sayım kontrol edildi
- [ ] Fire ve maliyet hesapları çapraz kontrol edildi
- [ ] Varsayımlar ve hariç tutulan kalemler raporda belirtildi
- [ ] Senaryo farkı garanti edilen tasarruf olarak sunulmadı
- [ ] PDF kontrol edildi ve teslim kaydı oluşturuldu
- [ ] Geri bildirim ve sonraki aksiyon işlendi

## 8. İkinci ürün için ürün gereksinimi
**Ürün:** İLK MADDE CNC Maliyet ve Fire Takip Excel Şablonu.

MVP: parti bazlı veri girişi, sağlam/fire adetleri, toplam ve birim maliyet, hedef marj, aylık özet, örnek veri, açıklama, veri doğrulama. Makro gerektirmeyen XLSX. Tek dosya, Türkçe. Satışa çıkmadan önce Excel formül testleri, kullanım kılavuzu, fiyatlandırma, lisans/teslim ve ödeme altyapısı tamamlanmalı.
