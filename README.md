# secretserver-cli

Release binaries for `ss`, the [SecretServer.io](https://secretserver.io)
command-line client. This repository holds **release assets only**; the
source is developed privately in `afterdarksys/secretserver.io` and the
binaries are built and uploaded by GoReleaser.

## Install

```bash
# macOS / Linux: verifies the SHA-256 before installing
curl -fsSL https://secretserver.io/install | sh

# Homebrew
brew install afterdarksys/tap/secretserver-cli
```

Or download from [Releases](https://github.com/afterdarksys/secretserver-cli/releases):
archives for darwin, linux and windows (amd64, arm64), `.deb`/`.rpm`, and
`ss_<version>_checksums.txt`. Verify before use:

```bash
shasum -a 256 -c ss_<version>_checksums.txt --ignore-missing
```

### From source

Requires read access to the private source repository:

```bash
git clone https://github.com/afterdarksys/secretserver.io
cd secretserver.io && scripts/build-cli.sh   # -> ~/.local/bin/ss
```

## Get started

```bash
ss login          # sign in with your organization's SSO
ss secrets --help
```

Docs: https://secretserver.io/docs/install

## Reporting issues

Email support@afterdarksys.com. Do not open issues containing secrets.
