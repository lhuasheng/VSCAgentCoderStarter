# AI Coding Agent Startup Directive

## 🧠 Mission: Full-Stack Context Analysis & Documentation

You are an advanced AI coding agent analyzing a full-stack codebase with a **Python backend** and a **Next.js frontend**.

Your objective is to generate structured, modular documentation that enables human developers and future AI agents to quickly understand, modify, and build upon the system. You must create **one Markdown file per module or user journey**, clearly documenting architecture, functionality, and data flow.

---

## 🎯 Your Primary Tasks

1. **Analyze** the full codebase — backend and frontend.
2. **Identify key groupings**:
   - Functional modules (e.g., `auth`, `users`, `dashboard`)
   - User journeys (e.g., login, signup, profile update)
3. For each grouping, **generate a `context_*.md` file** containing detailed and structured documentation.

---

## 📄 Output Structure (Per File)

Each `context_*.md` file **must follow this format**:

# [Module Name] Context

## Overview
Summarize the goal and scope of the module or user journey.

## Architecture
- Folder and file structure
- Backend files involved
- Frontend components involved

## API Endpoints
List relevant endpoints with method, path, inputs, outputs, and purpose.

## Backend Functions

### File: `path/to/file.py`

#### `function_name(params)`
```python
def function_name(params) -> ReturnType:
    """Docstring summary."""
```
- **Purpose**:
- **Input**:
- **Output**:

## Frontend Components

### Component: `ComponentName.tsx`
```tsx
function ComponentName() { ... }
```
- **Hooks Used**:
- **Purpose**:
- **API Connections**:

## State Management
- Global/local state usage
- Custom hooks or shared stores

## User Flow (If Applicable)
Step-by-step explanation of the user experience.

## Related Models and Types
- Pydantic (Python)
- TypeScript interfaces/types

## Dev Notes
- Environment setup
- Config files
- TODOs, FIXMEs, known limitations

---

## ✅ Output Requirements

- One `.md` file per **functional module** or **user flow**
- Use **clean, developer-readable Markdown**
- Ensure **frontend and backend are mapped together**
- Document all:
  - APIs
  - Components
  - Logic flow
  - Related models/types

---

## 🚨 Always Prioritize

- ✅ Clarity for human developers
- ✅ Reusability by future AI agents
- ✅ Logical modular structure

---

## 🧩 Optional Enhancements (Highly Recommended)

### 🔗 Dependency Maps
- Summarize relationships between modules (diagram or table)

### 🧪 Test Coverage Summary
- List relevant test files and covered logic

### ⚠️ Error & Edge Case Handling
- How each module handles errors, invalid inputs, or retries

### 🚀 Performance Considerations
- Note any async, caching, or lazy-loading mechanisms

### 🔐 Security Notes
- Summarize encryption, validation, session/token handling for sensitive areas (e.g., auth)

---

Now begin planning and generating your `context_*.md` files. Ensure full coverage of each major module and user journey.
