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

1. (Optional but recommended) Add a file at `.github/copilot-instructions.md` with your coding standards and best practices. Example:

    ```markdown
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
    - ...
    ```

## 4. Example Workspace Files

- `.github/copilot-agentic-template.md` — Your agentic code generation template.
- `.github/copilot-instructions.md` — Modern coding standards for Copilot.
- `.env` — Example environment variables for your stack.

## 5. Tips for Agentic Coding Workflows

- Use checklists (e.g., `.cursor-tasks.md`) to break down features for AI agents.

  **Example Tasks for a "Hello, World!" Project**
  This file outlines a set of tasks for building a simple Next.js project. In this project, the user enters their name in a text box on the Home Page and is then greeted with "Hello, {name}" on a separate Greeting Page.

  Here's an example prompt to use to generate this. Note that you'll first want to either provide a detailed set of notes / PRD of exactly what to build, or have a two-step process where you have the AI create the spec, then proceed with this step. Be sure to use an advanced thinking model with this, ideally "Deep Research" from OpenAI but o1-pro, o3-mini, flash-2-thinking, or (maybe?) DeepSeek R1 could work as well.

  Create a very very very detailed markdown checklist of all of the stories for this project plan, with one-story-point tasks (with unchecked checkboxes) that break down each story. It is critically important that all of the details to implement this are in this list. Note that a very competent AI Coding Agent will be using this list to autonomously create this application, so be sure not to miss any details whatsoever, no matter how much time and thinking you must do to complete this very challenging but critically important task.

  After you generate this task list, here is a prompt to use in cursor agent to kick this off (might be useful to put at the end of your cursorrules file as well?) Probably helpful to just @include the cursor-tasks.md file as well.

  Go through each story and task in the .cursor-tasks.md file. Find the next story to work on. Review each unfinished task, correct any issues or ask for clarifications (only if absolutely needed!). Then proceed to create or edit files to complete each task. After you complete all the tasks in the story, update the file to check off any completed tasks. Run builds and commits after each story. Run all safe commands without asking for approval. Continue with each task until you have finished the story, then stop and wait for me to review.

- Use templates (e.g., `.cursor-template.xml`) to generate task lists and stories.
- Always review and test generated code.
- Reference the Next AI Starter template for advanced patterns and integrations.

## 6. Further Customization

- You can add multiple instruction files or update your template as your workflow evolves.
- For more details, see the [Copilot Customization Docs](https://code.visualstudio.com/docs/copilot/copilot-customization).

---

By following these steps, you can fully customize Copilot to generate code and instructions tailored to your agentic, modern development workflow.
