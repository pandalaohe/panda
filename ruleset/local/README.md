# ruleset/local architecture

This branch keeps public rule/config architecture only. Private node subscription links stay local in OpenClash or client subscription inputs.

## Direct
- `direct/Passthrough.list`: renamed from old `UnBan.list`; high-priority allowlist plus Cloudflare Tunnel, remote-control, DDNS, and home-domain real/direct rules.
- `direct/HomeServices.list`: LAN/private/home service direct rules.
- `direct/SteamDownload.list`: Steam content CDN direct rules.
- `direct/ChinaMedia.list`: Mainland media direct rules.
- `direct/TransportFix_ChinaApp_QUIC.list`: iPhone Weibo/Xiaohongshu UDP/443 reject rules migrated from old live fix.

## Proxy
- `proxy/Claude.list`: Claude/Anthropic only.
- `proxy/OpenAI.list`: OpenAI/ChatGPT/Sora only.
- `proxy/AI.list`: AI services excluding Claude and OpenAI.
- `proxy/VPN1.list`, `proxy/VPN2.list`, `proxy/Mail.list`, `proxy/MailPort.list`, `proxy/Xbox.list`: migrated legacy specialty lists.
- `proxy/ProxyLite.list`, `proxy/ProxyMedia.list`: migrated legacy lists with obvious AI/OpenAI/Claude duplicates removed.

## Reject
- `reject/AdBlock_Allow.list`: false-positive protection, referenced as direct before reject rules.
- `reject/AdBlock_High.list`: high-confidence local ad/tracking blocklist.
- `reject/AdBlock_Low.list`: low-confidence catch-all blocklist, referenced late.

## DNS
- `dns/FakeIP_Filter_Wide.list`: wide real-IP protection material for `fakeip.ini`.

## Backups
- `config/backups/20260504_proxy_fakeip/` stores source files copied from `origin/Self` before migration.

