# Customizing GitHub Copilot for Agentic Code Generation

This guide explains how to configure GitHub Copilot in VS Code for advanced, agentic code generation workflows. It covers setting up custom code generation instructions, using templates, and integrating best practices for Next.js, Python, and AI-powered projects.

Inspired by https://github.com/kleneway/next-ai-starter - creating this for my own convenience.

## 1. Create Agentic Code Generation Instructions

1. In your project, create a file at `.github/copilot-agentic-template.md` with your agentic code generation template. For example:

    ```markdown
    <TEMPLATE>
    <INSTRUCTIONS>
    Use the <CODEBASE> code as reference, and convert the high-level <TASK> into a set of very detailed step-by-step instructions that an AI coding agent can complete. This could be very long, that's okay. The entire code is not needed, but give snippets if needed, but be very specific about the file names.
    Only include steps an AI coding agent can take. Do not include testing or any other work a human would do to confirm the task has been completed.
    ALWAYS have the agent run a build when it is complete. Be specific and decisive about what the agent should do.
    Do not include any additional meta instructions to the user. Use markdown formatting.
    </INSTRUCTIONS>
    <TASK>
    </TASK>
    <CURSOR_RULES>
    </CURSOR_RULES>
    <CODEBASE>
    </CODEBASE>
    <INSTRUCTIONS>
    Use the <CODEBASE> code as reference, and convert the high-level <TASK> into a set of very detailed step-by-step instructions that an AI coding agent can complete. This could be very long, that's okay. The entire code is not needed, but give snippets if needed, but be very specific about the file names.
    Only include steps an AI coding agent can take. Do not include testing or any other work a human would do to confirm the task has been completed.
    ALWAYS have the agent run a build when it is complete. Be specific and decisive about what the agent should do.
    Do not include any additional meta instructions to the user. Use markdown formatting.
    </INSTRUCTIONS>
    </TEMPLATE>
    ```

## 2. Configure VS Code Settings

1. Open your VS Code `settings.json` (User or Workspace settings).
2. Add or update the following setting to point Copilot to your agentic template:

    ```jsonc
    "github.copilot.chat.codeGeneration.instructions": [
        { "file": ".github/copilot-agentic-template.md" }
    ]
    ```

    This tells Copilot Chat to use your custom template for code generation instructions.

## 3. Provide Modern Coding Practice Instructions

1. (Recommended) Add instruction files in `.github/instructions/` for your coding standards and best practices. Example files:

    - `.github/instructions/general.instructions.md` — General coding, onboarding, and knowledge transfer practices for all languages and roles.
    - `.github/instructions/python.instructions.md` — Python-specific standards.
    - `.github/instructions/nextjs.instructions.md` — Next.js/TypeScript/React-specific standards.

    These files will be automatically picked up by Copilot if you are using the latest Copilot extension and VS Code (see [Copilot Customization Docs](https://code.visualstudio.com/docs/copilot/copilot-customization#_use-instructionsmd-files)).

    Example for `general.instructions.md`:

    ```instructions
    ---
    applyTo: "**"
    ---
    # General Coding & AI Project Guidelines for Copilot
    - Write clean, readable, and maintainable code.
    - Use descriptive names for variables, functions, and classes.
    - Add comments for complex logic and public APIs.
    - Prefer composition over inheritance.
    - Write modular, reusable code.
    - Always handle errors and edge cases.
    - Use a checklist of tasks (e.g., .cursor-tasks.md) to track progress and break down features.
    - Use templates (e.g., .cursor-template.xml) for generating task lists and stories.
    - Leverage AI coding tools for rapid prototyping and refactoring, but always review and test generated code.
    - Follow the best practices and structure from the Next AI Starter template for integrating AI, background jobs, and infrastructure services.
    - Never commit secrets or credentials to the repository.
    - Validate and sanitize all user input.
    - Use environment variables for sensitive configuration.
    - Keep dependencies up to date and review for vulnerabilities.
    - Write tests for critical paths and edge cases.
    - Document all setup, build, and deployment steps in README.md.
    - Provide onboarding documentation and checklists for new team members (e.g., setup steps, key contacts, project overview).
    - Encourage mentorship and knowledge sharing within the team.
    - Maintain up-to-date documentation for key decisions, architecture, and processes to support knowledge transfer.
    - Ensure departing team members document critical knowledge and hand off responsibilities effectively.
    ```

## 4. Example Workspace Files

- `.github/copilot-agentic-template.md` — Your agentic code generation template.
- `.github/instructions/general.instructions.md` — General coding standards and onboarding/knowledge transfer practices.
- `.github/instructions/python.instructions.md` — Python-specific standards.
- `.github/instructions/nextjs.instructions.md` — Next.js/TypeScript/React-specific standards.
- `.env` — Example environment variables for your stack.

## 5. Tips for Agentic Coding Workflows

- Use checklists (e.g., `.cursor-tasks.md`) to break down features for AI agents.
- Use templates (e.g., `.cursor-template.xml`) to generate task lists and stories.
- Always review and test generated code.
- Reference the Next AI Starter template for advanced patterns and integrations.

## 6. Further Customization

- You can add multiple instruction files or update your template as your workflow evolves.
- For more details, see the [Copilot Customization Docs](https://code.visualstudio.com/docs/copilot/copilot-customization).

---

By following these steps, you can fully customize Copilot to generate code and instructions tailored to your agentic, modern development workflow.
