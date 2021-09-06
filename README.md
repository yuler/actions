# GitHub Actions

> This repo is collection some GitHub Actions.

## About GitHub Action Refs

-   [Official Document](https://docs.github.com/en/actions)
-   [Awesome Actions](https://github.com/sdras/awesome-actions)
-   [Act](https://github.com/nektos/act) - Run your GitHub Actions locally
-   [TypeScript Action](https://github.com/actions/typescript-action) - A TypeScript Action Template

## gh download

The `gh download` command is come from [gh-download](https://github.com/yuler/gh-download)

## GitHub Release

> Recommend use [release-drafter](https://github.com/release-drafter/release-drafter) action.

```bash
gh download yuler/actions .github/release-drafter-config.yml .github/workflows/release-drafter.yml
```

**Note** Must first have the configuration file in the default branch

refs:

-   https://github.com/release-drafter/release-drafter
-   https://github.com/actions/create-release
-   https://github.com/semantic-release/cli#github-actions
-   https://github.com/yyx990803/release-tag
