<h1 align="center">yachiko/homebrew-tap</h1>
<p align="center"><strong>Homebrew casks for yachiko's tools</strong></p>

<p align="center">
  <a href=".github/workflows/tests.yml"><img src="https://github.com/yachiko/homebrew-tap/actions/workflows/tests.yml/badge.svg" alt="Tests"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/yachiko/homebrew-tap" alt="License"></a>
</p>

---

## Install

```sh
brew install yachiko/tap/clerk
brew install yachiko/tap/fossor
```

Either form works — `brew install yachiko/tap/<name>` auto-taps on first
use, or you can `brew tap yachiko/tap` once and then `brew install <name>`.
`brew install` autodetects casks, so no `--cask` flag is required.

## What's here

| Cask | Upstream | Description |
|---|---|---|
| [`clerk`](Casks/clerk.rb) | [yachiko/clerk](https://github.com/yachiko/clerk) | CLI for managing AWS Parameter Store secrets |
| [`fossor`](Casks/fossor.rb) | [yachiko/fossor](https://github.com/yachiko/fossor) | Terminal UI for managing multiple Git repos |

## How updates land

Casks in `Casks/` are written automatically by
[GoReleaser](https://goreleaser.com/customization/publish/homebrew_casks/)
on every upstream release. A dedicated GitHub App (`yachiko-homebrew-bot`)
signs the commits; no human pushes to this repo directly.

## License

MIT — see [LICENSE](LICENSE).
