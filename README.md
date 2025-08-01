# LanuxDavet Plugin

Bu Minecraft plugin'i, oyuncuların birbirlerini davet etmesi için bir sistem sağlar.
**Lanux Yazılım Hizmetleri** tarafından geliştirilmiştir.

## Özellikler

- `/davetet` komutu ile özel davet kodu oluşturma
- `/davetkod <kod>` komutu ile davet kodunu kullanma
- Davet kodu kullanıldığında her iki oyuncuya da 100 altın verme
- Aynı IP adresinden gelen oyuncuların davet kodunu kullanamaması
- Verilerin yerel olarak saklanması

## Kurulum

1. Plugin'i sunucunuzun `plugins` klasörüne kopyalayın
2. Sunucuyu yeniden başlatın
3. Plugin otomatik olarak yüklenecektir

## Komutlar

### `/davetet`
- Oyuncuya özel bir davet kodu verir
- Kod 8 karakter uzunluğunda ve rastgele oluşturulur
- Kod yerel olarak saklanır

### `/davetkod <kod>`
- Verilen davet kodunu kullanır
- Başarılı kullanımda her iki oyuncuya da 100 altın verilir
- Aynı IP adresinden gelen oyuncular kullanamaz
- Kod kullanıldıktan sonra silinir

## İzinler

- `davetplugin.davetet` - Davet kodu oluşturma izni
- `davetplugin.davetkod` - Davet kodunu kullanma izni

## Veri Saklama

Plugin verileri `plugins/LanuxDavet/davet_data.yml` dosyasında saklanır:
- Davet kodları
- Oyuncu IP adresleri

## Sürüm: 1.16x - 1.20x