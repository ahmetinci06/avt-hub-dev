# 🏎️ AVT Racing — Ana Geliştirme Hub'ı

> **avt-hub-dev** — AVT Racing takımının merkezi geliştirme deposu. Dashboard, web arayüzü ve tüm ekip koordinasyonunun yönetildiği ana repo.

[![TEKNOFEST 2026](https://img.shields.io/badge/TEKNOFEST-2026-red)](https://teknofest.org)
[![GitHub](https://img.shields.io/badge/GitHub-ahmetinci06-black)](https://github.com/ahmetinci06)

---

## 📋 İçindekiler

- [Proje Hakkında](#-proje-hakkında)
- [Ekip Yapısı](#-ekip-yapısı)
- [Repo Bağlantıları](#-repo-bağlantıları)
- [Proje Zaman Çizelgesi](#-proje-zaman-çizelgesi)
- [Mimari Genel Bakış](#-mimari-genel-bakış)
- [Geliştirme Ortamı Kurulumu](#-geliştirme-ortamı-kurulumu)
- [CI/CD Pipeline](#-cicd-pipeline)
- [GitHub Projects Kullanım Rehberi](#-github-projects-kullanım-rehberi)
- [Branch Yapısı](#-branch-yapısı)
- [Katkı Rehberi](#-katkı-rehberi)

---

## 🚀 Proje Hakkında

AVT Racing, TÜBİTAK TEKNOFEST Elektrikli Araç Yarışması için yarışmaya hazır bir elektrikli araç geliştiren Bahçeşehir Üniversitesi takımıdır. Bu repo, takımın tüm yazılım, elektronik, tasarım ve döküman çalışmalarını koordine eden merkezi hub'dır.

**Amaç:** TEKNOFEST 2026'da yarışacak, telemetri destekli, tam işlevsel bir elektrikli yarış aracı geliştirmek.

---

## 👥 Ekip Yapısı

### 🖊️ Teknik Çizim Ekibi
| İsim | Rol |
|------|-----|
| Mahir Cengiz | Teknik Çizim |
| Muhammet Yahya Karataş | Teknik Çizim |
| Utku Esirgen | Teknik Çizim |
| Büşra Duymuş | Teknik Çizim |

### ⚙️ Malzeme & Simülasyon Ekibi
| İsim | Rol |
|------|-----|
| Ömer Arda Dündar | Malzeme & Simülasyon |
| Emre Göğer | Malzeme & Simülasyon |
| Serhad Agın | Malzeme & Simülasyon |

### ⚡ Elektronik Ekibi
| İsim | Rol |
|------|-----|
| Onur Musaoğlu | Elektronik |
| Deniz Bayrak | Elektronik |
| Şeyma Hacıosmanoğlu | Elektronik |
| Can Aral Çol | Elektronik |
| Ömer Soner | Elektronik |
| Emir Gülserin | Elektronik |

### 💻 Yazılım Ekibi
| İsim | Rol |
|------|-----|
| Aybüke Pamukçu | Yazılım |
| Ali Efe Kaya | Yazılım |
| Nisa Yegin | Yazılım |
| Ata Doğan | Yazılım |
| Ege Dönmez | Yazılım |

### 📣 Sponsorluk & Sosyal Medya Ekibi
| İsim | Rol |
|------|-----|
| Ceren Atasoy | Sponsorluk & Sosyal Medya |
| Sezin Gülbahçe | Sponsorluk & Sosyal Medya |
| Yaprak İleez | Sponsorluk & Sosyal Medya |
| Gülce Yılmaz | Sponsorluk & Sosyal Medya |

---

## 🔗 Repo Bağlantıları

| Repo | Açıklama | Ekip |
|------|----------|------|
| [avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev) | 🏠 Ana hub (bu repo) | Tüm ekip |
| [avt-cad](https://github.com/ahmetinci06/avt-cad) | 🖊️ CAD dosyaları, teknik çizimler | Teknik Çizim |
| [avt-simulation](https://github.com/ahmetinci06/avt-simulation) | ⚙️ Simülasyon, FEA, malzeme analizi | Malzeme & Simülasyon |
| [avt-elektronik](https://github.com/ahmetinci06/avt-elektronik) | ⚡ PCB, firmware, VCU | Elektronik |
| [avt-yazilim](https://github.com/ahmetinci06/avt-yazilim) | 💻 Yazılım, telemetri, dashboard | Yazılım |
| [avt-docs](https://github.com/ahmetinci06/avt-docs) | 📄 Sponsorluk, TEKNOFEST dökümanları | Sponsorluk & Sosyal Medya |

---

## 📅 Proje Zaman Çizelgesi — TEKNOFEST 2026

```
Q1 2026 (Ocak–Mart)
├── ✅ Ekip kurulumu ve repo setup
├── ✅ Araç konsepti ve tasarım gereksinimleri
├── 🔄 CAD ön tasarım (chassis, süspansiyon)
└── 🔄 VCU elektronik tasarımı başlangıcı

Q2 2026 (Nisan–Haziran)
├── CAD finalizasyon
├── PCB v1 tasarım ve sipariş
├── Telemetri sistemi prototipi
└── TEKNOFEST başvuru dökümanları

Q3 2026 (Temmuz–Eylül)
├── Araç prototip üretimi
├── PCB v2 (revize)
├── Yazılım entegrasyon testleri
└── Simülasyon doğrulama

Q4 2026 (Ekim–Aralık)
├── Son testler ve düzeltmeler
├── TEKNOFEST hazırlığı
├── Sponsorluk sunumları
└── 🏁 TEKNOFEST 2026 Yarışması
```

---

## 🏗️ Mimari Genel Bakış

```
AVT Racing Araç Sistemi
│
├── 🚗 Fiziksel Araç
│   ├── Chassis (CAD → avt-cad)
│   ├── Süspansiyon sistemi
│   └── Powertrain
│
├── ⚡ Elektronik Sistem (avt-elektronik)
│   ├── VCU (Vehicle Control Unit)
│   ├── BMS (Battery Management System)
│   ├── Motor Controller
│   └── Sensör ağı (IMU, GPS, sıcaklık)
│
├── 💻 Yazılım Sistemi (avt-yazilim)
│   ├── VCU Firmware (C/C++)
│   ├── Telemetri stack (Python/Node.js)
│   └── Dashboard (React/Web)
│
└── 📊 Dashboard (avt-hub-dev)
    ├── Real-time telemetri görüntüleme
    ├── Veri loglama
    └── Araç durum monitörü
```

---

## ⚙️ Geliştirme Ortamı Kurulumu

### Gereksinimler
- Node.js 18+ (dashboard için)
- Python 3.10+ (telemetri araçları için)
- Git 2.x

### Kurulum

```bash
# 1. Repo'yu klonla
git clone git@github.com:ahmetinci06/avt-hub-dev.git
cd avt-hub-dev

# 2. Develop branch'ine geç
git checkout develop

# 3. Bağımlılıkları yükle (Node.js)
npm install

# 4. Bağımlılıkları yükle (Python)
pip install -r requirements.txt

# 5. Ortam değişkenlerini ayarla
cp .env.example .env
# .env dosyasını düzenle

# 6. Geliştirme sunucusunu başlat
npm run dev
```

### Klasör Yapısı

```
avt-hub-dev/
├── src/
│   ├── dashboard/       # Web dashboard (React)
│   ├── telemetry/       # Telemetri servisleri
│   └── api/             # Backend API
├── docs/                # Dökümanlar
│   ├── GITHUB-GUIDE.md  # GitHub kullanım rehberi
│   └── architecture/    # Mimari dökümanlar
├── scripts/             # Yardımcı scriptler
├── tests/               # Test dosyaları
├── .env.example         # Ortam değişkeni şablonu
├── CONTRIBUTING.md      # Katkı rehberi
└── README.md
```

---

## 🔄 CI/CD Pipeline

Bu repo GitHub Actions kullanır:

```yaml
# Her PR'da otomatik çalışır:
✓ Lint kontrol (ESLint, Prettier)
✓ Unit testler
✓ Build testi

# develop → main merge'de:
✓ Full test suite
✓ Build artifact oluşturma
✓ Release tag
```

GitHub Actions workflow dosyaları `.github/workflows/` klasöründe.

---

## 📊 GitHub Projects Kullanım Rehberi

Tüm görev takibi **GitHub Projects** üzerinden yapılır.

### Project Board'a Erişim
1. Repo sayfasında **Projects** sekmesine tıkla
2. AVT Racing Board'u aç

### Kart Durumları
| Durum | Anlam |
|-------|-------|
| 📋 Backlog | Planlanmış ama başlanmamış |
| 🔄 In Progress | Şu an üzerinde çalışılıyor |
| 👀 In Review | PR açıldı, inceleniyor |
| ✅ Done | Tamamlandı |

### Yeni Görev Ekleme
1. **+ Add item** tıkla
2. Başlık yaz veya mevcut Issue'yu bağla
3. Assignee ve label ekle
4. Durumu belirle

### Issue ile PR Bağlama
PR açıklamasına yaz:
```
Closes #42
```
Issue otomatik kapanır ve Done'a taşınır.

---

## 🌿 Branch Yapısı

```
main          ← Stabil, yarışmaya hazır kod
  └── develop ← Aktif geliştirme
        ├── feature/telemetri-dashboard
        ├── feature/vcu-iletişim
        └── fix/sensor-kalibrasyon
```

**Kural:** Her yeni iş için `develop`'tan branch aç, PR ile geri merge et.

---

## 📚 Katkı Rehberi

- [CONTRIBUTING.md](CONTRIBUTING.md) — PR kuralları, commit formatı
- [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md) — Git/GitHub başlangıç rehberi

---

## 📞 İletişim

**Takım Kaptanı:** Ahmet Alperen İnci  
**GitHub:** [@ahmetinci06](https://github.com/ahmetinci06)

---

*🏎️ AVT Racing — TEKNOFEST 2026 | Bahçeşehir Üniversitesi*
