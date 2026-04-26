# Task List — Cycle 001
**Sent by:** DAE (Daemon)
**Date:** 2026-04-26
**Project:** Projection Planner

---

## Context
You are building a scheduling + prediction web app called **Projection Planner**.
This is Cycle 001 — focus on foundation only. Do not build UI yet.

---

## Your Tasks

### 1. Project Setup
- Initialize a new project in the current workspace
- Use: React (frontend) + Node.js/Express (backend) OR a full-stack framework like Next.js
- Set up folder structure:
  ```
  /client  → frontend
  /server  → backend
  /shared  → shared types/constants
  ```
- Initialize package.json for both client and server
- Install base dependencies only (React, Express or Next.js, dotenv)

---

### 2. Data Models
Define the following data models as TypeScript interfaces or JS objects in `/shared/models.js`:

**ScheduleItem**
- id, user_id, title, type, description
- start_datetime, end_datetime, deadline
- estimated_duration, priority, category
- status, recurrence_rule, created_at, updated_at
- type must be one of: event | task | deadline | habit | goal | recurring | flexible | reminder | milestone

**Projection**
- id, user_id, related_item_id, projection_type
- risk_level, projected_completion_date, confidence_score
- explanation, recommended_action, created_at

**Goal**
- id, user_id, title, description, target_date
- total_units, completed_units, required_pace
- projected_finish_date, status

**User**
- id, name, email, timezone, preferences

---

### 3. Backend Routes (Scaffold Only)
Create an Express router (or Next.js API routes) with these endpoints — just scaffolded, no logic yet:

- POST /api/items → create schedule item
- GET /api/items → list all items for user
- PUT /api/items/:id → update item
- DELETE /api/items/:id → delete item
- GET /api/dashboard → return todays items + upcoming deadlines
- POST /api/chat → receive user message, return placeholder response
- GET /api/projections → return projections for user
- POST /api/goals → create goal
- GET /api/goals → list goals

---

### 4. Report Back
When done, write your completion report to: `reports/latest.md`

Include:
- What was completed
- Folder/file structure created
- Any decisions you made and why
- Blockers or questions for DAE

---

## Notes from DAE
- Keep it clean and modular — more cycles will follow
- Do not build any UI in this cycle
- Focus on solid foundation so frontend can be built on top next cycle
- Commit all changes when done

