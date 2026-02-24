# kami-jwt-decode

[![KAMI Plugin](https://img.shields.io/badge/KAMI-plugin-8A2BE2)](https://github.com/Hypijump31/KAMI)
[![Signed](https://img.shields.io/badge/Ed25519-signed-green)](https://github.com/Hypijump31/kami-registry)

Decode a JWT token and inspect its header, payload, and claims (read-only, no signature verification).

## Install

```bash
kami install Hypijump31/kami-jwt-decode@v0.1.0
```

## Usage

```bash
kami exec dev.kami.jwt-decode '{"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c"}'
```

## Arguments

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `token` | string | yes | JWT token string (`eyJ...`) |

## Output

Returns the decoded header, payload, and individual claims.

> **Note**: This plugin only **decodes** JWT tokens. It does not verify signatures.

## Build from source

```bash
git clone https://github.com/Hypijump31/kami-jwt-decode
cd kami-jwt-decode
cargo build --target wasm32-wasip2 --release
```

## Security

- Filesystem: none
- Network: none
- Max memory: 16 MB
- Max execution: 1000 ms

## License

MIT
