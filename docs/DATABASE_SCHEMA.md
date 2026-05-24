# Daily Dose Scheduler - Database Schema

## Overview

This document defines the core database structure for the application.

Database: PostgreSQL (via Supabase)

---

# 1. Users Table

Stores user account information.

## Fields
- id (UUID, primary key)
- name (text)
- email (text, unique)
- password_hash (text)
- created_at (timestamp)

---

# 2. Posts Table

Stores all user-created posts.

## Fields
- id (UUID, primary key)
- user_id (foreign key → Users.id)
- content (text)
- platform (text) // LinkedIn, Twitter, Facebook
- media_url (text, optional)
- status (draft | scheduled | published)
- created_at (timestamp)

---

# 3. Scheduled Posts Table

Handles scheduling logic.

## Fields
- id (UUID, primary key)
- post_id (foreign key → Posts.id)
- scheduled_time (timestamp)
- timezone (text)
- status (pending | executed | failed)

---

# 4. Social Accounts Table

Stores connected social media accounts.

## Fields
- id (UUID, primary key)
- user_id (foreign key → Users.id)
- platform (text)
- access_token (text)
- refresh_token (text)
- connected_at (timestamp)

---

# 5. AI Suggestions Table

Stores AI-generated outputs.

## Fields
- id (UUID, primary key)
- post_id (foreign key → Posts.id)
- caption_suggestions (text)
- hashtags (text)
- best_time (timestamp or text)
- tone (text)

---

# Data Relationships

Users
→ Posts
→ Scheduled Posts
→ AI Suggestions

Users
→ Social Accounts

---

# Key System Behavior

- Each user can create multiple posts
- Each post can have one schedule
- Each post can have multiple AI suggestions
- Each user can connect multiple platforms

---

# Future Enhancements

- engagement tracking table
- analytics events table
- viral scoring system
- content performance history