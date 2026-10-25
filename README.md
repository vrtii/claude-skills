# Claude Skills

Agent skills for Claude (Claude Code, Claude.ai, Claude API) by [Dávid Sámoczi](https://samoczi.com).

## Plugins

| Plugin | Skills | What it does |
|---|---|---|
| `cv-review` | `cv-diagnoser` → `cv-recruiter` → `cv-hiring-manager` → `cv-rewriter` | Four-stage CV/resume review pipeline |

### cv-review pipeline

1. **cv-diagnoser** — structural, ATS and content audit; severity-ranked findings.
2. **cv-recruiter** — 6-second scan, keyword match against a job description, advance/reject verdict.
3. **cv-hiring-manager** — credibility of claims, impact evidence, red flags, likely interview questions.
4. **cv-rewriter** — rewrites summary, bullets and structure with before/after and rationale.

Ask for a *"full CV review"* to run all four in order, or call any stage on its own.
Tip: attach the target job description — stages 2–4 are much sharper with it.

## Install

### Claude Code (recommended)

```
/plugin marketplace add vrtii/claude-skills
/plugin install cv-review@samoczi-skills
```

### Claude Code (manual)

```bash
git clone https://github.com/vrtii/claude-skills.git
cp -r claude-skills/plugins/cv-review/skills/* ~/.claude/skills/
```

### Claude.ai

Zip each folder under `plugins/cv-review/skills/` separately and upload it in Settings → Capabilities → Skills.

## License

[Apache-2.0](LICENSE) — see [NOTICE](NOTICE).
