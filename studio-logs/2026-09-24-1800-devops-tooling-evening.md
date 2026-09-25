---
date: 2026-09-24
time_start: "18:00"
time_end: "19:50"
timezone: America/Toronto
season: autumn
project: [historiotheque]
stream: [text]
session_type: admin
workspace: historiotheque
refcards: []
tags: [devops, vscode, python, venv, jupyter, github-desktop, tooling, cultural-software, feedback]
related:
  - studio-logs/2026-09-24-0845-workflow-methodology-pattern-harvest.md
---

## What I did

Evening session in the "DevOps" side chat — the chat itself was renamed in place
this evening (no duplicate created) to hold the whole Cultural DevOps learning
arc. This is the hands-on sequel to the morning's install session: everything the
morning set up (VS Code, the Python extension, GitHub Desktop) got actually used
tonight.

Day context, briefly: a morning walk to the cemetery, a midday visit from J. (long
strategy talk about the Art Operation), and a second walk in the afternoon after
he brought me home. Then the evening belonged to tooling.

In order:

1. **Verified the Python setup.** `python --version` → 3.13.13, on PATH
   (`c:\Program Files\Python313\python.exe`). The Microsoft Python extension and
   the Jupyter extension were installed — the Python extension was still finishing
   its install when the session began, which caused the first confusion of the
   evening (see Problems).
2. **Created `C:\Dev\Playground`** as the practice folder ("playground" being the
   programmer-conventional name for a scratch space) and opened it in VS Code.
3. **First notebook:** `first-notebook.ipynb`. Markdown cells render, code cells
   run. In it I wrote my own framing: *"a modified version of literate programming,
   what I am calling Cultural Software."*
4. **Built the first virtual environment:** `python -m venv .venv` inside the
   playground. It appeared to hang — Windows Defender scanning hundreds of small
   files — but the folder was complete (`Include/`, `Lib/`, `Scripts/`,
   `pyvenv.cfg`), so no rerun. The terminal auto-activates (the `(.venv)`
   prefix); manual activation is `.venv\Scripts\Activate.ps1`, with
   `Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned` first if
   PowerShell objects.
5. **Installed ipykernel twice** — once globally (the long dependency list
   installing computer-wide was alarming; it became the felt lesson for *why
   virtual environments exist*), once inside the venv (each venv needs its own
   kernel).
6. **The kernel-picker saga.** The picker showed no environments at first — the
   Python extension was still installing, not Python missing (an early
   misdiagnosis, owned and corrected). The `.venv` kernel only appeared after
   ipykernel was inside the venv *and* the interpreter path was entered manually
   (Ctrl+Shift+P → "Python: Select Interpreter" →
   `C:\Dev\Playground\.venv\Scripts\python.exe`). The kernel finally showed
   `.venv (3.13.13)` and the notebook ran.
7. **GitHub Desktop test loop, completed end to end.** Created a local-only repo
   `desktop-test` at `C:\Dev` (File → New repository; no org selection needed for
   a local test). Created `hello.md`, committed ("first test commit"). The empty
   Changes tab after committing is correct — it shows only uncommitted changes;
   History holds the commit. The Publish button still being present = nothing went
   to GitHub.
8. **Decided on Kate as the editor** for the test loop — any editor works; Desktop
   just watches the folder. (Kate's violet bottom panel is its own Git chatter;
   ignorable.)
9. **Filed two feature requests through the app's feedback channel** (missing-integration: a
   GitHub connector; broken-behavior: Library file browsing), establishing a
   standing rule: no situational context in any filing unless explicitly requested
   for that filing.

The season of heart for this session, in my own words: an **autumn of joyful
being**. There was a slight winter-of-the-soul touch the other day; tonight, work
was good, and when work is good, I feel good. A productive day — the Art Operation
at the Historiotheque is ready for business. Uncharted territory from here.

## Decisions

- **Decision:** Name the practice folder `Playground`. / **Reason:** it is the
  programmer-conventional name for a scratch space; naming things the way the
  tribe names them is part of learning the trade.
- **Decision:** Build a venv now, not later. / **Reason:** the global ipykernel
  install was the felt lesson — computer-wide installs are exactly what the venv
  exists to prevent.
- **Decision:** Park the venv-kernel fight; fall back to the main Python kernel
  when needed. / **Reason:** the venv still does its tidiness job in the terminal
  regardless of which kernel the notebook uses. Don't win fights; park them.
- **Decision:** Use Kate as the working editor for the Desktop test loop. /
  **Reason:** it's the editor at hand; Desktop doesn't care which editor writes
  the files, it only watches the folder.
- **Decision:** Keep test repos local-only until deliberately published. /
  **Reason:** the Publish button's continued presence is the proof nothing left
  the machine.
- **Decision:** Start filing feature requests and bug reports through the app's feedback channel
  as a standing practice. / **Reason:** the team counts how many people ask;
  planting seeds is the whole mechanism.
- **Decision:** No situational or personal context in any filing — not in the
  report, not in the local context field — unless explicitly requested for that
  specific filing. / **Reason:** the process works fine on the bare ask; anything
  more feels like surveillance.
