# GitHub Actions

> This repo is collection some GitHub Actions.

## About GitHub Action Refs

-   [Official Document](https://docs.github.com/en/actions)
-   [Awesome Actions](https://github.com/sdras/awesome-actions)
-   [Act](https://github.com/nektos/act) - Run your GitHub Actions locally
-   [TypeScript Action](https://github.com/actions/typescript-action) - A TypeScript Action Template

## gh download

The `gh download` command is come from [gh-download](https://github.com/yuler/gh-download)

## Node.js CI

```bash
gh download yuler/actions .github/workflows/nodejs-ci.yml
```

refs:

https://docs.github.com/en/actions/guides/building-and-testing-nodejs-or-python?langId=nodejs

## GitHub Release

> Recommend use [release-drafter](https://github.com/release-drafter/release-drafter) action.

```bash
gh download yuler/actions .github/release-drafter.yml .github/workflows/drafter.yml
```

**Note** Must first have the configuration file in the default branch

refs:

-   https://github.com/release-drafter/release-drafter
-   https://github.com/actions/create-release
-   https://github.com/semantic-release/cli#github-actions
-   https://github.com/yyx990803/release-tag

## NPM Publish

```bash
# Add NPM_TOKEN secret from `~/.npmrc`
gh secret set NPM_TOKEN -b"$(cat ~/.npmrc | grep _authToken | sed 's/\/\/registry.npmjs.org\/:_authToken=//')"
# Or add alias
gh alias set secret_add_npm_token "secret set NPM_TOKEN -b"$(cat ~/.npmrc | grep _authToken | sed 's/\/\/registry.npmjs.org\/:_authToken=//')""
# Download file
gh download yuler/actions .github/workflows/npm-publish.yml
```

refs:

-   https://docs.github.com/en/actions/guides/publishing-nodejs-packages
