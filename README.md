# GitHub Portfolio Builder

A review-focused plugin for assessing a GitHub profile or repository as a professional portfolio. It gives a short assessment, sourced and prioritized improvements, and a few worthwhile additions when they can be shared responsibly.

The reviewer can check current public GitHub pages without a GitHub token. A private target requires access you already have. The skill instructs Claude to review without editing GitHub, changing pins, opening pull requests, or publishing files. Those instructions are not a technical permission boundary; the host's tool permissions control what Claude can do.

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

## Data and permissions

This package contains a skill and reference text, with no bundled executable, hook, MCP server, analytics endpoint, or telemetry. The skill asks Claude to inspect the target profile or repository and the limited linked sources needed to support a finding. Claude and any tools you enable process the URLs and content under their own terms and account settings. A private target can expose private content to the Claude session, so review its permissions before use.

For a stricter review session in Claude Code, use host-level tool restrictions or a read-only GitHub MCP configuration. The plugin's prose alone cannot prevent writes when the host gives Claude write-capable tools. The plugin does not require a token for a public target.

## Distribution status

The GitHub repository is public and installable as a Claude Code marketplace. A Claude Directory listing is separate: validation, GitHub connection, data-handling and compliance disclosures, submission, and Anthropic review must be completed before calling it listed. No Directory publication is claimed here.

See [verification status](docs/verification.md) for the surfaces and behavior checked so far. Claude chat and Cowork have not yet been tested.

## Optional GitHub MCP

The plugin works without an MCP for public reviews. If you already use [GitHub's official MCP server](https://github.com/github/github-mcp-server), its read tools can make repository file, tree, release, and profile checks more reliable. Configure it in [read-only mode](https://github.com/github/github-mcp-server/blob/main/docs/server-configuration.md) and enable only the toolsets you need, such as `repos`, `users`, and `git`. GitHub publishes a [setup guide for Claude](https://github.com/github/github-mcp-server/blob/main/docs/installation-guides/install-claude.md). The plugin does not install the server or require a token for public repositories; its skill instructs Claude not to call write tools.

A browser remains useful for checking the visible profile, pins, rendered README, and linked demos; repository metadata alone cannot establish how those pages appear to a visitor.

## Package

The marketplace manifest is at `.claude-plugin/marketplace.json`. It points to the plugin and skill under `plugins/github-portfolio-builder/`.
