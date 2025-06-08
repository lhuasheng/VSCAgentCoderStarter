# PromptV2: Modular AI Workflow for Autonomous Coding Agents

This folder contains a modular set of prompts for orchestrating a full-stack software development workflow using specialized AI agents. Each prompt assigns a specific role and responsibility, enabling a team of AI agents to analyze, plan, execute, and review a project from any starting point (greenfield or ongoing).

## Entry Point: How to Use This Workflow

1. **Start Here:**
   - Review the current codebase and planning artifacts.
   - Assign each step to a specialized AI agent as described below.

---

## AI Agent Roles & Prompt Sequence

1. **Codebase Analyst** (`01_codebase_analysis.md`)
   - Analyze the codebase, summarize modules, user journeys, and existing work.
   - Output: Codebase summary, module list, completed/in-progress/missing features.

2. **Context Documentarian** (`02_context_generation.md`)
   - For each module/user journey, generate a detailed context file (architecture, APIs, flows, types, dev notes).
   - Output: `context_*.md` files for all major modules and flows.

3. **Requirements Facilitator** (`03_requirements_gathering.txt`)
   - Review existing work, then prompt the user for business goals, features, and constraints.
   - Output: Summarized requirements, ready for BRD.

4. **BRD Architect** (`04_brd_template.txt`)
   - Create or update the Business Requirements Document (BRD) using user input and existing artifacts.
   - Output: Comprehensive BRD.

5. **PRD Architect** (`05_prd_template.txt`)
   - Create or update the Product Requirements Document (PRD) from the BRD and codebase.
   - Output: Detailed PRD.

6. **Story Mapper** (`06_story_task_breakdown.txt`)
   - Break down the PRD into one-story-point user stories and granular tasks, or update existing ones.
   - Output: User stories and tasks, mapped to sprints.

7. **Checklist Engineer** (`07_checklist_generation.txt`)
   - Generate or update a detailed markdown checklist for implementation.
   - Output: Exhaustive, actionable checklist.

8. **Execution Agent** (`08_execution_kickoff.txt`)
   - Execute the checklist: review, code, test, build, commit, and update progress.
   - Output: Completed tasks, updated checklist, ready for review.

9. **Quality Reviewer** (`09_design_rubric.md`)
   - Review completed work using the design and implementation rubric.
   - Output: Rubric scores, improvement notes, and final review.

---

## Best Practices
- Always review existing code, documentation, and planning artifacts before starting a new phase.
- Cross-reference context, requirements, and checklists for consistency.
- Use the rubric for every review and acceptance step.
- Document all outputs and decisions for future agents and human collaborators.

---

**To begin:** Assign the Codebase Analyst role and follow the sequence above, passing outputs between agents as you progress.
