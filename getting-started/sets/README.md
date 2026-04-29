---
description: Live, filtered views of Objects in your Channel.
---

# Queries

### What is a Query?

A **Query** is a live, filtered view of Objects in your Channel. You define criteria — like "all Tasks" or "all Notes tagged with Design" — and the Query automatically shows every Object that matches. As you create or update Objects that fit, they appear in the Query automatically.

If you've used spreadsheet filters or smart playlists, Queries work the same way. They're not folders — they don't store Objects. They're filters that show you Objects from your Channel that match what you specified.

### Why it matters

As your Channel grows, you need ways to find and view your Objects without scrolling through everything. Queries let you create focused views — all your in-progress Tasks, all Books you've rated 5 stars, all Notes from this week — and keep them accessible from your sidebar.

A Query gives you:

- **Live filtering** — Objects appear and disappear as their Properties change
- **Multiple views** — the same Query as a List, a Board, a Calendar, a Gallery
- **Batch editing** — select multiple Objects and change their Properties at once
- **Reusability** — pin a Query in the sidebar, [embed it inline](../../advanced/feature-list-by-platform/inline-queries.md) in another Object, or use it as a Channel homepage

### How it works

A Query has three layers:

1. **Source** — what's the universe of Objects? Either *Type* (e.g., all Tasks) or *Property* (e.g., all Objects with a "Reviewed" property)
2. **Filters and sorts** — narrow and order the source
3. **Views** — different visual presentations of the same data (Grid, List, Board, etc.)

Each Query can have multiple Views — same data, different layouts. A "Tasks" Query might have one View as a Board (grouped by Status) and another as a Grid (showing all properties as columns). You switch between Views with one click.

<figure><img src="../../.gitbook/assets/image (111).png" alt="" width="563"><figcaption></figcaption></figure>

### Creating a Query

#### From the sidebar

1. Click the **+** button in the sidebar.
2. Hover over **Query** and choose either **Query by Type** or **Query by Property**.
3. Pick the Type or Property to query.
4. The Query opens — you can now configure filters, sort, and view.

#### From the slash menu

1. In any editor, type `/query`.
2. Pick Query by Type or Query by Property.
3. The Query becomes a block in your Object — see [Inline Queries](../../advanced/feature-list-by-platform/inline-queries.md).

#### Query by Type vs Query by Property

- **Query by Type** — pulls in all Objects of a specific Type (all Tasks, all Notes, all Books). The most common starting point.
- **Query by Property** — pulls in all Objects that have a specific Property defined (regardless of Type). Useful for cross-Type views — e.g., "everything with a Due Date".

You can switch between the two later in the Query's source settings.

### Building your first Query

Let's create a Query that shows all your in-progress Tasks:

1. From the sidebar, click **+ > Query > Query by Type**.
2. Select **Task**.
3. You'll see all Task objects in your Channel listed.
4. Click the filter icon and add: **Status > is > In Progress**.
5. Click the layout switcher and choose **Grid** to see your Tasks as a table with Property columns.
6. Pin this Query to your sidebar by opening it and clicking the pin icon — now you have a quick-access view of your active work.

### Filters

Filters narrow your Query to Objects matching specific conditions. Each filter has:

- **Property** — which Property to check (Status, Priority, Tags, Date, etc.)
- **Operator** — how to compare (is, is not, contains, is greater than, etc.)
- **Value** — what to compare against

Add multiple filters and they're joined by AND by default — every condition must match.

For more complex logic (OR, grouped conditions, dynamic values like "Current User"), see [Advanced Filters](../../advanced/feature-list-by-platform/advanced-filters.md).

#### The active filter bar

When you have one or more filters set, they appear in a **dedicated bar above your view**:

- Each filter chip shows the property, operator, and value
- Sort indicators sit alongside the filter chips
- Click any chip to edit it
- Click the × on any chip to remove it
- Click **Clear all** at the end to wipe the entire filter set

This makes it instantly clear what you're looking at. No more "wait, why am I not seeing X?"

#### Auto-open value picker

When you select a Property in the filter menu, the values picker opens automatically — saving you a click. Pick the values you want and the filter is applied.

### Sorts

Click the sort icon to add a sort:

- Pick a Property
- Choose ascending or descending

You can add multiple sorts — Anytype sorts first by the top sort, then by the next, and so on. Drag the sort entries to change priority.

#### Manual sorting

In any list view (Grid, List), you can also drag and drop Objects to manually reorder them. The order is saved per-View, giving you full control over presentation.

Manual sorting persists — close the Query, come back, and your order is preserved.

### Views

A View is one specific layout + filter + sort configuration. Every Query starts with one default View, but you can add more.

To add a View:

1. Click the View name at the top of the Query.
2. Click **+ Add View**.
3. Pick a layout type and name the View.

Each View has its own:

- Layout (Grid, List, Gallery, Board, Calendar, Graph)
- Visible Properties / columns
- View-level filters (in addition to Query-level filters)
- View-level sorts
- Grouping (where applicable)

