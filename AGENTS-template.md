---
title: AGENTS.md, a guide for AI and for people
owner: <first and last name>
area: rules
source: template version
valid_until: <YYYY-MM-DD, one year from the last revision>
status: draft
last_change: <YYYY-MM-DD (who)>
---

# AGENTS.md – a guide for AI and for people (read this first)

**Template, version 1.0** | November 2026 | Adam Le Hanka, trpAIzlíci s.r.o.

> **For the person adopting this template. AI ignores this block; after you edit the file, delete it together with the line above.**
>
> - This is a general version of the file. It assumes no particular field and no particular tool. It fits any folder where material is collected and work is produced from it: a project, a team's agenda, a knowledge base, personal notes.
> - Replace everything in `<angle brackets>` with your own details. Delete what does not apply. Section 1 matters most: without it, AI does not know what the folder is for.
> - Rename the file to `AGENTS.md` and put it in the root of the folder (a SharePoint library, a shared folder, a repository).
> - Claude Code, Cursor, and GitHub Copilot load a file with this name on their own. Microsoft 365 Copilot does not. Paste the text into the agent's instructions, or add the file to the agent's sources and point to it from the instructions. Try both, and keep whichever works better for you.
> - Keep it short. A rule belongs here when it applies to everyone working in the folder, and when a new colleague would need it on the first day.
> - After the first edit, set `status` in the header to `valid`, and fill in the owner and the revision date.

## 1. What this folder is for

- **Purpose:** `<one to three sentences: what is done here, and for whom>`
- **Who works here:** `<team, roles, or names>`
- **What is tracked here:** `<things that have a state and a history, for example projects, suppliers, products, cases, requests>`. Below, these are called **topics**.
- **What finished work is:** `<which outputs leave this folder, and who receives them>`
- **What does not belong here:** `<what is handled elsewhere, and where>`

## 2. Folder structure

```
<folder-name>/
├── AGENTS.md            # this guide
├── 00_materials/        # raw material, as it arrived. Append only
├── 10_knowledge/        # what holds over the long term
├── 20_current_state/    # what holds now: topic cards, todo.md, waiting-on.md
├── 30_outputs/          # what leaves this folder
├── _archive/            # finished tasks and outdated files. Nothing is deleted
└── processed.md         # which material has been processed, and where it was written
```

| Where | What belongs there |
|---|---|
| `00_materials/<kind>/` | Material sorted by kind: `<for example emails, minutes, documents, notes>`. One item of material = one file. |
| `10_knowledge/decisions.md` | What holds, who decided it, when, and how we know. |
| `10_knowledge/<name>.md` | Knowledge by topic, not by material: `<for example a glossary, procedures, definitions, templates>`. |
| `20_current_state/cards/<topic>.md` | Topic card: current state, people, risks and conflicts, history. |
| `20_current_state/todo.md` | What we have to do. Open tasks only. |
| `20_current_state/waiting-on.md` | What we are waiting for from others. Open items only. |
| `30_outputs/` | Texts and files we are preparing or have already delivered. |
| `_archive/task-archive.md` | Finished and dropped tasks, and settled waits. |
| `_archive/` | Files that no longer hold: replaced versions of outputs, cards of closed topics. |

How work moves: new material → `00_materials` → processing into `10_knowledge` and `20_current_state` → a row in `processed.md` → `30_outputs` are written from the valid state.

### Naming

- Material: `YYYY-MM-DD_topic_short-description.md`, lowercase, no diacritics, words separated by hyphens.
- Outputs: `topic_what-it-is-vN.md`. A new version is a new file (`-v2`). Do not overwrite the old one.

## 3. Basic rules

1. **Material is not edited.** Things are only added to `00_materials`: no rewriting, no typo fixes, no deletion. Interpretation and context belong on the cards and in the decisions.
2. **Every fact has a source:** the material's filename without the extension, in backticks, for example `2026-10-01_topic_short-description`. The reference must point to a file that exists in `00_materials`. Do not write anything down without a source.
3. **Material is processed in full** (read long files in parts) and then gets a row in `processed.md`.
4. **Do not lose changes.** Strike the old value through and write the new one with its source: ~~3 Dec~~ → 10 Dec (`source`). Do not delete a decision that has been replaced. Mark it SUPERSEDED and point to the new one.
5. **A decision always has four things:** what holds, who decided, when, and the source. Anything nobody has agreed to yet is a DRAFT, not a decision.
6. **Promises and requests.** A promise of ours ("I'll send it", "we will deliver") is a task in `todo.md`. A request of ours to someone else is an item in `waiting-on.md`. A question we have not answered is a task in `todo.md`.
7. **Compare deadlines with today's date.** A task past its deadline is marked ❗ OVERDUE. A wait longer than `<14 days>` with no reply needs a task to chase it.
8. **Do not guess what you do not know.** A missing detail, a question with no answer, or a conflict nobody has decided goes into `todo.md` as `- [ ] GAP: … – topic – source`.
9. **Language:** `<English; exceptions, for example with whom and when another language is used>`

