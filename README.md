# gh-actup

GitHub CLI extension wrapper for [`actup`](https://github.com/lynicis/actup) — a version
manager for GitHub Actions.

```sh
gh extension install lynicis/gh-actup
gh actup --help
```

This repository holds no source. Each release mirrors the prebuilt
`gh-actup-<os>-<arch>` binaries published by
[lynicis/actup releases](https://github.com/lynicis/actup/releases), because `gh`
refuses to install extensions whose repository name does not start with `gh-`.

```sh
gh extension upgrade actup   # or: gh extension install lynicis/gh-actup --force
```

Homebrew, Scoop, `go install`, `.deb`/`.rpm`, and Docker packages live in the main
repository: <https://github.com/lynicis/actup#installation>.

## Supported platforms

Binary assets exist for `darwin`/`linux` (`amd64`, `arm64`, `386`, `armv6`,
`armv7`, `ppc64le`, `riscv64`, `s390x`) and `windows/amd64`. `gh` resolves assets
by suffix `<goos>-<goarch>`, so 32-bit Linux ARM (`gh-actup-linux-armv6`/`armv7`)
is not reachable through `gh extension install`; install those from the main
repository instead.
