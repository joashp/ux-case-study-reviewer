# UX Case Study Reviewer: a Claude / Codex skill

A skill that sharpens UX and product design case studies using named "prompt codes" (`/challenge`, `/hm`, `/why`, `/audit`, and so on). Each code is one specific critique or rewrite lens, so you get pointed feedback instead of a vague "here are some thoughts".

<img width="800" height="500" alt="ux-case-study-reviewer-claude-skill" src="https://github.com/user-attachments/assets/71b3ece5-d18b-40fc-b974-9438c4611fc7" />

## Install

```bash
npx skills@latest add joashp/ux-case-study-reviewer
```

This installs the skill into your agent's skills folder (Claude Code, Codex and other supported agents). The CLI is interactive and lets you pick the agents and scope.

### Manual install

If you'd rather copy the folder yourself, clone the repo and copy `skills/ux-case-study-reviewer`:

| Tool | Destination |
|---|---|
| Claude Code (all projects) | `~/.claude/skills/` |
| Claude Code (one project) | `.claude/skills/` |
| Codex | `~/.codex/skills/` (the path can vary by version, so check its docs) |
| Claude desktop / claude.ai | zip the folder with the folder itself at the zip root, then upload under Settings → Capabilities → Skills |

```bash
git clone https://github.com/joashp/ux-case-study-reviewer.git
cp -R ux-case-study-reviewer/skills/ux-case-study-reviewer ~/.claude/skills/
```

Restart your agent afterwards. If your Codex version has no skills support, paste the body of `SKILL.md` (everything below the frontmatter) into an `AGENTS.md` at your repo root. You lose automatic triggering but keep the behavior.

## Repo layout

```
ux-case-study-reviewer/
├── README.md
└── skills/
    └── ux-case-study-reviewer/
        ├── SKILL.md        # frontmatter + the six codes
        └── references/
            ├── examples.md                   # one sample output per code
            ├── metrics-by-project-type.md    # used by /proof
            └── writing-principles.md         # loaded only for general feedback
```

The skill is a `SKILL.md` plus three reference files. `SKILL.md` says when to read each: `examples.md` before any response, `metrics-by-project-type.md` for `/proof`, and `writing-principles.md` when no code is named. Install the whole folder, because the reference files need to travel with it.

## How a skill works

1. At startup the agent loads only the `name` and `description` from the frontmatter.
2. When your request matches the description, the agent loads the full `SKILL.md` body.
3. The description is the trigger. It lists the codes and the situations (pasting case study text, asking for a critique, typing `/challenge`) so the skill fires even if you never name it.

## Usage

Paste a case study section and invoke a code:

```
/challenge  <paste your problem statement>
/why  <paste a design decision>
/tight <paste a long section>
```

You can also type the code alone after pasting text, or ask in plain language ("poke holes in this", "make this shorter") and the skill picks a code.

### Codes

| Code | What it does |
|---|---|
| `/challenge` | Devil's advocate attack on the logic with no softening, then a steelman of the rejected alternative |
| `/audit` | Grades the previous response for weak spots and guesses (follows another code) |
| `/hm` | Hiring-manager screen: 3 rejection reasons and 2 reasons to interview, what sticks after a 30-second skim, and gaps an outsider would hit |
| `/why` | Step-by-step reasoning with hidden assumptions, then 5 rounds of "why" |
| `/proof` | Finds missing quantitative evidence and suggests metrics |
| `/tight` | Rewrite that cuts length, removes buzzwords, and ends sentences on results |

### Recommended full pass

`/why` → `/challenge` → `/hm` → `/audit`. For a quick pass, `/challenge` + `/audit`.

The skill never stacks more than two codes per response unless asked.

## Modifying the skill

- Prefer extending an existing code over adding a new one. If you do add a code, add it to the table, the "Choosing a code" list, and the `description`.
- Keep `name` identical to the folder name.
- Keep the description specific. Include the phrases you actually type.

## Testing it

1. Paste a short, flawed case study paragraph.
2. Run `/challenge`. Expect blunt pushback with no praise first.
3. Run `/audit`. Expect a self-grade of the `/challenge` response.
4. Ask "help me improve this" with no code. Expect a question about where you are in the process, or a `/challenge` + `/audit` default.

## Limits

Built for case study and portfolio writing only. It is not for building the portfolio site or for general writing feedback.
