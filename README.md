<h1 align="center">yachiko/homebrew-tap</h1>
<p align="center"><strong>Homebrew casks and formulae for yachiko's tools</strong></p>

<p align="center">
  <a href=".github/workflows/tests.yml"><img src="https://github.com/yachiko/homebrew-tap/actions/workflows/tests.yml/badge.svg" alt="Tests"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/yachiko/homebrew-tap" alt="License"></a>
</p>

---

## Install

```sh
brew install --cask yachiko/tap/clerk
brew install --cask yachiko/tap/fossor
brew install --cask yachiko/tap/lege
brew install yachiko/tap/circitor
```

Either form works: `brew install --cask yachiko/tap/<name>` auto-taps on
first use, or run `brew tap yachiko/tap` once and then
`brew install --cask <name>`.

`circitor` is a formula, so it takes no `--cask`. Use its full name: since
Homebrew 6, that also trusts this one item from the tap.

## What's here

| Cask | Upstream | Description |
|---|---|---|
| [`clerk`](Casks/clerk.rb) | [yachiko/clerk](https://github.com/yachiko/clerk) | CLI for managing AWS Parameter Store secrets |
| [`fossor`](Casks/fossor.rb) | [yachiko/fossor](https://github.com/yachiko/fossor) | Terminal UI for managing multiple Git repos |
| [`lege`](Casks/lege.rb) | [yachiko/lege](https://github.com/yachiko/lege) | Minimal Markdown viewer and explorer |

| Formula | Upstream | Description |
|---|---|---|
| [`circitor`](Formula/circitor.rb) | [yachiko/circitor](https://github.com/yachiko/circitor) | Local daemon that watches GitHub pull requests for coding agents (macOS arm64, Linux x86-64 and arm64) |

## How updates land

Casks in `Casks/` are written automatically on every upstream release, by
[GoReleaser](https://goreleaser.com/customization/publish/homebrew_casks/)
(clerk, fossor) or by the project's own release workflow (lege, which builds
natively per platform). `Formula/circitor.rb` is written the same way, by
circitor's release workflow: a formula rather than a cask, because Homebrew
doesn't quarantine a formula's download, so its unsigned binary runs without
notarisation. A dedicated GitHub App (`yachiko-homebrew-bot`)
signs the commits; no human pushes to this repo directly.

## License

MIT — see [LICENSE](LICENSE).
