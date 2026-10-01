# GitHub Portfolio Review for Codex

A read-only Codex plugin for reviewing a GitHub profile or repository as a professional portfolio. It gives a short assessment, sourced and prioritized improvements, and a few worthwhile additions when they can be shared responsibly.

The reviewer checks current public GitHub pages without needing a GitHub token. A private target requires access you already have. The plugin does not edit GitHub, change profile pins, open pull requests, or publish files.

## Install

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

You can also ask: “Review my GitHub profile as a professional portfolio and tell me the most valuable improvements.”

The review links to evidence, separates verified facts from repository claims and inferences, and identifies gaps when a source cannot be inspected. Code correctness and security auditing are separate tasks.

## Package

The marketplace manifest is at `.agents/plugins/marketplace.json`; the plugin manifest and skill are under `plugins/github-portfolio-review/`.
