# 🏎️ AVT Racing — GitHub Yapılandırması Toplantı Notu

**Tarih:** 26 Mart 2026
**Sunan:** Aİ (Ahmet İnci)
**Konu:** GitHub repo yapısı, çalışma akışı ve ilerleme takip sistemi

---

## 📌 Neden GitHub?

arkadaşlar, TEKNOFEST 2026'ya hazırlanırken herkesin ne yaptığını takip etmemiz, dosyaları düzenli tutmamız ve birbirimizin işini bozmadan çalışmamız gerekiyor. bunun için GitHub kullanacağız.

GitHub sadece yazılımcılar için değil — teknik çizimler, simülasyon dosyaları, dökümanlar, sponsorluk materyalleri... her şey burada olacak.

---

## 🗂️ Repo Yapısı

her ekip için ayrı bir repo oluşturduk. hepsi `ahmetinci06` hesabı altında, public:

| Repo | Ekip | Ne İçin? | Link |
|------|------|----------|------|
| **avt-hub-dev** | 🏠 Merkez | Ana dashboard, tüm repo linkleri, genel koordinasyon | [github.com/ahmetinci06/avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev) |
| **avt-cad** | 🖊️ Teknik Çizim | CAD dosyaları, teknik çizimler, montaj planları | [github.com/ahmetinci06/avt-cad](https://github.com/ahmetinci06/avt-cad) |
| **avt-simulation** | ⚙️ Malzeme & Sim | FEA, CFD, malzeme analizi, simülasyon sonuçları | [github.com/ahmetinci06/avt-simulation](https://github.com/ahmetinci06/avt-simulation) |
| **avt-elektronik** | ⚡ Elektronik | PCB tasarımları, VCU firmware, devre şemaları | [github.com/ahmetinci06/avt-elektronik](https://github.com/ahmetinci06/avt-elektronik) |
| **avt-yazilim** | 💻 Yazılım | Telemetri, veri analizi, dashboard kodu | [github.com/ahmetinci06/avt-yazilim](https://github.com/ahmetinci06/avt-yazilim) |
| **avt-docs** | 📄 Sponsorluk & SM | Sponsorluk dosyaları, sosyal medya, TEKNOFEST dökümanları | [github.com/ahmetinci06/avt-docs](https://github.com/ahmetinci06/avt-docs) |

> 💡 **avt-hub-dev** ana merkez — buradan diğer tüm repo'lara ulaşabilirsiniz.

---

## 👥 Ekipler ve Sorumluluklar

### 🖊️ Teknik Çizim Ekibi → `avt-cad`
- Mahir Cengiz
- Muhammet Yahya Karataş
- Utku Esirgen
- Büşra Duymuş

### ⚙️ Malzeme & Simülasyon Ekibi → `avt-simulation`
- Ömer Arda Dündar
- Emre Göğer
- Serhad Agın

### ⚡ Elektronik Ekibi → `avt-elektronik`
- Onur Musaoğlu
- Deniz Bayrak
- Şeyma Hacıosmanoğlu
- Can Aral Çol
- Ömer Soner
- Emir Gülserin

### 💻 Yazılım Ekibi → `avt-yazilim`
- Aybüke Pamukçu
- Ali Efe Kaya
- Nisa Yegin
- Ata Doğan
- Ege Dönmez

### 📄 Sponsorluk & Sosyal Medya Ekibi → `avt-docs`
- Ceren Atasoy
- Sezin Gülbahçe
- Yaprak İleez
- Gülce Yılmaz

---

## 🔄 Çalışma Akışı (Herkes Bunu Bilmeli!)

```
1. Branch Oluştur    →  develop'tan yeni branch aç
2. Çalış & Commit    →  değişikliklerini yap, commit at
3. Push & PR Aç      →  push et, Pull Request oluştur
4. Review            →  Aİ & Yaver review eder
5. Merge             →  onay sonrası develop'a merge
6. Release           →  develop → main (stabil sürüm)
```

### Branch Kuralları

| Branch | Amaç | Kim Push Eder? |
|--------|-------|----------------|
| `main` | Stabil, son sürüm | ❌ Sadece PR ile (korumalı) |
| `develop` | Aktif geliştirme | ❌ Sadece PR ile |
| `feature/xxx` | Yeni özellik | ✅ Herkes kendi branch'inde |
| `fix/xxx` | Bug fix | ✅ Herkes kendi branch'inde |
| `docs/xxx` | Döküman güncellemesi | ✅ Herkes kendi branch'inde |

> ⚠️ **ÖNEMLİ:** `main` veya `develop`'a direkt push YAPMAYIN! Her zaman PR açın.

### Commit Mesajı Formatı

```
feat: yeni özellik ekle
fix: hata düzelt
docs: döküman güncelle
refactor: kodu yeniden düzenle
test: test ekle/güncelle
```

**örnek:**
```
feat: motor kontrol algoritması eklendi
fix: sıcaklık sensörü okuma hatası düzeltildi
docs: PCB şeması güncellendi
```

---

## 📊 İlerleme Takip Sistemi

her repo'da 3 önemli dosya var:

### 1. PROGRESS.md — Görev Takibi

görevlerinizi buraya yazın, durumunu güncelleyin:

| Etiket | Anlam |
|--------|-------|
| ✅ Yapıldı | Tamamlandı, test edildi |
| 🔄 Yapılıyor | Aktif olarak üzerinde çalışılıyor |
| 💡 Fikir Aşaması | Henüz başlanmadı, planlama/araştırma |
| 🐛 Debug | Hata ayıklama aşamasında |
| 🔍 Review Bekliyor | PR açıldı, review bekleniyor |
| ⏸️ Beklemede | Başka bir şeye bağımlı, bekliyor |

**örnek:**

| Görev | Sorumlu | Durum | Tarih | Notlar |
|-------|---------|-------|-------|--------|
| VCU PWM kontrol kodu | @onur | 🔄 Yapılıyor | 2026-03-26 | STM32 HAL kullanılıyor |
| Şasi 3D model | @mahir | ✅ Yapıldı | 2026-03-25 | v2 onaylandı |

### 2. BUGS.md — Bug/Hata Takibi

karşılaştığınız hataları buraya yazın:

| Öncelik | Anlam |
|---------|-------|
| 🔴 Kritik | Acil çözülmeli |
| 🟡 Orta | Önemli ama acil değil |
| 🟢 Düşük | Zaman olunca |

> çözülen buglar silinmez! "Çözüldü" bölümüne taşınır — gelecekte referans olur.

### 3. WORKFLOW.md — Detaylı Akış Rehberi

adım adım nasıl çalışılacağı yazıyor. emin olmadığınızda buraya bakın.

---

## 🚀 İlk Adımlar (Herkesin Yapması Gereken)

### 1. GitHub Hesabı Oluşturun
- [github.com](https://github.com) → Sign Up
- **GitHub username'inizi bana gönderin** → sizi repo'ya collaborator olarak ekleyeceğim

### 2. Git Kurun
- **Windows:** [git-scm.com](https://git-scm.com/download/win) → indir, kur
- **Mac:** Terminal → `xcode-select --install`
- **Linux:** `sudo apt install git`

### 3. GitHub Desktop (kolay yol)
Git komutlarıyla uğraşmak istemiyorsanız:
- [desktop.github.com](https://desktop.github.com) → indir, kur
- GitHub hesabınızla giriş yapın
- "Clone a repository" → repo URL'sini yapıştırın

### 4. Repo'yu Clone Edin
```bash
git clone https://github.com/ahmetinci06/avt-cad.git    # (kendi ekibinizin reposunu)
cd avt-cad
```

### 5. İlk Branch'inizi Açın
```bash
git checkout develop
git pull origin develop
git checkout -b feature/ilk-gorev
```

### 6. Dosyalarınızı Ekleyin, Commit Atın
```bash
git add .
git commit -m "feat: ilk CAD dosyası eklendi"
git push -u origin feature/ilk-gorev
```

### 7. PR Açın
- GitHub'a gidin → "Compare & pull request" → açıklama yazın → oluşturun

> 📚 detaylı rehber her repo'nun `docs/GITHUB-GUIDE.md` dosyasında var!

---

## 🤝 Review Süreci

| Reviewer | Rol |
|----------|-----|
| @ahmetinci06 (Aİ) | her şeyi yapan adam ☕ — final onay |
| Yaver (AI CTO) | uyumayan co-founder 🤖 — kod kalitesi & teknik review |

her PR en az 1 review alacak. değişiklik istenirse düzeltin, tekrar push edin.

---

## 📅 Haftalık Rutin

| Gün | Ne Yapılır? |
|-----|-------------|
| Pazartesi | PROGRESS.md'yi güncelle — bu hafta ne yapacaksın? |
| Her gün | commit at, push et — küçük adımlar büyük işler |
| Cuma | Haftalık özet — ne tamamlandı, ne bloke? |
| Pazar | Bug review — BUGS.md'yi kontrol et |

---

## ❓ Sıkça Sorulan Sorular

**S: Git hiç bilmiyorum, sorun olur mu?**
C: Hayır! Her repo'da `docs/GITHUB-GUIDE.md` var — sıfırdan anlatan Türkçe rehber. Ayrıca GitHub Desktop kullanabilirsiniz, komut satırı gerektirmez.

**S: Yanlışlıkla bir şey bozarsam?**
C: Git'te her şey geri alınabilir. `main` branch korumalı olduğu için yanlışlıkla oraya push edemezsiniz. Kendi branch'inizde rahatça çalışın.

**S: CAD dosyaları çok büyük, GitHub'a yüklenir mi?**
C: 100MB altı dosyalar direkt yüklenir. Daha büyük dosyalar için Git LFS kullanacağız (gerekirse kurarız).

**S: Ben sadece döküman/sponsorluk ekibindeyim, bana ne?**
C: `avt-docs` repo'su tam size göre — sponsorluk dosyaları, sunumlar, sosyal medya içerikleri hepsi orada. Word/PDF dosyalarınızı da yükleyebilirsiniz.

**S: Sorun yaşarsam kime soracağım?**
C: Yazılım ekibindeki arkadaşlara veya direkt Aİ'ye mesaj atın.

---

## 📞 Sonraki Adımlar

1. ✅ **Bugün:** GitHub hesabı oluşturun (yoksa)
2. ✅ **Bugün:** Username'inizi Aİ'ye gönderin
3. 📥 **Bu hafta:** Kendi repo'nuzu clone edin
4. 📝 **Bu hafta:** PROGRESS.md'ye ilk görevinizi ekleyin
5. 🚀 **Gelecek hafta:** İlk PR'ınızı açın!

---

> 🏎️ **TEKNOFEST 2026 bizi bekliyor. organize çalışırsak, kazanırız.**
>
> — Aİ & Yaver 🌿
