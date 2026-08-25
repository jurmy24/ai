# ai

Rules and configuration for the AIs I work with (Claude Code, ChatGPT/Codex, Cursor, whatever comes next). One repo, one source of truth, so I never paste the same style guide into a third CLAUDE.md again.

## layout

```
rules/
  writing-style.md    how I want prose written (docs, READMEs, comments, articles)
  git.md              commit message format (emoji prefixes), branches, git conduct
  diagrams.md         architecture diagrams for research writeups (layout, shapes, colors)
```

Each rule is a single self-contained Markdown file. That is deliberate. A rule an AI can load with one file read or one URL fetch is a rule that actually gets used. Don't split a rule across files, and keep reference examples inside the rule they belong to.

## using this from any project

The point is to never copy these files into other repos. Three ways to hook it in, from most to least convenient.

### 1. Claude Code (global, works in every project)

Clone this repo once, anywhere:

```bash
git clone git@github.com:jurmy24/ai.git ~/ai
```

Then add one import line to `~/.claude/CLAUDE.md` (create the file if it doesn't exist):

```markdown
@~/ai/rules/writing-style.md
```

Claude Code inlines `@`-imported files into its context in every session, in every project on the machine. Add one line per rule you want always active. `git pull` in `~/ai` updates every project at once.

### 2. Any tool that reads AGENTS.md or a project rules file

For tools that only read per-project files (Codex, Cursor, etc.), the project file stays a one-liner that points here instead of containing the rules:

```markdown
Before writing any documentation or prose, read and follow ~/ai/rules/writing-style.md.
```

A symlink works too and never goes stale:

```bash
ln -s ~/ai/rules/writing-style.md .cursor/rules/writing-style.md
```

### 3. Any AI with web access (no clone at all)

If the repo is public, every rule has a stable raw URL:

```
https://raw.githubusercontent.com/jurmy24/ai/main/rules/writing-style.md
```

So in ChatGPT, claude.ai, or any agent with fetch access, one sentence is enough:

> Fetch https://raw.githubusercontent.com/jurmy24/ai/main/rules/writing-style.md and follow it when writing.

This is also the fallback on machines where I haven't cloned anything.

> **Note:** options 1 and 2 read from the local clone, so remember to `git pull` occasionally. Option 3 always sees the latest `main` but requires the repo to be public.

## writing a new rule

Keep the format of `rules/writing-style.md`:

- One topic per file, named `rules/<topic>.md`.
- Start with a sentence saying when the rule applies.
- Prefer short imperative bullets over prose about prose.
- Include verbatim examples of what "good" looks like. Examples constrain an AI far better than adjectives do.
- End examples with a sanity-check instruction (e.g. "remove wording more polished than these examples") so the AI self-edits against them.

## ideas for future rules

Things worth writing down once instead of re-explaining per session:

- `python.md`: uv over pip, ruff, type hints, project layout, test conventions.
- `typescript.md`: same for the JS side (package manager, formatter, framework defaults).
- `about-me.md`: who I am, what I know well, what to explain vs. assume. Lets the AI calibrate answers instead of guessing my level.
- `answering.md`: how I want questions answered (lead with the answer, state uncertainty, don't pad).
- `reviewing.md`: what I care about in code review, so AI reviews match my priorities instead of generic linting.
- `scaffolding.md`: defaults for new projects (license, .gitignore, CI, README skeleton).
- `secrets.md`: never commit keys, where env vars live, what counts as sensitive.
- `naming.md`: conventions for repos, branches, files, and variables I keep re-deciding.
