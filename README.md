# Study Plan Generator

**Study Plan Generator** is a AI agent skill that creates structured, goal-oriented study plans for any subject over a specified time period. It supports both initial plan generation and iterative edits of existing plans, ensuring practical, actionable learning roadmaps.

---

## Features

- **Full Study Plan Generation**
  - Generate plans based on subject and timeline.
  - Supports overview, roadmap, weekly breakdown, daily templates, milestones, and capstone projects.
- **Edit Existing Plans**
  - Modify timeline, intensity, daily hours, milestones, or weekly focus.
  - Preserves structure and logical progression.
- **Flexible Constraints**
  - Supports custom hours/day, experience level, and focus (exam prep vs mastery).
- **Saves Final Output as Word document(.docx)**

---

## Operational Modes

### 1. Create Mode (Default)

Triggered when the user requests:

- "Create a study plan"
- "Make a learning roadmap"

**Workflow:**

1. Collect mandatory inputs: time period & subject.
2. Optionally clarify constraints: daily hours, intensity, experience.
3. Generate a structured plan:
   - Overview
   - High-Level Roadmap
   - Weekly Breakdown
   - Daily Study Template
   - Milestones
   - Final Capstone
4. Save the plan as `{subject}-{time-period}-study-plan.docx`.

---

### 2. Edit Mode (Refinement Mode)

Triggered when the user requests:

- "Edit the study plan"
- "Modify the file"

**Workflow for edit:**

1. Load the existing study plan.
2. Identify requested changes:
   - Specific week, timeline, daily workload, milestones, or difficulty.
3. Apply targeted edits while preserving unaffected sections.
4. Save updated version.
5. Confirm the updated file to the user.

---

# Instructions for Use

1. Make sure you have Node.js and npm installed on your system (required for using npx).

2. Install this skill using one of the following methods:
   - Using the [`Skills CLI`](https://skills.sh/):
     ```bash
     npx skills add https://github.com/tejasashinde/study-plan-generator
     ```
   - OR manually:
     - Clone the repository.
     - Place the `study-plan-generator` folder inside the `skills` directory (e.g., `.claude/skills`).

3. Trigger the skill using:
   ```bash
   make study plan for topic of python django for duration of 1 month
   ```

## License

This project is licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.
