# Notes

## Scan Scope

Target subnet: `192.168.0.0/24`

## Most Exposed Host Identified

Host: `192.168.0.45`

Open ports observed:

- `22/tcp` — SSH
- `80/tcp` — HTTP / Apache
- `443/tcp` — HTTPS / Apache
- `8080/tcp` — Web service / HTTP proxy

## Security Observation

The host with the most open services may have a larger attack surface because each exposed service could require review, patching, configuration checks, and access control validation.

## Portfolio Wording Reminder

Use safe wording such as:

- Controlled lab environment
- Internal network enumeration
- Service discovery
- Attack surface analysis
- Authorized training scenario

Avoid wording that sounds like unauthorized activity.
