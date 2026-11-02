# BRF Tech

Open-source software from BRF Tech: **filex**, a self-hosted file manager, with
the apps that run inside it, its language packs and the packaging that installs
it, and **RunR**, a serverless platform for your own Kubernetes, with its runtime
images, Terraform provider and Helm charts.

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
winget install BRFTech.filex             # Windows 10/11
```

The desktop app's winget package, `BRFTech.filex-app`, is submitted and waiting
for review in [winget-pkgs](https://github.com/microsoft/winget-pkgs).

How to run the server, plus the Windows installer, portable builds, AppImage,
`.deb`, `.rpm` and `.dmg`: [Installation](https://docs.filex.sh/INSTALLATION) ·
[Desktop app](https://docs.filex.sh/DESKTOP) ·
[latest release](https://github.com/BRF-Tech/filex/releases/latest).

To embed the file manager in your own web app, use
[`@brftech/filex`](https://www.npmjs.com/package/@brftech/filex) (web component) or
[`@brftech/filex-react`](https://www.npmjs.com/package/@brftech/filex-react) from npm.

## RunR

<img src="https://raw.githubusercontent.com/BRF-Tech/runr/main/logo/runr-icon-dark.svg" alt="" width="64" align="right">

**RunR is an open-source serverless platform on your own Kubernetes: functions,
containers and WebAssembly with scale-to-zero on Knative, on clusters you operate,
connected or air-gapped.**

Every change is a version you can deploy, compare and roll back; blue-green and
canary rollouts, environments, event triggers, durable workflows, sandboxes for AI
agents, GPU and Hugging Face models and a built-in MCP server come with it. MIT licensed.

**[runr.sh](https://runr.sh)** · **[Documentation](https://runr.sh/docs/)** ·
[Source](https://github.com/BRF-Tech/runr) ·
[Releases](https://github.com/BRF-Tech/runr/releases)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/BRF-Tech/runr/main/landing/shots/projects-dark.png">
  <img src="https://raw.githubusercontent.com/BRF-Tech/runr/main/landing/shots/projects-light.png" alt="The RunR console: the projects of an organization" width="820">
</picture>

### Install

```sh
# Control plane on Kubernetes: the Helm chart brf-tech/runr; domain is the only required value
helm repo add brf-tech https://helm.brf.sh
helm upgrade --install runr brf-tech/runr --namespace runr --create-namespace --set domain=runr.example.com

# CLI
curl -fsSL https://runr.sh/install.sh | sh     # Linux, macOS; other platforms: https://runr.sh/dl/
```

The single-host install with Docker Compose, the Terraform provider (`brf-tech/runr`
on the Terraform Registry) and the GitHub Action:
[Quick start](https://github.com/BRF-Tech/runr#quick-start) ·
[Documentation](https://runr.sh/docs/).

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
| [**runr**](https://github.com/BRF-Tech/runr) | The serverless platform: control plane, console, Helm chart, CLI, SDKs, examples and documentation. |
| [**runr-runtimes**](https://github.com/BRF-Tech/runr-runtimes) | RunR's language runtime images, the universal wrapper and hf-serve, published to ghcr.io. |
| [**terraform-provider-runr**](https://github.com/BRF-Tech/terraform-provider-runr) | Terraform / OpenTofu provider for RunR (`brf-tech/runr` on the Terraform Registry). |
| [**helm-charts**](https://github.com/BRF-Tech/helm-charts) | Helm charts for BRF Tech products, served from helm.brf.sh. |

Apps and language packs are installed from the filex admin panel, under
*Plugins → Apps*. See [Apps](https://docs.filex.sh/APP-PLUGINS) and
[writing your own](https://docs.filex.sh/PLUGIN-KIT).

## Contributing

- **Bugs and feature requests:** open an issue in the repository concerned. For
  filex itself, that is [BRF-Tech/filex/issues](https://github.com/BRF-Tech/filex/issues);
  for RunR, [BRF-Tech/runr/issues](https://github.com/BRF-Tech/runr/issues).
- **Questions and ideas:** [filex Discussions](https://github.com/BRF-Tech/filex/discussions) ·
  [RunR Discussions](https://github.com/BRF-Tech/runr/discussions).
- **Code:** read the project's contributing guide first:
  [filex](https://github.com/BRF-Tech/filex/blob/main/docs/CONTRIBUTING.md) ·
  [RunR](https://github.com/BRF-Tech/runr/blob/main/CONTRIBUTING.md).
- **Translations:** start a new language from
  [filex-lang-template](https://github.com/BRF-Tech/filex-lang-template). Corrections
  to the German, Spanish and French packs are welcome as pull requests.

## Security

Please do not report vulnerabilities in public issues. Follow the security policy of
[filex](https://github.com/BRF-Tech/filex/blob/main/SECURITY.md) or
[RunR](https://github.com/BRF-Tech/runr/blob/main/SECURITY.md), or write to
**security@brf.sh**.

## Contact

**hello@brf.sh** · [brf.sh](https://brf.sh)

<sub>The store badges are the stores' own artwork, used unmodified: Microsoft and the
Microsoft Store badge are trademarks of the Microsoft group of companies; the Snap Store
badge is © Canonical Ltd., licensed
[CC BY-ND 2.0 UK](https://creativecommons.org/licenses/by-nd/2.0/uk/).</sub>
