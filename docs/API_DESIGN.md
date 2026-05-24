# Daily Dose Scheduler - API Design

## Overview

This document defines all backend API endpoints used by the application.

Base URL:
```
/api
```

---

# 1. Authentication APIs

## Register User
```
POST /auth/register
```

### Body:
- name
- email
- password

### Response:
- user object
- token

---

## Login User
```
POST /auth/login
```

### Body:
- email
- password

### Response:
- user object
- token

---

# 2. Posts APIs

## Create Post
```
POST /posts
```

### Body:
- content
- platform
- media_url (optional)

---

## Get All Posts
```
GET /posts
```

Returns all user posts.

---

## Get Single Post
```
GET /posts/:id
```

---

## Update Post
```
PUT /posts/:id
```

---

## Delete Post
```
DELETE /posts/:id
```

---

# 3. Scheduling APIs

## Schedule Post
```
POST /schedule
```

### Body:
- post_id
- scheduled_time
- timezone

---

## Get Scheduled Posts
```
GET /schedule
```

---

# 4. AI APIs

## Generate Caption
```
POST /ai/generate-caption
```

### Body:
- topic
- tone
- platform

---

## Improve Caption
```
POST /ai/improve-caption
```

---

## Generate Hashtags
```
POST /ai/hashtags
```

---

## Best Time Recommendation
```
POST /ai/best-time
```

### Body:
- platform
- audience_region

---

# 5. Social Accounts APIs

## Connect Account
```
POST /accounts/connect
```

---

## Get Connected Accounts
```
GET /accounts
```

---

## Disconnect Account
```
DELETE /accounts/:id
```

---

# Data Flow Summary

Frontend → API → Database → AI → Scheduler → Social Platforms

---

# Future Enhancements

- Webhook APIs for real-time posting
- Analytics APIs
- Engagement tracking APIs
- Bulk scheduling APIs