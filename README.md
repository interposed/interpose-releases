# interpose-releases

Pre-built binaries of [`interpose`](https://github.com/interposehq/interpose-kernel#related-repos) — the per-host daemon that gates AI agent actions behind hardware-backed human approvals (passkey, YubiKey, phone-via-QR).

This repo holds **binary tarballs only**. Source lives in a separate (currently private) repo.

## Install

One-liner, picks the right binary for your OS and arch:

```bash
curl -fsSL https://github.com/interposehq/interpose-releases/releases/latest/download/install.sh | sh
```

Pin to a specific version:

```bash
curl -fsSL https://github.com/interposehq/interpose-releases/releases/download/v0.9.0/install.sh | sh -s -- --version v0.9.0
```

Install to a custom prefix (default `/usr/local/bin`):

```bash
curl -fsSL https://github.com/interposehq/interpose-releases/releases/latest/download/install.sh | sh -s -- --prefix ~/.local/bin
```

Verify the install:

```bash
interpose --version
interpose doctor      # host preflight (Linux: KVM/BPF caps; macOS: noop)
```

## Supported platforms

| OS | Arch | Status |
|---|---|---|
| Linux  | amd64 (x86_64)  | ✅ |
| Linux  | arm64 (aarch64) | ✅ |
| macOS  | arm64 (Apple Silicon) | ✅ broker only — Linux enforcer is the platform with full functionality; macOS-native enforcer (Endpoint Security) is queued at Apple for entitlement approval |
| Windows | — | not yet |
| Linux  | armv7 / 32-bit  | not yet |

## What you actually do with this

The shortest useful thing: gate Claude Code (or any agent that execs commands) with your passkey, on a Linux box.

```bash
# install
curl -fsSL https://github.com/interposehq/interpose-releases/releases/latest/download/install.sh | sh

# one-time passkey registration
interpose register

# start the daemon with the claude-code trust profile preloaded
sudo interpose serve --profile=claude-code --auth-addr=localhost:7422

# in another terminal, use claude as normal — dangerous execs prompt your passkey
claude
```

Full walkthrough including troubleshooting + the exact list of what gets prompted vs. trusted:
**[quickstart-claude-code](https://github.com/interposehq/interpose-kernel/blob/main/docs/where-this-fits.md)** ← (mirrored here once the main interpose repo is public)

For the architecture rationale — why kernel-level enforcement rather than a hook system, and how the cooperative AAuth path layers on top — see the [interpose-kernel "where this fits"](https://github.com/interposehq/interpose-kernel/blob/main/docs/where-this-fits.md) doc, which describes the broader stack.

## What's in each release

Each tagged release contains:

- `interpose-vX.Y.Z-linux-amd64.tar.gz`   — Linux x86_64 binary + LICENSE + README
- `interpose-vX.Y.Z-linux-arm64.tar.gz`   — Linux arm64 binary + LICENSE + README
- `interpose-vX.Y.Z-darwin-arm64.tar.gz`  — macOS arm64 binary + LICENSE + README
- `checksums.sha256`                      — SHA-256 of all tarballs (the install script verifies)
- `install.sh`                            — the OS/arch-detecting installer

## License

See [`LICENSE.md`](LICENSE.md). interpose is **proprietary software** distributed under a custom license: **free for personal and non-commercial use; commercial deployment requires a separate license** (`contact@stateful.art`).

The binaries in this repo are the official builds. Don't trust binaries from anywhere else.

## Reporting vulnerabilities

Security issues: please report privately first — see [`SECURITY.md`](SECURITY.md).

## Related repos

| Repo | What |
|---|---|
| [`interpose-kernel`](https://github.com/interposehq/interpose-kernel) | Linux kernel images (Ubuntu + Debian) with BPF-LSM enabled, for microVM sandbox runtimes. Public. |
| [`interpose-sandbox`](https://github.com/interposehq/interpose-sandbox) | Firecracker microVM wrapper using interpose-kernel — for hard-isolation agent sandboxing on Linux. Public. |
| `interpose-sdk-go` | Go client SDK for cooperative-mode agents that want to call interpose's broker directly. Currently private; will open to integration partners. |
