# AI Agent Prompt: Deep Codebase Analysis for Python Backend + Next.js Frontend

You are an AI coding agent assigned to analyze a full-stack project consisting of a **Python backend** and a **Next.js frontend**. Your task is to extract **comprehensive architectural context** and **detailed documentation**, and save everything into a structured `context.md` file. This file will help another AI or developer understand and work with the codebase efficiently.

---

## 🔧 Your Tasks

1. **Read and analyze the full codebase**, including both backend and frontend.
2. Extract both:
   - **High-level architecture and flow**
   - **Low-level function/component-level understanding**
3. Document the following:
   - Function and method docstrings
   - Purpose and behavior of each component or function
   - Inputs/outputs and data contracts
4. Store everything in a **Markdown file named `context.md`** using the structure below.

---

## 📄 Required `context.md` Structure

```markdown
# Project Overview
Brief summary of the project, main functionality, and how frontend communicates with backend.

# Python Backend

## Framework & Project Structure
- Backend framework (e.g., FastAPI, Django)
- Entry point(s) of the app
- Folder/module structure with short descriptions

## API Routes & Services
List all API endpoints, grouped by module or router.

### Example: `/api/users`
- `GET /users`: Retrieves all users
- `POST /users`: Creates a new user
- Located in: `users.py`

## Functions (Detailed)

### Module: `app/users.py`

#### `get_users()`
```python
def get_users() -> List[User]:
    """Retrieve all users from the database."""
```
- **Purpose**: Fetches user list.
- **Returns**: List of `User` objects.

#### `create_user(user: UserCreate)`
```python
def create_user(user: UserCreate) -> User:
    """Create and persist a new user."""
```
- **Purpose**: Inserts a user into the DB.
- **Parameters**: `user` - validated user input
- **Returns**: The created `User` record

(Repeat for all significant functions)

## Data Models
- Document key ORM or Pydantic models, with field types and purposes.

## Configuration
- Configuration strategy (`.env`, `settings.py`)
- Environment tools (Docker, poetry, pipenv, etc.)

# Next.js Frontend

## Structure & Routing
- Pages vs App Directory
- Routing structure
- SSR, SSG, or CSR usage

## Components (Detailed)

### Component: `UserTable.tsx`
```tsx
function UserTable({ users }: { users: User[] }) {
    ...
}
```
- **Props**: `users: User[]`
- **Hooks Used**: `useEffect`, `useState`
- **Purpose**: Displays a user table.
- **Data Source**: Calls `GET /api/users`

(Repeat for all relevant components)

## API Integration
- HTTP client used (fetch, Axios, SWR)
- Endpoint mappings
- Data fetching patterns

## State Management
- Global (Redux, Context API, Zustand)
- Local state strategies

# Backend–Frontend Integration
- Authentication mechanism
- Data contracts (OpenAPI, shared schemas)

# Development & Deployment
- Setup instructions
- Scripts and CI/CD pipelines
- Docker or virtualenv usage

# TODOs and Known Issues
- Extract `TODO`, `FIXME`, or `# NOTE` comments
- Mention known issues or deprecated areas

# Getting Started Tips
- Suggested file/modules to read first
- Fragile areas to watch out for
```

---

## ✅ Output Format Guidelines

- Use fenced code blocks with language identifiers (e.g., ` ```python `, ` ```tsx `)
- Ensure consistent, readable Markdown formatting
- Write in a way that helps both human developers and AI agents

---

Begin now and produce the `context.md` file.
