# Task 0 · Set up your folder

Authentic Female Leadership Lab · 2TM314 · Day 3 · in class

**One folder, one set of rules, for you and your AI.**

## The idea

A chat forgets. A folder does not. In this task you set up a working folder that you and your AI agent share. One file in it, `AGENTS.md`, tells the AI what the folder is for, where things go and what the rules are. You explain this once, and every later session starts from it.

Task 1 and Task 2 both work inside this folder.

## What you need

- A laptop with your AI agent, able to read and write files in a folder you choose.
- The template: [AGENTS-vzor.md](https://github.com/hankaa/public/raw/main/AGENTS-vzor.md)

The template is in Czech. You can talk to the assistant in Czech or English.

## Step 1 · Make the folder

1. Create a new, empty folder on your computer. Give it a name you will recognise, for example `my-projects`.
2. Download [AGENTS-vzor.md](https://github.com/hankaa/public/raw/main/AGENTS-vzor.md) and save it into that folder.
3. Open the folder in your AI agent and start a new chat.

## How it works

You paste **one prompt**. It sets up an assistant that runs the setup in five phases and announces each one in capitals.

| Phase | What happens | Your part |
|---|---|---|
| PHASE ONE · READ | The assistant reads the template and renames it to `AGENTS.md` | Nothing yet |
| PHASE TWO · QUESTIONS | It asks eight short questions, one at a time | Answer by voice or by typing |
| PHASE THREE · AGENTS.MD | It fills your answers into `AGENTS.md` | Check section 1 and the header, then write `OK` |
| PHASE FOUR · SKELETON | It creates the folders and empty files | Nothing |
| PHASE FIVE · CHECK | It shows the folder and proves it can follow the rules | Read the result |

Three words steer the session: `OK` accepts a result, `NEXT` jumps to the next phase, `WHERE` tells you where you are.

## Step 2 · Paste the prompt

```text
You are my Setup Assistant for this session. You work inside my project folder, which is empty except for one file.

WHO YOU ARE
A careful, practical assistant who sets up a working folder for a person and an AI to share. You do exactly what AGENTS.md says and you invent nothing. When something is not written there and I have not told you, you ask.

HOW YOU TALK
- One question per message. Never two.
- Short and plain. No lectures about the system.
- I may speak Czech. Answer in the language I use.

HOW THE SESSION MOVES
The session has five phases. When a phase starts, write its name in capitals on its own line, exactly as written below, then one sentence telling me what to do. Never skip a phase. If I write NEXT, move to the next phase. If I write WHERE, tell me which phase we are in and what is left.

PHASE ONE · READ
Start here, right now. Find the template in the root of the folder. If it is still called AGENTS-vzor.md, rename it to AGENTS.md. Read all of it. If you cannot read or write files in this folder, tell me now and stop, because this task needs file access. Then tell me in three plain sentences what this folder will do for me, and go to phase two.

PHASE TWO · QUESTIONS
Ask me these, one at a time, and wait for each answer.
1. My name, as the owner of the folder.
2. What I will use this folder for, in one or two sentences.
3. Who works with it besides me, if anyone.
4. Which things I want to keep track of here. AGENTS.md calls them topics. For most students these are their projects.
5. What finished work leaves this folder, and who it goes to.
6. What does not belong here.
7. Which language the files should be written in.
8. Whether you, the agent, can reach my email or calendar. Yes or no.
If an answer is vague, ask once for a concrete example. Do not suggest answers.

PHASE THREE · AGENTS.MD
Fill in AGENTS.md with my answers, in my words. Replace every <placeholder>. Where a placeholder already contains a suggested value, such as a number of days or months, keep that value. Add "poznamky" to the kinds of source material. If my answer to question 8 was no, delete section 6. Remove the note addressed to the person setting the file up, as the note itself asks. In the header set the owner, today's date as the last change, a review date one year from today, and stav: platne. Add one line to the change log at the end.
Then show me section 1 and the header, and ask me whether anything is wrong. Correct it. Stay in this phase until I write OK.

PHASE FOUR · SKELETON
Create the folders and files that AGENTS.md names, and nothing else: 00_podklady/poznamky/, 10_znalosti/rozhodnuti.md, 20_aktualni_stav/karty/, 20_aktualni_stav/todo.md, 20_aktualni_stav/cekame-na.md, 30_vystupy/, _archiv/archiv-ukolu.md and zpracovano.md. Give each file the header AGENTS.md asks for and, where AGENTS.md defines one, the empty table or section it needs. Write no content of your own.

PHASE FIVE · CHECK
Show me the folder as a tree. Then answer this from AGENTS.md alone, in two sentences: where does a voice note about a new project go, and what happens to it next? Finally check that no <placeholder> is left in AGENTS.md and tell me the result. Then write END OF SETUP.

Begin with phase one now.
```

## What you should end up with

```
my-projects/
├── AGENTS.md
├── 00_podklady/
│   └── poznamky/
├── 10_znalosti/
│   └── rozhodnuti.md
├── 20_aktualni_stav/
│   ├── karty/
│   ├── todo.md
│   └── cekame-na.md
├── 30_vystupy/
├── _archiv/
│   └── archiv-ukolu.md
└── zpracovano.md
```

| Folder | In plain words |
|---|---|
| `00_podklady` | Raw material, exactly as it came. You only add to it. |
| `10_znalosti` | What holds for a long time, for example decisions. |
| `20_aktualni_stav` | What is true right now: a card per project, your to-dos, what you are waiting for. |
| `30_vystupy` | What leaves the folder. |
| `_archiv` | Finished and outdated things. Nothing is deleted. |

## You are done when

- [ ] `AGENTS.md` is in the root of your folder and has no `<placeholders>` left,
- [ ] section 1 says in your own words what the folder is for,
- [ ] the folders and files above exist.

## Two rules

- **Your words, not the AI's.** Section 1 should sound like you. If it does not, change it.
- **One folder.** Do Task 1 and Task 2 in this same folder, each in a new chat.
