# Baseball Practice Tracker

A proposed Java command-line tool for recording baseball practice and reviewing practice consistency.

## Project goal

Help baseball players keep their practice sessions in one place and see how much time they spend on different skills. This is a CS 19300 final-project plan; the application has not been implemented yet.

## MVP scope

- Record a practice session with a date, practice type, minutes, and optional notes.
- View recorded sessions and save/load them from a local text file.
- View total sessions, total minutes, minutes by practice type, and a seven-day summary.

Proposed practice types: hitting, pitching, fielding, and conditioning. Progress means practice consistency and time spent, not a claim that more minutes prove improved athletic performance.

## Future plans

- Edit or delete an existing session.
- Set weekly practice goals and show progress toward them.
- Add performance measurements such as hits and at-bats.

## Tech stack

- Java with the standard library; no external dependencies or online APIs.
- `Scanner` for command-line input and `ArrayList` for sessions in memory.
- `java.time.LocalDate` for dates and the seven-day summary.
- `BufferedReader` and `BufferedWriter` for local text storage.
- Java collection sorting for ordering sessions by date.
- IntelliJ IDEA for development; Git and GitHub for version history.

## Planned structure

```text
src/       Java application source added during implementation
tests/     Small test programs or test cases
docs/      Project proposal and student-created diagram files
data/      Local practice records, excluded from version control
```

Proposed classes: `Main` handles the menu, `PracticeSession` represents one record, `PracticeTracker` manages records and summaries, and `SessionFile` loads and saves them. These names are planning suggestions to review before implementation.

## Data storage

Use `data/sessions.txt`, with one session per line. A proposed format is `date|type|minutes|notes`; reject vertical bars and line breaks in user-entered notes so records remain readable. Load saved sessions at startup and save changes before reporting that a session was recorded. A missing data file means a new empty tracker; a malformed file or failed save should show a clear error without silently deleting previous data.

## Build plan

1. Set up repository folders, README, and the project proposal.
2. Implement `PracticeSession` and validate dates, types, and positive minute values.
3. Add a menu that can record sessions and list them in memory.
4. Add text-file loading and saving, then check persistence after restarting.
5. Add total sessions, total minutes, and minutes by practice type.
6. Add the seven-day summary using a documented inclusive date range.
7. Test invalid input, missing files, malformed records, empty summaries, and date boundaries.
8. Improve prompts and documentation, draw the system diagram, and prepare the walkthrough.

Each completed step should produce one meaningful Git commit. Do not create commits for work that has not been done.

## Running the project

There is no runnable application yet. Setup and run instructions will be added after the first working implementation.

## Documentation

See [the proposal](docs/design-proposal.md). The required system diagram must be drawn by the student using a diagramming tool and added with its editable source file.
