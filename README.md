# Trump.skill

`Trump.skill` is a Codex skill that models Donald J. Trump's public rhetorical persona from publicly accessible materials.
It is designed for roleplay, speech rewriting, rhetoric analysis, and scene-specific dialogue generation.

This repository does **not** claim to reproduce a private or fully authentic person.
The skill focuses on observable public behavior across speeches, debates, interviews, campaign videos, statements, and archived social posts.

## What It Does

- Produces Trump-like first-person dialogue for public-facing scenes
- Rewrites neutral text into a Trump-like public style
- Explains Trump's rhetoric and behavior patterns in analysis mode
- Switches between rally, interview, debate, formal-address, and short-post modes
- Uses source-aware guidance instead of pretending to know private motives or undocumented facts

## Repository Structure

```text
.
├─ SKILL.md
├─ README.md
├─ agents/
│  └─ openai.yaml
└─ references/
   ├─ scene-playbooks.md
   ├─ source-index.md
   └─ style-profile.md
```

## Installation

Clone or copy this repository into your local Codex skills directory.

Windows example:

```powershell
git clone https://github.com/5udu/Trump.skill.git C:\Users\<you>\.codex\skills\川普
```

If the folder already exists, copy the repository contents into that folder instead.

## Usage

Invoke the skill explicitly with `$川普`.

Example prompts:

```text
Use $川普 to rewrite this campaign paragraph in Trump's public rally style.
```

```text
Use $川普 to answer this reporter question in a Trump-like interview voice.
```

```text
Use $川普 to analyze the rhetorical tactics in this debate exchange.
```

```text
Use $川普 to generate a short Truth Social-style post about border policy.
```

## Modes

The skill defaults to four task types:

- `roleplay`: public persona dialogue, speeches, and scene acting
- `rewrite`: convert neutral prose into a Trump-like public style
- `analysis`: explain tactics, framing, and persuasion patterns without roleplay
- `contrast`: compare Trump's likely framing with a neutral or opposing framing

It also tunes output by scene:

- `rally`
- `interview`
- `debate`
- `formal address`
- `social post`

## Source Base

The source map in [references/source-index.md](./references/source-index.md) draws from public materials such as:

- Trump White House archives
- American Presidency Project
- Commission on Presidential Debates transcripts
- TIME interview transcripts
- DonaldJTrump.com videos
- C-SPAN event video pages
- Archived Trump social-post indexes

These are used to distill style and behavior patterns rather than to reproduce long verbatim passages.

## Boundaries

- Public persona only
- No claim of literal identity
- No fabricated private memories or secret motives
- Date-sensitive stances should be grounded in documented public material when possible
- The goal is believable cadence and behavioral framing, not parody

## Notes For Maintainers

- Keep `SKILL.md` compact and procedural
- Add new source categories to `references/source-index.md`
- Put nuanced style additions in `references/style-profile.md`
- Put scene-specific rules in `references/scene-playbooks.md`
- Prefer pattern distillation over large quoted corpora
