# Lazy Second Brain Agent Instructions

## Start Here

1. `README.md`
2. `START_HERE.md`
3. `GUARDRAILS.md`
4. `handoff.md`

## Repo Role

This is a Paia `project` repo and public Obsidian vault starter for building a practical second brain with an LLM. Keep it small, beginner-friendly, and usable immediately after cloning into Obsidian.

## Operating Model

Agents should enter from chrollo at `/workspaces/chrollo`. Treat this repository as docs and starter-vault content: notes, setup guidance, guardrails, vault maps, and local handoff notes. Preserve Obsidian-friendly Markdown links and existing file names, including paths with spaces.

## Write Boundaries

Allowed when this repo is active:

- Root docs and starter-vault Markdown content.
- `.github/workflows/docs-checks.yml`.
- `paia.repo.json`.

Avoid unless explicitly requested:

- App scaffolding, package manifests, package locks, or generated verifier tooling.
- Private or personal vault content that does not belong in the public starter.
- Sibling repo edits without explicit elevation from chrollo.

## Verification

Run the smallest relevant set:

- `python3 -m json.tool paia.repo.json >/dev/null`
- `bash -lc 'shopt -s globstar nullglob; files=(**/*.json); for file in "${files[@]}"; do python3 -m json.tool "$file" >/dev/null; done'`
- `git diff --check`

No package verifier exists in this repo; do not add npm tooling just to create one.

## Handoff

Cross-repo resume state belongs in `/workspaces/chrollo/handoff.md` and `/workspaces/chrollo/handoff.index.json`.

Use this repo's `handoff.md` for local parking notes, repo-specific links, or a pointer back to chrollo.
