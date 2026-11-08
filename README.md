# NFG — Nicomachos Food Graph Schema

Open vocabulary for restaurant, dish, ingredient, and food data. Provided by **NGraph Inc.**, powering [OMISEAI](https://omiseai.com/).

## Live

- Site: https://nfg.ngraph.jp/
- v0.3 context: https://nfg.ngraph.jp/schema/v0.3/context.jsonld
- v0.2 context: https://nfg.ngraph.jp/schema/v0.2/context.jsonld（引き続き配信）
- 日本語: https://nfg.ngraph.jp/ ／ English: https://nfg.ngraph.jp/en/

## Use

Embed in your HTML:

```html
<script type="application/ld+json" data-aeo="restaurant">
{
  "@context": [
    "https://schema.org",
    "https://nfg.ngraph.jp/schema/v0.3/context.jsonld"
  ],
  "@type": ["Restaurant", "nfg:SeafoodRestaurant"],
  "name": "Sakanaya (fictional)",
  "nfg:vadCertified": true,
  "nfg:vadSource": "owner_verified",
  "nfg:confidenceScore": 0.95
}
</script>
```

## Deploy

NGraph の Cloudflare の Worker `nfg-schema`（静的アセット・nfg.ngraph.jp）。2026-10-26 に LION の Pages から移行。**GitHub に push しても本番には出ない**（自動公開なし）。手順は shingo-brain `projects/github-brand-separation.md` の 2026-10-26 の節。

## Versioning

- **v0.3** — current (2026-10-26)：実サイトで使っていた KaisekiRestaurant・habitat・courseFlow・certificationTag を定義に追加。seasonStart/seasonEnd は実データに合わせ MM-DD（xsd:date 指定を外す）。vadSource の値は規格書 §7.7 の4つ（ai_inferred / owner_verified / official_published / third_party）
- **v0.2** — 2026-05-29（引き続き配信）
- Pre-1.0 phase: breaking changes increment minor.
- v1.0 will be cut after community stabilization.

## License

**NFG Core Schema and Metadata (Layer 1 & 2) — [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)** © NGraph Inc. The JSON-LD contexts under `/schema/` and the specification pages at https://nfg.ngraph.jp/ are the licensed material. Full text: [LICENSE](./LICENSE). Layer 3 Service Extensions are proprietary to NGraph Inc. The OMISEAI software is separate and not covered by this license.

Attribution example: `NFG (Nicomachos Food Graph) by NGraph Inc., https://nfg.ngraph.jp/ — CC BY 4.0`

NFG の公開部分（Layer 1 Core Schema・Layer 2 Metadata＝`/schema/` の JSON-LD context と規格ページ）は **CC BY 4.0**（クリエイティブ・コモンズ 表示 4.0 国際）です（© 株式会社NGraph）。全文は [LICENSE](./LICENSE)。Layer 3（Service Extensions）は NGraph 独自（proprietary）で、OMISEAI のソフトウェアもこのライセンスの対象外です。

出典表示の例：`NFG (Nicomachos Food Graph) by NGraph Inc., https://nfg.ngraph.jp/ — CC BY 4.0`（2026-11-08 確定）
