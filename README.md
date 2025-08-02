# 🎮 LanuxDavet Plugin

> **Lanux Yazılım Hizmetleri** tarafından geliştirilmiş gelişmiş Minecraft davet sistemi plugin'i

[![Minecraft](https://img.shields.io/badge/Minecraft-1.16%2B-brightgreen.svg)](https://www.minecraft.net/)
[![Spigot](https://img.shields.io/badge/Spigot-API-blue.svg)](https://www.spigotmc.org/)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange.svg)](https://github.com/lanux/davetplugin/releases)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📥 İndirme Linkleri

### 🔥 Son Sürüm
- **GitHub Releases:** [LanuxDavet v1.0.0](https://github.com/nylithra/lanuxdavetplugin/releases/latest)
- **SpigotMC:** [SpigotMC Sayfası](https://www.spigotmc.org/resources/lanuxdavet.123456/)
- **Direct Download:** [JAR Dosyası](https://github.com/nylithra/lanuxdavetplugin/LanuxDavet-1.0.0.jar)

### 📋 Gereksinimler
- **Minecraft:** 1.16x - 1.20x
- **Sunucu:** Spigot, Paper, Bukkit
- **Java:** 8 veya üzeri
- **PlaceholderAPI:** (Opsiyonel) Placeholder desteği için

## ✨ Özellikler

### 🎯 Ana Özellikler
- ✅ **Çift Davet Sistemi** - Eski ve yeni sistem birlikte çalışır
- ✅ **Süreli Kodlar** - Tarih bazlı kod geçerliliği
- ✅ **Tek Kullanımlık** - Her oyuncu kod sadece 1 kez kullanabilir
- ✅ **Otomatik Ödül** - 100 altın otomatik verilir
- ✅ **IP Kontrolü** - Aynı IP'den gelen oyuncular engellenir
- ✅ **Placeholder Desteği** - `%davetplugin_bitis%` placeholder'ı
- ✅ **Gelişmiş Yardım** - `/ld-help` komutu ile detaylı yardım

### 🔄 Eski Sistem (Davet Kodu)
- `/davetet` - Davet kodu oluşturur
- `/davetkod <kod>` - Davet kodunu kullanır
- Her kod sadece 1 kez kullanılabilir (kod silinmez)
- Aynı IP'den gelen oyuncular kod kullanamaz
- Kod kullanan ve davet eden oyuncuya 100 altın verilir

### 🆕 Yeni Sistem (Süreli Davet Kodu)
- `/ldavetkur <başlangıç_tarihi> <bitiş_tarihi>` - Süreli davet kodu oluşturur
- Tarih formatı: `dd.MM.yyyy` (örn: 01.01.2025)
- Kodlar sadece yeni oyuncular tarafından 1 kez kullanılabilir
- Süresi dolan kodlar otomatik olarak geçersiz olur
- Kod kullanan oyuncuya 100 altın verilir

### 📊 Placeholder Desteği
- `%davetplugin_bitis%` - En yakın bitiş tarihini gösterir
- PlaceholderAPI gereklidir

## 🎮 Komutlar

| Komut | Açıklama | Kullanım | İzin |
|-------|----------|----------|------|
| `/davetet` | Davet kodu oluşturur | `/davetet` | `davetplugin.davetet` |
| `/davetkod` | Davet kodunu kullanır | `/davetkod <kod>` | `davetplugin.davetkod` |
| `/ldavetkur` | Süreli davet kodu oluşturur | `/ldavetkur <başlangıç> <bitiş>` | `davetplugin.ldavetkur` |
| `/ld-help` | Yardım menüsünü gösterir | `/ld-help` | `davetplugin.ldhelp` |

## 🔐 İzinler

| İzin | Açıklama | Varsayılan |
|------|----------|------------|
| `davetplugin.davetet` | Davet kodu oluşturma | `true` |
| `davetplugin.davetkod` | Davet kodunu kullanma | `true` |
| `davetplugin.ldavetkur` | Süreli davet kodu oluşturma | `op` |
| `davetplugin.ldhelp` | Yardım menüsü görüntüleme | `true` |

## 🚀 Kurulum

### 1. Plugin İndirme
```bash
# GitHub'dan indir
wget https://github.com/nylithra/lanuxdavetplugin/releases/LanuxDavet-1.0.0.jar

# veya manuel olarak indirin
```

### 2. Sunucuya Yükleme
1. İndirilen JAR dosyasını `plugins` klasörüne kopyalayın
2. Sunucuyu yeniden başlatın
3. Plugin otomatik olarak yüklenecektir

### 3. PlaceholderAPI (Opsiyonel)
```bash
# PlaceholderAPI'yi de yükleyin (placeholder desteği için)
# https://www.spigotmc.org/resources/placeholderapi.6245/
```

## 📁 Dosya Yapısı

```
plugins/
├── LanuxDavet/
│   ├── davet_data.yml          # Davet verileri
│   └── config.yml              # Plugin ayarları
└── LanuxDavet-1.0.0.jar       # Plugin dosyası
```

## 🔧 Konfigürasyon

### davet_data.yml
```yaml
# Davet kodları
davet_kodlari:
  ABC12345: "OyuncuAdi"
  
# Süreli davet kodları
davet_kur_kodlari:
  XYZ789: "AdminAdi"
  
# Bitiş tarihleri
davet_kur_tarihleri:
  XYZ789: "31.12.2024"
  
# Kod kullanan oyuncular
kod_kullanan_oyuncular:
  "OyuncuAdi:ABC12345": true
```

## 💡 Kullanım Örnekleri

### Süreli Kod Oluşturma
```
/ldavetkur 01.01.2024 31.12.2024
```
**Çıktı:** `Yeni davet kodu oluşturuldu: ABC12345`

### Kod Kullanma
```
/davetkod ABC12345
```
**Çıktı:** `Davet kodunu başarıyla kullandınız! 100 altın kazandınız!`

### Yardım Menüsü
```
/ld-help
```
**Çıktı:** Detaylı yardım menüsü


### Bağımlılıklar
- **Spigot API:** 1.20.4-R0.1-SNAPSHOT
- **PlaceholderAPI:** 2.11.3 (opsiyonel)

## 📞 Destek

### 🆘 Yardım
- **Discord:** [Lanux Discord](https://discord.gg/lanux)
- **Email:** nylithra@gmail.com
- **Website:** [https://lanux.xyz](https://lanux.xyz)


## 📄 Lisans

Bu proje **MIT Lisansı** altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## 👨‍💻 Geliştirici

**Lanux Yazılım Hizmetleri**

- 🌐 **Website:** [https://lanux.xyz](https://lanux.xyz)
- 📧 **Email:** info@lanux.xyz
- 💬 **Discord:** [Lanux Discord](https://discord.gg/lanux)
- 📱 **Telegram:** [@lanux](https://t.me/lanux)

---

<div align="center">

**⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın! ⭐**

[![GitHub stars](https://img.shields.io/github/stars/lanux/davetplugin.svg?style=social&label=Star)](https://github.com/lanux/davetplugin)
[![GitHub forks](https://img.shields.io/github/forks/lanux/davetplugin.svg?style=social&label=Fork)](https://github.com/lanux/davetplugin/fork)

</div> 