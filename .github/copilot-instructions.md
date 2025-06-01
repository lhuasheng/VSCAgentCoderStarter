# GitHub Copilot Instructions for Modern Coding Practices

## General Guidelines
- Write clean, readable, and maintainable code.
- Use descriptive names for variables, functions, and classes.
- Add comments for complex logic and public APIs.
- Prefer composition over inheritance.
- Write modular, reusable code.
- Always handle errors and edge cases.

## Next.js (JavaScript/TypeScript)
- Use TypeScript for all new code and components.
- Use functional React components and React hooks.
- Keep components small and focused; one component per file.
- Use CSS Modules or styled-components for styling.
- Use Next.js data fetching methods (getStaticProps, getServerSideProps) appropriately.
- Prefer async/await for asynchronous code.
- Validate props and API responses with TypeScript types or Zod/Yup schemas.
- Use environment variables for configuration, never hardcode secrets.
- Organize code in feature-based folders (e.g., /components, /pages, /lib, /hooks).
- Write unit and integration tests for all business logic and components.
- Use the App Router and follow the project structure: `app/`, `src/components/`, `src/lib/`, `src/stories/`, `prisma/`.
- Integrate with tools like Prisma, NextAuth.js, Supabase, and Inngest as needed.
- Use Tailwind CSS for styling and Framer Motion for animation.
- Use Storybook for component development and testing.
- Follow the deployment and environment setup practices from the Next AI Starter template (e.g., Vercel, Supabase, .env management).

## Python
- Follow PEP 8 style guide for code formatting.
- Use type hints and static type checking (mypy, Pyright).
- Prefer pathlib for file paths and f-strings for formatting.
- Use virtual environments for dependencies.
- Organize code into packages and modules.
- Write docstrings for all public functions, classes, and modules.
- Handle exceptions explicitly and log errors with context.
- Use Black for code formatting and Ruff or Flake8 for linting.
- Write unit tests with pytest or unittest.
- Avoid global variables and side effects in modules.

## Security & Quality
- Never commit secrets or credentials to the repository.
- Validate and sanitize all user input.
- Use environment variables for sensitive configuration.
- Keep dependencies up to date and review for vulnerabilities.
- Write tests for critical paths and edge cases.
- Document all setup, build, and deployment steps in README.md.

## AI Coding & Project Management
- Use a checklist of tasks (e.g., .cursor-tasks.md) to track progress and break down features.
- Use templates (e.g., .cursor-template.xml) for generating task lists and stories.
- Leverage AI coding tools for rapid prototyping and refactoring, but always review and test generated code.
- Follow the best practices and structure from the Next AI Starter template for integrating AI, background jobs, and infrastructure services.

---
These instructions apply to all code generated in this workspace. Follow modern best practices for Next.js, Python, and AI-powered projects. Reference the Next AI Starter template for advanced patterns and integrations.
