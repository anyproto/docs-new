# Project Board

### What you'll build

A project management board that tracks initiatives across your team — each project as an Object with linked tasks, timelines, and status.

{% hint style="info" %}Screenshot needed: project board view from your team space{% endhint %}

### Concepts used

- [Types](../../getting-started/types/README.md) — a "Project" Type
- [Properties](../../getting-started/types/relations.md) — Status, Owner, Start/End Date, Team
- [Queries](../../getting-started/sets/README.md) — a board view of all projects
- [Collections](../../getting-started/sets/collections.md) — to group tasks and docs under each project
- [Links](../../getting-started/object-editor/linking-objects.md) — to connect tasks to their project

### Step-by-step setup

1. **Create a "Project" Type.** Add Properties:
   - **Select:** "Status" (Planning, In Progress, On Hold, Completed)
   - **Object:** "Owner" (the person responsible)
   - **Select:** "Team" (Engineering, Design, etc.)
   - **Date:** "Start Date" and "Target Date"
2. **Create your first Project Object.** Name it, fill in the Properties, and use the body to describe the project goals and scope.
3. **Link tasks to the project.** Add an **Object** property called "Project" to your Task Type. When creating tasks, link them to the relevant project. This lets you see all tasks for a project through its backlinks.
4. **Create a Projects Query.** Filter by Type: Project. Use Board view grouped by Status to see your project pipeline at a glance. Or use Grid view to see timelines and owners.
5. **Create per-project Collections.** For each major project, create a Collection containing the Project Object, its tasks, design docs, meeting notes, and any other related Objects.
6. **Pin the Projects Query to the sidebar.** This becomes your team's project dashboard.

For more templates, check out the [ANY Experience Gallery](../../advanced/community/any-experience-gallery.md).
