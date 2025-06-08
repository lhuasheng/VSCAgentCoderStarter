---
applyTo: "**/*.{js,jsx,ts,tsx}"
---
# Next.js (JavaScript/TypeScript) Coding Standards for Copilot

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
- Never commit secrets or credentials to the repository.
- Validate and sanitize all user input.
- Use environment variables for sensitive configuration.
- Keep dependencies up to date and review for vulnerabilities.
- Write tests for critical paths and edge cases.
- Document all setup, build, and deployment steps in README.md.
