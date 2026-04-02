---
description: >-
  Implement Tiago Forte's popular PARA method for organizing your digital life.
---

# PARA Method

{% hint style="info" %}
**Shortcut:** You can import this use case directly into your Channel using this [gallery link](https://gallery.any.coop/?experience=para_lite). The walkthrough below explains how to build it from scratch.
{% endhint %}

### What you'll build

A workspace organized around four categories — **Projects**, **Areas**, **Resources**, and **Archive** — following Tiago Forte's PARA method for personal knowledge management.

<figure><img src="../.gitbook/assets/screenshot-1.png" alt=""><figcaption></figcaption></figure>

### Concepts used

- [Types](../getting-started/types/README.md) — you'll create or use Types for Projects, Notes, and Resources
- [Properties](../getting-started/types/relations.md) — to categorize items into PARA categories
- [Queries](../getting-started/sets/README.md) — to create live views for each PARA category
- [Sidebar](../getting-started/customize-and-edit-the-sidebar.md) — to pin your PARA views for quick access

### Step-by-step setup

1. **Create a "PARA Category" Property.** Open Channel Settings > Content Model > Properties. Create a new **Select** property called "PARA Category" with four options: Project, Area, Resource, Archive.
2. **Add the Property to your main Types.** Open the Types you use most (Note, Task, Page) and add the "PARA Category" property to each.
3. **Create Queries for each category.** Create four Queries, each filtered by the "PARA Category" property:
   - "Projects" — PARA Category is Project
   - "Areas" — PARA Category is Area
   - "Resources" — PARA Category is Resource
   - "Archive" — PARA Category is Archive
4. **Pin Queries to your sidebar.** Pin each of the four Queries to your sidebar's Pinned section. You now have one-click access to each PARA category.
5. **Start categorizing.** As you create or revisit Objects, assign them a PARA Category. They'll automatically appear in the right Query.

{% hint style="info" %}
**Tip:** Projects are time-bound (they have a finish line). Areas are ongoing responsibilities. If you're unsure, ask: "Does this have an end date?" If yes, it's a Project.
{% endhint %}

For more use cases, check out the [ANY Experience Gallery](../advanced/community/any-experience-gallery.md).
