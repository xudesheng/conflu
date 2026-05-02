# Install Conflu

## Quick Install

```bash
npm i -g @xudesheng/conflu
conflu --version
```

## npx

```bash
npx @xudesheng/conflu --version
```

## GitHub Release Binaries

Use the latest release from:

<https://github.com/xudesheng/conflu/releases/latest>

Assets:

- `conflu-v<version>-windows-x64.zip`
- `conflu-v<version>-linux-x64-musl.tar.gz`
- `conflu-v<version>-macos-universal.zip`

Also download:

- `conflu-v<version>-SHA256SUMS.txt`
- `distribution-state.json` for the public release state snapshot

## Verify Checksums

Linux/macOS:

```bash
sha256sum -c conflu-v<version>-SHA256SUMS.txt
```

Windows PowerShell:

```powershell
Get-FileHash .\conflu-v<version>-windows-x64.zip -Algorithm SHA256
```

Compare the output hash with the corresponding line in `conflu-v<version>-SHA256SUMS.txt`.

## Extract and Run

After extraction, add `conflu` (`conflu.exe` on Windows) to `PATH` and run:

```bash
conflu --version
conflu --help
```

## macOS Trust

Conflu macOS release binaries are signed with Developer ID and submitted to Apple notarization.

For CLI binaries, public verification checks `codesign --verify`; `spctl --assess` is intentionally not treated as a release gate because Conflu is distributed as a standalone CLI binary rather than an `.app`, `.pkg`, or `.dmg`.

