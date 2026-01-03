
![Image](https://capsule-render.vercel.app/api?type=blur&height=300&color=gradient&text=rbac-logic)

<p align="center">RBAC is a system where user roles determine which actions a user is allowed to perform in a system


#### Objective
Define the core roles, their allowed actions, and the forbidden actions in the system.  
Introduce the concept of Role-Based Access Control (RBAC).

#### Roles
1. **Admin**
   - Can perform all actions on files (move, edit, delete, create, read)
2. **Editor**
   - Can create and edit files where allowed
   - Cannot delete or move files
3. **Viewer**
   - Can only read files
   - Cannot create, edit, delete, or move files

#### Actions
- move file
- edit file
- delete file
- create file
- read file

#### Forbidden Actions
- Viewer: cannot delete, edit, move, or create  
- Editor: cannot delete or move  
- Admin: (no restrictions)

