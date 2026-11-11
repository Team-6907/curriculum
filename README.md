# Team 6907 Curriculum

Teaching material written and used by FRC Team 6907 to introduce new and junior members to programming. Each chapter is a self-contained folder with its own README, so a mentor can pick one up and run it as a single session or assignment.

**中文简介：** FRC 6907 队的编程教学资料合集，按章节组织（Java 入门、Junior Academy 作业、Python Turtle 游戏课），每个章节目录自带说明，可单独使用。

## Chapters

| Chapter | Audience | Language | Time | What you need |
|---------|----------|----------|------|---------------|
| [`java-basics/`](java-basics/) — five short intro programs: variables, booleans, conditionals, methods, classes and objects | New members with no programming background | Java (comments in English) | Self-paced; five short programs | A JDK, or any online Java runner |
| [`junior-academy/2025-prisoners-dilemma/`](junior-academy/2025-prisoners-dilemma/) — FRC Junior Academy 2025 assignment: write a strategy for a three-player prisoner's dilemma tournament | Junior Academy students who know basic Java syntax and classes | Java (handout in Chinese) | Take-home assignment | A JDK (`javac` / `java`) and a text editor |
| [`python-turtle/`](python-turtle/) — build a "dodge the asteroids" game in seven fill-in-the-blank steps (step 7 is a bonus) | Middle-school students (grades 7–9) who know Python basics | Python 3 (material in Chinese) | One 90-minute lesson | Python 3 with the built-in `turtle` module (needs Tk) |

## How the repository is organised

```
curriculum/
├── README.md               # this file
├── LICENSE                 # MIT, covers Team 6907's own material
├── NOTICE.md               # what the MIT license does NOT cover
├── java-basics/            # one folder per chapter
├── junior-academy/         # a series: one sub-folder per year/assignment
│   └── 2025-prisoners-dilemma/
└── python-turtle/
```

- **One chapter = one top-level folder**, named in lowercase ASCII with hyphens. A recurring programme (such as Junior Academy) is a folder containing one sub-folder per edition, prefixed with the year.
- **Every chapter has a `README.md`** that says who it is for, how long it takes, what to install and how to run it.
- **File and folder names are ASCII.** The content itself can be in Chinese or English.
- **Student-facing files only.** Worked solutions are kept out of this repository (see [Solutions](#solutions)).
- Each chapter was imported from its original repository with its git history (`git subtree`), so `git log -- <chapter>/` still shows who wrote what. The `python-turtle/` history was filtered on import so that it never contains the teacher solutions.

## Adding a new chapter

1. Create a folder at the root (or under the series it belongs to), e.g. `wpilib-command-based/` or `junior-academy/2026-<topic>/`.
2. Add a `README.md` covering: audience, prerequisites, time needed, what to install, and how to run the material.
3. Keep file and folder names ASCII, and do not commit files named after, or containing personal data about, real students.
4. Put student-facing starter code in the chapter. Put answers in the private solutions repository under the same path (see below), never here.
5. If the chapter adapts someone else's material, credit it in the chapter README and in [Credits](#credits). If that material has no license, or one that is incompatible with MIT, also list it in [`NOTICE.md`](NOTICE.md).
6. Add a row to the [Chapters](#chapters) table above.

To bring in an existing repository with its history:

```bash
git subtree add --prefix=<chapter-folder> <repository-url> <branch>
```

## Solutions

Worked solutions and teacher-only reference code live in the **private** repository [`Team-6907/curriculum_solutions`](https://github.com/Team-6907/curriculum_solutions), which mirrors the chapter layout of this one (for example `python-turtle/solutions/`). Access is limited to team mentors and teachers; ask a team mentor if you need it. Please do not copy solutions into this repository or share them with students before a lesson.

## Credits

- **`java-basics/`** is adapted from FRC **Team 3847 Spectrum**'s *C1.1 Intro to Java Programming* training material by Team 3847 and Allen Gregory. See [`java-basics/README.md`](java-basics/README.md) for links to the originals. Thank you, Spectrum!
- **`junior-academy/2025-prisoners-dilemma/ThreePrisonersDilemma.java`** is a tournament harness adapted from a widely circulated university course exercise; the original author is not identified in the file.

## License

Unless stated otherwise, Team 6907's own material in this repository is released under the [MIT License](LICENSE).

Two parts are **not** covered by that license, because they are adapted from third-party material that came without a license: the whole of `java-basics/` (from Team 3847 Spectrum) and the file `junior-academy/2025-prisoners-dilemma/ThreePrisonersDilemma.java` (original author not identified). Both are included with attribution, as far as it is known, for educational use only. See [`NOTICE.md`](NOTICE.md).
