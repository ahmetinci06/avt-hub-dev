# 🏎️ AVT Racing — Ana Geliştirme Hub'ı

<div align="center">

**Alternatif Vasıta Teknolojileri — BAU**
**TEKNOFEST Efficiency Challenge 2026 — Elektromobil**

[![TEKNOFEST 2026](https://img.shields.io/badge/TEKNOFEST-2026-red)](https://teknofest.org)
[![MCU](https://img.shields.io/badge/MCU-STM32G491RE-blue)]()
[![Yerli ESC](https://img.shields.io/badge/ESC-Yerli%20%E2%9C%85-green)]()
[![Target](https://img.shields.io/badge/Hedef-%3C110%20Wh%2Fkm-orange)]()

</div>

---

## 📊 İlerleme & Çalışma Akışı

- [🏠 HOME.md](HOME.md) — **Ana Harita (Obsidian MOC)** — her şeye buradan ulaş
- [📅 TIMELINE.md](TIMELINE.md) — Zaman çizelgesi ve deadline'lar
- [🔄 WORKFLOW.md](WORKFLOW.md) — PR kuralları ve git akışı
- [📊 PROGRESS.md](PROGRESS.md) — Görev durumları
- [🐛 BUGS.md](BUGS.md) — Bug raporları
- [📖 CONTRIBUTING.md](CONTRIBUTING.md) — Katkı rehberi

> Her değişiklik PR ile yapılır. Review: @ahmetinci06 (Aİ) ☕ & Yaver (AI CTO) 🤖

---

## 🗺️ Proje Bilgi Tabanı (Obsidian Vault)

Bu repo aynı zamanda bir **Obsidian vault**'tur. Klonlayıp Obsidian'da açabilirsiniz — graph view'da tüm bağlantıları görün.

```
avt-hub-dev/
├── 📊 00-dashboard/         → Proje durumu, toplantı, blocker takibi
├── 🔌 01-elektronik/        → AKS board BOM, güç katı, batarya, CAN, sensörler
├── 💻 02-yazilim/            → 9 firmware modülü, CubeMX, test prosedürleri
├── 🏗️ 03-mekanik/           → Şasi, gövde, direksiyon, fren, süspansiyon
├── ⚙️ 04-simulasyon/        → FEA, CFD, enerji modeli, yarış stratejisi
├── 📋 05-yaris-hazirlik/     → Kurallar, güvenlik, dokümanlar, jüri, lojistik
├── 👥 06-takim/              → Ekip listesi, görev matrisi, iletişim
├── 💰 07-sponsorluk/         → Bütçe, potansiyel sponsorlar
├── 📝 _templates/            → Toplantı, görev, test raporu şablonları
├── 📄 HOME.md                → Ana harita (Map of Content)
└── 📅 TIMELINE.md            → Zaman çizelgesi
```

### Obsidian Nasıl Kullanılır?
1. Repoyu klonla: `git clone https://github.com/ahmetinci06/avt-hub-dev.git`
2. [Obsidian](https://obsidian.md) indir (ücretsiz)
3. "Open folder as vault" → `avt-hub-dev/` dizinini seç
4. Graph View aç (sol menü) → tüm bağlantıları gör 🗺️

---

## 🚀 Proje Durumu

### ✅ Tamamlanan
- Yerli ESC firmware (6-step BLDC, TIM1 complementary PWM)
- VCU state machine (OFF→READY→DRIVE→FAULT)
- CAN haberleşme (BMS + telemetri)
- Enerji izleme (Wh/km tracking)
- Telemetri (UART CSV 5Hz)
- AKS board şematik (KiCad)

### 🚧 Devam Eden
- PCB üretim + lehimleme
- Sensör testleri (7 test — Aybüke)
- CubeMX .ioc güncellemesi
- Şasi imalatı

### 📋 Sırada
- Motor + board entegrasyon testi
- Batarya paketi montajı
- Gövde üretimi
- Teknik Tasarım Raporu (7 Temmuz!)

---

## 📂 Tüm Repolar

| Repo | Açıklama | Durum |
|------|----------|-------|
| **[avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)** | 🏠 Ana hub + Obsidian vault | ✅ Aktif |
| **[AVT-VCU-DEV](https://github.com/ahmetinci06/AVT-VCU-DEV)** | 🚗 VCU + ESC firmware | ✅ Aktif |
| [avt-yazilim](https://github.com/ahmetinci06/avt-yazilim) | 💻 Yazılım ekibi | ✅ Sync |
| [avt-elektronik](https://github.com/ahmetinci06/avt-elektronik) | ⚡ Elektronik dosyalar | 📋 |
| [avt-cad](https://github.com/ahmetinci06/avt-cad) | 🖊️ CAD dosyaları | 📋 |
| [avt-simulation](https://github.com/ahmetinci06/avt-simulation) | ⚙️ Simülasyon | 📋 |
| [avt-docs](https://github.com/ahmetinci06/avt-docs) | 📄 Dökümanlar | 📋 |
| [avt-obsidian](https://github.com/ahmetinci06/avt-obsidian) | 📖 Obsidian vault (standalone) | ✅ |

---

## 👥 Ekip

| Ekip | Üyeler | Lead |
|------|--------|------|
| 🖊️ Teknik Çizim | Mahir, Yahya, Utku, Büşra | — |
| ⚙️ Malzeme & Sim | Arda, Emre, Serhad | — |
| ⚡ Elektronik | Onur, Deniz, Şeyma, Can, Ömer S., Emir | Onur |
| 💻 Yazılım | Aybüke, Ali Efe, Nisa, Ata, Ege | Aybüke |
| 📢 Sponsorluk | Ceren, Sezin, Yaprak, Gülce | — |

**Takım Lideri:** Ahmet Alperen İnci (Aİ) — @ahmetinci06

Detaylı roller: [06-takim/Ekip-Listesi.md](06-takim/Ekip-Listesi.md)

---

## 📅 Önemli Tarihler

| Tarih | Etkinlik |
|-------|---------|
| ~~21 Mar 2026~~ | ~~Gelişme Raporu~~ |
| **7 Tem 2026** | 📄 Teknik Tasarım Raporu |
| **24-31 Ağu 2026** | 🏁 Yarış Haftası |

---

## 🏁 Hedef

| Metrik | Hedef |
|--------|-------|
| Enerji verimliliği | < 110 Wh/km |
| Batarya | ≤ 3 kWh |
| Mesafe | 22.5 km / 29 dakika |
| Yerli ESC | ✅ AKS Board |

---

## 📜 Lisans

Apache License 2.0

<div align="center">

**AVT Racing Team** | BAU | [TEKNOFEST 2026](https://teknofest.org)
🏆 Hedef: < 110 Wh/km | ✅ Yerli ESC

</div>
