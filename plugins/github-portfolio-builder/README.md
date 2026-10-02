# GitHub Portfolio Builder

Review any GitHub profile or repository as professional portfolio evidence. The plugin inspects the public material you name, gives a concise assessment, and suggests a few specific improvements with direct source links. It separates checked facts from self-reported claims and names gaps when a page cannot be inspected.

The review is read-only. It does not change repositories, profile pins, issues, or pull requests. Public reviews need no GitHub token. An already configured GitHub MCP can help read repository metadata and files, but it is optional and the plugin never installs one or uses write tools. For private repositories, the reviewer uses only access you already have. Treat case-study rights, third-party attribution, and sensitive details as prerequisites before recommending a public upload.

Invoke `/github-portfolio-builder:github-portfolio-builder` with a GitHub profile or repository URL. The plugin reads only the public GitHub pages for the target you name. It sends no data anywhere else, stores nothing, and needs no token for a public target. Installation instructions and source are in the [project repository](https://github.com/RachaelQuisel/github-portfolio-builder).
