# homebrew-tap

Homebrew tap for [git-account](https://github.com/achekulaev/git-account).

## Install

```bash
brew install achekulaev/tap/git-account
```

That is shorthand for tapping this repo and installing the formula:

```bash
brew tap achekulaev/tap
brew install git-account
```

Upgrades come via `brew upgrade`.

## Releasing a new version

1. Tag and release in the [git-account](https://github.com/achekulaev/git-account) repo (e.g. `gh release create vX.Y.Z`).
2. Compute the tarball hash:
   ```bash
   curl -fsSL https://github.com/achekulaev/git-account/archive/refs/tags/vX.Y.Z.tar.gz | shasum -a 256
   ```
3. Bump `url`, `version`, and `sha256` in `Formula/git-account.rb`, then commit and push.
