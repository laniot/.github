# LAN IoT

Secure, LAN-first IoT building blocks for industrial and lab equipment.

- **core** — ESP32-S3 WebSocket-over-TLS bridge for serial devices (RS-232/TTL).  
- **signer** — Local certificate signer API for device enrollment and short-lived certs.

---

## Value in one sentence
Browser → WSS → ESP32 → RS-232, with your own LAN CA. No cloud required.

## Why this exists
Most serial instruments live on isolated networks. This stack gives them a safe, modern, TLS endpoint that web apps can use on the LAN.

## Architecture
```
Browser (WSS)
     ⇅ TLS
ESP32 "core" ─── UART ─── Serial device
     ⇵ REST/TLS
   "signer" CA API
```

## Quick start

**Device side**
```bash
# Flash core (ESP-IDF). Configure Wi-Fi, UART pins, and cert bootstrap.
# Open https://device.local and connect via WSS from your app.
```

**Signer**
```bash
git clone https://github.com/laniot/signer && cd signer
npm ci && npm start
# POST /enroll to exchange a CSR for a device certificate
```

## Security model
- Private Root and Intermediate. LAN trust only.
- Short-lived leaf certs. Rotation by policy.
- Move keys to HSM/KMS for production.

## What you can build
- Browser dashboards for scales and moisture readers.  
- Factory HMIs that talk WSS directly to devices.  
- Air-gapped benches with auditable certificates.

## Repositories
- [`core`](https://github.com/laniot/core) — ESP32-S3 WSS bridge.
- [`signer`](https://github.com/laniot/signer) — Local CA and enrollment API.

## Roadmap
- v0.1 tagged releases and CI.
- Example: “RS232 moisture reader → browser.”
- Devcontainer for signer and docs site.

## Contributing
Issues and PRs are welcome. Look for `good first issue` and `help wanted`.

## License
Apache-2.0
