# Task Tracker

### What you'll build

A team task tracker with per-team views, status tracking, and assignments — a lightweight alternative to dedicated project management tools.

{% hint style="info" %}Screenshot needed: task tracker Grid view from your team space{% endhint %}

### Concepts used

- [Channels](../../getting-started/vault-and-key/space.md) — a shared Channel for your team
- [Types](../../getting-started/types/README.md) — the built-in Task Type
- [Properties](../../getting-started/types/relations.md) — Status, Assignee, Priority, Due Date, Team
- [Queries](../../getting-started/sets/README.md) — filtered views per team or per person
- [Templates](../../getting-started/types/templates.md) — for consistent task creation

### Step-by-step setup

1. **Set up the Task Type.** Open Channel Settings > Content Model > Object Types and find the built-in Task Type. Add or adjust Properties:
   - **Select:** "Status" (To Do, In Progress, In Review, Done)
   - **Select:** "Priority" (Low, Medium, High, Urgent)
   - **Object:** "Assignee" (links to a Person or Member)
   - **Select:** "Team" (if your Channel has multiple teams)
   - **Date:** "Due Date"
2. **Create a Template.** Set up a Task Template with default Properties pre-filled (e.g., Status: To Do, Priority: Medium).
3. **Create team-specific Queries.** For each team, create a Query by Type: Task, filtered by Team. Switch to Grid view for a spreadsheet-like overview, or Board view to see tasks organized by Status.
4. **Create a "My Tasks" Query.** Filter by Assignee: yourself. Pin it to the sidebar for a personal task view.
5. **Pin the main Queries to the sidebar.** Team leads can see their team's board, while individual contributors see their own tasks.

{% hint style="info" %}
**Tip:** Use the Board layout with Status as the grouping property to get a Kanban-style view of your team's work.
{% endhint %}

For more templates, check out the [ANY Experience Gallery](../../advanced/community/any-experience-gallery.md).
