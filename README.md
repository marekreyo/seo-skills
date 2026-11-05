# SEO skills for Claude

Six SEO skills for Claude Code and other agents that read `SKILL.md` files. Picked and maintained by [Orchory](https://orchory.com).

We read about 880 public SEO skills from 40 repos. Most of them were long checklists with invented scores, keyword density targets or paid link schemes. These six teach an agent a method: what to do first, what to check before it acts, and how to tell a real cause from a guess.

## The skills

| Skill | Use it when | Source |
|---|---|---|
| [seo-traffic-drop](skills/seo-traffic-drop) | Traffic or rankings fell. Proves the drop is real, dates it, finds its shape, and confirms the cause with a test that could have failed. | Thibaultbm/claude-seo-geo |
| [refresh-sprint](skills/refresh-sprint) | You refresh pages that already rank. Every heading must come from content the page already has. | RyanCraggs/claude-seo-skills |
| [link-building](skills/link-building) | You want backlinks. It first checks if links are the real problem. | coreyhaines31/marketingskills |
| [entity-seo](skills/entity-seo) | Google or AI answers do not connect your name, company and products. | saadsalmankhan/entity-seo-skill |
| gsc-analysis | You read Search Console data and want the numbers to be right. | [younesbenallal/seo-skills](https://github.com/younesbenallal/seo-skills/tree/main/gsc-analysis) (placeholder, installs on first use) |
| technical-audit | You want a technical audit that keeps only checks that move rankings. | [younesbenallal/seo-skills](https://github.com/younesbenallal/seo-skills/tree/main/technical-audit) (placeholder, installs on first use) |

The last two have no license, so we cannot copy them here. This repo ships a small placeholder for each that downloads the real skill on first use.

## Install

```bash
npx skills add marekreyo/seo-skills
```

Or by hand:

```bash
git clone https://github.com/marekreyo/seo-skills
cp -R seo-skills/skills/* ~/.claude/skills/
```

Restart Claude Code after you install. Type `/` and the skill names show in the list.

### The two linked skills install on first use

`gsc-analysis` and `technical-audit` come in as small placeholders. The first time you ask a Search Console or audit question, Claude asks if it may download the real skill from github.com/younesbenallal/seo-skills. Say yes, restart Claude Code, and ask again. The placeholder is replaced by the real skill.

To install them up front instead:

```bash
git clone --depth 1 https://github.com/younesbenallal/seo-skills younes-seo-skills
cp -R younes-seo-skills/gsc-analysis younes-seo-skills/technical-audit younes-seo-skills/docs ~/.claude/skills/
rm -rf younes-seo-skills
```

The `docs` folder is needed: both skills read a shared file from it.

## Use them

You do not have to name a skill. Describe the problem and Claude picks the right one. Or call it by name, for example `/seo-traffic-drop`.

| Skill | Say something like | Have this ready |
|---|---|---|
| seo-traffic-drop | "Our organic traffic fell 30% since March 10. Find out why." | Search Console exports (Pages, Queries, Dates) for a healthy period and the bad period, and a list of what you shipped |
| refresh-sprint | "Refresh these 12 URLs. Here is the scope." | The URLs, the scope (what the writer may and may not add), Search Console data |
| link-building | "Our pricing page is stuck at position 8. Do we need links?" | The target page and query, a backlink tool (Ahrefs, Semrush or DataForSEO) if you have one |
| entity-seo | "Google does not connect me to my company. Map my entities." | Your site, your profiles (LinkedIn, GitHub, company page) |
| gsc-analysis | "Analyse our Search Console data for the last 3 months." | A Search Console MCP connected to Claude |
| technical-audit | "Run a technical SEO audit on example.com." | Python 3. A Search Console MCP and Chrome help but are optional |

Start with `seo-traffic-drop` if you lost traffic, and with `gsc-analysis` if you only want to know where you stand.

## What we changed

We fixed the flaws we found before we added each skill: invented numbers, word-count floors, a vendor plug, and links to skills that are not in this repo. Each skill folder has a `CHANGES.md` with the exact edits and keeps its original license.

## Credits

- seo-traffic-drop: [Sorank](https://sorank.com) / [Thibaultbm/claude-seo-geo](https://github.com/Thibaultbm/claude-seo-geo), MIT
- refresh-sprint: [Ryan Craggs](https://github.com/RyanCraggs/claude-seo-skills), Apache-2.0
- link-building: [Corey Haines](https://github.com/coreyhaines31/marketingskills), MIT
- entity-seo: [Saad Salman](https://github.com/saadsalmankhan/entity-seo-skill), MIT
- gsc-analysis, technical-audit: [younesbenallal](https://github.com/younesbenallal/seo-skills)

## Who maintains this

[Orchory](https://orchory.com) is an agent that writes the pages ChatGPT, Perplexity and Google quote, in your own design. You approve every page.
