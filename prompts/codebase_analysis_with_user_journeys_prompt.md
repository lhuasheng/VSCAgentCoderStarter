# AI Agent Prompt: Deep Codebase Analysis for Python Backend + Next.js Frontend

You are an AI coding agent assigned to analyze a full-stack project consisting of a **Python backend** and a **Next.js frontend**. Your task is to extract **comprehensive architectural context**, **detailed function-level documentation**, and **user journeys** from a product perspective. Store everything in a structured `context.md` file.

---

## 🔧 Your Tasks

1. **Read and analyze the entire codebase**, backend and frontend.
2. Extract:
   - **High-level architecture and execution flow**
   - **Function-level and component-level details**
   - **All available docstrings**
   - **Inputs/outputs for each function or component**
3. As a **senior product manager**, identify and describe key **user journeys** based on the code and UI logic.
4. Write everything to a file named `context.md`, following the structure below.

---

## 📄 Required `context.md` Structure

```markdown
# Project Overview
Summary of what the project does, its primary purpose, and how the backend and frontend interact.

# Python Backend

## Framework & Project Structure
- Framework (e.g., FastAPI, Flask)
- Entry points
- Folder/module layout and roles

## API Routes & Services
Document key endpoints grouped by module.

### Example: `/api/users`
- `GET /users`: Get user list
- `POST /users`: Add a new user

## Functions (Detailed)

### Module: `users.py`

#### `get_users()`
```python
def get_users() -> List[User]:
    """Retrieve all users from the database."""
```
- **Purpose**: Fetch user list
- **Returns**: `List[User]`

#### `create_user(user: UserCreate)`
```python
def create_user(user: UserCreate) -> User:
    """Insert a new user record into the database."""
```
- **Purpose**: Adds a user
- **Parameters**: `user` - validated payload
- **Returns**: `User` object

(Repeat for all important functions)

## Data Models
Describe all ORM or Pydantic models, with fields, types, and purpose.

## Configuration
Explain how configuration is handled (e.g., `.env`, settings modules) and environment setup (Docker, pipenv, etc.)

# Next.js Frontend

## Structure & Routing
- App or Pages directory
- Routing logic
- Use of SSR/SSG/CSR

## Components (Detailed)

### `UserTable.tsx`
```tsx
function UserTable({ users }: { users: User[] }) {
    ...
}
```
- **Props**: `users: User[]`
- **Hooks Used**: `useState`, `useEffect`
- **Purpose**: Display paginated user list
- **API Calls**: `GET /api/users`

(Repeat for each key component)

## API Integration
- How frontend fetches data (fetch, Axios, SWR)
- Endpoint mappings

## State Management
- Global: Redux, Zustand, Context API
- Local state and props handling

# Backend–Frontend Integration
- Auth flow (tokens, cookies, sessions)
- Data contract management (shared types, OpenAPI, schema generation)

# Development & Deployment
- How to run locally
- Dev scripts, Docker usage
- CI/CD pipelines

# TODOs and Known Issues
- Collect all `TODO`, `FIXME`, or `NOTE` comments
- Outline known issues or deprecated sections

# Getting Started Tips
- What to read and run first
- Tricky areas, fragile modules

# User Journeys (Product Perspective)

From the perspective of a senior product manager, outline the most important user journeys based on application behavior:

## Example User Journey: New User Signup
1. **Frontend**: User fills out signup form at `/signup`.
2. **Frontend**: Form data submitted to `POST /api/users`.
3. **Backend**: `create_user()` validates and saves the user.
4. **Backend**: Returns 201 response with user ID.
5. **Frontend**: Navigates to `/dashboard`.

## Example User Journey: Viewing User Dashboard
1. **Frontend**: User logs in via `/login`.
2. **Frontend**: On success, fetches `GET /api/users/{id}`.
3. **Backend**: Returns user profile and dashboard data.
4. **Frontend**: Renders dashboard view.

Document 2–5 such journeys, including:
- User actions
- Corresponding UI components
- Triggered API endpoints
- Backend functions and data flow

```

---

## ✅ Output Format Guidelines

- Use fenced code blocks with language identifiers (` ```python `, ` ```tsx `, ` ```markdown `)
- Use clear Markdown hierarchy and bullet points
- Write so it is useful for both human and AI readers

---

Begin now and generate the complete `context.md` file.
