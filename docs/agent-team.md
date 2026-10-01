# Agent team

I will use GitHub Copilot CLI in a Codespace to coordinate this custom agent team while building Mona's Project Pulse dashboard:

- **Orchestrator** (Claude Opus 4.7): Coordinates the Planner, Designer, and Coder; assigns explicit file scopes, orders dependent work, and verifies that the integrated dashboard is complete. Definition: [.github/agents/orchestrator.agent.md](../.github/agents/orchestrator.agent.md).

- **Planner** (Claude Opus 4.7): Researches the repository and relevant documentation, then produces an implementation plan with file assignments, dependencies, edge cases, and validation expectations. It plans but does not write code. Definition: [.github/agents/planner.agent.md](../.github/agents/planner.agent.md).

- **Designer** (Gemini 3.1 Pro): Shapes the dashboard's usability, accessibility, information hierarchy, responsive behavior, and visual style. For Project Pulse, this includes clear project cards, status and priority treatments, and polished dashboard styling. Definition: [.github/agents/designer.agent.md](../.github/agents/designer.agent.md).

- **Coder** (GPT-5.5): Implements the assigned application behavior and support files, follows repository patterns, and validates the result. For the runnable dashboard, it can create `.vscode/launch.json` to open `app/index.html` in the browser. Definition: [.github/agents/coder.agent.md](../.github/agents/coder.agent.md).