Switch Views with one click using the View tabs at the top.

#### Layout types

| Layout | Best for |
|---|---|
| **Grid** | Spreadsheet-style — every Property as a column. Best for batch editing and detail. |
| **List** | Compact list view — minimal Properties shown, more rows visible. |
| **Gallery** | Visual cards with cover image. Best for media, books, projects. |
| **Board** | Kanban — Objects grouped into columns by a chosen Property (typically Status). |
| **Calendar** | Date-based — Objects appear on the date of their Date Property. |
| **Graph** | Connection-based — Objects shown as nodes with their links. |

{% hint style="warning" %}
Kanban (Board), Calendar, and Graph views are available on desktop only.
{% endhint %}

#### Grid as default

New Queries and Collections now use **Grid** as the default layout. Properties are immediately visible as columns, making them easier to discover and use. You can switch to a different layout at any time, or change the default for any Type by editing the Type's settings.

#### List view sizing

The List view has a Size setting:

- **Compact** — minimum row height
- **Regular** — comfortable spacing with more visible Properties

Choose in View settings > Size.

#### Kanban (Board) view

In Board view:

- Pick a Property to group by (typically Select properties like Status or Priority)
- Each column is one option of that Property
- Drag Objects between columns to update their Property value
- Add or remove columns by editing the Property's options

The Board view is ideal for Tasks and any Object with a status workflow.

#### Calendar view

In Calendar view:

- Pick a Date Property to drive the calendar
- Objects appear on the date of that Property
- Click an empty slot to create a new Object on that date
- Drag Objects between dates to update their Date Property

Useful for deadlines, journals, content calendars, scheduled meetings.

#### Horizontal scrollbar in Grid and Kanban

Grid and Kanban views show a sticky horizontal scrollbar — you can scroll sideways even when you're not at the bottom of the list. Especially helpful when you have many columns and aren't using a touchpad.

### Toggling Properties

Each View shows a chosen subset of Properties. To change which Properties are visible:

1. Click the layout settings icon (or right-click a column header in Grid view).
2. Toggle Properties on or off.
3. Drag to reorder them.

You can also add a Property to all Objects of a Type at once: click the **+** in the Property list. The Property is added to the Type — it appears on every Object of that Type going forward.

### Editing Objects in Grid view

Grid view supports inline editing for all Property types:

- Click a cell to enter edit mode
- Tab between cells
- Edit titles by clicking the title cell
- Multi-select Objects with Shift + Click and apply a bulk update

#### Click-to-edit title behavior

A toggle in **Vault Settings > Application > Preferences** controls what happens when you click a title in Grid view:

- **Click to edit** (default) — clicking the title puts you in edit mode
- **Click to open** — clicking the title opens the Object directly (legacy behavior)

Toggle to whichever fits your workflow.

#### Property editing behavior

When you click outside an edit dropdown in Grid view, the dropdown now closes first instead of immediately opening the next field. This makes inline editing feel more deliberate.

### Full-text search inside a Collection

Collections support full-text search across Object content — not just titles. Use Cmd/Ctrl + F inside a Collection view to search.

### Grouping

In Grid view, you can group Objects by a Property:

1. Click the layout settings icon.
2. Choose **Group by**.
3. Pick a Property (Select, Multi-select, Object Properties work best).

Each group becomes a section header with a count of Objects, and you can collapse / expand groups individually. With formulas enabled, each group can show subtotals — see [Formulas](../../advanced/feature-list-by-platform/formulas.md).

### Dragging Objects between Views

You can drag an Object from one View to another inside the same Query or Collection. When you drop it into another View, its Properties update to match that View's filters automatically — same behavior as creating a new Object directly in that View.

For example: drag a task from your "To Do" View to your "Done" View, and the Status Property updates to "Done" automatically.

### Counts and search results

When you use local search inside a View, the count at the top reflects the number of *visible* results — not the total in the Query. This makes it easy to see how many matches you've narrowed to.

### Tips

{% hint style="info" %}
**Pin your most-used Queries.** A pinned `Tasks: In Progress` Query in the sidebar acts as your daily worklist. A pinned `Notes: This Week` Query helps you find recent thoughts. They update themselves.
{% endhint %}

{% hint style="info" %}
**Save important filter combinations as Views, not new Queries.** If you find yourself repeatedly filtering the same Query the same way, save it as a View. The View tabs let you switch between configurations in one click.
{% endhint %}

{% hint style="info" %}
**Use Object Properties to query relationships.** A "Tasks where Project is X" Query gives you a project-specific worklist without needing a separate Channel. The Project Property handles the relationship; the Query handles the view.
{% endhint %}

{% hint style="info" %}
**Drag Objects between Board columns to change Status.** This is faster than opening each Object and editing. Same idea for Calendar (drag to reschedule) and grouped Grid views (drag to change group).
{% endhint %}
