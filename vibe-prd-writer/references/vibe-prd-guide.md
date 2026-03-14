# Vibe PRD Writing Guide

## The 5 Essential Questions

### 1. Why are we doing this?
**Why it matters:** If we can't articulate why, everything else is just guesswork. This grounds our entire effort.

**What to look for:** Clear business value, user benefit, strategic alignment.

### 2. Who are we building this for?
**Why it matters:** "Everyone" is not a user. Let's get specific about who benefits and how.

**What to look for:** Primary user persona, secondary users, specific user needs.

### 3. What's the ONE core thing it must do?
**Why it matters:** If you can only pick one feature, what is it? This helps us focus on the MVP.

**What to look for:** Single most important functionality, user journey flow.

### 4. What are we NOT doing?
**Why it matters:** Boundaries are more important than features. A PRD without boundaries is a recipe for disaster.

**What to look for:** Clear scope exclusions, technical constraints, timeline boundaries.

### 5. How will we know it worked?
**Why it matters:** Without success metrics, we're just building and hoping.

**What to look for:** Measurable KPIs, acceptance criteria, success definitions.

## Tech Stack Recommendations

### Pure Showcase (Landing Pages, Portfolios)
- **Tech:** HTML + Tailwind + Static hosting
- **Why:** Simple, fast, no backend needed, perfect for static content

### AI Interaction (Content Gen, Chat)
- **Tech:** Next.js + AI APIs + Vercel
- **Why:** Server-side rendering, API integration, deployment simplicity

### Data Storage Needed (User Records, History)
- **Tech:** Next.js + Supabase + Vercel
- **Why:** Full-stack solution, database integration, real-time capabilities

### Default Option
- **Tech:** Next.js + Tailwind + Vercel
- **Why:** Versatile, scalable, great developer experience

## Quality Check Checklist

### ✅ Can you explain the product in one sentence?
- Test: "What does this product do?" → Should be clear and concise

### ✅ Is the MVP doable in an afternoon?
- Test: Look at core features → Should be achievable in a short timeframe

### ✅ Are boundaries clearly defined?
- Test: Check "What's NOT included" section → Should have specific exclusions

### ✅ Does each feature have acceptance criteria?
- Test: Each feature should have clear success metrics

### ✅ Does the tech stack match the requirements?
- Test: Tech choices should align with product needs

### ✅ Can your AI start working immediately?
- Test: PRD should have clear execution instructions

## PRD Structure Best Practices

### Product Positioning
- One clear sentence that explains what the product is
- Should be memorable and easy to understand

### Target Users
- 2-3 sentences maximum
- Specific user personas, not generic groups

### Core Features
- Maximum 3 features
- Each feature should have:
  - User action
  - Expected result
  - Acceptance criteria

### Technical Approach
- Clear tech stack recommendation
- Reasoning for each choice
- Dependencies and constraints

### Agent Instructions
- Direct, actionable instructions
- Clear execution flow
- Specific deliverables

## Common Pitfalls to Avoid

- ❌ Don't skip the "why" question
- ❌ Don't accept vague user definitions
- ❌ Don't include too many features
- ❌ Don't forget boundaries
- ❌ Don't omit success metrics
- ❌ Don't choose tech without reasoning

## Example: Good vs Bad PRD

**Bad PRD:**
```
# Product: Task Manager
- Users: Everyone
- Features: Task creation, editing, deletion
- Tech: React
```

**Good PRD:**
```
# Product Requirements Document: Remote Team Task Manager

## Product Positioning
A simple task management tool for remote teams to track work and deadlines.

## Target Users
Primary: Remote team members and managers who need better visibility into project progress.

## Core Features
1. Task Creation & Assignment
   - User action: Team members create tasks and assign to others
   - Expected result: Tasks appear in team dashboard with assignee and deadline
   - Acceptance: Tasks can be created, assigned, and viewed by assigned user

2. Real-time Status Updates
   - User action: Users update task status (todo/in-progress/done)
   - Expected result: All team members see status changes immediately
   - Acceptance: Status updates propagate in real-time to all viewers

3. Deadline Reminders
   - User action: System sends notifications for upcoming deadlines
   - Expected result: Users receive timely reminders via email/notifications
   - Acceptance: Reminders trigger 24h before deadline and on deadline day

## Scope Boundaries
- Out of Scope: Mobile apps, advanced analytics, complex workflows
- Constraints: Must integrate with existing team communication tools
- Timeline: 2-week MVP focused on core functionality

## Technical Approach
- Technology: Next.js + Supabase + Vercel
- Reasoning: Full-stack solution with real-time database for collaboration
- Dependencies: Supabase for auth and database, Vercel for deployment

## Agent Instructions
1. Create a Next.js app with Tailwind CSS
2. Set up Supabase database with tasks table
3. Implement task creation, assignment, and status update features
4. Add real-time updates using Supabase realtime
5. Deploy to Vercel with environment variables
```