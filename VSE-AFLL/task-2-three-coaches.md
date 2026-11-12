# Task 2 · Three coaches, one Manifesto

Authentic Female Leadership Lab · 2TM314 · Day 3 · starts in class

**They ask. You decide.**

## The idea

Your Leadership Manifesto says who you are. Now you decide where that takes you. Three AI coaches read your Manifesto and coach you towards your career Blue Ocean, each from a different angle. They work in your project folder, so everything you work out stays there.

The coaches are not prompts you paste. They are files in your folder. You start one with a single command, and you can open the file to see exactly who is coaching you and why they ask what they ask.

## Before you start

- Task 0 is done: your folder has `AGENTS.md` and the folder structure.
- Your **Leadership Manifesto 3.1** is in the folder, in `00_materials/`. Copy the file there. Remove other people's names first.
- The folder is open in your AI agent.

## Step 1 · Put the coaches into your folder

Copy the folder `coaches` from the course repository into `10_knowledge/` in your project folder. You should end up with:

```
10_knowledge/
└── coaches/
    ├── _session.md      # the frame every coach follows
    ├── strategist.md
    ├── strengths.md
    ├── questions.md
    └── _template.md     # for your own coach
```

## Step 2 · Start a coach

Open a **new chat** in your folder and type:

```text
COACH strategist
```

When the session ends, open another new chat for the next coach:

```text
COACH strengths
```

```text
COACH questions
```

`COACH` on its own lists your coaches and tells you which ones you have already run.

If your agent does not recognise the command, write it out in full:

```text
Read 10_knowledge/coaches/_session.md and then 10_knowledge/coaches/strategist.md. Become that coach and begin with phase one.
```

## The three coaches

Run them in this order. Each coach reads what the one before left behind.

| Command | Coach | Modelled on | Looks at | You leave with |
|---|---|---|---|---|
| `COACH strategist` | The Strategist | W. Chan Kim and Renée Mauborgne, Blue Ocean Strategy | Where you compete like everyone else, and what to eliminate, reduce, raise and create | Your Red Ocean and a first ERRC grid |
| `COACH strengths` | The Strengths Coach | Marcus Buckingham, Love + Work | What actually gave you energy last week, against what your grid says | A grid that fits your energy, and your shadows with a way to protect yourself |
| `COACH questions` | The Question Coach | Hal Gregersen, Questions Are the Answer | The assumptions hiding in your Manifesto and your grid | Three questions you cannot answer yet, and your Blue Ocean in one sentence |

The coaches are modelled on how these people work and teach. They are not those people and they never quote them.

## How every session moves

Each coach runs five phases and announces each one in capitals.

| Phase | What happens |
|---|---|
| PHASE ONE · READING | The coach reads your Manifesto, tells you how it will work with you, and quotes the lines it will build on |
| PHASE TWO and THREE | The coach's own work. Different for each coach |
| PHASE FOUR · DISAGREE | You tell the coach where it is wrong. This is required, not optional |
| PHASE FIVE · SAVE | Your answers, your decisions and one key exchange go into your folder |

Words that steer the session: `OK` accepts a result, `NEXT` jumps to the next phase, `WHERE` tells you where you are, `SKIP` drops a question you do not want to answer.

## Two rules

1. **Disagree with each coach at least once.** AI tends to agree with you. Test it, don't obey it.
2. **Your words, not the coach's.** The coaches ask and write down what you said. They do not write your answers.

## After the three coaches

**Say it out loud.** Explain your Blue Ocean to a friend or classmate in two minutes. Then tell your agent, in any chat in the folder:

```text
Follow AGENTS.md. Add a section "What my friend said" to 20_current_state/cards/blue-ocean.md with this, in my words: [the one thing they said that stuck]
```

**Look at your card.** `20_current_state/cards/blue-ocean.md` now holds your Red Ocean, your ERRC grid, your shadows, your three questions, your Blue Ocean in one sentence, and an Archive with the three exchanges that changed your thinking most. That is the raw material for Part A of your final task. Writing it up is your job, not the coach's.

## Optional · Design your own coach

The first three coaches each look from one angle. Design a fourth who catches what they missed.

1. Copy `10_knowledge/coaches/_template.md` and give the copy a short name without spaces, for example `sceptic.md`.
2. Replace everything in angle brackets. Read one of the three coach files first to see how much detail a coach needs.
3. Start it like the others: `COACH sceptic`.

"Be critical and honest" is not a coach. A coach has a point of view.

## You are done when

- [ ] you have run all three coaches, each in its own chat,
- [ ] you disagreed with each of them at least once,
- [ ] your card has a section from each coach and three exchanges in the Archive,
- [ ] you have explained your Blue Ocean to one person and added what they said.

## Good to know

- **This is not therapy.** If a question goes somewhere you do not want to go, write `SKIP`.
- **Your Manifesto is personal.** Use your own account, remove other people's names, and leave out anything you would not pin on a noticeboard.
- **If a coach forgets itself** and starts giving advice or praising you, write `WHERE`, or remind it: "one question at a time, no advice".
- **You can read the coaches.** Open any file in `10_knowledge/coaches/`. If you think a coach is wrong about how to coach you, change the file. It is your folder.
