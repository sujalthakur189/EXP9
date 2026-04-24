# Experiment 3.1.3 – Role-Based Access Control (RBAC)

## Aim
To implement RBAC with role-specific routes and API access restrictions.

## Setup

### Terminal 1 – Backend
```bash
cd rbac-app/server
npm install
node server.js
# Server runs at http://localhost:3001
```

### Terminal 2 – Frontend
```bash
cd rbac-app/client
npm install
npm start
# App runs at http://localhost:3000
```

## Test Credentials
| Role  | Username | Password |
|-------|----------|----------|
| Admin | admin    | admin123 |
| User  | user     | user123  |

## Role Permissions
| Route     | Admin | User |
|-----------|-------|------|
| /profile  | ✅    | ✅   |
| /admin    | ✅    | ❌   |

Additional RBAC behavior:
- Role hierarchy is enforced for protected frontend routes.
- Permission-based middleware is enforced for protected backend APIs.
- Role-based menu options are shown in the UI.

## Key Technologies
- React 18 + React Router 6 + Context API
- Express 4 + jsonwebtoken 9
- Role-based middleware (`requireRole`) + permission middleware (`requirePermission`)
