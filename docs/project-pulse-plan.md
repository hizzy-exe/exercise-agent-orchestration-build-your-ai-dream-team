# Project Pulse dashboard plan

## Summary

Build a small static Project Pulse dashboard for Mona's team using a coordinated agent workflow. The final result should be a polished, contributor-friendly dashboard that presents active projects, owners, status, recent activity, priority, and a concise summary in a clear card-based layout. The app should run from the `app/` directory and open `index.html` via a VS Code launch configuration named `Run Project Pulse Dashboard`.

## Scope and targeted files

- `app/index.html` – dashboard structure, semantic HTML, project cards, status badges, summary sections, and script hook points
- `app/styles.css` – visual design, layout system, card styling, status/priority treatments, responsive behavior, and spacing
- `app/project-data.json` – top-level `projects` array containing `name`, `owner`, `status`, `recentActivity`, and `priority`
- `.vscode/launch.json` – strict JSON launch configuration that serves `app/` and opens `index.html` locally

## Phase plan

### Phase 1: Planning and requirements alignment

- Orchestrator defines the work order and file ownership.
- Planner reviews the brief, confirms the accepted dashboard behaviors, and turns the brief into a concrete execution plan.
- Deliverable: a clear implementation plan with sequence, file ownership, and dependencies.

### Phase 2: UI/UX design and information hierarchy

- Designer defines the dashboard layout, hierarchy, status treatment, card design, and accessibility decisions.
- Designer should specify how the first screen should feel: clear heading, visible project cards, strong status badges, and readable spacing.
- Output informs the HTML and CSS structure and the data model used by the app.

### Phase 3: Data and front-end implementation

- Coder builds the actual static dashboard in `app/index.html` and `app/styles.css`.
- Coder also creates the data file in `app/project-data.json` using the required top-level `projects` array and required fields.
- Coder validates the app structure and ensures the page renders with the expected project data.

### Phase 4: Launch configuration and final validation

- Coder creates `.vscode/launch.json` using strict JSON and the required `cwd` to `${workspaceFolder}/app`.
- The launch target must open `index.html` so the dashboard appears instead of a directory listing.
- Orchestrator checks the end-to-end result and confirms the final handoff is complete.

## Designer responsibilities

The Designer is responsible for:

- dashboard layout and information hierarchy
- project card structure and readability
- visible status and priority treatment
- accessibility and contrast choices
- spacing, typography, rounded corners, shadows, and responsive layout
- ensuring the first view clearly reads as a polished Project Pulse dashboard

## Coder responsibilities

The Coder is responsible for:

- implementing the static HTML structure in `app/index.html`
- translating design decisions into CSS in `app/styles.css`
- creating the project dataset in `app/project-data.json`
- generating the strict JSON launch configuration in `.vscode/launch.json`
- validating the final static app renders as intended and can be launched from VS Code

## Dependencies

- The planner output must be approved before implementation begins.
- The Designer output should precede the final HTML/CSS implementation so layout and styling decisions are anchored to the intended UI structure.
- The Coder depends on the project data contract (`projects`, `name`, `owner`, `status`, `recentActivity`, `priority`) before rendering the cards.
- The launch configuration depends on the final app structure and should be created after the `app/` files are in place.
- The final validation depends on all dashboard files being present and compatible.

## Parallel work decisions

- Parallelizable work: initial repo review, brief analysis, and planner research can happen in parallel with early design exploration, as long as they do not overlap file ownership.
- Sequential work: the Designer’s decisions should happen before the Coder finalizes CSS; the data contract should be defined before the HTML is wired to rendering logic.
- The `.vscode/launch.json` file should only be created after the app layout is stabilized, because the launch target depends on the final file layout and the dashboard entry page.
- Avoid overlapping edits to the same file across specialist agents; each file should have a single responsible owner for the implementation phase.

## Validation expectations

The completed dashboard should satisfy the following checks:

1. `app/index.html` renders a dashboard-like page, not a blank or generic directory page.
2. `app/styles.css` contains dashboard styling with visible project cards and status/priority treatments.
3. `app/project-data.json` contains a top-level `projects` array and includes `name`, `owner`, `status`, `recentActivity`, and `priority`.
4. `.vscode/launch.json` is valid JSON, uses `cwd` as `${workspaceFolder}/app`, and opens `index.html`.
5. The launch configuration is named `Run Project Pulse Dashboard` and serves the app directory so the dashboard opens correctly.
6. The page is polished, readable, and responsive enough to present project health at a glance.
7. The result aligns with the project brief: contributor-friendly summary, status visibility, ownership clarity, recent activity, and priority awareness.

## Recommended execution order

1. Planner researches the brief and repository.
2. Designer defines the dashboard layout and design language.
3. Coder implements the app files and launch setup.
4. Orchestrator validates the full result and confirms completion.

This plan keeps the work organized, preserves file ownership, and aligns the implementation with the Project Pulse brief while staying consistent with the custom agent workflow in `.github/agents/`.
