---
description: Visualize the connections between your Objects.
---

# Graph

### What is the Graph?

The **Graph** is a live, visual map of every Object in your Channel and how they connect to each other. Each Object is a node; each link or Property reference is an edge. Open the Graph and you see your Channel's structure — what's central, what's isolated, what clusters around which projects.

In other apps, this is sometimes called a "knowledge graph" or "mind map." In Anytype, it's not a separate feature — it's just another way of looking at the same data you already have.

{% hint style="warning" %}
The Graph is currently available on desktop only. A mobile version is in development.
{% endhint %}

### Why it matters

Your sidebar shows what you've pinned. Your Queries show what matches a filter. The Graph shows **everything, and how it relates** — a perspective you can't get from any other view.

This is useful when:

- You want to find an Object you remember but can't name — looking at the cluster around the related project often reveals it
- You're exploring a knowledge area and want to see what you've already written about it
- You're cleaning up — Objects floating outside the main graph are often candidates for deletion or relinking
- You're planning a project and want to see how it connects to existing work

### Opening the Graph

The Graph icon (a small node-and-edge symbol) appears at the top of every Channel sidebar. Click it to switch to Graph view.

You can also press the keyboard shortcut listed in your shortcut settings to open Graph from any Object.

<figure><img src="../../.gitbook/assets/image (105).png" alt="" width="375"><figcaption></figcaption></figure>

### Reading the Graph

Each **node** is an Object. Hover over a node to see its title, Type, and any other Properties you've enabled in the display settings.

Each **edge** (line connecting two nodes) represents a relationship — either a link in the editor, an Object Property pointing to another Object, or a backlink.

The **direction of the edge** (when arrows are enabled) shows which Object references which:

- A → B means Object A links to or references Object B
- A bidirectional connection (A ↔ B) means both link to each other

**Cluster patterns** emerge naturally:

- **Hubs** — Objects with many connections, typically projects, indexes, or central concepts
- **Clusters** — groups of Objects densely linked to each other (a project team, a topic, a course)
- **Bridges** — Objects that connect two otherwise separate clusters
- **Orphans** — Objects with no connections (often candidates for cleanup or relinking)

<figure><img src="../../.gitbook/assets/image (108).png" alt="" width="563"><figcaption></figcaption></figure>

### Display settings

Click the gear icon (or settings menu) on the top right of the Graph view to access display options:

#### Appearance

- **Show titles** — display Object names next to each node (toggle off for a cleaner view)
- **Show arrows** — show edge direction
- **Show icons** — display Object icons at each node
- **Node size** — change how prominently nodes are drawn

#### Connections

- **Show links** — show editor links between Objects
- **Show Properties** — show Object Property relationships
- **Show backlinks** — show implied connections from Objects pointing back

Each toggle changes the Graph in real time. You can build a focused view (e.g., "show only Property connections, hide editor links") to study one type of relationship at a time.

#### Filtering by Type

The **Filter by Types** menu lets you show only certain Object Types in the Graph:

1. Click the filter icon.
2. Toggle Types on or off.
3. Use the **Hide all** toggle to clear everything quickly, then enable just the Types you want to see.

This is the fastest way to study a slice — for example, "show only Tasks and Projects" to see how your work breaks down.

#### Unlinked Objects

By default, the Graph shows only connected Objects. To include orphans:

1. Open Graph display settings.
2. Toggle on **Show unlinked Objects**.

Unlinked Objects appear floating around the main graph. This is the best way to find Objects you've forgotten about.

<figure><img src="../../.gitbook/assets/image (222).png" alt="" width="288"><figcaption></figcaption></figure>

### Search in the Graph

The search box at the top of the Graph lets you find specific Objects:

- Type any portion of an Object's title to highlight matching nodes
- Press Enter to navigate to the first match
- Use arrow keys to cycle through matches

Matched nodes are highlighted; the rest of the Graph dims so you can see them at a glance.

### Navigating from the Graph

- **Click any node** to open that Object
- **Right-click any node** for the standard Object context menu (open in tab, link to, delete, etc.)
- **Drag the canvas** to pan around
- **Scroll** to zoom in and out
- Use the **+ / -** buttons in the corner for precise zoom control
- Click the **center** button to reset the view

### Performance

The Graph renders all Objects in your current Channel. In Channels with thousands of Objects, the Graph may take a moment to load and can become visually dense.

To make the Graph more usable in large Channels:

- **Filter by Type** — show only the Types relevant to what you're studying
- **Hide unlinked Objects** — keep the focus on the connected core
- **Use Properties off** — Property edges add a lot of lines; toggling them off simplifies the view

### Differences from the Channel Graph and the Vault Graph

Each Channel has its own Graph — the Graph view inside a Channel only shows that Channel's Objects. Connections across Channels (e.g., a link from a Personal Channel to a Team Channel) are not represented in either Channel's Graph.

A future feature is being explored to provide a Vault-wide Graph that spans all your Channels. For now, treat the Graph as a per-Channel tool.

### Tips

{% hint style="info" %}
**Use the Graph as a "did I forget about this?" check.** Open the Graph with unlinked Objects shown — anything floating disconnected is something you should either delete, archive, or connect to your active work.
{% endhint %}

{% hint style="info" %}
**Filter to a single Type to study structure.** Filtering to only "Project" Objects, for example, shows you how your projects relate to each other (via shared people, shared tasks, etc.) without the noise of every note.
{% endhint %}

{% hint style="info" %}
**Right-click → Open in Tab** to keep the Graph open while exploring. The Graph stays in one tab; you open Objects in others. See [Tabs](tabs.md).
{% endhint %}
