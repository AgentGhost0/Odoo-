# QuickDesk – Help Desk Ticketing System

**QuickDesk** is a no-code help desk platform built using **Glide Tables**, designed for internal support within organizations like colleges or companies. It allows users to raise and track tickets, while support agents and admins manage and resolve them with ease.

---

## 🎯 Features

- ✍️ Create support tickets with attachments and category
- 📊 Status flow: Open → In Progress → Resolved → Closed
- 🧑‍🤝‍🧑 Role-based dashboard (User, Agent, Admin)
- 💬 Threaded comments on tickets
- 🔍 Filter by status, category, reply count, or recency
- 👍 Upvote/downvote support questions
- 📩 Email notifications on ticket creation or updates

---

## 🧱 Stack

| Layer        | Tech         |
|--------------|--------------|
| Frontend     | Glide App    |
| Backend/Data | Glide Tables |
| Automation   | Glide built-in actions (optional: Make/Zapier) | (Yet to be implemented)

---

## 👥 Roles

- **End User**: Create & track tickets, reply, vote
- **Agent**: View and manage tickets, update status, comment
- **Admin**: Manage categories, assign roles, view all activity

---

## 🗂️ Data Tables

Documented in [`/data-structure/glide-tables.md`](./data-structure/glide-tables.md)

---

## 🧠 Logic

- Role-based visibility for screens and actions
- Conditional button visibility (based on ticket status or user)
- Dynamic filtering for tickets by multiple parameters
- Comment threading using relations and timestamps

Detailed logic in [`/logic`](./logic)

---

## 🌐 Live App

[Access QuickDesk App](https://private-mine-3240.glide.page)

---

## 📸 Screenshots

See `/assets/` folder for UI and demo GIFs.

---

## 📄 License

[MIT License](./LICENSE)

---

## 👏 Made for Hackathon

