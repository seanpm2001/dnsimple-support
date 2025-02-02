---
title: CoreDNS
excerpt: Sync your zones managed at DNSimple to one or more CoreDNS instances.
categories:
- DNS
- Integrations
---

# CoreDNS

### Table of Contents {#toc}

* TOC
{:toc}

---

DNSimple supports the ability to sync managed zones to [CoreDNS](https://coredns.io/). The CoreDNS integrated provider is configured per zone and returns the current sync state for all zone records to the [Deployment Editor](/articles/deployment-editor#record-syncing).

## Video Walk-through

<div class="mb4 aspect-ratio aspect-ratio--16x9 z-0">
  <iframe src="https://www.youtube.com/embed/9yO2Oo_N1ms" class="aspect-ratio--object" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>
</div>

## Prerequisites

- CoreDNS binary compiled with the [coredns-dnsimple](https://github.com/dnsimple/coredns-dnsimple) plugin
  - [DNSimple CoreDNS Binary](https://github.com/dnsimple/coredns-dnsimple/releases)
  - [DNSimple CoreDNS Docker Container](https://hub.docker.com/r/dnsimple/coredns-dnsimple/tags)
- Administrator access to a DNSimple account

## Supported Features

- **Management of integrated zone records**: List, create, update, and delete integrated zone records from DNSimple using the [Deployment Editor](/articles/deployment-editor).
- **Sync integrated zone records**: Sync your zone records from DNSimple to multiple CoreDNS instances, and verify the sync state with the [Deployment Editor](/articles/deployment-editor#record-syncing).

The CoreDNS integrated provider supports one-way syncing of zone records configured at DNSimple. All records configured for the zone at DNSimple will be synced to CoreDNS on startup and again during each refresh interval. Zone records for any other integrated DNS provider must first be synced to DNSimple before they will be available to CoreDNS instances.

#### Supported Record Types

All DNSimple record types can be synced to CoreDNS:

- A
- AAAA
- ALIAS
- CNAME
- HINFO
- MX
- NS
- POOL
- PTR
- SOA
- SPF
- SRV
- SSHFP
- TXT
- URL
