# GitHub Portfolio Builder

**Build a GitHub portfolio that shows what you can do.**

GitHub Portfolio Builder helps you highlight your strongest work, explain your contributions, and show employers, clients, and collaborators why your projects matter. Share your profile or a repository to get a prioritized plan for what to feature, improve, and add, grounded in your actual work.

Use it to prepare your portfolio for a job application, a client pitch, or your next collaboration.

Claude's directory reports [over 5,000 installs as of November 1, 2026](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/docs/verification.md#directory-install-count).

## What you get

- **A short assessment.** See what the inspected profile or project communicates about the work.
- **Up to five priorities.** Each recommendation includes a source link, why it matters to your audience, and a concrete change to make.
- **Worthwhile additions.** When the evidence supports them, get up to three suggestions for examples, case studies, or other work worth sharing. Each includes any permission, privacy, or attribution requirements.
- **Clear limits.** Know what was checked, what the repository only claims, and what could not be verified.

The review uses your actual pages and files. It checks whether a recommended addition already exists and gives fewer suggestions when fewer are useful.

## What it looks at

For a **profile review**, Claude checks your bio, profile README, visible pins, and a small selection of projects. It looks for a clear explanation of your role and representative work.

For a **repository review**, Claude checks the README and the supporting material needed for your question. That can include examples, setup instructions, licenses, documentation, and linked demos. It looks for what helps someone understand the project or decide whether to use it.

[See an example review](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/docs/example-review.md). It shows a specific recommendation with supporting links and clearly stated limits. The example is illustrative, not a new runtime test.

## Start a review

After installing the plugin, share a GitHub URL and tell Claude who the work is for. You can add a focus, such as the README, project examples, or how clearly your role comes across.

Try one of these requests:

> Review my GitHub profile for employers hiring automation developers. What should I improve first? [profile URL]

> Review this project for a potential client. Can they understand the problem it solves and my contribution? [repository URL]

> Review this repository for someone who wants to reuse it. Check the explanation, examples, and setup instructions. [repository URL]

You can also invoke the skill directly:

```text
/github-portfolio-builder:github-portfolio-builder https://github.com/OWNER/REPOSITORY
```

Claude asks for missing details only when they would change the review. You receive recommendations in chat and choose which changes to make.

## Install in Claude Code

Run these commands in your terminal with Claude Code installed:

```sh
claude plugin marketplace add RachaelQuisel/github-portfolio-builder
claude plugin install github-portfolio-builder@github-portfolio-builder
```

Start a new Claude Code session after installation. These commands follow the [Claude Code installation guide](https://code.claude.com/docs/en/discover-plugins). GitHub installation and Claude Directory publication are separate; see the [dated verification record](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/docs/verification.md) for the versions checked.

## Access and scope

Public reviews need access to current GitHub pages, but do not require a GitHub token. Private reviews use access you already have. An existing GitHub connection is optional.

The skill is designed to recommend changes without editing repositories, changing pins, opening pull requests, or publishing files. Your host's tool permissions determine what actions are technically possible. Use read-only permissions if you need to enforce that boundary.

The review assesses presentation and supporting evidence. It does not establish code correctness, security, measured business results, or hiring outcomes. The [privacy notice](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/plugins/github-portfolio-builder/PRIVACY.md) explains how the host and requested sites process review content.

## Help and details

Maintained by Rachael Quisel. [Ask a question or report a problem](https://github.com/RachaelQuisel/github-portfolio-builder/issues).

Read [how the review works](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/plugins/github-portfolio-builder/GitHub-Portfolio-Builder-HowItWorks-2026-10-03.md) or the [working instructions](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/plugins/github-portfolio-builder/skills/github-portfolio-builder/SKILL.md). Released under the [MIT license](https://github.com/RachaelQuisel/github-portfolio-builder/blob/main/LICENSE).
