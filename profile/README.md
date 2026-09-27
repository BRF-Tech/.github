# BRF Tech

Open-source software from BRF Tech. Most of what lives here is **filex**, a
self-hosted file manager, and the pieces around it: apps that run inside it,
language packs, and the packaging that installs it.

## filex

<img src="https://raw.githubusercontent.com/BRF-Tech/filex/main/docs/logo.png" alt="" width="64" align="right">

**filex is a self-hosted file manager: one Go binary with a full web UI, storage
that plugs in (local, S3, SFTP, WebDAV, FTP, SMB), and the same files reachable
over S3, SFTP, FTPS, WebDAV and NFS.**

It also comes as a desktop app with folder sync, as a web component you can embed
in your own application, and with a built-in MCP server. MIT licensed.

**[filex.sh](https://filex.sh)** · **[Documentation](https://docs.filex.sh)** ·
**[Live demo](https://demo.filex.sh)** · [Source](https://github.com/BRF-Tech/filex) ·
[Releases](https://github.com/BRF-Tech/filex/releases)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/BRF-Tech/filex/v0.47.0/docs/screenshots/v0.47.0/explorer-grid-dark.png">
  <img src="https://raw.githubusercontent.com/BRF-Tech/filex/v0.47.0/docs/screenshots/v0.47.0/explorer-grid-light.png" alt="The filex file explorer showing a thumbnail grid" width="820">
</picture>

### Install

<p>
<a href="https://apps.microsoft.com/detail/9PKXDJLVZWXW"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/BRF-Tech/filex/main/docs/badges/ms-store-light.svg"><img src="https://raw.githubusercontent.com/BRF-Tech/filex/main/docs/badges/ms-store-dark.svg" alt="filex File Manager in the Microsoft Store" height="52"></picture></a>&nbsp;&nbsp;&nbsp;
<a href="https://snapcraft.io/filex-app"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/BRF-Tech/filex/main/docs/badges/snap-store-white.svg"><img src="https://raw.githubusercontent.com/BRF-Tech/filex/main/docs/badges/snap-store-black.svg" alt="filex-app in the Snap Store" height="52"></picture></a>
</p>

```sh
# Server: container image on the GitHub Container Registry
docker pull ghcr.io/brf-tech/filex:latest

# Desktop app
brew install brf-tech/filex/filex-app    # macOS 13+, Apple Silicon
sudo snap install filex-app              # Linux with snapd

# CLI
brew install brf-tech/filex/filex        # macOS, Linux
```

The winget packages, `BRFTech.filex-app` and `BRFTech.filex`, are submitted and
waiting for review in [winget-pkgs](https://github.com/microsoft/winget-pkgs).

How to run the server, plus the Windows installer, portable builds, AppImage,
`.deb`, `.rpm` and `.dmg`: [Installation](https://docs.filex.sh/INSTALLATION) ·
[Desktop app](https://docs.filex.sh/DESKTOP) ·
[latest release](https://github.com/BRF-Tech/filex/releases/latest).

To embed the file manager in your own web app, use
[`@brftech/filex`](https://www.npmjs.com/package/@brftech/filex) (web component) or
[`@brftech/filex-react`](https://www.npmjs.com/package/@brftech/filex-react) from npm.

## Repositories

| Repository | What it is |
|---|---|
| [**filex**](https://github.com/BRF-Tech/filex) | The file manager: server, web UI, desktop app and CLI. |
| [**filex-sign**](https://github.com/BRF-Tech/filex-sign) | e-Signature app for filex: sign PDFs, request signatures and verify them. |
| [**filex-convert**](https://github.com/BRF-Tech/filex-convert) | Convert app for filex: converts files between formats, as a WebAssembly app. |
| [**filex-app-template**](https://github.com/BRF-Tech/filex-app-template) | Start your own filex app: a working example, tests, a reproducible build and a release workflow. |
| [**filex-lang-template**](https://github.com/BRF-Tech/filex-lang-template) | Translate filex into your language and ship it as a language pack. |
| Language packs | [German](https://github.com/BRF-Tech/filex-lang-de), [Spanish](https://github.com/BRF-Tech/filex-lang-es) and [French](https://github.com/BRF-Tech/filex-lang-fr). AI-translated and awaiting review by native speakers. |
| [**homebrew-filex**](https://github.com/BRF-Tech/homebrew-filex) | Homebrew tap for the filex CLI and desktop app. |

Apps and language packs are installed from the filex admin panel, under
*Plugins → Apps*. See [Apps](https://docs.filex.sh/APP-PLUGINS) and
[writing your own](https://docs.filex.sh/PLUGIN-KIT).

## Contributing

- **Bugs and feature requests:** open an issue in the repository concerned. For
  filex itself, that is [BRF-Tech/filex/issues](https://github.com/BRF-Tech/filex/issues).
- **Questions and ideas:** [filex Discussions](https://github.com/BRF-Tech/filex/discussions).
- **Code:** read [CONTRIBUTING](https://github.com/BRF-Tech/filex/blob/main/docs/CONTRIBUTING.md) first.
- **Translations:** start a new language from
  [filex-lang-template](https://github.com/BRF-Tech/filex-lang-template). Corrections
  to the German, Spanish and French packs are welcome as pull requests.

## Security

Please do not report vulnerabilities in public issues. Follow the
[security policy](https://github.com/BRF-Tech/filex/blob/main/SECURITY.md) or write
to **security@brf.sh**.

## Contact

**hello@brf.sh** · [brf.sh](https://brf.sh)

<sub>The store badges are the stores' own artwork, used unmodified: Microsoft and the
Microsoft Store badge are trademarks of the Microsoft group of companies; the Snap Store
badge is © Canonical Ltd., licensed
[CC BY-ND 2.0 UK](https://creativecommons.org/licenses/by-nd/2.0/uk/).</sub>
