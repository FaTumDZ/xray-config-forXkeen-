Configuration file for Xkeen, including routing setup for major websites.

# xray-config-forXkeen

Configuration file for Xkeen, including routing setup for major websites.

### Routing Overview
The configuration file specifies routing for main sites using the following entries:

```
"ext:geosite_v2fly.dat:google-gemini",
"ext:geosite_zkeen.dat:domains",
"ext:geosite_zkeen.dat:other"
```

### Direct Connection for YouTube
A direct (bypass) connection is configured for YouTube and related domains, bypassing routing, using the following rule:

```json
{
  "inboundTag": ["redirect", "tproxy"],
  "outboundTag": "direct",
  "type": "field",
  "domain": [
    "youtube.com",
    "youtube-nocookie.com",
    "youtube.googleapis.com",
    "ytimg.com",
    "googlevideo.com"
  ]
}
```

---

This file provides the main routing configuration for Xkeen, where certain sites are routed through specified external configuration files, while YouTube traffic is routed directly.
