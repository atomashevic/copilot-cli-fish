# Setup GitHub Copilot CLI for fish shell

[Copilot for CLI](https://githubnext.com/projects/copilot-cli) integrates Copilot into your CLi.

If have access to this feature, few steps are needed to activate Copilot in your shell. [Official instructions](https://www.npmjs.com/package/@githubnext/github-copilot-cli#alias-convenience-commands) support zsh and bash shells, but with few changes the aliases for Copilot CLI can be integrated into fish.

First step is to install Copilot for CLI from fish:

```fish
npm install -g @githubnext/github-copilot-cli
```

Second step is to authenticate your GH account:

```
github-copilot-cli auth
```

After authentication is completed you essentially have everything you need except aliases for three commands of Copilot workflow in CLI. You need to edit your fish config file (e.g. `~\.config\fish`) and add the code from [`copilot.fish`](copilot.fish) at the end of your config file.
