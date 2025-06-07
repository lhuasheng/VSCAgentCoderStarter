# AI Agent Prompt: Structured Context Planning and Multi-File Extraction

You are an advanced AI coding agent analyzing a full-stack project composed of a **Python backend** and a **Next.js frontend**. Your job is to **analyze, organize, and document the system** by creating **multiple structured context files**, grouped by **user journeys** and **project modules**.

---

## 🎯 Objective

1. **Understand the entire codebase**, including backend and frontend.
2. **Identify logical groupings** of code based on:
   - Functional modules (e.g., `auth`, `users`, `dashboard`)
   - User journeys (e.g., signup, login, profile management)
3. For each grouping, **generate a separate `context_*.md` file** that documents:
   - Architecture
   - Function and component details
   - Related API endpoints and data models
   - Configuration, state, and integration logic
   - Flow of the user journey or module

---

## 🗂 How to Organize the Context Files

Generate one `context_*.md` file per functional domain or user journey. Examples:

- `context_auth.md` – Covers login, signup, session handling, auth middleware
- `context_users.md` – User profiles, updates, listing, roles
- `context_dashboard.md` – Main dashboard flow and widgets
- `context_shared.md` – Shared utilities, types, hooks, models

---

## 📄 Required Format for Each `context_*.md` File

```markdown
# [Module/User Journey Name] Context

## Overview
Describe the purpose of this module or journey. Explain what features it covers.

## Architecture
- Folder and file structure
- Backend files involved
- Frontend components involved

## API Endpoints
List and describe all relevant backend endpoints.

## Backend Functions

### File: `app/auth.py`

#### `login_user(credentials: LoginInput)`
```python
def login_user(credentials: LoginInput) -> AuthResponse:
    """Validate user credentials and return access token."""
```
- **Purpose**: Login logic
- **Input**: `LoginInput` from form
- **Output**: `AuthResponse` with token

(Repeat for each function)

## Frontend Components

### Component: `LoginForm.tsx`
```tsx
function LoginForm() { ... }
```
- **Hooks Used**: `useForm`, `useState`
- **Purpose**: Handles login UI and sends form to `/api/auth/login`

## State Management
- Describe global and local state usage
- Note custom hooks or shared stores

## User Flow (If Applicable)
Outline the user journey this file supports.

### Example: "User logs in"
1. Enters credentials into `LoginForm`
2. Calls `POST /api/auth/login`
3. Backend runs `login_user()`
4. Token is returned and stored
5. UI navigates to `/dashboard`

## Related Models and Types
- Pydantic models
- TypeScript interfaces

## Dev Notes
- Config files
- Environment setup
- TODOs, FIXMEs, known issues
```

---

## ✅ Output Requirements

- Generate multiple `.md` files — one per module or journey
- Use clean and consistent Markdown
- Write for both human developers and future AI agents

---

Now plan and generate the complete set of `context_*.md` files based on the codebase structure and user flows.
