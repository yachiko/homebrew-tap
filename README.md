<h1 align="center">yachiko/homebrew-tap</h1>
<p align="center"><strong>Homebrew formulas for yachiko's tools</strong></p>

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

Either form works — `brew install yachiko/tap/<formula>` auto-taps on first
use, or you can `brew tap yachiko/tap` once and then `brew install <formula>`.

## What's here

| Formula | Upstream | Description |
|---|---|---|
| [`clerk`](Formula/clerk.rb) | [yachiko/clerk](https://github.com/yachiko/clerk) | CLI for managing AWS Parameter Store secrets |
| [`fossor`](Formula/fossor.rb) | [yachiko/fossor](https://github.com/yachiko/fossor) | Terminal UI for managing multiple Git repos |

## How updates land

Formulas in `Formula/` are written automatically by
[GoReleaser](https://goreleaser.com/customization/homebrew/) on every
upstream release. A dedicated GitHub App (`yachiko-homebrew-bot`) signs the
commits; no human pushes to this repo directly.

## License

MIT — see [LICENSE](LICENSE).
