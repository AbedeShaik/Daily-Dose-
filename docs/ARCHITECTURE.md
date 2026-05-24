# Daily Dose Scheduler - System Architecture

## Overview

Daily Dose Scheduler is a full-stack AI-powered social media automation system.

It follows a simple flow:

User → Frontend → Backend → Database + AI → Scheduler → Social Platforms

---

## High-Level Flow

1. User creates a post in frontend
2. Frontend sends data to backend API
3. Backend processes:
   - saves post
   - calls AI services if needed
   - schedules post
4. Database stores all data
5. Scheduler triggers post at correct time
6. Social APIs publish content

---

## Frontend Layer (React)

Responsibilities:
- UI rendering
- Create Post page
- Dashboard
- Calendar
- AI interaction UI
- Sending API requests

Communicates with backend via REST APIs.

---

## Backend Layer (Node.js)

Responsibilities:
- Authentication
- Post creation
- Scheduling logic
- AI integration
- Platform API integration

Key Modules:
- auth service
- post service
- scheduler service
- ai service

---

## AI Layer (OpenAI API)

Used for:
- caption generation
- rewriting content
- hashtag suggestions
- best posting time prediction

Flow:
Frontend → Backend → OpenAI → Backend → Frontend

---

## Database (Supabase PostgreSQL)

Stores:
- users
- posts
- scheduled posts
- AI suggestions
- connected social accounts

---

## Scheduler System

Core engine that:
- checks database for scheduled posts
- triggers publishing at correct time
- updates post status

Runs as background job (cron-like system).

---

## Social Media Integration Layer

Handles posting to:
- LinkedIn API
- Twitter/X API
- Facebook Graph API

Backend sends formatted content to APIs.

---

## Data Flow Summary

User Input
→ Frontend
→ Backend API
→ Database + AI
→ Scheduler
→ Social Platform
→ Status Update

---

## Future Enhancements

- Real-time analytics engine
- AI content optimization loop
- Viral prediction system
- Multi-user team collaboration
- Webhook-based integrations