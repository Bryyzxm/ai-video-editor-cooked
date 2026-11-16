# Updating the kembar editor

This checkout develops the editor and the hosted application. Its remotes are:

- `origin`: `https://github.com/Bryyzxm/ai-video-editor-cooked.git` (our fork).
- `upstream`: `https://github.com/nextwork-projects/ai-video-editor-cooked.git` (NextWork).

## Landing page ownership

`Bryyzxm/kembar-site` is the source of truth for the public landing page. Its
`main` branch is documented as connected to the Cloudflare Worker `kembar` at
`https://kembar.web.id`; its `wrangler.toml` serves `site/`.
The local checkout is `/Users/bryyzxm/kembar-site`.

The `site/` and `brand/` directories here are historical copies used during the
initial development. Make landing page changes in `kembar-site`. Do not merge
that repository's history into this repository, automatically copy this `site/`
over it, or attach the editor fork to the existing landing page deployment.
Any future transfer of individual changes must compare both versions first.

On 2026-11-16, the working copies of shared `site/` files were byte-identical.
`kembar-site` additionally contained `site/robots.txt` and `site/sitemap.xml`.
The fork setup did not change the landing page repository or its deployment.

## Update procedure

1. Inspect `git status --short`. Review and commit pending work before merging;
   include intended new files explicitly and keep credentials and local runtime
   files out of commits.
2. Run `git fetch upstream --prune` and
   `git log --oneline HEAD..upstream/main`. Empty output means there is no update
   to merge.
3. When updates exist, create a backup with a unique name, such as
   `git branch backup/before-update-YYYYMMDD-HHMMSS`. This preserves committed
   work only; it does not back up uncommitted files.
4. Inspect `git diff --stat HEAD...upstream/main`, then
   `git merge upstream/main`. Resolve overlapping changes while preserving the
   kembar customizations. If upstream introduces `site/`, `brand/`, or deployment
   changes, inspect them explicitly; the production landing page remains owned
   by `kembar-site`.
5. Run `python3 tests/check_plugins.py` and `bash tests/demos.sh` with the Python
   environment containing the editor dependencies (set `PY` if necessary).
6. After checks pass, push to the fork with `git push origin main`.

Avoid force pushes and resets when incorporating upstream updates. Pushes to
this fork are separate from pushes to the landing page repository.

## Fork setup verification (2026-11-16)

The initial fork snapshot preserves existing local work; no upstream merge was
needed. It is a backup of development state, not a release with passing checks.

- `git diff --check`: passed for the tracked working changes.
- Landing page and brand: all 45 pre-sync file checksums preserved; the separate
  `kembar-site` checkout remained clean at `467a0742f55cead3119edbee8818306a45f49c49`.
- `tests/check_plugins.py`: 182 existing em-dash style violations in BMad files,
  planning outputs, and `brand/README.md`. The AGENTS/GEMINI consistency check
  passes after both copies received the repository ownership instructions.
- `tests/demos.sh`: failed at `home.py demo` on its skill-list assertion with
  installed skills visible. The `plan.py demo` passed. The log also reported a
  preview division-by-zero warning and a skipped warm-up with a no-space error.
  These results need investigation before a release; they are not merge conflicts.
