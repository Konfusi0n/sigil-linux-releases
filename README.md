# Sigil Linux releases

One-click Sigil installers for Linux Mint and Debian, with checksums and the
verification record used for each build. No credentials, source trees, customer
data, or private notes belong in this repository.

## Download — Sigil 0.6.9.5 for Linux Mint / Debian

**One-click page:** https://konfusi0n.github.io/sigil-linux-releases/

**Direct installer link**

https://github.com/Konfusi0n/sigil-linux-releases/releases/download/v0.6.9.5-linux.1/Install-Sigil-0.6.9.5-Linux-Mint.deb

**SHA-256**

```
4f2a956490a20fd367613b5b248c2471bea30a077ec41411d9fcc9d090c28b6f
```

**Mirror**

https://gofile.io/d/rHOdLVf6

## Install

Double-click the downloaded `.deb` and choose **Install**, or run:

```sh
sudo apt install ./Install-Sigil-0.6.9.5-Linux-Mint.deb
```

Open **Sigil** from the application menu, or run:

```sh
sigil-launch
```

Check it with:

```sh
sigil-ai setup status --json
```

## What is included

The native Linux build of the same 0.6.9.5 release used by the Windows bundle:

- patched Sigil engine (OpenCode fork 2.0.18, displayed as `opencode v0.6.9.5`);
- full operator harness (plugins and skills);
- private Python 3.13 runtime and pinned cryptography wheels;
- unmodified DonSeTch 5.1.2;
- bundled CA trust; no system Python, Node, Bun, Git or WSL required.

Verified on a clean Ubuntu 22.04 / glibc 2.35 baseline (covers Linux Mint 21.x;
Mint 22 is newer): `.deb` install, 6,327-file payload verification, five customer
plugins admitted, TUI service start, DonSeTch 5.1.2, and bundled CA trust. See
`verification.txt` and `PARITY-EVIDENCE.md` in the release assets.

## Important notes

- The package is named `sigil-operator` to avoid Debian's unrelated `sigil` EPUB
  editor package. The editor is left untouched.
- Commands are `sigil-ai` and `sigil-launch`. `/usr/local/bin/sigil` is added
  only when that name is free.
- User state lives under `~/.local` and survives package removal.
- The package is unsigned. Verify the SHA-256 above for byte-level assurance.
- Engineering candidate, not a public production release.
