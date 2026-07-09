# scoop-bucket

[![Tests](https://github.com/yeroo/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/yeroo/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/yeroo/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/yeroo/scoop-bucket/actions/workflows/excavator.yml)

[Scoop](https://scoop.sh) bucket for **[agwinterm](https://github.com/yeroo/agwinterm)** — a native
Windows terminal built for AI coding agents.

## Install

```pwsh
scoop bucket add agwinterm https://github.com/yeroo/scoop-bucket
scoop install agwinterm
```

Updates arrive automatically with each tagged release ([Excavator](https://github.com/yeroo/scoop-bucket/actions/workflows/excavator.yml)
bumps the manifest); upgrade with:

```pwsh
scoop update agwinterm
```

The package uses the **portable single-file build** — no installer, no admin rights, settings live in
`%LOCALAPPDATA%\agwinterm`. Binaries are unsigned but every release carries a
[Sigstore build-provenance attestation](https://github.com/yeroo/agwinterm/attestations):

```pwsh
gh attestation verify (scoop prefix agwinterm)\agwinterm.exe --repo yeroo/agwinterm
```

## Issues

Report packaging problems here; app issues go to
[yeroo/agwinterm/issues](https://github.com/yeroo/agwinterm/issues).
