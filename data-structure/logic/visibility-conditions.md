# Visibility & Logic Conditions – QuickDesk

This document outlines key conditional logic used in the QuickDesk Glide app to enforce role-based visibility and business workflows.

---

## 🎭 Role-Based Screen Access

| Role     | Can See                                               |
|----------|--------------------------------------------------------|
| User     | My Tickets, Create Ticket, Profile                     |
| Agent    | Assigned Tickets, All Tickets, Ticket Details          |
| Admin    | All Tickets, Category Management, User Management      |

> Implemented using Glide's “User Profile → Role” field in conditional visibility and tab filtering.

---

## 📝 Ticket Status Logic

| Status        | Who Can Change     | Next Status Options            |
|---------------|--------------------|--------------------------------|
| Open          | Agent/Admin        | In Progress, Resolved          |
| In Progress   | Agent/Admin        | Resolved                       |
| Resolved      | Agent/Admin        | Closed                         |
| Closed        | —                  | — (read-only)                  |

> Buttons for status updates are conditionally shown based on the ticket's current status and the signed-in user’s role.

---

## 💬 Comment Visibility

- Users see only their own tickets and related comments.
- Agents see all comments on tickets they are assigned to.
- Admins see all comments.

---

## 🔍 Filtering Logic (on ticket list)

- **Users:** Filter to "Created By = Current User"
- **Agents:** View all or assigned tickets, filter by:
  - Category
  - Status
  - Last Updated
  - Most Commented
- **Admins:** Access to all filtering options, plus dashboards

---

## 👍 Voting Logic

- Each user can only vote once per ticket.
- Votes are shown as a counter (Upvotes – Downvotes).
- Vote buttons are conditionally disabled if the user has already voted.

---

## 🔔 Notifications Logic

- Email sent when:
  - A ticket is created
  - Status is updated
  - Agent responds with a comment

> Uses Glide’s built-in “Send Email” action or optional Make.com integration for richer formatting.

