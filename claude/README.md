# Claude Code Tips
 
A collection of useful tips and commands for getting more out of Claude Code.
 
## Setup
 
- **`/plugin install claude-code-setup@claude-plugins-official`** — Recommended first step after installing Claude Code. Sets up sensible defaults and configuration automatically.
## Skills
 
- **[grill-me](https://github.com/mattpocock/skills/blob/733d312884b3878a9a9cff693c5886943753a741/skills/productivity/grill-me/SKILL.md)** — A skill that has Claude quiz and challenge you on a topic to deepen your understanding.
- **[grill-with-docs](https://github.com/mattpocock/skills/blob/main/skills/engineering/grill-with-docs/SKILL.md)** — Like grill-me, but grounded in specific documentation — great for learning a new library or API.
## Interface & Modes
 
- **`/remote-control`** — Continue your current Claude Code session from a browser or mobile device.
- **`/tui fullscreen`** — Enables flicker-free terminal UI mode for a smoother experience in the terminal.
- **`/voice`** — Toggles voice input mode. Hold the space bar to speak.
- **Auto mode** — Lets Claude autonomously decide when to use tools and take actions, reducing the need for manual confirmation on each step.
## Parallelism & Scheduling
 
- **`claude --worktree` / `claude -w`** — Spins up multiple Git worktrees so several Claude agents can work on different tasks simultaneously without interfering with each other.
- **`/loop`** — Schedules a recurring job within a session, useful for repeated checks or automated workflows during a working session.
## Code Review
 
- **`/ultrareview`** — Performs a thorough review of your PR before pushing to GitHub, catching issues early.
## Automation (Claude Desktop)
 
- **Routines** — Define repeatable workflows in Claude Desktop that can run locally or remotely on a schedule, similar to a lightweight automation system.
 
