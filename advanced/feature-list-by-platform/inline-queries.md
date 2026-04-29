---
description: Display a live filtered view of Objects directly inside another Object.
---

# Inline Queries

### What is an Inline Query?

An **Inline Query** is a Query embedded inside another Object. Instead of opening a separate Query as its own page, you display the Query's results directly in the editor — alongside your text, images, and other blocks.

The Query stays live: as Objects are added, modified, or removed in your Channel, the inline display updates automatically.

### Why it matters

Inline Queries turn ordinary pages into **dashboards**. A project page can show:

- A list of all open tasks for that project
- A gallery of related documents
- A status board grouped by progress
- Recent activity from team members

…all rendered live, all in one Object. You don't have to click into a separate Query page to see what's happening — it's right there.

This pattern is especially valuable for:

- **Project hubs** — one page that gives you the full view of a project
- **Personal dashboards** — your homepage with "today's tasks", "this week's notes", "in-progress reading"
- **Team docs** — a documentation page with embedded queries of related decisions, RFCs, or specs
- **Type pages** — when you open a Type, the built-in Query shows all Objects of that Type. The same pattern works inline anywhere.

### How it works

An Inline Query has two parts:

1. **The source** — a Query you've already created, OR a new Query defined inline
2. **The view** — how it's displayed (Grid, List, Gallery, Board, Calendar, etc.)

The source is **shared** with any other place that uses the same Query — change the filter on the source, and every inline reference updates. The view is **per-block** — change the layout in one inline reference, and other places using the same Query keep their own layout.

This separation is intentional: the *what* (filter, sort, source) is centralized, but the *how* (visual presentation) is contextual.

### Creating an Inline Query

#### Method 1: Embed an existing Query

If you've already created a Query you want to show in another Object:

1. In the editor, type `/inline`.
2. Choose **Inline Query** from the menu.
3. Search for the existing Query by name and select it.
4. The Query renders inline using the default view from the source.

#### Method 2: Create a new inline Query from scratch

If you want a one-off Query that lives only inside this Object:

1. Type `/inline`.
2. Choose **New Inline Query**.
3. Pick the source: **Query by Type** or **Query by Property**.
4. Configure filters and sort as you would for any Query.
5. The new Query is saved as a standalone Object too — you can find it in the sidebar and reuse it elsewhere.

You can also embed an Inline Collection the same way — useful for manually-curated lists embedded in a project page.

<figure><img src="../../.gitbook/assets/image (107).png" alt="" width="563"><figcaption></figcaption></figure>

### Sync vs. copy: what's shared, what isn't

Understanding what stays in sync between an inline Query and its source is important:

| | Stays in sync (shared) | Independent (copied) |
|---|---|---|
| **Source filter** | ✓ | |
| **Source sort** | ✓ | |
| **Query icon** | ✓ | |
| **Query name** | ✓ | |
| **View layout** (Grid, List, Gallery...) | | ✓ |
| **View-level filters** | | ✓ |
| **Visible Properties / columns** | | ✓ |
| **Grouping** | | ✓ |

In other words: **the data being queried is shared**, but **how it's displayed in this specific inline block is yours**. You can show the same Query as a Gallery in your dashboard and as a Grid in your project page without affecting one another.

### Customizing an Inline Query view

Click the inline Query block to focus it, then use the standard Query controls:

- **Layout** — switch between Grid, List, Gallery, Board, Calendar, Graph
- **Properties** — toggle which columns or fields show
- **View-level filters** — add filters that apply only to this inline display
- **Sort** — within this view's results
- **Grouping** — for Board view, choose the property to group by

These changes are saved to the inline block, not back to the source Query.

### Dynamic filter values

Inline Queries pair beautifully with [dynamic filter values](advanced-filters.md). Two especially useful values:

- **Current User** — filters Objects by who's viewing. Embed the same `Tasks where Assignee = Current User` Query in a shared dashboard, and every member sees their own tasks.
- **This Object** — filters Objects related to the Object containing the inline Query. Embed `Tasks where Project = This Object` in a Project Object, and the Query automatically scopes to that project. Move the same Object to a different Project, and the inline Query updates.

This means you can build a single Project template with an inline `Tasks for This Object` Query and reuse it for every project — no manual filter setup per project.

### Multiple inline Queries on one Object

You can put as many inline Queries as you want on a single Object. A common dashboard pattern:

```
# Today

[Inline Query: Tasks where Status = In Progress AND Assignee = Current User]

# This week

[Inline Query: Notes where Created in last 7 days]

# Reading

[Inline Query: Books where Status = Reading]
```

Each Query block is independent. They render side by side, refresh in real time, and let you build a personal "command center" page.

### Removing or changing the source

To change which Query an inline block references:

1. Click the inline Query.
2. Click the three-dot menu in the block.
3. Choose **Change source**.

To remove the inline Query (without affecting the source):

1. Click the block handle on the inline Query.
2. Choose **Delete block**.

The source Query remains in your Channel.

### Performance

Inline Queries run live every time you open the Object. In Channels with thousands of Objects, very broad inline Queries (e.g., "all Objects in this Channel") can take a moment to render.

To keep things fast:

- **Filter narrowly** — `Tasks where Status = In Progress` is faster than `Tasks` with no filter
- **Limit results** in the View settings — most layouts let you cap at 50 or 100 visible items
- **Use Board or Gallery** for visual scan, **List or Grid** for detail — Board and Gallery render fewer details per item

### Tips

{% hint style="info" %}
**Build a daily homepage with inline Queries.** Set this Object as your Channel Homepage (Channel Settings > Preferences > Homepage). Every time you open the Channel, you see today's view.
{% endhint %}

{% hint style="info" %}
**Use This Object filtering for templates.** A Project template with an inline `Tasks where Project = This Object` Query becomes a dynamic project hub for every project you create from the template.
{% endhint %}

{% hint style="info" %}
**Mix Inline Collections and Queries.** Use an Inline Collection for "things I manually want here" (curated reading list, key references) and Inline Queries for "things matching criteria" (active tasks, recent edits). The combination is powerful.
{% endhint %}
