# GitHub Portfolio Review

Review any GitHub profile or repository as professional portfolio evidence. The plugin inspects the public material you name, gives a concise assessment, and suggests a few specific improvements with direct source links. It separates checked facts from self-reported claims and names gaps when a page cannot be inspected.

The review is read-only. It does not change repositories, profile pins, issues, or pull requests. Public reviews need no GitHub token. An already configured GitHub MCP can help read repository metadata and files, but it is optional and the plugin never installs one or uses write tools. For private repositories, the reviewer uses only access you already have. Treat case-study rights, third-party attribution, and sensitive details as prerequisites before recommending a public upload.

The plugin contains one shared skill for Claude and Codex. In Claude, invoke `/github-portfolio-review:github-portfolio-review` with a GitHub profile or repository URL. In Codex, invoke `$github-portfolio-review` with the URL. Installation instructions and source are in the [project repository](https://github.com/RachaelQuisel/github-portfolio-review).
