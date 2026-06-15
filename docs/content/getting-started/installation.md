---
title: "Installation"
description: "Install mogi from a release, with go install, or from source."
weight: 20
---

## Prebuilt binaries

Every [release](https://github.com/tamnd/mogi-cli/releases) carries archives for Linux, macOS,
and Windows on amd64 and arm64, plus deb, rpm, and apk packages for Linux.
Download, unpack, put `mogi` on your `PATH`, done. The `checksums.txt`
on each release is signed with keyless [cosign](https://docs.sigstore.dev/) if
you want to verify before running.

## With Go

```bash
go install github.com/tamnd/mogi-cli/cmd/mogi@latest
```

That puts `mogi` in `$(go env GOPATH)/bin`, which is `~/go/bin` unless
you moved it. Make sure that directory is on your `PATH`.

## From source

```bash
git clone https://github.com/tamnd/mogi-cli
cd mogi-cli
make build        # produces ./bin/mogi
./bin/mogi version
```

## Container image

```bash
docker run --rm ghcr.io/tamnd/mogi:latest --help
```

## Checking the install

```bash
mogi version
```

prints the version and exits.
