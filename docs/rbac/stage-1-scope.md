# Stage 1 — System Scope & Access Model

## Objective
Define the roles, actions, and high-level access boundaries of the system.
This stage focuses on what the system allows, not how it is implemented.


## Roles

### Admin
Represents a system owner or administrator with full control.

**Intent**
- Manage files and system-level actions
- Has the highest level of access



### Editor
Represents a user who can create and modify content.

**Intent**
- Work on files and content
- Cannot perform destructive or structural actions


### Viewer
Represents a read-only user.

**Intent**
- Consume content
- Must never modify system data



## Actions

The system supports the following user actions:

- read — view file contents
- create — create new files
- edit — modify existing files
- delete — remove files
- move — change file location


## High-Level Role → Action Mapping

| Role   | Allowed Actions                     |
|--------|-------------------------------------|
| Admin  | read, create, edit, delete, move    |
| Editor | read, create, edit                  |
| Viewer | read                                |



## Access Boundaries

- Viewer must never create, edit, delete, or move files
- Editor must never delete or move files
- Admin has no restrictions



## RBAC Definition (System Context)

Role-Based Access Control (RBAC) is a mechanism where a user’s role determines which actions they are permitted to perform within the system.
