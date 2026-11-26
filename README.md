# claude-plugins

One Claude Code marketplace for all of my plugins. Each plugin lives in its own repo (with its own
tests, versions and releases); this repo only lists them.

## Install

```
/plugin marketplace add robbydf/claude-plugins
/plugin install skills@robbydf-plugins
/plugin install lightcraft@robbydf-plugins
/plugin install photocraft@robbydf-plugins
```

Install only the ones you want. To pick up new versions later: `/plugin marketplace update robbydf-plugins`.

## Plugins

| Plugin | Repo | What it does |
| --- | --- | --- |
| `skills` | [robbydf/skills](https://github.com/robbydf/skills) | Grilling interviews, design alternatives, throwaway prototypes, and review loops. |
| `lightcraft` | [robbydf/lightcraft-skills](https://github.com/robbydf/lightcraft-skills) | Cull, edit and export photos in LightCraft. |
| `photocraft` | [robbydf/photocraft-skills](https://github.com/robbydf/photocraft-skills) | Drive PhotoCraft and remove bystanders from photos. |

## Adding a plugin

Add an entry to `.claude-plugin/marketplace.json` with `"source": { "source": "github", "repo": "robbydf/<repo>" }`.

## Migrating from the per-repo marketplaces

The old marketplaces (`robbydf/skills`, `robbydf/lightcraft-skills`, `robbydf/photocraft-skills`) still
work, so nothing breaks. To move over, remove them (`/plugin marketplace remove <name>`), add this one,
and reinstall the plugins from it. Plugin names are unchanged, so skill names (`lightcraft:cull`, ...)
stay the same.
