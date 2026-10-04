# Stark-OS 6.0 — kurulum ve yenilikler

## Kurulum

1. Bu klasördeki **bütün dosyaları** sitenin kök klasörüne yükle (eskilerin üzerine yaz):
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`
2. Uygulamayı kapat, iki kez aç. İkinci açılışta yeni sürüm gelir.
3. Ayarlar'ın en altında **"Stark-OS version 6.0"** yazıyorsa güncelleme tamamdır.
4. Birden fazla cihaz kullanıyorsan hepsini güncelle. Eski sürümde hedefleri kaydedersen yeni günlük hedefler varsayılana döner.

Verilerin (PIN, kasa, Firebase ayarı, API anahtarı) yerinde kalır. Eski kasa ilk açılışta yeni alanlarla tamamlanır.

## Yeni ne var

| Bölüm | Ne yapar |
|---|---|
| Üst panel | Günün puanı (halka), sınava kalan gün, sıradaki hedef, mikrofon, hızlı düğmeler |
| Missions | Günlük yapılacaklar. Bitmeyenler ertesi güne geçer, "Tomorrow" ile yarını planlarsın |
| Habits | Alışkanlık + seri. Sayaçlı alışkanlık (8 bardak su gibi). Oklarla 6 gün geriye işaretleme |
| Mission log | 1–5 ruh hali + günlük not |
| Countdown | Sınav tarihi, konu listesi, haftalık gereken tempo, AI konu planı |
| Error log | Yanlış soru defteri. Fotoğraftan AI ile ekleme, 1-3-7-14-30-60 gün aralıklı tekrar |
| Class schedule | Haftalık ders programı |
| Weekly report | Haftalık özet, geçen haftayla karşılaştırma, derse göre çalışma, içgörüler, seviye, rekorlar |
| Daily briefing | Günde bir kez açılışta otomatik brifing; sesli okuma ve AI gün planı |
| Alerts | Saatli hatırlatmalar, akıllı uyarılar, takvime aktarma (.ics) |
| J.A.R.V.I.S. | Mikrofon + internetsiz kısa komutlar |
| Log past day | Unuttuğun günü sonradan doldurma |
| Ayarlar | Günlük hedefler, ses seviyesi, otomatik tema, otomatik kilit, geri yükleme noktaları |

## İnternetsiz çalışan komutlar (yaz ya da söyle)

`20 şınav` · `kilo 60,4` · `45 dakika ders çalıştım` · `7.5 saat uyudum` · `8500 adım` ·
`çalışmaya başla` / `çalışmayı bitir` · `görev ekle: ...` · `yarın görev ekle ...` ·
`<alışkanlık adı> yaptım` · `haftalık raporu aç`

Soru cümleleri, olumsuz cümleler ("yapmadım") ve uzun cümleler kendiliğinden kaydedilmez, AI'ye gider (API anahtarı gerekir).

## Bilmen gerekenler

- **Bildirimler:** Uygulama açıkken ya da arka planda dururken çalışır. Tamamen kapalı bir web uygulaması telefonu uyandıramaz. Her zaman çalması gereken alarmlar için Alerts → *Export to calendar* ile telefon takvimine aktar.
- **Sesli komut:** Tarayıcının konuşma tanımasına bağlı. Android Chrome'da çalışır; iPhone'da ana ekrana eklenmiş uygulamada çalışmayabilir.
- **Günün puanı:** Çalışma, şınav, adım, uyku, protein hedefleri ile alışkanlıkların ortalaması. Varsayılan hedefler: 120 dk, 50 şınav, 8000 adım, 8 saat. Ayarlar'dan değiştir; 0 yazarsan o hedef sayılmaz.
- **Otomatik tema (HUD):** Puan %90'a ulaşınca altın, 15:00'ten sonra geride kalınca turuncu. Elle tema seçersen kendiliğinden kapanır.
- **Hata defteri fotoğrafları ve geri yükleme noktaları** yalnızca o cihazda saklanır, buluta gitmez.
- **Senkron:** Uygulama artık buluttaki kopyayı okumadan buluta yazmıyor. Yeni ya da verisi silinmiş bir cihaz, dolu bir kasanın üzerine boş veri yazamaz.

## v5 yenilikleri

- **Yumuşak MODE geçişi:** HUD ↔ Minimal artık ~0,6 sn'lik çapraz solma ile değişir. Hareket azaltma ayarı açıksa anında geçer.
- **Net calculator:** TYT ve AYT (Sayısal) için doğru/yanlış girince net (doğru − yanlış/4) hesaplar, sonuç geçmişi tutar.
- **Export CSV:** Ayarlar'dan son 90 günün tablosu (Excel'de açılır).
- **Konfeti:** Günün puanı %100 olunca günde bir kez.

## v6 yenilikleri

- **Focus timer (Pomodoro) kaldırıldı.**
- **HUD temaları:** Ice Blue, Quantum Violet, Neon Rose, Arc Teal, Wayne Silver + kendi seçtiğin renk (Custom). Ayarlar → Theme.
- **Minimal görünüm:** Auto / Light / Dark seçimi ve 5 vurgu rengi (Clay, Sage, Ocean, Plum, Gold) + özel renk.
- **Tema geçişleri** artık yumuşak solarak değişir.
- **Efektler (HUD):** FX Full / Calm / Off. Calm hareketleri durdurur, Off tarama çizgileri ve köşe işaretlerini de kapatır (pil ve okunabilirlik için).
- **Focus mode:** Üstteki çipe basınca sadece "Today" bölümü kalır, gerisi gizlenir.
- **Seri rozeti:** Gün puanı %70+ olan ardışık gün sayısı (2 ve üzeri olunca çıkar).
- **Net calculator:** son sonuçların küçük trend grafiği.
