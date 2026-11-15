# NOKVA Balıklı V51 | 15.11.2026 | Profesyonel lokal rötuş denemesi

- Gerçek Mac V51 kaynak dosyasından, Imagine/image_gen olmadan OpenCV, fotoğraf kaynaklı gökyüzü pikselleri ve GIMP kullanılarak V52(A/B/C), V53(A/B), V54(A/B/C), V55(A/B/C), V56(A/B/C) ayrı immutable adaylar üretildi.
- Hedef yalnız saç-kulak-yanak-çene dış matte/halo bandı. Göz, burun, ağız, yüzün iç pikselleri, sakal/neck ana bölümü, gövde, kıyafet, balık, eller, ağ ve göl kaynak-kilitli.
- V52/V53 çevreyi fazla sertleştirdi. V55/V56 alt çene kenarında yeni çizgi/halo oluşturdu. Yakın plan bağımsız Qwen3.5 görsel denetim ve 1×/4× insan gözü incelemesi V51'i korumanın daha güvenli olduğunu gösterdi; V54A yalnız 275 dış kenar pikselinde en hafif renk düzeltme alternatifi.
- ÖZNEL MODEL PUANLARI ÇELİŞİYOR. V54 yakın plan denetiminde V51 foto gerçeklik 9.0, V54A 8.5; V56 modeli en iyi olarak V51'i seçti ama bütün adaylarda jaw halo gördü. Bu nedenle '8.5/10 kesin onaylı final' iddiası YOK. Bağımsız insan/biyometrik QA yok.
- Teknik QA: V54A görüntü ve V51 554×554 PNG, piksel koruma testleri PASS. GIMP editable ORA iki katman RGB exact, native XCF aç-kaydet-tekrar aç PASS. Kaynaklar değişmedi.
- KALİTE KARARI: V51 en güçlü kabul edilen kaynak; V54A ise yerel retuş kontrol kopyası, henüz müşteri GO değil. Fotoğrafı yüksek kaliteli, orijinal yüksek çözünürlükteki gerçek oyuncu kaynaklarıyla yeniden maskeye oturtmak gerekecek.
