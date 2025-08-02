# Glide Table Structure for QuickDesk

This document outlines the structure and relationships of tables used in the QuickDesk app, built with Glide Tables.

---

## 📋 Tables Overview

### 1. Users
- `Name`: Full name
- `Email`: Unique identifier for login
- `Role`: User / Agent / Admin
- `Profile Picture`: Optional avatar

### 2. Tickets
- `Title`: Brief issue summary
- `Description`: Detailed explanation
- `Category`: Linked to Categories table
- `Status`: Linked to Statuses table
- `Created By`: Relation to Users table
- `Created Time`: Timestamp
- `Last Updated Time`: Auto-updated timestamp
- `Attachment`: Optional file/image

### 3. Comments
- `Ticket`: Relation to Tickets
- `Author`: Relation to Users
- `Comment Body`: Rich text or plain text
- `Timestamp`: Comment creation time

### 4. Categories
- `Category Name`: e.g., Technical, Maintenance, Finance

### 5. Statuses
- `Status Label`: Open, In Progress, Resolved, Closed

### 6. Votes
- `Ticket`: Relation to Tickets
- `Voted By`: Relation to Users
- `Vote Type`: Upvote / Downvote

---

## 🔁 Relationships

- **Users ↔ Tickets** (1:N)
- **Tickets ↔ Comments** (1:N)
- **Users ↔ Comments** (1:N)
- **Tickets ↔ Categories** (M:1)
- **Tickets ↔ Statuses** (M:1)
- **Users ↔ Votes ↔ Tickets** (M:N)

