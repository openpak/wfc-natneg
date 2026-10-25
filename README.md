# Wii/DS NAT Negotiation Server

OpenPak's Wii/DS NAT Negotiation Server.

| | |
| --- | --- |
| Network | Wii, DS |
| Role | NAT negotiation UDP sessions; QR2 receives negotiation results |
| Depends on | [`wfc-qr2`](https://github.com/openpak/wfc-qr2) (`WFC_QR2_URL`) |
| Image | `ghcr.io/openpak/wfc-natneg` |
| Based on | WiiLink WFC (AGPL-3.0) |
| Licence | AGPL-3.0-only |

## What it serves

| Endpoint | What |
| --- | --- |
| UDP 27901 | NAT negotiation sessions |
| HTTP `:20204`, `GET /healthz` | Health check, unauthenticated |
| HTTP `:20204`, protocol and internal paths | Require `WFC_INTERNAL_KEY`; console HTTP reaches this service through wfc-nas |
| QR2 (`WFC_QR2_URL`) | Receives negotiation results |

## Run

```sh
cp example.env .env   # fill in the existing WFC values
```

The service runs as the `openpak-wfc-natneg` container from
`deploy/openpak-wfc-natneg.container`.

## Build

```sh
docker build -t wfc-natneg .
```

## Docs

- [Protocol](docs/protocol.md)
- [Evidence](docs/evidence.md)
- [Deploy](docs/deploy.md)
- [Notes](docs/notes.md)

## Licence

AGPL-3.0-only. See [LICENSE](LICENSE).
