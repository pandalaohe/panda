# AdBlock sources

This branch internalizes ad blocking into active and source layers:

- `AdBlock_Allow.list`: false-positive protection.
- `AdBlock_Core.list`: active high-confidence domain blocking.
- `AdBlock_High.list`: source-only curation material already merged into Core.
- `AdBlock_Low.list`: broad keyword and low-confidence catch-all blocking placed at the end of the routing tree.

Reference sources used as material:

- `privacy-protection-tools/anti-AD`: strong mainland China ad-block material, MIT license.
- `Cats-Team/AdRules`: China-focused ad-block material.
- `ACL4SSR/ACL4SSR`: Clash `BanAD`, `BanProgramAD`, and common hijacking lists.
- `blackmatrix7/ios_rule_script`: `Hijacking` and `AdvertisingLite`.
- `easylist/easylist`: global web ad/privacy material.

The runtime config references conservative known Clash-classical third-party lists and keeps broader/format-sensitive sources as material for local curation.

