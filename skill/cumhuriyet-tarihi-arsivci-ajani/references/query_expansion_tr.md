# Query Expansion (TR + EN)

Use modern term + historical variant + abbreviation together.

## Term Variants

| Turkish modern term | Historical/legacy variant | English helper term |
|---|---|---|
| bakanlar kurulu | heyet-i vekile, icra vekilleri heyeti | council of ministers |
| cumhurbaskanligi | reisicumhurluk, riyaset-i cumhur | presidency |
| meclis tutanagi | zabit ceridesi, tutanak dergisi | parliamentary proceedings |
| resmi gazete | resmi ceride (early period context) | official gazette |
| genelge | tamim | circular |
| yasa/kanun | kanun layihasi, kanun teklifi | law bill, act |
| disisleri | hariciye | foreign affairs |
| milli savunma | mudafaa-i milliye | national defense |

## Person Variant Rule

1. For pre-surname period, query name + title + office combinations.
2. Add abbreviation and spelling variants (example: M. Kemal, Mustafa Kemal).
3. Allow transliteration variants.

## Institution Variant Rule

1. List historical institution name changes.
2. Query both abbreviation and full name (example: TBMM + Turkiye Buyuk Millet Meclisi).
3. Add sub-entities and commission names.

## Date Window Rule

1. Search at least `-7/+30` day window around key events.
2. For legislation/appointments, check previous and next issues/sessions.
3. Use normalized dates: `YYYY-MM-DD`, or `YYYY` if day/month unknown.

## Bilingual Query Rule

1. For Turkish questions, keep TR terms primary and add EN helper terms only when needed.
2. For English questions, keep EN terms primary and always add Ottoman/Turkish historical variants.
