# GitHub Portfolio Builder

See your GitHub the way a hiring manager does, before they do.

Point it at a profile or a repository. It inspects the public pages, tells you what the work actually proves to a visitor, and hands back up to five ranked changes with a direct evidence link behind each one.

- Labels every claim verified, reported, inferred, or unresolved, so your README's numbers never pass as checked facts
- Ranks up to five changes by what a prospective employer, collaborator, or user would learn from them
- Names up to three things worth adding, with the proof, permission, or attribution each one needs first
- States what it could not inspect instead of guessing past it
- Says plainly when a mature repository needs nothing, rather than manufacturing five priorities

How it works: give it a URL, read the Scope, Assessment, Priorities, and Limits sections, then fix the top item.

Invoke `/github-portfolio-builder:github-portfolio-builder` with a GitHub profile or repository URL.

## Read-only, end to end

The review changes nothing. It does not edit repositories, move profile pins, open issues or pull requests, or publish files. Public reviews need no GitHub token. For a private target, the reviewer uses only access you already have.

An already configured GitHub MCP can make repository metadata and file checks more reliable, but it is optional. The plugin never installs one and never uses write tools.

Before recommending that you publish anything, it treats case-study rights, third-party attribution, and sensitive details as prerequisites rather than afterthoughts.

## What this plugin reads and sends

It reads the public GitHub pages for the profile or repository you name, and nothing else. It sends no data to any service beyond the GitHub pages it reads, stores nothing, and has no endpoint of its own. There is no account to create and no token required for a public target. Every action is a read.

Installation instructions and source are in the [project repository](https://github.com/RachaelQuisel/github-portfolio-builder).
