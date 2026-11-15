# NOKVA Balıkçı V57C, 15 Kasım 2026
Kaynak V55A (554x554), yalnız sağ dış yanak-çene ve gökyüzü arasında 509 kenar pikseli yeniden hesaplandı. Yeni bir yüz veya sahne üretilmedi. Fotoğrafın iç kısmı, mimik, kıyafet, eller, balık, su, ağ kaynağın aynı RGB pikselleridir. Daha önceki iyi V55A dosyası korunuyor.

**Yöntem:** Adobe'nin anti-aliased selection/fringe rehberindeki gibi karışmış arka plan renğini ayrıştırıp maskenin kısmi opaklığını kontrollü daraltma. Uygulama Python OpenCV + Pillow, yerel Mac dosyaları; Imagine kullanılmadı. Kaynak: https://helpx.adobe.com/photoshop/desktop/make-selections/refine-modify-selections/fringe-pixels-around-a-selection.html

**QA:** Ayrı yerel Qwen3.5 görsel karşılaştırması, V57C'yi en doğal seçti. Foto gerçekçilik 9/10, **kenar bütünlüğü yalnız 7/10**. Hâlâ hafif gri halo/karanlık kontur olabiliyor, 8.5+ kesin geçişi yok. Modelin sayısal notu insan onayı veya biyometrik doğrulama değildir ve önceki turlarda tutarsızlık gösterdi. Bu sürüm müşteri GO değil, sahibinin son incelemesine sunulan en başarılı yerel de-fringe adayı.

**Teknik:** OpenRaster iki katman orijinal ve 509 piksel onarımdan birebir reconstruct ediliyor; GIMP XCF native aç/kaydet/aç testi ayrıca çalıştırılacak. Orijinal görüntü bozulmadı.
