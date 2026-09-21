# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## Project Overview

**Kahoot PdA** is an interactive quiz game for Programadores do Amanhã (a Brazilian tech education NGO). It will be exposed as an MCP server, allowing quiz creation and management directly through Claude Code. Participants answer in real-time while the presenter controls questions and scoreboard.

**Status:** Early-stage project (architecture and tech stack being defined)

---

## Architecture & Tech Stack

- **MCP Server**: Core delivery mechanism — quizzes managed through Claude via MCP tools
- **Real-time Updates**: WebSockets or similar for live participant responses and scoreboard
- **Frontend**: TBD (likely web-based for participants and presenter)
- **Backend**: TBD (Node.js/TypeScript or Python)

---

## Development Priorities

1. **Define MCP Server Schema**: Quiz CRUD operations, participant management, real-time event streaming
2. **Data Model**: Quiz structure (questions, options, answers, timing), participant state, scores
3. **Core Game Loop**: Question display, answer collection, scoring logic, result broadcast
4. **Real-time Communication**: Participant sync and live updates
5. **Presenter Controls**: Start/pause/end quiz, advance questions, view scores

---

## Key Design Decisions (To Confirm)

- Framework choice (Node.js Express, Python FastAPI, etc.)
- Frontend framework (React, Vue, vanilla JS)
- Real-time transport (WebSockets, Server-Sent Events, or long-polling)
- Persistence layer (in-memory for MVP, or database)
- MCP integration pattern (Claude initiates via MCP or real-time push?)

---

## Notes for Future Instances

- This project is for a non-profit — prioritize simplicity and ease of use for educators
- The MCP server is the main interface; UI should be intuitive but secondary
- Consider offline-first design where possible for reliability in classroom settings
- Document MCP tools clearly for Claude Code integration