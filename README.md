# GitHub Portfolio Builder

A read-only plugin for reviewing a GitHub profile or repository as a professional portfolio. It gives a short assessment, sourced and prioritized improvements, and a few worthwhile additions when they can be shared responsibly.

The reviewer checks current public GitHub pages without needing a GitHub token. A private target requires access you already have. The plugin does not edit GitHub, change profile pins, open pull requests, or publish files.

## Install in Claude Code

```sh
claude plugin marketplace add RachaelQuisel/github-portfolio-builder
claude plugin install github-portfolio-builder@github-portfolio-builder
```

Then invoke `/github-portfolio-builder:github-portfolio-builder` with a GitHub profile or repository URL. This repository will also be submitted to the Claude plugin directory, which has a separate review and publication process.

## Use

Give Claude a public profile or repository URL and invoke the skill:

```text
/github-portfolio-builder:github-portfolio-builder https://github.com/OWNER/REPOSITORY
```

You can also just ask: “Review my GitHub profile as a professional portfolio and tell me the most valuable improvements.”

The review links to evidence, separates verified facts from repository claims and inferences, and identifies gaps when a source cannot be inspected. Code correctness and security auditing are separate tasks.

## What this plugin reads and sends

The plugin reads the public GitHub pages for the profile or repository you name, and nothing else. It sends no data to any service that Anthropic or GitHub does not already host, and it stores nothing. There is no account to create, no token required for a public target, and no telemetry. Every action is a read. The plugin never writes to GitHub.

## Optional GitHub MCP

The plugin works without an MCP for public reviews. If you already use [GitHub's official MCP server](https://github.com/github/github-mcp-server), its read tools can make repository file, tree, release, and profile checks more reliable. Configure it in [read-only mode](https://github.com/github/github-mcp-server/blob/main/docs/server-configuration.md) and enable only the toolsets you need, such as `repos`, `users`, and `git`. GitHub publishes a [setup guide for Claude](https://github.com/github/github-mcp-server/blob/main/docs/installation-guides/install-claude.md). The plugin does not install the server, require a token for public repositories, or use write tools.

A browser remains useful for checking the visible profile, pins, rendered README, and linked demos; repository metadata alone cannot establish how those pages appear to a visitor.

## Package

The marketplace manifest is at `.claude-plugin/marketplace.json`. It points to the plugin and skill under `plugins/github-portfolio-builder/`.
