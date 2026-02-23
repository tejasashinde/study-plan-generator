# Study Plan Generator

**Study Plan Generator** is a agent skill that creates structured, goal-oriented study plans for any subject over a specified time period. It supports both initial plan generation and iterative edits of existing plans, ensuring practical, actionable learning roadmaps.

---

## Features

- **Full Study Plan Generation**
  - Generate plans based on subject and timeline.
  - Includes overview, roadmap, weekly breakdown, daily templates, milestones, and capstone projects.
- **Edit Existing Plans**
  - Modify timeline, intensity, daily hours, milestones, or weekly focus.
  - Preserves structure and logical progression.
  - Versioned saving for iterative improvements.
- **Flexible Constraints**
  - Supports custom hours/day, experience level, and focus (exam prep vs mastery).

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

**Workflow:**

1. Load the existing study plan.
2. Identify requested changes:
   - Specific week, timeline, daily workload, milestones, or difficulty.
3. Apply targeted edits while preserving unaffected sections.
4. Save updated version.
5. Confirm the updated file to the user.

---

# Instructions for Use

1. Download and place the `study-plan-generator` folder inside `skills` folder (.cline/skills OR .claude/skills)
2. Trigger skill using - `make study plan for topic of python django for duration of 1 month`
3. Trigger edit using - `edit the study plan to add/remove ...`


## License

This project is licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.
