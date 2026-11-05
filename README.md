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
| gsc-analysis | You read Search Console data and want the numbers to be right. | [younesbenallal/seo-skills](https://github.com/younesbenallal/seo-skills/tree/main/gsc-analysis) (install from there) |
| technical-audit | You want a technical audit that keeps only checks that move rankings. | [younesbenallal/seo-skills](https://github.com/younesbenallal/seo-skills/tree/main/technical-audit) (install from there) |

The last two have no license, so they are not copied here. Install them from the author's repo.

## Install

```bash
# the four skills in this repo
npx skills add marekreyo/seo-skills

# the two from the original author
npx skills add https://github.com/younesbenallal/seo-skills --skill gsc-analysis
npx skills add https://github.com/younesbenallal/seo-skills --skill technical-audit
```

Or copy a folder from `skills/` into `~/.claude/skills/`.

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
