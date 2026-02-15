# Manus Test Analizi - Guncel Durum

Bu dokuman, `sessionId: Xvhe6BF2NjKyRBLpKRnEOQ` testinden cikan bulgularin **guncel durumunu** verir.
Amac: onceki sorunlarin hala acikmis gibi gorunmesini engellemek.

## Olculebilir Gozlemler

- Toplam event: `202`
- Tool event: `42`
- Tool dagilimi:
  - `browser:success = 19`
  - `search:success = 8`
  - `text_editor:success = 7`
  - `suggestion:success = 5`
  - `terminal:success = 2`
  - `browser:rollback = 1`

## Durum Tablosu (Issue -> Status)

| Konu | Onceki Durum | Guncel Durum | Not |
|---|---|---|---|
| Direkt belge linki gorunurlugu | Eksik | RESOLVED | `Direct Source Links` zorunlu ciktiya eklendi. |
| Claim status etiketi (`validated/uncertain`) | Eksik | RESOLVED | `SKILL.md` icine zorunlu kural olarak eklendi. |
| Birincil kaynak yokken kesin dil | Riskli | RESOLVED | Quality gate: primary yoksa `uncertain`. |
| State'te link listesi alani | Yok | RESOLVED | `direct_source_links` state schema'ya eklendi. |
| Sablonda direct links bolumu | Yok | RESOLVED | `output_templates.md` icine F bolumu eklendi. |
| Cift dilli calisma | Yok | RESOLVED | Agent TR+EN davranis kurallariyla guncellendi. |
| UTF-8/mojibake otomatik kontrol | Kismi | OPEN | Ayrica otomatik encode-check adimi script ile eklenebilir. |

## Uygulanan Guncellemeler

1. `skill/cumhuriyet-tarihi-arsivci-ajani/SKILL.md`
   - TR+EN bilingual mode
   - link-first ve claim-status disiplini
2. `skill/cumhuriyet-tarihi-arsivci-ajani/references/output_templates.md`
   - `Direct Source Links` sablonu
   - dil kurali (TR/EN/bilingual)
3. `skill/cumhuriyet-tarihi-arsivci-ajani/references/state_schema.json`
   - `direct_source_links` alani
4. `skill/cumhuriyet-tarihi-arsivci-ajani/agents/openai.yaml`
   - bilingual tanim ve prompt

## Sonraki Teknik Iterasyon (Acik Oge)

1. UTF-8 cikti denetimini otomatik script'e tasimak.
2. "Aylik TBMM gundemi" icin altin test seti eklemek (Kasim 1924, Aralik 1924 gibi).
