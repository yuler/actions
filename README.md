# GitHub Actions

> This repo is collection some GitHub Actions.

Recommend use `gh download`[^gh-download] command.

## Node.js

### [ci.yml](./nodejs/ci.yml)

```bash
gh https://github.com/yuler/actions/blob/main/nodejs/ci.yml --outdir .github/workflows
```

Related:

- <https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-nodejs>

### [npm-publish](./nodejs/npm-publish.yml)

```bash
gh https://github.com/yuler/actions/blob/main/nodejs/npm-publish.yml --outdir .github/workflows
# Add NPM_TOKEN secret from `~/.npmrc`
gh alias set add-npm-token "secret set NPM_TOKEN --body "$(cat ~/.npmrc | grep _authToken | sed 's/\/\/registry.npmjs.org\/:_authToken=//')""
gh add-npm-token
```

Related:

- <https://docs.github.com/en/actions/guides/publishing-nodejs-packages>

## Misc

### [sync-gitlab](./misc/sync-gitlab.yml)

```bash
gh https://github.com/yuler/actions/blob/main/misc/sync-gitlab.yml --outdir .github/workflows
gh secret set GITLAB_TOKEN <$YOUR_GITLAB_TOKEN>
```

### [cron](./misc/cron.yml)

```bash
gh https://github.com/yuler/actions/blob/main/misc/cron.yml --outdir .github/workflows
gh secret set GITLAB_TOKEN <$YOUR_GITLAB_TOKEN>
```

Related:

- <https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule>

### [release](./misc/release-drafter.yml)

> Recommend use [release-drafter](https://github.com/release-drafter/release-drafter) action.

```bash
gh https://github.com/yuler/actions/blob/main/misc/drafter.yml --outdir .github/workflows
gh https://github.com/yuler/actions/blob/main/misc/release-drafter.yml --outdir .github
```

**Note** Must first have the configuration file in the default branch

Related:

- <https://github.com/semantic-release/cli#github-actions>
- <https://github.com/yyx990803/release-tag>

## Related

- [Awesome Actions](https://github.com/sdras/awesome-actions)
- [Act](https://github.com/nektos/act) - Run your GitHub Actions locally

[^gh-download]: The `gh download` command is come from [gh-download](https://github.com/yuler/gh-download)
