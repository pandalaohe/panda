# AdBlock sources

This branch internalizes ad blocking into three local layers:

- `AdBlock_Allow.list`: false-positive protection.
- `AdBlock_High.list`: high-confidence blocking.
- `AdBlock_Low.list`: low-confidence catch-all blocking.

Reference sources used as material:

- `privacy-protection-tools/anti-AD`: strong mainland China ad-block material, MIT license.
- `Cats-Team/AdRules`: China-focused ad-block material.
- `ACL4SSR/ACL4SSR`: Clash `BanAD`, `BanProgramAD`, and common hijacking lists.
- `blackmatrix7/ios_rule_script`: `Hijacking` and `AdvertisingLite`.
- `easylist/easylist`: global web ad/privacy material.

The runtime config references conservative known Clash-classical third-party lists and keeps broader/format-sensitive sources as material for local curation.

