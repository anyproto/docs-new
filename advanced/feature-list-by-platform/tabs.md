---
description: Open multiple Objects side by side in a tab bar.
---

# Tabs

### What are Tabs?

**Tabs** let you keep multiple Objects open at once in the same window — just like in a browser. Each tab is one Object. Click between tabs to switch instantly without losing your scroll position or your edit cursor.

Before tabs, switching between two Objects meant clicking between them in the sidebar and reloading each time. With tabs, both Objects stay open — you can reference one while editing the other, copy between them quickly, or have your task list open in one tab while you work in another.

### Why it matters

Most knowledge work involves jumping between things — a note while you're editing a doc, a task while you're in a meeting, a reference while you're writing. Tabs make this fluid:

- **Keep context open** — read your notes in one tab, write the report in another
- **Compare side by side** — open two related Objects and reference them simultaneously
- **Stack work in progress** — open every Object you're touching today, close them as you finish
- **Restore your session** — open tabs come back when you relaunch the app

### Opening a tab

There are several ways to open an Object in a new tab:

| Method | When to use |
|---|---|
| **Cmd/Ctrl + Click** an Object link | Quickest — works on any link in the editor, sidebar, or Graph |
| **Right-click an Object > Open in new tab** | When you're already in a context menu |
| **Middle-click** (on three-button mice) | Same as Cmd/Ctrl + Click |
| **Drag a sidebar item to the tab bar** | Drop where you want it |
| **Cmd/Ctrl + T** in the tab bar | Opens a new empty tab; pick an Object via search |

By default, plain clicks still navigate within the current tab — so your existing single-tab workflow keeps working.

### The tab bar

The tab bar appears at the top of the Channel content area. Each tab shows the Object's icon and title, plus a close (×) button on hover.

#### Display modes

Open **Vault Settings > Application > Preferences** and look for **Tabs** to choose:

- **Contextual** — the tab bar only appears when you have more than one tab open. With a single tab, you see the full editor surface (recommended for most users)
- **Always visible** — the tab bar is always on screen, even with one tab. Useful if you frequently switch between contexts and want the bar's actions always at hand

#### Reordering tabs

Drag tabs left or right to reorder them. The order persists between sessions.

<figure><img src="../../.gitbook/assets/unknown.png" alt=""><figcaption></figcaption></figure>

### Pinning tabs

Important tabs you want to keep around can be **pinned** — they shrink to icon-only, move to the left side of the tab bar, and don't disappear when you close other tabs.

To pin a tab:

1. Right-click the tab.
2. Choose **Pin tab**.

To unpin, right-click again and choose **Unpin tab**.

Pinned tabs survive app restarts and stay pinned even if you accidentally try to close them (the close button is hidden for pinned tabs — you have to unpin first).

### Drag a tab out to a new window

To move a tab to its own window:

1. Click and drag the tab downward, away from the tab bar.
2. Release to drop it as a new window.

The Object now lives in a separate window. You can drag it back into the original window's tab bar to merge.

This is especially useful with multiple monitors — keep your task tracker on a second screen while editing on your primary one.

### Closing tabs

| Action | Effect |
|---|---|
| Click the **×** on a tab | Close that tab |
| **Cmd/Ctrl + W** | Close the active tab |
| Right-click > **Close other tabs** | Close all tabs except this one |
| Right-click > **Close tabs to the right** | Close everything to the right of this tab |
| Click the new-tab button while holding Shift | (varies by configuration) |

Pinned tabs can't be closed without unpinning first.

### Restoring tabs after a relaunch

When you quit Anytype and reopen it, your tabs come back the way you left them — same Objects open, same order, same active tab. This applies to:

- All open tabs (including pinned ones)
- The currently active tab
- Tab order

If you don't want this behavior, see **Vault Settings > Application > Preferences > Tabs** for the option to start with a blank slate each time.

### Reopening a recently closed tab

If you close a tab by mistake, you can reopen it:

- **Cmd/Ctrl + Shift + T** — reopens the most recently closed tab
- Press it repeatedly to keep walking back through closed tabs

This works for the current session — once you quit the app, the closed-tab history clears.

### Tabs vs. windows

Tabs live inside one Anytype window. Windows are separate top-level instances. Both use the same Channel data and stay in sync — edit an Object in one window and it updates in another instantly.

When to use a window vs. a tab:

- **Use tabs** for related work in the same Channel
- **Use a new window** for cross-Channel work (e.g., a Personal Channel in one window, a Team Channel in another)

To open a new window:

- **File > New Window** (in the menu bar)
- **Cmd/Ctrl + Shift + N**
- Right-click the Anytype dock/taskbar icon > **New Window**

### Keyboard shortcuts

Most tab actions have keyboard shortcuts. The exact bindings depend on your OS and any customizations:

| Action | Default shortcut |
|---|---|
| Open new tab | Cmd/Ctrl + T |
| Close current tab | Cmd/Ctrl + W |
| Reopen closed tab | Cmd/Ctrl + Shift + T |
| Switch to next tab | Cmd/Ctrl + Tab |
| Switch to previous tab | Cmd/Ctrl + Shift + Tab |
| Switch to specific tab | Cmd/Ctrl + 1 through 9 |

Customize these in **Vault Settings > Application > Keyboard Shortcuts**.

### Tips

{% hint style="info" %}
**Pin your daily-driver Objects.** Pin your "Today" page, your active project, and your inbox as the leftmost tabs. They're always one click away and survive restarts.
{% endhint %}

{% hint style="info" %}
**Use Cmd/Ctrl + Click in the sidebar instead of regular click.** This builds a habit of keeping your current context open while you peek at something else — far less disruptive than navigating away.
{% endhint %}

{% hint style="info" %}
**Drag a tab out for reference docs.** A reference Object you keep peeking at — a glossary, a pricing table, a contact list — works great as a separate small window pinned to a corner of your screen.
{% endhint %}
