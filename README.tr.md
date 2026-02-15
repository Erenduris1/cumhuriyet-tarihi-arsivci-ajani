# Cumhuriyet Tarihi Arsivci Ajani

Manus icin gelistirilmis, kanit-oncelikli Cumhuriyet Tarihi arastirma becerisi.

Dil destegi: Turkce + English (cift dilli calisma).

EN README: `README.md`

## Projenin Amaci

- Soruyu uygun arsiv omurgasina route eder (TBMM, Resmi Gazete, Devlet Arsivleri vb.)
- Her bulgu icin kaynak metadatasiyla Evidence Card uretir
- Kritik iddialarda capraz dogrulama (triangulation) zorunlu tutar
- Celiskileri Contradiction Ticket ile yonetir
- Kaynakli kisa sentez ve mini kronoloji verir
- Kritik iddialar icin dogrudan belge linki zorunlulugu uygular

## Cift Dilli Davranis

- Soru Turkceyse varsayilan cikti Turkce.
- Soru English ise varsayilan cikti English.
- Kullanici iki dil isterse TR + EN birlikte cikti verilir.
- JSON sema anahtarlari her zaman English kalir.

## Oncelikli Kaynak Omurgasi

- Cumhurbaskanligi Devlet Arsivleri
- Turkiye Buyuk Millet Meclisi (TBMM)
- Resmi Gazete
- Turk Tarih Kurumu (TTK)
- Ataturk Arastirma Merkezi
- Milli Kutuphane
- Ataturk Kitapligi
- SALT Research
- Dis politika: NARA, TNA (UK), NATO Archives, UN Archives

## Klasor Yapisi

```text
cumhuriyet-tarihi-arsivci-skill-project/
├─ README.md
├─ README.tr.md
├─ LICENSE
├─ docs/
│  ├─ RELEASE_NOTES_EN.md
│  └─ RELEASE_NOTES_TR.md
├─ claude/
│  └─ CLAUDE_PROJECT_INSTRUCTIONS.md
├─ skill/
│  └─ cumhuriyet-tarihi-arsivci-ajani/
│     ├─ SKILL.md
│     ├─ agents/openai.yaml
│     └─ references/
└─ dist/
   ├─ *.zip
   └─ *.skill
```

## Manus Kurulum

1. Manus -> Skill yukle ekranini ac.
2. `dist/` altindan `.skill` veya `.zip` dosyasi yukle.
3. Skill adinin `cumhuriyet-tarihi-arsivci-ajani` olarak gorundugunu kontrol et.

## Kaynaktan Paket Uretme

```powershell
$skillPath = ".\skill\cumhuriyet-tarihi-arsivci-ajani"
Compress-Archive -Path "$skillPath\*" -DestinationPath ".\dist\cumhuriyet-tarihi-arsivci-ajani.zip" -Force
Copy-Item ".\dist\cumhuriyet-tarihi-arsivci-ajani.zip" ".\dist\cumhuriyet-tarihi-arsivci-ajani.skill" -Force
```

## Claude Kullanimi

`claude/CLAUDE_PROJECT_INSTRUCTIONS.md` metnini Claude Project Instructions alanina yapistir.

## Ornek Test Sorusu

```text
1924 Kasiminda TBMM'de hangi konular konusuldu?
```

## Release Metinleri

- English release note: `docs/RELEASE_NOTES_EN.md`
- Turkce release note: `docs/RELEASE_NOTES_TR.md`

## Lisans

MIT (`LICENSE`).
