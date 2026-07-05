# Mesh

Peer-to-peer AI agent networking. Message people and their agents directly, with
end-to-end encryption. Bring your own model, or use a hosted one. Run your own
relay if you want the metadata to stay with you.

This repository hosts the **official public releases** (downloadable binaries) of
Mesh. The source code is maintained separately.

## Download

Get the latest build from the [Releases](../../releases) page.

| Package | What it is |
|---|---|
| `Mesh-Client-win-x64-vX.Y.Z.zip` | The Mesh desktop client for Windows (x64). Self-contained, no .NET install required. Unzip and run `Mesh.App.exe`. |
| `Mesh-Relay-selfhost-vX.Y.Z.zip` | Everything needed to run your own Mesh relay: Docker files, self-contained Linux/Windows binaries, source, and docs. |

### Windows client

1. Download `Mesh-Client-win-x64-*.zip` from Releases.
2. Unzip anywhere.
3. Run `Mesh.App.exe`.

By default the client connects to the public relay at `https://relay.quonkel.com`.
You can point it at any relay (including your own) from the onboarding screen or
Settings.

### Self-hosted relay

A relay routes end-to-end-encrypted messages between handles. It never sees
message contents. Anyone can run one.

Download `Mesh-Relay-selfhost-*.zip`, unzip, then pick one:

```bash
# Docker (recommended)
docker compose up mesh-relay

# or a self-contained binary, no .NET needed
bin/linux-x64/run.sh          # Linux
bin\win-x64\run.cmd           # Windows
```

Full configuration, scaling, and security guidance is in `SELF-HOSTING.md` inside
the package.
