# Verification and publication

## November 3, 2026

The source release is **1.1.8**. This release removes Oxford commas from the READMEs, release guide and skill instructions. The review behavior is unchanged. Release 1.1.7 added portfolio page output (`references/portfolio-page.md`, sample in `docs/sample-portfolio-page.html`).

Before this documentation release, the authenticated Claude publisher portal showed **1.1.3** at commit `8196f3112ad2b7f65c3b69c7144577adfab310a0` as approved after its security scan. The serving public version was **1.1.0** at `d54312ec485c2d2089e52c65e1269d2ea336dd2f`. The portal required an Anthropic reviewer to publish the update. That observation does not establish approval or publication of 1.1.6.

The [existing publisher record](https://claude.ai/directory/manage/plugins/611e353e-bed6-4959-8f32-d24f37881603) retains the same listing identity. Its publisher view requires owner access. The [repository marketplace](https://github.com/RachaelQuisel/github-portfolio-builder) is the source for the documented Claude Code installation commands.

This README was checked against the working skill and its review references, [GitHub's README guidance](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes), and [Claude Code's plugin installation guide](https://code.claude.com/docs/en/discover-plugins). The install-count statement below is supported by the inspected publisher dashboard. No hiring, performance, or business-result claim was added.

The package README is generated from the root README through `release-registry.json`. Edit the root README and run `python3 scripts/release_sync.py --write` to keep them identical.

## Directory install count

On November 3, 2026, the authenticated [Claude publisher Usage page](https://claude.ai/directory/manage/plugins/611e353e-bed6-4959-8f32-d24f37881603?tab=usage) reported **5,183 all-time installs**, with data through **November 1, 2026**. This is the basis for the README's one-sentence statement about over 5,000 installs. The page requires publisher access. Installs are not a measure of active users, endorsements, or portfolio outcomes.

## Earlier publication observations

The repository previously recorded a Marketplace partner-waitlist submission on October 5 through XRAY Automation. Acceptance was not confirmed. That partner program is separate from plugin installation and directory approval. On October 12, the inspected Claude organization could not find this submission. On October 16, publication remained unverified from that environment. The authenticated November 3 check above supersedes those access-limited observations.

Historical checks below were recorded October 3, 2026 against the local plugin package. They are not a verification of every later revision.

## Historical verification gap: October 16, 2026

At that check, the plugin manifest was version **1.1.0**. The recorded fresh-install test below covers **1.0.1**, not 1.1.0. A new installation and behavior test for 1.1.0 is still required. The audit environment did not have Claude Code, so it did not run `claude plugin validate` or an installation test.

The October 16 repository inspection confirmed parseable plugin and marketplace JSON, matching package names, a resolvable marketplace package path, one SKILL.md and the referenced icon file. These are structural checks only, not a security scan, live behavior test or Anthropic approval.

The icon fix is committed at [021198c](https://github.com/RachaelQuisel/github-portfolio-builder/commit/021198ca0bbebc1ac530e42d701c39993fdf0f25). Its follow-up portal scan and approval remain unverified. The publisher portal requires access through the submitting account and organization.

## Historical checks

| Surface | Status | Evidence |
| --- | --- | --- |
| Claude Code marketplace manifest | Passed | `claude plugin validate .` |
| Claude Code plugin manifest | Passed | `claude plugin validate plugins/github-portfolio-builder` |
| Skill metadata | Passed | `quick_validate.py` with PyYAML |
| Claude Code repository reviews | Previously exercised | Two unrelated public repositories were reviewed during initial development. Re-run after material behavior changes. |
| Claude Code profile review | Passed local behavior check | With the local plugin loaded, a review of an unrelated public profile (`jvns`) identified the profile README and pins, sampled relevant repositories, linked file-specific claims, labeled role uncertainty and stated coverage limits. No write action was requested or observed. |
| Empty or ambiguous public profile | Passed local behavior check | A separate public username with no visible work produced a scope and identity gap instead of invented portfolio recommendations. |
| Claude chat and Cowork | Not tested | A Claude Code result does not establish behavior on these surfaces. |
| Fresh install from the public marketplace | Passed | Using an isolated `CLAUDE_CONFIG_DIR`, `claude plugin marketplace add RachaelQuisel/github-portfolio-builder` and `claude plugin install github-portfolio-builder@github-portfolio-builder` succeeded. `claude plugin details` showed version 1.0.1 and one skill. |
| Claude Directory | Listing unverified | Portal validation, source connection, disclosures, submission, review and visible listing are separate checks. |

These checks establish package validity and sampled review behavior. They do not enforce read-only access. The host controls tool permissions, and a read-only GitHub MCP is optional.

Public GitHub targets require no test account or token. The three public URLs in the README provide sample targets for directory reviewers. Private-repository behavior depends on the reviewer's own host permissions and is outside these checks.
