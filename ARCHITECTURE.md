# Architecture & Agent Setup

## The Two-Agent System

This project was built entirely using a two-agent orchestration system, specifically designed for the Forge 2 Qualifier. The system operates via a human-in-the-loop chat interface on Slack.

### 1. Hermes (The Brain)
- **Role**: Product Owner & Orchestrator.
- **Channel**: `#sprint-main`
- **Responsibilities**: Receives high-level requirements from me (the human), breaks them down into actionable engineering tasks, manages memory (recalling project structure), and delegates coding tickets to OpenClaw.
- **Skill**: Utilizes a custom `status-report` skill to generate structured updates of "What I Did / What's Left / What Needs Your Call".

### 2. OpenClaw (The Hands)
- **Role**: Autonomous Coder.
- **Channel**: `#agent-coder`
- **Responsibilities**: Receives delegated tasks from Hermes, writes the actual Laravel PHP code and React TSX code, executes shell commands (like `php artisan make:model` or `npm install`), and reports back when the code compiles successfully.

## Tech Stack

- **Frontend**: React 19, TypeScript, Vite, TailwindCSS v4, `@dnd-kit` for drag-and-drop.
- **Backend**: Laravel 13, PHP 8.3, SQLite database (for zero-config setup).
- **Communication**: REST API using Axios.

## Slack Channel Scheme
- `#sprint-main`: Strategic planning and architecture decisions with Hermes.
- `#agent-coder`: Tactical code execution and terminal output from OpenClaw.
- `#agent-log`: Raw background logging and autonomous event triggers.

*Authored by Ishita Modi.*
