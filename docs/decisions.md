# Decisions & Notes

## Why this document exists
This document explains *why* certain choices were made during the project.
It’s mainly for:
- My future self
- Anyone reading the repo who wants to understand the thinking behind it


## Stage 1 – Basics

### Why RBAC?
RBAC (Role-Based Access Control) was chosen because:
- It’s common in real-world products
- Easy to reason about
- A good way to practice permission logic in Python

Stage 1 was only about understanding the concept, not building a full system.

### Roles before users
Roles and permissions were defined first, before adding users.
This felt more natural and closer to how real systems are designed:
rules first, users later.

### No database
Everything is in memory.
This keeps the focus on:
- Python logic
- Clear structure
- Learning fundamentals

Adding storage at this stage would add unnecessary complexity.


## Stage 2 – Policies and logic

### Why policies?
Instead of checking permissions everywhere, rules are grouped as policies.
This makes the system:
- Easier to read
- Easier to modify
- Less error-prone as it grows

### Separation of concerns
Even though the project is small, logic is not dumped into one place.
Roles, actions, and permission checks are treated as separate pieces.
This is mainly to build good habits early.

### Plain Python only
No frameworks or external libraries are used.
The goal is to actually understand how access control works, not hide it behind abstractions.


## Notes for later stages
Some decisions here are intentionally simple.
They may not be production-ready, but they are easy to understand and improve later.
