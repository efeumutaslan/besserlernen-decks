# BesserLernen Decks

[BesserLernen](https://github.com/efeumutaslan/besser-learner) uygulamasinin Deste Marketi icerikleri. Kullanicilar bu repodaki hazir desteleri uygulama icerisinden tek tikla indirebilir.

## Mevcut Desteler

| Deste | Kategori | Kart Sayisi | Aciklama |
|-------|----------|-------------|----------|
| Goethe A1 - Temel Kelimeler | Goethe A1 | 50 | Selamlasma, sayilar, renkler ve gunluk yasam |
| Goethe A1 - Yiyecek & Icecek | Goethe A1 | 40 | Restoran, market ve mutfak kelimeleri |
| Goethe A2 - Onemli Fiiller | Goethe A2 | 40 | A2 fiilleri ve ornek cumleleri |
| Gunluk Konusma Kaliplari | Gunluk Konusma | 30 | Almanya'da gunluk hayat ifadeleri |
| Artikel Kurallari & Istisnalar | Gramer | 35 | Der/die/das kurallari ve istisnalar |

## Yapi

```
besserlernen-decks/
├── index.json          # Kategori ve deste katalogu
└── decks/
    ├── goethe-a1-temel.json
    ├── goethe-a1-yiyecek.json
    ├── goethe-a2-fiiller.json
    ├── gunluk-konusma.json
    └── artikel-ozel.json
```

## Deste Formati

Her deste JSON dosyasi asagidaki yapidadir:

```json
{
  "name": "Deste Adi",
  "description": "Deste aciklamasi",
  "cards": [
    {
      "word": "Almanca kelime",
      "wordTranslation": "Turkce anlami",
      "artikel": "der/die/das",
      "exampleSentence": "Ornek cumle",
      "exampleTranslation": "Cumle cevirisi",
      "note": "Ek not (fiil cekimi vb.)",
      "nominativ": "Nominativ hali",
      "akkusativ": "Akkusativ hali",
      "dativ": "Dativ hali"
    }
  ]
}
```

### Alan Aciklamalari

| Alan | Zorunlu | Aciklama |
|------|---------|----------|
| `word` | Evet | Almanca kelime |
| `wordTranslation` | Evet | Turkce anlami |
| `artikel` | Hayir | der, die, das veya - (fiiller icin) |
| `exampleSentence` | Hayir | Almanca ornek cumle |
| `exampleTranslation` | Hayir | Ornek cumlenin Turkce cevirisi |
| `note` | Hayir | Ek not (fiil cekimi, kullanim notu vb.) |
| `nominativ` | Hayir | Nominativ hali (gramer drill icin) |
| `akkusativ` | Hayir | Akkusativ hali |
| `dativ` | Hayir | Dativ hali |

## Yeni Deste Ekleme

1. `decks/` klasorune yeni bir JSON dosyasi olustur
2. Yukaridaki formata uygun kartlari ekle
3. `index.json` dosyasina deste bilgilerini ekle
4. Pull Request gonder

### index.json'a Ekleme Ornegi

```json
{
  "id": "deste-id",
  "name": "Deste Adi",
  "description": "Kisa aciklama",
  "category": "goethe-a1",
  "cardCount": 50,
  "author": "Yazar Adi",
  "file": "decks/deste-id.json",
  "tags": ["A1", "temel"]
}
```

### Mevcut Kategoriler

| ID | Ad |
|----|-----|
| `goethe-a1` | Goethe A1 |
| `goethe-a2` | Goethe A2 |
| `kelime` | Genel Kelime |
| `gramer` | Gramer |
| `gunluk` | Gunluk Konusma |

## Iliskili Repolar

| Repo | Aciklama |
|------|----------|
| [besser-learner](https://github.com/efeumutaslan/besser-learner) | Ana uygulama |
| [besserlernen-decks](https://github.com/efeumutaslan/besserlernen-decks) | Deste Marketi (bu repo) |
| [besser-learner-storage](https://github.com/efeumutaslan/besser-learner-storage) | Resim depolama |
