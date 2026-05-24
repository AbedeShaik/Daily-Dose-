# Daily Dose Scheduler - Build Execution Plan (Replit Ready)

## Overview

This document provides the exact step-by-step implementation plan to build the MVP of Daily Dose Scheduler.

Follow this in order. Do NOT skip steps.

---

# PHASE 1 — PROJECT SETUP

## Step 1: Initialize Frontend (React)

In Replit:
- Create new React project
- Install dependencies:
  - react-router-dom
  - axios
  - tailwindcss
  - supabase-js

---

## Step 2: Initialize Backend (Node.js)

Create Express server:
- express
- cors
- dotenv
- nodemon

Folder structure:
```
server/
  index.js
  routes/
  controllers/
  services/
```

---

## Step 3: Connect Supabase

Create Supabase project:
- Get API keys
- Add to .env file

Backend config:
- supabase client setup
- auth integration

---

# PHASE 2 — FRONTEND BUILD

## Step 4: Create UI Structure

Pages:
- Dashboard
- Create Post
- Calendar
- Queue
- Settings

Setup React Router.

---

## Step 5: Build Create Post Page

Components:
- Platform selector
- Caption editor
- AI tools panel
- Media upload
- Scheduling panel
- Best time widget

---

## Step 6: Dashboard UI

Show:
- upcoming posts
- stats cards
- quick create button

---

# PHASE 3 — BACKEND BUILD

## Step 7: Auth APIs

Implement:
- register
- login
- JWT authentication

---

## Step 8: Post APIs

Create endpoints:
- create post
- update post
- delete post
- fetch posts

---

## Step 9: Scheduling Engine

Logic:
- cron job runs every minute
- checks scheduled posts
- publishes when time matches

---

# PHASE 4 — AI INTEGRATION

## Step 10: OpenAI Setup

Add API key:
- OpenAI SDK

---

## Step 11: AI Features

Implement:
- caption generation
- caption improvement
- hashtag generator
- best time recommendation

---

# PHASE 5 — SOCIAL INTEGRATION

## Step 12: Platform APIs

Start with:
- LinkedIn API
- Twitter/X API

Later:
- Facebook Graph API

---

# PHASE 6 — FINAL MVP

## Step 13: Connect Frontend + Backend

Axios integration:
- posts API
- AI API
- scheduling API

---

## Step 14: Testing

Test flows:
- create post
- generate AI caption
- schedule post
- verify backend execution

---

## Step 15: Deployment

Frontend:
- Vercel

Backend:
- Replit / Render

Database:
- Supabase

---

# MVP SUCCESS CRITERIA

User must be able to:
- sign up
- create post
- use AI caption
- schedule post
- see it in dashboard

---

# IMPORTANT RULES

- Do NOT build advanced features first
- Do NOT over-engineer
- Focus ONLY on MVP flow
- Ship fast, improve later

---

# FUTURE PHASE

After MVP:
- analytics
- viral scoring
- AI content recycling
- team collaboration
- automation workflows