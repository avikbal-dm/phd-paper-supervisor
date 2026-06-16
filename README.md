# PhD Paper Supervisor

A Claude Agent Skill that turns a rough research idea into a published, citable paper. It acts as a demanding but supportive PhD supervisor: it interrogates your contribution until it is clear, holds every claim to a real evidence standard, and walks the paper all the way to a DOI and an audience.

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Claude Agent Skill](https://img.shields.io/badge/Claude-Agent%20Skill-da7756)
![Status](https://img.shields.io/badge/status-stable-brightgreen)

## Why this exists

Most research drafts fail for the same handful of reasons. They name a framework without explaining the mechanism behind it. They cite a statistic with no traced primary source. They dress up a summary as a contribution. They would not survive one hostile reviewer.

This skill is built to catch those failures before you ship. It runs your paper through a fixed pipeline with honest gates, refuses to wave thin work through, and verifies claims instead of asserting from memory. The result is work that holds up in front of a real reviewer and earns a citation.

It is tuned for marketing, SEO, AI search, analytics, and B2B strategy research, but the discipline applies to any field where evidence quality decides whether the paper lives or dies.

## What it does

The supervisor takes a paper through six phases, each with a question you have to answer honestly before moving on.

1. **Define the contribution.** Gate: what is actually new here? If the honest answer is "a good summary," it stops you.
2. **Source discovery.** A literature tool gives a starting pool, never the final bibliography.
3. **Deep research and verification.** Find the primary study behind every load-bearing claim, pull the real numbers and method, and grade each source into three evidence tiers.
4. **Build the argument.** Lead with mechanism, give every framework element a definition, evidence, a worked example, and a measurable signal, then convert it into falsifiable propositions.
5. **Write to standard.** Apply your anti-AI writing voice and synthesis discipline, and carry the target venue's house style.
6. **The reviewer pass.** Gate: would this survive review? Attack the weakest claim, then fix it.

After the manuscript is done, a publishing playbook steers it to a free DOI on the right preprint server (SSRN, Zenodo, Preprints.org, OSF, arXiv), then to distribution that doubles as a citation surface for your own work.

It also pushes you to publish as a connected series rather than one-offs, so each paper raises the authority of the next.

## What's in this repo

```
phd-paper-supervisor/
├── README.md                      <- you are here
├── LICENSE                        <- MIT
├── phd-paper-supervisor/
│   └── SKILL.md                   <- the skill itself
└── phd-paper-supervisor.skill     <- zipped bundle, ready to upload to Claude.ai
```

The README lives at the repo root and the skill stays in its own folder with `SKILL.md`. That is the structure Claude expects.

## Install

Pick the path that matches how you use Claude. Full details are in the [official Agent Skills docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview).

### Claude.ai (web or desktop app)

1. Download `phd-paper-supervisor.skill` from this repo, or zip the `phd-paper-supervisor/` folder yourself.
2. Open **Settings > Capabilities > Skills**.
3. Upload the file. The skill loads on your next message.

### Claude Code or Claude Desktop

Copy the skill folder into your skills directory.

```bash
# Personal: available across all projects
git clone https://github.com/YOUR-USERNAME/phd-paper-supervisor.git
cp -r phd-paper-supervisor/phd-paper-supervisor ~/.claude/skills/

# Project-scoped: committed with a specific repo
cp -r phd-paper-supervisor/phd-paper-supervisor .claude/skills/
```

Start a new session. Confirm the folder sits directly inside `skills/` with `SKILL.md` at its top level, not nested an extra level deep.

### Claude Code plugin marketplace

If you publish this repo as a marketplace, others can install it in two lines.

```bash
/plugin marketplace add YOUR-USERNAME/phd-paper-supervisor
/plugin install phd-paper-supervisor@YOUR-MARKETPLACE-NAME
```

## How to use it

Once installed, the skill triggers on its own when you bring up a paper. You can also call it directly. A few prompts that fire it:

- "Help me turn this framework into a publishable paper."
- "Is this draft rigorous enough to survive peer review?"
- "Find the primary source behind every statistic in this section."
- "Get this preprint a DOI and tell me where to post it."

Expect the supervisor to ask sharpening questions first, end each phase with one clear next action, and tell you plainly where the paper is still weak.

## Companion skills

The skill is stronger when paired with two others, if you have them installed:

- `anti-ai-writing-style-avikbal` for the writing voice.
- `research-synthesis` for evidence handling.

It works fine on its own without them.

## A note on trust

Treat any skill the way you would treat code you are about to run. Review `SKILL.md` before you install, and only use skills from sources you trust. This one is read-only guidance and a workflow. It does not ship scripts.

## Author

Avik Bal is a B2B digital marketing practitioner specializing in web architecture, SEO, content strategy, and marketing analytics. He has helped enterprise software, fintech, and technology companies drive growth through scalable digital marketing programs. Avik is the author of *CITED: The Growth Operating System for AI Search*.

### Find Avik

- LinkedIn: https://www.linkedin.com/in/avikbal/
- YouTube: https://www.youtube.com/@avik-bal
- Udemy: https://www.udemy.com/user/avik-bal/
- ResearchGate: https://www.researchgate.net/profile/Avik-Bal
- GitHub: https://github.com/avikbal-dm
- Amazon author page: https://www.amazon.in/stores/AVIK-BAL/author/B072Q716KM


## Contributing

Issues and pull requests are welcome. If you extend the pipeline or add a venue to the publishing playbook, open a PR and explain the reasoning behind the change.

## License

Released under the MIT License. See [LICENSE](LICENSE). Keep the attribution if you adapt it.
