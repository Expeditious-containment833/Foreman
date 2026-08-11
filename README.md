# Foreman

**A build playbook for shipping real websites with coding agents.**

[![Claude Code](https://img.shields.io/badge/Claude%20Code-plugin-D97757?style=flat&logo=claude&logoColor=white)](https://code.claude.com/docs/en/plugins)
[![Version](https://img.shields.io/badge/version-1.2.0-4C8EDA?style=flat&logo=semanticrelease&logoColor=white)](CHANGELOG.md)
[![Validate](https://img.shields.io/github/actions/workflow/status/Turki-Sh/Foreman/validate.yml?style=flat&logo=githubactions&logoColor=white&label=validate)](https://github.com/Turki-Sh/Foreman/actions/workflows/validate.yml)
[![Scripts](https://img.shields.io/badge/executable%20code-none-16A34A?style=flat&logo=markdown&logoColor=white)](#no-scripts)
[![License](https://img.shields.io/badge/license-MIT-3DA639?style=flat&logo=opensourceinitiative&logoColor=white)](LICENSE)
[![Author](https://img.shields.io/badge/by-Turki%20Alshuaibi-FFB400?style=flat)](https://turkialshuaibi.com/)

Coding agents removed the cost of writing a site. They did not remove the cost of deciding what it should be. So the internet now has thousands of sites that were built in an afternoon and look like each other: the same cream background, the same serif hero, the same three cards, the same accent, no domain, no metadata, no 404.

Foreman is the missing half. It turns the agent you are already talking to into a foreman: it interviews you, forces the decisions you would have delegated, locks a visual system before any code exists, writes one high-quality build brief, hands that brief to a coding agent, and then walks you through verification, DNS, and indexing until the thing is actually live.

You do not read Foreman. Your agent does.

## Install

**Claude Code**

Type both lines inside Claude Code, in this order.

```
/plugin marketplace add Turki-Sh/Foreman
/plugin install foreman@alshuaibi
```

The marketplace is named `alshuaibi`, so the install id is `foreman@alshuaibi`.

**Claude apps**

Download [`foreman.skill`](https://github.com/Turki-Sh/Foreman/raw/main/dist/foreman.skill) and upload it as a skill.

**Anything else that reads SKILL.md**

Copy `plugins/foreman/skills/foreman/` into your agent's skills directory.

## Then say

> help me build my portfolio

The agent should answer with two questions, not with code. That is the whole point.

## What changes

| | Without Foreman | With Foreman |
|---|---|---|
| First move | Generates a page | Asks what the site is for and who reads it |
| Copy | Written by the model | Extracted from you, with numbers |
| Design | Whatever the model defaults to | Locked tokens you chose from three variants |
| Scope | Everything it can think of | Explicit non-goals, written before the build |
| Done | It renders on your laptop | 375px, keyboard, Lighthouse, incognito, real 404 |
| Live | "Deployed" | DNS, SSL, sitemap, Open Graph, submitted and indexed |

## What is in the box

**Session flow.** Seven phases with gates, written for the agent, not for you. It does not advance until each gate is met.

**Nine references**, loaded only when the phase arrives: content interview, design direction, stack choice, the build brief, performance and accessibility, metadata and 404, bilingual and RTL, verify and ship, and a full worked example.

**Six fillable assets:** a brand harness with three variants, a head metadata block with Open Graph and JSON-LD, a custom 404, robots.txt, sitemap.xml, and llms.txt.

<a id="no-scripts"></a>
**No executable code.** Foreman ships no scripts, no hooks, no MCP servers, and no slash commands. It is markdown and fill-in-the-blank templates, so you can read every line of it before you trust it. The one `<script>` tag in the repo is a `type="application/ld+json"` structured data block inside `assets/head-metadata.html`: inert JSON meant for your site's `<head>`, not code that runs when you install this.

**See it run before you install it.** [The worked example](plugins/foreman/skills/foreman/references/worked-example.md) is a full session from the first question to a frozen brief, including the thing that went wrong afterwards.

## The three ideas it enforces

1. **The agent's ceiling is your brief.** Model choice is a rounding error next to the quality of the specification.
2. **Non-goals are the highest-leverage lines you will write.** Agents over-build by default, and one line prevents it.
3. **Decisions are yours, typing is theirs.** Delegate the implementation. Delegating the judgment is what produces the default look.

## Contributing

Issues welcome, especially failure modes the playbook does not intercept yet. If your build broke in a way Foreman should have caught, that is the most useful thing you can file.

## Author

Built by **Turki Alshuaibi**, AI engineer, from a session delivered to the KAUST Academy AI cohort on building and shipping with agents. Everything in it came from shipping, and from watching capable engineers get stuck in the same nine places, which are the nine listed at the end of the skill.

[![Portfolio](https://img.shields.io/badge/Portfolio-turkialshuaibi.com-FFB400?style=flat&logo=astro&logoColor=white)](https://turkialshuaibi.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/turki-alshuaibi)
[![GitHub](https://img.shields.io/badge/GitHub-Turki--Sh-181717?style=flat&logo=github&logoColor=white)](https://github.com/Turki-Sh)
[![Email](https://img.shields.io/badge/Email-turki@turkialshuaibi.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:turki@turkialshuaibi.com)

## License

MIT. Use it, fork it, teach with it. Attribution appreciated, not required.
