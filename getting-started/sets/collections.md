---
description: Manually-curated groups of Objects.
---

# Collections

### What is a Collection?

A **Collection** is a manual grouping of Objects. You pick which Objects go in, and they stay until you remove them. Unlike Queries — which automatically pull in everything matching certain criteria — Collections start empty and you build them up by hand.

The key difference: **a Collection can hold Objects of different Types together**. A "Product Launch" Collection might contain tasks, notes, design files, meeting minutes, and reference documents — all in one place.

### Why it matters

Sometimes you need to group things that don't share a Type or a clean filter rule. They just belong together because of context — they're all part of the same project, the same trip, the same research effort, the same person's onboarding.

A Query says: "show me everything that matches *X*."
A Collection says: "show me these specific things, because I said so."

Both are useful, in different situations. Use Collections for:

- **Project workspaces** — tasks, notes, files, and references for one specific project
- **Reading lists** — books, articles, bookmarks you've decided to read
- **Research collections** — papers, notes, web clippings on one topic
- **Onboarding sets** — every Object a new team member should see
- **Curated content** — your favorite recipes, your top references, your "best work"

### How it works

A Collection is its own Object. It has:

- **Members** — the Objects you've added (any Type, any number)
- **Views** — different layouts (Grid, List, Gallery, Board, Calendar) like a Query
- **Properties** — like any Object, you can give the Collection itself Tags, a description, etc.

Adding an Object to a Collection doesn't move it — the Object still lives wherever it lived before. Collections store *references*. The same Object can appear in multiple Collections without being copied.

{% hint style="warning" %}
**The main difference between Queries and Collections** is that Queries draw Objects from your entire graph based on filter criteria, whereas Collections start empty and you add Objects to them manually.
{% endhint %}

### Building a Collection

#### From the sidebar

1. Click the **+** dropdown.
2. Choose **Collection**.
3. Name the Collection (e.g., "Q1 Marketing").
4. The empty Collection opens. Add Objects with the **+ New** button or **Existing object** option.

#### From the editor

Type `/collection` in any Object to insert an Inline Collection — embedded right inside the page. It functions the same as a standalone Collection but lives within another Object.

### Adding Objects to a Collection

#### Create new Objects directly

1. Open the Collection.
2. Click **New** to create a new Object inside the Collection.
3. Pick the Type — Tasks, Notes, Pages, anything.

The new Object is created in your Channel and added to the Collection in the same step.

#### Add existing Objects

1. Hover over the **▾** next to the **New** button.
2. Click **Existing object**.
3. Search for any Object in your Channel.
4. Select it.

The Object is added to the Collection. It still lives in its original location.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### From outside the Collection

Open any Object you want to add. Open the three-dot menu > **Add to Collection** > pick the Collection.

This is the fastest path when you're already in an Object and decide it belongs in a Collection.

#### Drop a folder of files

Drag a folder of files from your operating system onto the sidebar. Anytype creates a new Collection that mirrors the folder structure — files become File Objects inside the Collection.

This is the fastest way to import an existing on-disk archive (a photo collection, a project folder, a music library). See [Files & Media](files-and-media.md) for details on file Objects.

### Removing Objects from a Collection

Right-click the Object in the Collection's view > **Remove from Collection**. The Object stays in your Channel — only its membership in this Collection is removed.

To delete the Object entirely, use **Move to Bin** instead. (Removing from Collection ≠ deleting.)

### Views in a Collection

Collections support the same View types as Queries: Grid, List, Gallery, Board, Calendar, Graph. Each View can have its own layout, visible Properties, sort, and filters.

#### Grid as default

New Collections use **Grid** as the default layout. Properties show as columns immediately, making them easier to discover and edit.

#### Filters within a Collection

You can apply filters to a Collection's View. Filters narrow down the *members* of the Collection — they don't pull in new Objects. Useful when:

- A Collection has many Objects and you want to focus on a subset
- You want a Board view organized by Status of just the Tasks in a project Collection
- You want a Calendar view of just the Date-bearing Objects

For more on filtering, see [Advanced Filters](../feature-list-by-platform/advanced-filters.md).

### Multiple Views per Collection

Like Queries, Collections support multiple Views. A "Q1 Marketing" Collection might have:

- **Tasks (Board)** — only Tasks, grouped by Status
- **Documents (Gallery)** — only Documents, with cover images visible
- **All (Grid)** — everything, sortable

Switch between Views with one click using the View tabs at the top of the Collection.

### Dragging Objects between Views

Inside a Collection, you can drag an Object between Views. When you drop it into another View, its Properties update to match that View's filters — same as creating a new Object directly in that View.

For example: drag a task from your "To Do" View to your "Done" View, and the task's Status Property updates to "Done" automatically.

### Full-text search inside a Collection

Collections support full-text search across Object **content**, not just titles. Press Cmd/Ctrl + F inside a Collection View to search.

This is the fastest way to find "the Object I added to this Collection that mentions X" without having to open each one.

### Inline Collections

You can embed a Collection directly inside another Object using `/collection > Inline`. The Collection becomes a block in the editor — you can add Objects to it from within that page.

This pattern works well for:

- Project hub pages with an inline Collection of project Objects
- Reference pages with curated Object lists embedded in context
- Templates where the Inline Collection holds the structure-relevant Objects

See [Inline Queries](../feature-list-by-platform/inline-queries.md) — Inline Collections work the same way.

### Collections vs Queries: when to use which

| | Use a Collection | Use a Query |
|---|---|---|
| You want to manually pick what's in | ✓ | |
| You want auto-population by criteria | | ✓ |
| Different Types together | ✓ | (Query by Property can do this too) |
| Same Type with consistent structure | (Either works) | ✓ |
| Curated reading list, project box | ✓ | |
| Daily worklist, reading queue, status board | | ✓ |

In practice, you often use both together: a project Collection that you populate manually, with an inline Query inside it showing "Tasks where Project = This Object" for live status.

### Tips

{% hint style="info" %}
**Use Collections for projects, Queries for views into your data.** A "Q1 Marketing" project lives in a Collection (because its membership is curated). "All my in-progress Tasks" lives in a Query (because membership is determined by status).
{% endhint %}

{% hint style="info" %}
**Pin Collections like other Objects.** A pinned project Collection in your sidebar acts as a project hub — one click to see everything in scope.
{% endhint %}

{% hint style="info" %}
**Use the Gallery layout for visual Collections.** Reading lists, recipe collections, photo archives all benefit from cover images. Switch to Gallery in the layout switcher.
{% endhint %}

{% hint style="info" %}
**Drop a folder onto the sidebar to convert it.** This is the fastest way to onboard an on-disk archive — Anytype creates a Collection that mirrors the folder, with files as File Objects inside.
{% endhint %}
