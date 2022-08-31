# Building ICU Shards

The ICU is divided by locales and features. <br/>

By locale:
- EFIGS (en, fr, it, de, es)
- CJK (zh, ja, ko)
- no CJK (all locales except for zh, ja, ko)

By features:
- Collation
- Normalization
- Currency
- Locales
- Zones

To generate ICU shards run:

`make -C ./eng -f icu.mk shards`

which will create `json` files in `icu-filters` and build the project with all shards from `icu-filters/`. Output files will be located in `artifacts/bin/icu-{platform}-{architecture}`.
