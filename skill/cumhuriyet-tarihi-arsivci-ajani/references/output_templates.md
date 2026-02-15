# Output Templates

Asagidaki sirayi degistirme.
Dil kurali:
- Varsayilan: kullanicinin dili (TR veya EN).
- Kullanici iki dil isterse ayni ciktiyi TR ve EN olarak ver.
- JSON alan adlari her zaman English kalir.

## A) Scope Brief (Markdown)

```markdown
## Scope Brief
- Konu: <1 cumle>
- Tarih Araligi: <YYYY-MM-DD - YYYY-MM-DD veya YYYY>
- Cografya: <ulke/bolge/sehir>
- Aktorler: <kisi/kurum listesi>
- Hedef Cikti: <short_summary|bibliography|timeline|mixed>
```

## B) Query Matrix (Markdown tablo)

```markdown
## Query Matrix
| Route | Keywords | Person Variants | Institution Variants | Critical Dates |
|---|---|---|---|---|
| <route> | <k1; k2; ...> | <p1; p2> | <i1; i2> | <d1; d2> |
```

## C) Evidence Cards (JSON list)

```json
[
  {
    "doc_id": "DOC-001",
    "title": "",
    "date": "YYYY-MM-DD or YYYY",
    "source_type": "archive|parliament|official_gazette|press|library|international|secondary",
    "repository": "",
    "reference_code": "",
    "pages_or_section": "",
    "access_url_or_location": "",
    "access_status": "open|login_required|unavailable",
    "captured_at": "ISO-8601",
    "language": "tr|en|...",
    "keywords": [],
    "excerpt_short": "",
    "claim_supported": "",
    "reliability_notes": "",
    "confidence": "low|medium|high",
    "next_leads": []
  }
]
```

## D) Synthesis (Markdown)

```markdown
## Synthesis
<10-15 satirlik kaynakli ozet. Her kritik cumle/paragraf sonunda [DOC-xxx] atfi kullan.>
<Her ana bulguda durum etiketi belirt: validated veya uncertain.>

## Mini Kronoloji
- YYYY-MM-DD: <olay> [DOC-xxx]
- YYYY-MM-DD: <olay> [DOC-yyy]

## Sonraki Aramalar
1. <fon/seri/anahtar kelime>
2. <fon/seri/anahtar kelime>
```

## E) Archive Log (madde listesi)

```markdown
## Archive Log
- searched: <kaynak + sorgu>, got: <adet/none>, note: <kisa not>
- searched: <kaynak + sorgu>, got: <adet/none>, note: <kisa not>
```

## F) Direct Source Links (madde listesi)

```markdown
## Direct Source Links
- [DOC-001] <dogrudan belge URL'si> - <kisa not>
- [DOC-002] <dogrudan belge URL'si> - <kisa not>
```

## Contradiction Ticket (gerektiginde)

```json
{
  "topic": "",
  "conflict": "",
  "sources": ["DOC-001", "DOC-002"],
  "hypotheses": [],
  "resolution_plan": [],
  "status": "resolved|unresolved"
}
```
