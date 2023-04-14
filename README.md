# Setup GitHub Copilot CLI for fish shell

[Copilot for CLI](https://githubnext.com/projects/copilot-cli) integrates Copilot into your shell.

If have access to this feature, few steps are needed to activate Copilot in your shell. [Official instructions](https://www.npmjs.com/package/@githubnext/github-copilot-cli#alias-convenience-commands) support zsh and bash shells, but with few changes the aliases for Copilot CLI can be integrated into fish.

First step is to install Copilot for CLI from fish:

```fish
npm install -g @githubnext/github-copilot-cli
```

Second step is to authenticate your GitHub account:

```
github-copilot-cli auth
```

After authentication is completed you essentially have everything you need except aliases for three commands of Copilot workflow in CLI. You need to edit your fish config file (e.g. `~\.config\fish`) and add the code from [`copilot.fish`](copilot.fish) at the end of your config file.

Restart your shell and you will have aliases for three comands at your disposal:

1. `wts <query>` : Runs what-the-shell which gives shell commands from natural language descriptions
2. `gitq <query>`: Runs git-assist which gives git commands from natural language descriptions
3. `ghq <query>` : Runs gh-assist which gives gh (official GitHub cli tool) commands from natueral language descriptions

You can customize the aliases in your fish .config file.

### Limitations

Calling `wts` may often return shell commands which will only work in bash or zsh. According to the official documentation you can try to revise the request by adding `on fish shell` to your query.
