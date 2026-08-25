# Git

Apply this when writing commit messages, naming branches, or doing any git
operations on my behalf.

## Commit messages

The subject line is an emoji, a space, then a short lowercase description in the
imperative mood. The emoji replaces the conventional-commit type word, so it is
`✨ add browser inference` and never `feat: ✨ add browser inference`.

| emoji | type     | use for                                             |
| ----- | -------- | --------------------------------------------------- |
| ✨    | feat     | new features or capabilities                        |
| 🎨    | ui       | visual and layout changes                           |
| 🐛    | fix      | bug fixes                                           |
| 📝    | docs     | documentation, READMEs, comments                    |
| ♻️    | refactor | restructuring without behavior change               |
| 🧩    | misc     | anything that doesn't fit the other types           |
| ✅    | test     | adding or fixing tests                              |
| 🔧    | chore    | config, tooling, dependencies, CI                   |

Examples of good subject lines:

```
✨ add CEM planner for action search
🐛 handle empty retriever results
📝 explain why inference runs in the browser
🔧 pin onnxruntime-web version
```

- Keep the subject under ~60 characters. Add a body only when the why isn't
  obvious from the diff, as short plain sentences.
- One logical change per commit. Don't bundle a refactor with a feature.
- Pick the type by the dominant change. A feature that also touches docs is
  still ✨.

## Branches and history

- Branch names are short kebab-case, optionally with a type prefix, like
  `fix/empty-retriever` or `browser-inference`.
- Never force-push shared branches. Force-pushing my own feature branch after a
  rebase is fine.
- Don't commit or push unless I asked for it. Never commit secrets, `.env`
  files, or large generated artifacts.