## 4. Archiving

`todo.md` and `waiting-on.md` contain only what is still open. Settled items move to the archive, so the working files stay short and the history is not lost.

1. **A finished or dropped task**, in the same step, is deleted from `todo.md` and appended to `_archive/task-archive.md`. Do not leave it in `todo.md` checked or struck through.
2. **A settled wait** (the reply came, or we are no longer waiting) is moved out of `waiting-on.md` the same way.
3. **An archive entry** says how it ended and where the result is. For a dropped task, write "dropped" and briefly why. Group entries by month, newest at the top.
4. **A file that no longer holds** (a replaced version of an output, the card of a closed topic, knowledge that no longer applies) is moved to `_archive/`, and its header is set to `status: stale`.
5. **Nothing in the archive is deleted, and nothing in it is rewritten.** The archive is not a source for the valid state: when the archive disagrees with a card or a decision, the card and the decision hold.
6. **Material is not archived.** It stays in `00_materials`, even after the topic is closed.

## 5. File header

Every file in `10_knowledge`, `20_current_state`, and `30_outputs` has a header. Material does not, because material is not edited. While working, compare `valid_until` with today's date. A file past that date, or one with status `stale`, is not a valid source. Say so in the output.

```
---
title: <name, as a person would say it>
owner: <name>
area: <area>
source: `<material-1>`, `<material-2>`
valid_until: <YYYY-MM-DD>
status: valid
last_change: <YYYY-MM-DD (who)>
---
```

| Field | What belongs there |
|---|---|
| `title` | The name of the file, as a person would say it. |
| `owner` | Who decides what in the file holds. |
| `area` | One of your areas: `<a list, for example decisions, cards, operations, output, rules>` |
| `source` | The main material. For cards and decisions, "on each fact" is enough. |
| `valid_until` | When to check the file again. Cards, `todo.md`, and `waiting-on.md`: `<3 months>` from the last change. Decisions and rules: `<12 months>`. An output: until it is delivered. |
| `status` | `draft`, `valid`, or `stale`. AI creates files in `30_outputs` as `draft`. Only a person switches them to `valid`. |
| `last_change` | The date, and who. Rewrite this on every edit. |

A file with no header: add one at the next edit, and record that in `processed.md`. In SharePoint, the same fields can also be library columns.

## 6. Actions outside the folder

`<Delete this section if, where you work, AI does not touch mail, the calendar, or other systems.>`

1. **Nothing leaves without a person.** Mail only as a draft. A write into another system only as a proposal. Send or confirm only when a person explicitly says so.
2. **Calendar:** a new event has `[HOLD]` in the title until the other party confirms it. Before creating it, check for clashes. Do not create a clashing time. Propose another one.
3. **Every action outside the folder leaves a trace inside the folder:** the draft or the event is a line in `todo.md` or `waiting-on.md` (what, where it is, source).
4. **Do not invent a detail you cannot find** (an address, a number, a name). Leave it empty, and write in `todo.md` what needs to be filled in.

## 7. Line formats

- todo: `- [ ] task – topic – source – deadline`
- waiting on: `- what – from whom – since when – source – status`
- processed: a table row `| material | topic | processed | written into |`
- archive: `- date – task or wait – topic – how it ended, where the result is`

## 8. Commands

When a person writes one of these commands as the whole message, do exactly what it says. Commands are written in capitals.

| Command | What to do |
|---|---|
| `COACH` | List the coaches in `10_knowledge/coaches/`: every `.md` file whose name does not start with an underscore, one line each, with the name and the line "Looks at". From the card `20_current_state/cards/blue-ocean.md`, say which coaches have already run. Do nothing else. |
| `COACH <name>` | Read `10_knowledge/coaches/_session.md` and then `10_knowledge/coaches/<name>.md`. Become that coach and start with phase one, as `_session.md` describes. If no file has that name, list the coaches that exist and ask which one to start. |

During a session, the words `OK`, `NEXT`, `WHERE` and `SKIP` mean what `_session.md` says.

## Changes

- `<YYYY-MM-DD – who – what – why>`
