# Verification status

Historical checks below were recorded October 3, 2026 against the local plugin package. They are not a verification of every later revision.

## Current verification gap: October 16, 2026

The current plugin manifest is version **1.1.0**. The recorded fresh-install test below covers **1.0.1**, not 1.1.0. A new installation and behavior test for 1.1.0 is still required. The audit environment did not have Claude Code, so it did not run `claude plugin validate` or an installation test.

The October 16 repository inspection confirmed parseable plugin and marketplace JSON, matching package names, a resolvable marketplace package path, one SKILL.md, and the referenced icon file. These are structural checks only, not a security scan, live behavior test, or Anthropic approval.

The icon fix is committed at [021198c](https://github.com/RachaelQuisel/github-portfolio-builder/commit/021198ca0bbebc1ac530e42d701c39993fdf0f25). Its follow-up portal scan and approval remain unverified. The publisher portal requires access through the submitting account and organization.

## Historical checks

| Surface | Status | Evidence |
| --- | --- | --- |
| Claude Code marketplace manifest | Passed | `claude plugin validate .` |
| Claude Code plugin manifest | Passed | `claude plugin validate plugins/github-portfolio-builder` |
| Skill metadata | Passed | `quick_validate.py` with PyYAML |
| Claude Code repository reviews | Previously exercised | Two unrelated public repositories were reviewed during initial development. Re-run after material behavior changes. |
| Claude Code profile review | Passed local behavior check | With the local plugin loaded, a review of an unrelated public profile (`jvns`) identified the profile README and pins, sampled relevant repositories, linked file-specific claims, labeled role uncertainty, and stated coverage limits. No write action was requested or observed. |
| Empty or ambiguous public profile | Passed local behavior check | A separate public username with no visible work produced a scope and identity gap instead of invented portfolio recommendations. |
| Claude chat and Cowork | Not tested | A Claude Code result does not establish behavior on these surfaces. |
| Fresh install from the public marketplace | Passed | Using an isolated `CLAUDE_CONFIG_DIR`, `claude plugin marketplace add RachaelQuisel/github-portfolio-builder` and `claude plugin install github-portfolio-builder@github-portfolio-builder` succeeded. `claude plugin details` showed version 1.0.1 and one skill. |
| Claude Directory | Listing unverified | Portal validation, source connection, disclosures, submission, review, and visible listing are separate checks. |

These checks establish package validity and sampled review behavior. They do not enforce read-only access. The host controls tool permissions, and a read-only GitHub MCP is optional.

Public GitHub targets require no test account or token. The three public URLs in the README provide sample targets for directory reviewers. Private-repository behavior depends on the reviewer's own host permissions and is outside these checks.
