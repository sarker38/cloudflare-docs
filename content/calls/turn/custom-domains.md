---
pcx_content_type: get-started
title: Custom TURN domains
weight: 15
---

#  Custom TURN domains

Cloudflare Calls TURN service supports using custom domains for UDP, and TCP - but not TLS protocols. Custom domains do not affect any of the performance of Cloudflare Calls TURN and is set up via a simple CNAME DNS record on your domain.

| Protocol      | Custom domains | Primary port | Alternate port |
| ------------- | -------------- | ------------ | -------------- |
| STUN over UDP | ✅             | 3478/udp     | 53/udp         |
| TURN over UDP | ✅             | 3478/udp     | 53 udp         |
| TURN over TCP | ✅             | 3478/tcp     | 80/tcp         |
| TURN over TLS | No             | 5349/tcp     | 443/tcp        |

## Setting up a CNAME record

To use custom domains for TURN, you must create a CNAME DNS record pointing to `turn.cloudflare.com`. 

{{<Aside type="warning">}}

Do not resolve the address of `turn.cloudflare.com` or `stun.cloudflare.com` or use an IP address as the value you input to your DNS record. Only CNAME records are supported.

{{</Aside>}}

Any DNS provider, including Cloudflare DNS can be used to set up a CNAME for custom domains. 

{{<Aside>}}

If Cloudflare's authoritative DNS service is used, the record must be set to [DNS-only or "grey cloud" mode](/dns/manage-dns-records/reference/proxied-dns-records/#dns-only-records).`

{{</Aside>}}

There is no additional charge to using a custom hostname with Cloudflare Calls TURN.