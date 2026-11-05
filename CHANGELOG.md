# Changelog

## v0.2.0 - 2026-11-05

- WFC_PROXY_LISTEN: the UDP socket also takes PROXY v2 framed datagrams from wfc-front and sends to those players through it, so NAT negotiation exchanges players' real public addresses and ports (prds#149). Vendors wfc-common v0.9.0.

## v0.1.2 - 2026-11-03

- Internal `/internal/` polls are counted and summarised once a minute instead of logged per call (wfc-common v0.3.1).

## v0.1.1 - 2026-11-03

- Every natneg message now logs one line to stderr, `natneg cmd <name> -> <result> <ms>ms` (verb and result only, never payload values). Internal HTTP logs as above through wfc-common v0.3.0 `httplog`.

