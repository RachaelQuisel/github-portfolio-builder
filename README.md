# GitHub Portfolio Review for Claude and Codex

A read-only plugin for reviewing a GitHub profile or repository as a professional portfolio. It gives a short assessment, sourced and prioritized improvements, and a few worthwhile additions when they can be shared responsibly. The Claude and Codex packages use the same skill and review checks.

The reviewer checks current public GitHub pages without needing a GitHub token. A private target requires access you already have. The plugin does not edit GitHub, change profile pins, open pull requests, or publish files.

## Install in Claude Code

```sh
claude plugin marketplace add RachaelQuisel/github-portfolio-review
claude plugin install github-portfolio-review@github-review
```

Then invoke `/github-portfolio-review:github-portfolio-review` with a GitHub profile or repository URL. This repository will also be submitted to the Claude plugin directory, which has a separate review and publication process.

## Install in Codex

In a terminal with Codex installed:

```sh
codex plugin marketplace add RachaelQuisel/github-portfolio-review
codex plugin add github-portfolio-review@github-review
```

## Use

Give Codex a public profile or repository URL and invoke the skill:

```text
$github-portfolio-review https://github.com/OWNER/REPOSITORY
```

You can also ask either assistant: “Review my GitHub profile as a professional portfolio and tell me the most valuable improvements.”

The review links to evidence, separates verified facts from repository claims and inferences, and identifies gaps when a source cannot be inspected. Code correctness and security auditing are separate tasks.

## Optional GitHub MCP

The plugin works without an MCP for public reviews. If you already use [GitHub's official MCP server](https://github.com/github/github-mcp-server), its read tools can make repository file, tree, release, and profile checks more reliable. Configure it in [read-only mode](https://github.com/github/github-mcp-server/blob/main/docs/server-configuration.md) and enable only the toolsets you need, such as `repos`, `users`, and `git`. GitHub has separate setup guides for [Claude](https://github.com/github/github-mcp-server/blob/main/docs/installation-guides/install-claude.md) and [Codex](https://github.com/github/github-mcp-server/blob/main/docs/installation-guides/install-codex.md). The plugin does not install the server, require a token for public repositories, or use write tools.

A browser remains useful for checking the visible profile, pins, rendered README, and linked demos; repository metadata alone cannot establish how those pages appear to a visitor.

## Package

Claude's marketplace manifest is at `.claude-plugin/marketplace.json`; Codex's is at `.agents/plugins/marketplace.json`. Both point to the same plugin and skill under `plugins/github-portfolio-review/`.
