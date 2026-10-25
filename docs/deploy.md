# Deploy: wfc-natneg

Use example.env with the existing WFC database and shared WFC_TOKEN_KEY_FILE.
Never rotate token material or change profile IDs during ordinary service releases.
Dependencies: WFC_QR2_URL.

```sh
GOWORK=off go test -mod=vendor ./...
GOWORK=off go vet -mod=vendor ./...
docker build -t wfc-natneg .
```
