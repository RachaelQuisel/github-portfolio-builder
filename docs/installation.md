# Set up GitHub Portfolio Builder in Claude Code

## First installation

Run these commands in your terminal with [Claude Code installed](https://code.claude.com/docs/en/setup):

```sh
claude plugin marketplace add RachaelQuisel/github-portfolio-builder
claude plugin install github-portfolio-builder@github-portfolio-builder
claude
```

The first two commands install the plugin. The last opens Claude Code. In the Claude Code conversation, ask it to use GitHub Portfolio Builder and provide your GitHub URL.

## Update an existing installation

Check which source your installation uses. Run this in your terminal:

```sh
claude plugin marketplace list
```

Find `github-portfolio-builder`. Follow the instructions below for the source shown.

### Installed from GitHub

Run these commands in your terminal:

```sh
claude plugin marketplace update github-portfolio-builder
claude plugin update github-portfolio-builder@github-portfolio-builder
```

### Installed from a local checkout

Claude Code loads this installation from the folder shown in the marketplace list. Update that existing folder before updating the plugin record.

1. Open a terminal in that repository folder.
2. Run `git status --short`. If it lists local changes, preserve and resolve them before continuing.
3. Run the following commands from that folder:

```sh
git pull --ff-only
claude plugin update github-portfolio-builder@github-portfolio-builder
```

If Git cannot fast-forward, stop and resolve the branch difference. Do not reset the repository or delete the installation to bypass the error.

### Confirm the update

Run this in your terminal:

```sh
claude plugin details github-portfolio-builder@github-portfolio-builder
```

Check the displayed version and the `github-portfolio-builder` skill. Start a new Claude Code session with `claude`, or type `/reload-plugins` inside your current Claude Code conversation.

## Fix a terminal error for a slash command

An error such as `zsh: no such file or directory: /github-portfolio-builder:github-portfolio-builder` means the command was entered in the shell. The shell treats the leading `/` as a file path.

Run `claude` in your terminal first. Then type this in the Claude Code conversation, replacing the example URL with your own:

```text
/github-portfolio-builder:github-portfolio-builder https://github.com/RachaelQuisel/github-portfolio-builder
```

## Fix a marketplace source mismatch

The error `its source doesn't match its extraKnownMarketplaces entry` means Claude Code settings already declare this marketplace from a different source. A local folder and a GitHub repository are different sources, even when their plugin names match.

Run `claude plugin marketplace list` in your terminal. If `github-portfolio-builder` is listed, keep that source and follow the matching update instructions above. An `already installed` message confirms that another installation is unnecessary.

If the marketplace is missing from the list, inspect its `extraKnownMarketplaces` entry in Claude Code settings. Add it from the exact declared source. If managed settings control that entry, ask your administrator. See [Claude Code's source-mismatch guidance](https://code.claude.com/docs/en/plugins/troubleshooting).

These instructions follow the [official plugin command reference](https://code.claude.com/docs/en/plugins/cli-reference). They cover Claude Code. A successful terminal installation does not establish which version is serving in the Claude Directory.
