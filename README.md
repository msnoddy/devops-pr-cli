# devops-pr-cli

Simple CLI tool that dumps Azure Dev Ops pull request for a team of developers into a table, grouped by dev name and ordered by age.

## Quickstart

- Copy the config file [bin/config.yml](bin/config.yml) and fill it out with your settings

- Define an environment variable that points to your new config file

```bash
export DEV_OPS_PR_CLI_CFG="/some/path/to/config.yml"
```

- Define an environment variable that points to a secret file that contains an authentication token for Dev Ops (you will need to create this in Dev Ops if you don't have one):

```bash
export DEV_OPS_AUTH_TOKEN_FILE="/some/path/to/secret/stuff"
```

- Ensure you have the `yarn` package manager installed, then run:

```bash
yarn install
```

- Run the tool:

```bash
./bin/devops-pr-cli
```

## JIRA Support

If you format your pull requests with your JIRA code and ticket number, you can output a link to the related JIRA item for each PR.

Example PR title in Dev Ops: `CODE-1234: Some Amazing Feature`

If you set `jira.enabled` to `true` in the config file the tool will also output a JIRA url in the format:

```
JIRA: https://jira.some.domain.com/browse/CODE-1234
```
