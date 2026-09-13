# Dev Project Stable Plugins

This release contains only the two stable Codex plugins:

- `dev-engineering`
- `dev-productivity`

The repository marketplace lists both plugins, while the archives under `dist/`
package each plugin with its own minimal marketplace so they can be distributed
and installed independently. Project notes, upstream source snapshots, evaluation
records, and other development documentation are intentionally excluded.

## Install from this worktree

```bash
codex plugin marketplace add /home/donk/plugins/dev-project-release
codex plugin add dev-engineering@dev-project-release
codex plugin add dev-productivity@dev-project-release
```

Either `codex plugin add` command may be run independently.

## Install from an archive

Extract one ZIP from `dist/` to a persistent directory, add the extracted root as
a marketplace, then install the plugin using the marketplace name embedded in the
archive:

```bash
codex plugin marketplace add /path/to/dev-engineering-<version>
codex plugin add dev-engineering@dev-engineering-dist
```

```bash
codex plugin marketplace add /path/to/dev-productivity-<version>
codex plugin add dev-productivity@dev-productivity-dist
```

Verify the result with `codex plugin list`. Start a new Codex conversation after
installing or updating so the plugin's skills are reloaded.