- **Decision:** Log this session, frustration and all, as a studio log. /
  **Reason:**
  > "A log that only shows mastery is advertising. A log that shows the learning
  > curve is documentation."
  > Transparency and accountability are principles of the operation; the honest
  > record is the useful one.
- **Decision:** The role is *operator* (technician), not *engineer*. / **Reason:**
  in Canada "engineer" is a protected title and I am not one. "Cultural DevOps"
  names the practice; "Art Operator" names the role.

## Problems and friction

- The kernel picker showed no environments because the Python extension was still
  installing. The early misdiagnosis — that Python itself might not be installed — was proved wrong by my
  `python --version` screenshot proved 3.13.13 was on PATH. Misdiagnosis owned
  and corrected in the same breath.
- `python -m venv .venv` appeared to hang — Windows Defender scanning hundreds of
  files. Resolved by checking the folder contents instead of rerunning.
- The `.venv` kernel refused to appear in the picker until ipykernel was installed
  *inside* the venv and the interpreter path entered manually.
- The notebook kernel hung on "Connecting to kernel" late in the session; Run All
  and restart hide under the "..." toolbar menu. Unresolved at session end —
  parked, per the decision above.
- **The frustration.** Mid-session I hit the wall: "I want to give up on all of
  this crap." An engineer friend (electrical, I believe) once helped me with VS
  Code and said that to code you have to like solving little puzzles — and I
  *hate* solving puzzles. That dislike is the honest source of the friction: every
  configuration snag feels like a puzzle I never wanted. I know frustration is
  part of learning anything new; a little bit every day, keep coming back, and
  I'll get the hang of it. I stopped, shut VS Code off, came back calmer, and
  finished the Desktop loop. This paragraph is in the log because the log
  documents the learning curve, not the mastery.

## Ideas and sketches

- **Versioned notes (`seed`):** Desktop's diff view is a time machine for
  writing — every save a new diff, History a diary of thought. A personal
  `notes` repo (e.g. for agentic-AI experiments) would make the tool do double
  duty: publishing pipeline *and* thinking instrument. Same recipe as the test
  repo; stays local until deliberately published.
- **"Cultural Software" (`sketch`):** my own name, written in the first
  notebook, for what I'm doing — a modified literate programming where programs
  are designed as cultural objects. The Historiotheque is the flagship instance;
  Official Releases with semantic versioning mark significant changes to how the
  Art Operation runs.
- **The DevOps rhythm (`sketch`):** change → review → commit. Each commit a
  snapshot. This is the heartbeat the whole operation will run on.

## Research and references

None this session — no books, papers, or docs consulted beyond the tools
themselves.

## Feedback and collaboration

- The engineer friend's puzzle remark (above), recalled and offered for the log
  by me, kept because it names the friction honestly.
- Two feedback filings sent through the app's feedback channel as private notes (see Decisions):
  GitHub connector (missing-integration), Library file browsing
  (broken-behavior). Both filed as the bare ask, no context, shown verbatim
  before sending.

## Reproducibility notes

- Windows 11, Dell Latitude 3520. VS Code (user installer, "Add to PATH"
  checked).
- Extensions: Microsoft Python, Microsoft Jupyter.
- Python 3.13.13 at `c:\Program Files\Python313\python.exe`.
- `C:\Dev\Playground\.venv` via `python -m venv .venv`; `pip install ipykernel`
  inside it; manual interpreter selection
  (`C:\Dev\Playground\.venv\Scripts\python.exe`) to surface the `.venv` kernel.
- Activation: automatic in the VS Code terminal; manual via
  `.venv\Scripts\Activate.ps1` (+ `Set-ExecutionPolicy -Scope Process
  -ExecutionPolicy RemoteSigned` if PowerShell objects).
- GitHub Desktop: File → New repository, local path only; identity "A.G." +
  GitHub noreply email (already configured). Test repo `desktop-test` at
  `C:\Dev`; `hello.md`; commit "first test commit"; History tab = the record;
  Publish untouched.

## Artifacts produced

**Text:**
`title` · 2026-09-24-1800-devops-tooling-evening.md · `abstract` · Studio log for
the evening DevOps tooling session: VS Code + Python + venv + first notebook,
GitHub Desktop local commit loop, two feature requests filed, the frustration
logged honestly. · `keywords` · devops, tooling, vscode, github-desktop ·
`date` · 2026-09-24 · `file` ·
`studio-logs/2026-09-24-1800-devops-tooling-evening.md`

(Local-only artifacts this session: `C:\Dev\Playground\first-notebook.ipynb`,
`C:\Dev\desktop-test\hello.md` — practice material, not repo-bound.)

## Next actions

- [ ] Retry the `for`-loop cell on the main Python kernel (owner: me)
- [ ] `pip install requests` in the playground + `pip freeze > requirements.txt`
  (owner: me) — the original requirements question, still open
- [ ] Create the personal `notes` repo in GitHub Desktop (owner: me)
- [ ] Continue the feedback-filing practice as gaps surface (owner: me)
- [ ] Decide timing for the first real publish via Desktop (owner: me)
