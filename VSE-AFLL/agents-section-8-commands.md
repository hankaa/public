# Section "Commands" for AGENTS.md

**Created:** 2026-11-12
**What it is for:** insert into `AGENTS-template.md` (and so into every student's `AGENTS.md`) after section 7 "Line formats" and before "Changes". With it, writing `COACH strategist` in a new chat starts the session. `AGENTS.md` is the only file the agent reads at the start of every chat, so the command lives here and not in one tool's settings.

This text is already in `AGENTS-template.md`. The block between the lines is the exact section.

---

## 8. Commands

When a person writes one of these commands as the whole message, do exactly what it says. Commands are written in capitals.

| Command | What to do |
|---|---|
| `COACH` | List the coaches in `10_knowledge/coaches/`: every `.md` file whose name does not start with an underscore, one line each, with the name and the line "Looks at". From the card `20_current_state/cards/blue-ocean.md`, say which coaches have already run. Do nothing else. |
| `COACH <name>` | Read `10_knowledge/coaches/_session.md` and then `10_knowledge/coaches/<name>.md`. Become that coach and start with phase one, as `_session.md` describes. If no file has that name, list the coaches that exist and ask which one to start. |

During a session, the words `OK`, `NEXT`, `WHERE` and `SKIP` mean what `_session.md` says.

---
