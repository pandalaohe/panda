# ruleset/local architecture

This branch keeps public rule/config architecture only. Private node subscription links stay local in OpenClash or client subscription inputs.

## Direct
- `direct/Passthrough.list`: renamed from old `UnBan.list`; high-priority allowlist plus Cloudflare Tunnel, remote-control, DDNS, and home-domain real/direct rules.
- Private tracker domains are maintained inside `direct/Passthrough.list`; a separate PT runtime list is intentionally avoided.
- `direct/HomeServices.list`: LAN/private/home service direct rules.
- `direct/SteamDownload.list`: Steam content CDN direct rules.
- `direct/ChinaMedia.list`: Mainland media direct rules.
- `direct/TransportFix_ChinaApp_QUIC.list`: iPhone Weibo/Xiaohongshu UDP/443 reject rules migrated from old live fix.

## Proxy
- `proxy/Claude.list`: Claude/Anthropic only.
- `proxy/OpenAI.list`: OpenAI/ChatGPT/Sora only.
- `proxy/AI.list`: AI services excluding Claude and OpenAI.
- `proxy/VPN1.list`, `proxy/VPN2.list`, `proxy/Mail.list`, `proxy/Xbox.list`: migrated legacy specialty lists. Mail port rules are folded into `proxy/Mail.list`.
- `proxy/ProxyLite.list`, `proxy/ProxyMedia.list`: migrated legacy lists with obvious AI/OpenAI/Claude duplicates removed.

## Reject
- `reject/AdBlock_Allow.list`: false-positive protection, referenced as direct before reject rules.
- `reject/AdBlock_Core.list`: active high-confidence domain blocklist.
- `reject/AdBlock_High.list`: source-only curation material already merged into `AdBlock_Core.list`.
- `reject/AdBlock_Low.list`: broad keyword and low-confidence catch-all blocklist, referenced after business, AI, media, and generic proxy rules.

## DNS
- `dns/FakeIP_Filter_Wide.list`: supplementary wide real-IP protection material; generated strong-DIRECT bindings stay in `FakeIP_Direct_RealIP.list`.
- `dns/FakeIP_Direct_RealIP.list`: generated real-IP binding for every local ruleset that routes domains to DIRECT.
- `proxy/IntlMedia_Priority.list` and `proxy/AI.list` override broad real-IP filters with fake-IP and foreign DNS where required.

## Backups
- `config/backups/20260504_proxy_fakeip/` stores source files copied from `origin/Self` before migration.

