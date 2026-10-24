# Megalinter Plugins

[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/refs/heads/master/img/badge/black-badge.json)](https://github.com/copier-org/copier)

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for setup, checks, and the contribution workflow.


## Agent instructions

Common guidance lives in `.config/capabilities/instructions/project.md`;
generated-project context and recommendations live in
`.config/capabilities/instructions/template.md`. Engineering, commit, AI co-author,
AI work-log, AI review, and tooling policies live in `.config/capabilities/rules/`. `AGENTS.md` contains the
rendered instructions, including when capa is not enabled.
The sources use level-two headings; generated provider files supply the level-one
heading. Local `.rumdl.toml` files validate the source fragments.


Edit these Markdown sources, then run `mise run ai-setup` to refresh capa-managed
provider files. Use `capa open` through mise to edit their declarations in the browser.
Keep editable sources outside `.agents/rules/`, which capa uses for generated output.






## Recommendations

### Configuration directory

If this project is a tool, CLI, or library that reads its own configuration,
support resolving it from a project-level `.config/` directory
(e.g. `.config/megalinter-plugins.toml`) alongside
any other locations you accept. It keeps consumers' repo roots tidy and follows
an emerging cross-ecosystem convention:

- <https://github.com/numtide/prj-spec> — project directory specification
- <https://dot-config.github.io/> — the `.config/` directory convention
- <https://github.com/pi0/config-dir> — reference implementation for resolving it
