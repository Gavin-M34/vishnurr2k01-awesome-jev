# Contributing to Awesome Jev

Thanks for helping. This list only stays useful if the entries are accurate and the descriptions are honest, so most of what follows is about those two things.

By contributing, you agree that your contribution is released under [CC0 1.0](LICENSE) — dedicated to the public domain.

## Table of contents

- [What belongs here](#what-belongs-here)
- [What doesn't](#what-doesnt)
- [Entry format](#entry-format)
- [Writing a good description](#writing-a-good-description)
- [Where to put it](#where-to-put-it)
- [Adding a benchmark or eval](#adding-a-benchmark-or-eval)
- [Adding your own project](#adding-your-own-project)
- [Opening the pull request](#opening-the-pull-request)
- [Removing or fixing an entry](#removing-or-fixing-an-entry)
- [Maintainer notes](#maintainer-notes)

## What belongs here

A project qualifies if **both** of these are true:

1. It is actually built on Jev, or is clearly and explicitly inspired by Jev's interface (typed Choice / Score / Noul questions over a state).
2. Someone could plausibly use it, learn from it, or be entertained by it. Working toys and honest failures both count.

That includes SDKs and clients, production applications, demos and games, agent tooling and MCP servers, open reimplementations, benchmarks, cookbooks, and written analysis.

It does not need to be popular. A three-day-old repo with a clear README is a better entry than a starred repo that doesn't explain what it does. The ecosystem launched on 15 September 2026 — almost everything here is new.

## What doesn't

- **Anything that isn't really about Jev.** A general LLM tool with a Jev checkbox bolted on is not a Jev project.
- **Dead links, empty repos, and abandoned scaffolding.** If the README is a placeholder, it's too early.
- **Closed-source products with no technical substance.** A closed-source entry needs a public write-up with real detail — measurements, architecture, traces. [Yappy](https://yappy.biz/jev/) is in the list on those terms; a pricing page is not.
- **Paywalled or signup-walled content** presented as a resource.
- **Slopsquatted or typosquatted packages.** Report these instead; we'll note them.
- **AI-generated listicles and SEO content farms.** The Articles section is for people who measured something or explained something, not for pages that restate the launch post.
- **Anything implying a TypeSafe affiliation that doesn't exist.**

## Entry format

One project, one line:

```markdown
- [Name](https://url) - What it does, in a sentence.
```

Rules:

- A hyphen-minus and a single space between the link and the description: ` - `. Not an en dash, not a colon.
- Description starts with a capital letter and ends with a period.
- Keep it to one or two sentences. If it needs three, it probably needs a blog post instead.
- Use the project's own name and capitalisation.
- Link to the source repository where one exists, and put a live demo inside the description rather than in the main link.
- Wrap install commands, package names, function names and model ids in backticks.

Good:

```markdown
- [jev-go](https://github.com/Gaurav-Gosain/jev-go) - Go client for typed judgments and calibrated probabilities. `go get github.com/Gaurav-Gosain/jev-go`.
```

## Writing a good description

**Say what it does, not how good it is.** The reader decides whether it's good.

| Don't | Do |
| --- | --- |
| "A powerful, blazing-fast Jev library." | "Go client for typed judgments and calibrated probabilities." |
| "The best way to use Jev in the browser." | "Chrome extension: Jev judges whether a DOM element is an ad and removes it." |
| "Revolutionary AI-powered code review." | "Staged code-review workflow and local dashboard driven by focused Jev calls." |

Two more things that make an entry genuinely useful:

- **Say what Jev is doing specifically.** "Jev picks the operation and DOM element in one request" tells the reader far more than "uses Jev for browser automation."
- **Include real numbers when the project publishes them,** and attribute them. "Author-reported: 275–690 ms per decision" is useful. "Incredibly fast" is not.

Label anything unofficial as unofficial. Label official TypeSafe projects as official. Don't let the reader guess.

## Where to put it

| Section | For |
| --- | --- |
| **Official** | TypeSafe's own sites, docs, blog posts, and hosted routes |
| **Community** | Chat, social, and discussion venues |
| **SDKs & Clients** | Libraries whose job is to call the API from a language or framework |
| **Applications** | Things that put Jev in a real loop and do a job |
| **Demos & Games** | Toys, playgrounds, and game-playing agents |
| **Agent Tools** | MCP servers, coding-agent skills, plugins, and hooks |
| **Research & Open Models** | Reimplementations, open weights, and independent benchmarks |
| **Cookbooks** / **Patterns** | Official workflows and architectural recipes from the docs |
| **Articles** | Explainers, measurements, experiments, and news |

**Applications** is sub-grouped (browser & computer agents / search, code & data / infrastructure, guardrails & code quality / consumer & everything else). Pick the closest bucket; if it straddles two, pick the one matching its primary job.

Within a section, keep related projects near each other rather than enforcing alphabetical order. If a project belongs in two sections, list it in the better-fitting one and cross-reference from the other with "Same project as above."

## Adding a benchmark or eval

Benchmarks are the highest-value contributions to this list, and **results where Jev loses are explicitly welcome** — several are already in the list and called out in bold. A list that only shows wins is marketing.

For a benchmark entry to be useful, the linked project should make clear:

- What the task and dataset were, and how many examples.
- What Jev was compared against.
- Whether the raw responses and scoring code are published.
- What the author thinks the limits of the result are.

Say the direction of the result in the description. "Haiku wins accuracy here" is the single most useful clause in that entry.

## Adding your own project

Self-promotion is fine and expected — most of this ecosystem is people shipping things in public. Two asks:

1. Mention in the PR description that it's yours.
2. Describe it the way you'd describe someone else's. Apply the [description rules](#writing-a-good-description) to your own work especially strictly.

Please don't open a PR for a project you announced but haven't published.

## Opening the pull request

1. Fork, branch, and edit `README.md`.
2. **Update the table of contents** if you added or renamed a section.
3. **Check your links.** Every one of them, including the demo link inside the description.
4. Keep the PR focused — one project, or one coherent batch of related fixes. Don't mix an addition with a reformatting pass.
5. Title it plainly: `Add jev-foo` or `Fix dead link in Applications`.
6. In the body, say in a sentence why it belongs and note whether it's yours.

A quick self-check before you submit:

- [ ] Correct section, sensible position within it
- [ ] Format is `- [Name](url) - Description.` with a period at the end
- [ ] Description says what it does, with no marketing adjectives
- [ ] Official vs. unofficial is stated where it could be ambiguous
- [ ] Numbers are attributed to whoever reported them
- [ ] All links resolve
- [ ] TOC updated if needed

## Removing or fixing an entry

Open a PR or an issue for any of these — no ceremony needed:

- Dead link, moved repository, or renamed project
- Project abandoned or archived
- Description no longer matches what the project does
- A claim in the description turned out to be wrong
- An entry misrepresents its relationship to TypeSafe

If you're reporting a security problem with a listed package (a slopsquat, a leaked key, an exfiltration), open an issue and say so clearly. We'll remove first and discuss after.

## Maintainer notes

Guidelines for whoever is merging:

- **Accuracy beats completeness.** An entry with a wrong description is worse than a missing entry.
- **Don't gatekeep on stars.** This list has no star threshold; [MrJev/awesome-jev](https://github.com/MrJev/awesome-jev) exists for people who want one.
- **Edit descriptions freely on merge.** Trimming marketing language is not a reason to send a PR back — just fix it and say so in the merge comment.
- **Keep the explainer current.** Pricing, latency, rate limits, the 255-option cap, and the jaggedness link at the top of the README are all load-bearing for new readers and all subject to change during early access. Verify against [the official docs](https://docs.typesafe.ai/introduction) rather than against this file.
- **Re-check vendor numbers periodically,** and keep them labelled as vendor-reported.

## Questions

Open an issue. For questions about Jev itself rather than about this list, the [TypeSafe Discord](https://discord.gg/typesafe) and [docs](https://docs.typesafe.ai/introduction) are the better venue.
