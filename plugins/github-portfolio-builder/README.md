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

## Review boundaries

The skill instructs Claude to suggest changes without editing repositories, moving profile pins, opening issues or pull requests, or publishing files. This is an instruction, not an enforced permission boundary. The host's enabled tools and permissions determine what Claude can actually access or change. Public reviews need no GitHub token. For a private target, use only access you already have.

An already configured GitHub MCP can make repository metadata and file checks more reliable, but it is optional. The package does not install one, and the skill instructs Claude to avoid write tools.

Before recommending that you publish anything, it treats case-study rights, third-party attribution, and sensitive details as prerequisites rather than afterthoughts.

## Data handling

The package contains instructions and reference text, with no bundled executable, hook, MCP server, or telemetry endpoint. The skill asks Claude to inspect the named target and a small set of linked sources when needed. Claude and any enabled browser, GitHub, or MCP tools handle that content under their own terms and settings. For stronger read-only behavior, configure host permissions and any optional GitHub MCP for read access only.

Installation instructions and source are in the [project repository](https://github.com/RachaelQuisel/github-portfolio-builder).
