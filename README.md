# Homebrew tap for sqz

This tap packages [`ojuschugh1/sqz`](https://github.com/ojuschugh1/sqz) for Homebrew.

## Install

```sh
brew tap withakay/sqz
brew install sqz
```

The formula installs both `sqz` and `sqz-mcp` from the upstream GitHub release artifacts.

## Update automation

`.github/workflows/update-sqz.yml` runs nightly and can also be triggered manually. It checks the latest upstream release, rewrites `Formula/sqz.rb` with the matching URLs and SHA256 checksums, and opens a pull request if anything changed.

## Local validation

```sh
ruby .github/scripts/update_formula.rb
brew audit --formula Formula/sqz.rb
brew install --formula Formula/sqz.rb
brew test sqz
```
