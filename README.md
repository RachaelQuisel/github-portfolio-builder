# GitHub Portfolio Builder

A review-focused plugin for assessing a GitHub profile or repository as a professional portfolio. It gives a short assessment, sourced and prioritized improvements, and a few worthwhile additions when they can be shared responsibly.

The reviewer can check current public GitHub pages without a GitHub token. A private target requires access you already have. The skill instructs Claude to review without editing GitHub, changing pins, opening pull requests, or publishing files. Those instructions are not a technical permission boundary; the host's tool permissions control what Claude can do.

## Claude Marketplace and Directory status

Status updated on **October 12, 2026**:

- **Marketplace partner waitlist:** submitted on **October 5, 2026**, through XRAY Automation. Submission confirmation was received; partner-program acceptance has not been confirmed.
- **Claude Directory:** current review and public-listing status remain **unverified**. The [earlier directory review record](https://claude.ai/directory/manage/plugins/611e353e-bed6-4959-8f32-d24f37881603) was not accessible from the current organization on October 12: “That submission wasn’t found in this organization.” This does not establish rejection or removal; the original submitting account or organization may be required.
- **Icon review follow-up:** commit [`021198c`](https://github.com/RachaelQuisel/github-portfolio-builder/commit/021198ca0bbebc1ac530e42d701c39993fdf0f25) was pushed to address the earlier icon-inspection hold. A follow-up scan result and Anthropic approval have not been verified.

The [Marketplace partner waitlist](https://claude.com/marketplace-partners), Claude Code installation and Claude Directory review are separate stages. These are dated observations, not a claim that the plugin is publicly listed.

### Evidence audit: October 16, 2026

- **Partner waitlist:** Submission confirmation recorded for 2026-10-05, through XRAY Automation. This is retained repository evidence, not a newly inspected confirmation receipt.
- **Plugin directory:** Icon fix pushed; re-scan and review outcome unverified.
- **Approved:** Unverified. **Publicly listed:** Unverified. No verified public listing URL is recorded.
- **Verification limit:** The publisher portal requires sign-in. Public searches and the connected mailbox search did not establish approval; missing results are not proof of rejection or non-publication.
- **Next action:** Open the existing submission in the original submitting Claude account and organization; record its current decision and any public listing URL.

The [partner waitlist](https://claude.com/marketplace-partners) is for Claude-powered enterprise products. It is separate from plugin-directory review and GitHub marketplace installation. A waitlist application is not directory approval.


## Install in Claude Code

```sh
claude plugin marketplace add RachaelQuisel/github-portfolio-builder
claude plugin install github-portfolio-builder@github-portfolio-builder
```

Then invoke `/github-portfolio-builder:github-portfolio-builder`. Supply a GitHub profile or repository URL. If details are missing, the plugin asks up to three questions about the target, intended audience, and review focus. It waits for required answers and remembers supplied choices. Claude Directory review and publication are separate from marketplace installation; see [submission status](#claude-marketplace-and-directory-status).

## Use

Give Claude a public profile or repository URL and invoke the skill:

```text
/github-portfolio-builder:github-portfolio-builder https://github.com/OWNER/REPOSITORY
```

You can also just ask: “Review my GitHub profile as a professional portfolio and tell me the most valuable improvements.”

### Example requests

- “Review `https://github.com/jvns` as a public portfolio. Check the visible pins and a small sample of original projects, then give only evidence-backed improvements.”
- “Review `https://github.com/github/docs` for how clearly its README explains the project, intended users, and reuse path. Link each finding to a current source.”
- “Review `https://github.com/pallets/flask` as a repository portfolio piece. What does its public presentation establish, and what remains unverified?”

The review links to evidence, separates verified facts from repository claims and inferences, and identifies gaps when a source cannot be inspected. Code correctness and security auditing are separate tasks.

See a [finished example review](docs/example-review.md) of a public Airtable webinar repository.
It shows the assessment, one evidence-backed priority, and the limits a reviewer should state.

## Data and permissions

This package contains a skill and reference text, with no bundled executable, hook, MCP server, analytics endpoint, or telemetry. The skill asks Claude to inspect the target profile or repository and the limited linked sources needed to support a finding. Claude and any tools you enable process the URLs and content under their own terms and account settings. A private target can expose private content to the Claude session, so review its permissions before use.

The review may request public GitHub pages or APIs and visit websites or demos linked from the target. Those requests disclose the requested URL and normal request metadata to GitHub or the linked site's operator. The skill does not call for uploading private repository content to a linked site.

For a stricter review session in Claude Code, use host-level tool restrictions or a read-only GitHub MCP configuration. The plugin's prose alone cannot prevent writes when the host gives Claude write-capable tools. The plugin does not require a token for a public target.

## Distribution status

The GitHub repository is public and installable as a Claude Code marketplace. See [Claude Marketplace and Directory status](#claude-marketplace-and-directory-status) for the confirmed waitlist submission and the limits of the latest Directory check. Public Directory publication has not been verified.

See [verification status](docs/verification.md) for the surfaces and behavior checked so far. Claude chat and Cowork have not yet been tested.
See the [plugin privacy notice](plugins/github-portfolio-builder/PRIVACY.md) for data handling details.

## Optional GitHub MCP

The plugin works without an MCP for public reviews. If you already use [GitHub's official MCP server](https://github.com/github/github-mcp-server), its read tools can make repository file, tree, release, and profile checks more reliable. Configure it in [read-only mode](https://github.com/github/github-mcp-server/blob/main/docs/server-configuration.md) and enable only the toolsets you need, such as `repos`, `users`, and `git`. GitHub publishes a [setup guide for Claude](https://github.com/github/github-mcp-server/blob/main/docs/installation-guides/install-claude.md). The plugin does not install the server or require a token for public repositories; its skill instructs Claude not to call write tools.

A browser remains useful for checking the visible profile, pins, rendered README, and linked demos; repository metadata alone cannot establish how those pages appear to a visitor.

## Package

The marketplace manifest is at `.claude-plugin/marketplace.json`. It points to the plugin and skill under `plugins/github-portfolio-builder/`.

Read [how it works](plugins/github-portfolio-builder/GitHub-Portfolio-Builder-HowItWorks-2026-10-03.md) for the complete review process.
