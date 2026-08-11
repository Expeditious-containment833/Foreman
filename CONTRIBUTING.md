# Contributing to Foreman

Foreman is an authored playbook, not a community standard. It has a point of view, and that point of view is the product. A version of Foreman that accommodated every preference would be a worse tool than this one, because the thing it sells is decisiveness.

So contributions are welcome in the places where more input makes the playbook **more correct**, and closed in the places where more input would make it **less decisive**. This page says which is which, so nobody spends an evening on a change that was never going to land.

Every change is reviewed and merged by Turki Alshuaibi. Nothing lands without that.

## Most valuable thing you can send

**A failure the playbook did not intercept.** You ran a build, it went wrong, and Foreman never asked you the question that would have prevented it. That is worth more than a patch, because it changes what the playbook asks every future user.

Post it on the [meta issue](https://github.com/Turki-Sh/Foreman/issues/1):

- What you were building, in one line
- Which phase you were in, or "after shipping"
- What broke
- **What question would have prevented it**

That last line is the contribution. If it becomes a gate, a constraint, or a failure mode, you get credited in the changelog.

## Wanted, send a pull request

**Install paths for agents I cannot test.** `AGENTS.md` maps tools to the directory they read skills from. Those paths move, and I do not run every agent. If Foreman loads in Cursor, Windsurf, Codex, Copilot, Cline, Gemini CLI or anything else, and the documented path is wrong or missing, correct it. Say which version you tested on.

**Factual corrections.** A DNS instruction that no longer matches a registrar's panel. A host that changed its build settings. A dead link. A Lighthouse threshold that moved. Anything where the playbook states something that is no longer true.

**Bugs in the templates.** `assets/` ships a 404, a head block, a brand harness, robots.txt, sitemap.xml and llms.txt. If one of them is invalid, inaccessible, or wrong in a browser I did not check, fix it.

**Translations.** A second language for the skill is genuinely valuable and I cannot write most of them. Open an issue first so we agree on scope before you translate nine reference files.

## Not wanted, please open an issue instead

**New reference documents.** The playbook stays small on purpose. Nine references is already close to the limit of what an agent will load usefully. New material has to displace something.

**Changes to the seven phases or their gates.** The session flow is the design. If a gate is wrong, that is a conversation, not a patch.

**Options, alternatives, and "you could also".** This is the one that kills opinionated tools. A rule that offers three ways to do something is not a rule. If you disagree with a rule, tell me why it produced a bad result for you, with the build that proves it. That will move me. A PR adding a second option will not.

**Anything executable.** Foreman ships no scripts, no hooks, no MCP servers and no network calls, and that is a feature people rely on when deciding to trust it. CI enforces this.

## Before you open a pull request

The `validate` workflow runs on every pull request. It will fail if:

- The manifests disagree or drop a required field
- `SKILL.md` frontmatter is missing or the description exceeds the limit
- `SKILL.md` names a file that does not exist
- Anything executable appears under `plugins/`
- `dist/foreman.skill` has drifted from the source skill
- An em dash or en dash appears in the prose

That last one is a house style rule, not a moral position. Commas, colons and full stops.

If you change anything under `plugins/foreman/skills/foreman/`, rebuild the bundle in the same commit:

```
rm -f dist/foreman.skill
cd plugins/foreman/skills && zip -rq ../../../dist/foreman.skill foreman -x '*.DS_Store'
```

Keep pull requests to one concern. A branch that fixes a Windsurf path and rewrites the brief template will be asked to split.

## Writing style

The playbook is written to be run by an agent, not read by a person. Prose that a model has to wade through is a cost paid on every session.

- Plain verbs, sentence case, no filler.
- Do not justify a decision to the reader. If an ordering needs defending, the ordering is wrong.
- No em dashes.
- Specific beats clever. Numbers beat adjectives.

## Licence

Foreman is MIT. Contributions are accepted under the same licence, and the copyright notice travels with any copy. There is no contributor licence agreement to sign.

## Credit

Anything that changes the playbook gets its contributor named in `CHANGELOG.md` against the release it shipped in. If a failure report becomes a gate, that counts.
