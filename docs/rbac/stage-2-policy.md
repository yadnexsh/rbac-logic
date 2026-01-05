# Stage 2 — RBAC Access Policy

## Objective
Define the authoritative permission rules and system behavior for access enforcement.
This policy is the single source of truth for all future implementation.



## Protected Actions

All actions require permission checks:

- read
- create
- edit
- delete
- move



## Role Permissions

### Admin
- Allowed: read, create, edit, delete, move
- Forbidden: none

### Editor
- Allowed: read, create, edit
- Forbidden: delete, move

### Viewer
- Allowed: read
- Forbidden: create, edit, delete, move



## Violation Handling

If a user attempts an action they are not permitted to perform:
- The action is denied
- An explicit error message is returned
- The system state remains unchanged



## Unknown Role Handling

- If a role is not recognized, all actions are denied by default
- The system follows a deny-by-default security model



## Multiple Roles per User

- If a user has multiple roles, the highest privilege role is applied
- Privilege order: Admin > Editor > Viewer



## Known Edge Cases

- Requested action is not defined
- User has conflicting roles
- Permissions are misconfigured
- Admin permissions are accidentally restricted
