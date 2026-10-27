# Baseball Practice Tracker Proposal

## 1.1 The problem

Baseball players need a simple way to record their practice sessions and see how consistently they work on different skills. I played varsity baseball in high school, so I want to build a tool connected to a sport I care about. Keeping the date, practice type, and time spent in one place would make it easier to review a week of practice.

## 1.2 The solution

I want to build a Java command-line baseball practice tracker that saves sessions and shows practice summaries. A player will enter a date, practice type, minutes, and optional notes, then review saved sessions and time spent practicing.

## 2.1 Eisenhower matrix

### Do - MVP

1. Add a session with a valid date, practice type, positive number of minutes, and optional notes.
2. List sessions and save/load them from a local text file so records survive restarts.
3. Show total sessions, total minutes, minutes by practice type, and a seven-day summary.

### Schedule - Version 2

1. Edit or delete a saved session.
2. Set weekly practice goals and display progress toward them.
3. Record performance measurements such as hits and at-bats.

### Delegate - Use existing libraries

1. Date parsing and calendar calculations: use `java.time.LocalDate`.
2. Reading and writing files: use Java's buffered file I/O classes.
3. Sorting sessions by date: use Java collection sorting instead of writing a sorting algorithm.

### Delete - Cut from this project

1. Live MLB scores and sports API integration.
2. Social feeds, public profiles, and team messaging.
3. AI coaching and automatic video analysis.

The Do items form one complete workflow: record practice, keep it between runs, and review practice consistency. The Delegate items are implementation tasks handled with existing libraries, not additional product features.

## 2.2 Tech stack

- **Language:** Java, using the version provided for CS coursework.
- **Input and collections:** `Scanner`, `ArrayList`, and standard collection sorting.
- **Dates:** `LocalDate` for validation and date comparisons.
- **Storage:** `data/sessions.txt`, one session per line with four fields separated by vertical bars. Input validation will prevent separators and line breaks inside notes.
- **Files:** `BufferedReader` and `BufferedWriter`; no external libraries or database.
- **Development tools:** IntelliJ IDEA, Git, and GitHub.
- **Data source:** Records entered by the user. No external API, account, or internet connection is needed to use the tracker.

## 2.3 Chunked build plan

1. **Repository setup:** Create folders, README, and proposal. Check that the public repo opens and the plan is readable. Commit: `Set up baseball tracker project`.
2. **Session model:** Implement a session object and input validation. Check valid input and reject invalid dates, unknown types, and nonpositive minutes. Commit: `Add practice session model`.
3. **Working menu:** Add a menu to record and list in-memory sessions. Check adding two different sessions and returning to the menu. Commit: `Add session entry and list menu`.
4. **Persistence:** Load and save sessions. Check that records remain after restarting and that missing files start an empty library. Commit: `Save and load practice sessions`.
5. **Basic summaries:** Show session count, total minutes, and minutes by type. Check the totals against a small hand-calculated example. Commit: `Add practice totals by type`.
6. **Weekly summary:** Summarize the selected date and previous six dates, inclusive. Check sessions on both boundaries and just outside the range. Commit: `Add seven day practice summary`.
7. **Error handling:** Test empty data, malformed files, invalid menu input, and failed saves. Verify that errors do not silently overwrite previous records. Commit: `Handle invalid input and file errors`.
8. **Finish documentation:** Improve prompts, add real setup instructions, create the diagram, and prepare a 3-4 minute demonstration. Commit: `Polish tracker and project documentation`.

## 2.4 System diagram

**Not completed.** The student must draw the diagram in a diagramming tool, export a PNG/JPG, and keep the editable source. Insert the finished image here before submitting.

Use the drawing guide in `diagram-instructions.md` to understand the requirements. The final diagram and its design must be your own work.

## 3.1 GitHub repository

https://github.com/andersonyaen13/baseball-practice-tracker

## Review before submission

This is a proposed plan to review and understand before using it. Confirm that the fields, summaries, MVP scope, and class responsibilities match what you want to implement and can explain. Do not submit until the diagram and repository link have been added.
