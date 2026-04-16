---
description: >-
  Cultivate a practice of daily journaling to notice thought patterns and
  develop new ideas.
---

# Daily Notes

{% hint style="info" %}
**Shortcut:** You can import this use case directly into your Channel using this [gallery link](https://gallery.any.coop/?experience=daily_journal). The walkthrough below explains how to build it from scratch.
{% endhint %}

### What you'll build

A daily journaling system where each day gets its own Object, and you can browse past entries through a Query.

<div><figure><img src="../.gitbook/assets/screenshot-1 (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/screenshot-2.png" alt=""><figcaption></figcaption></figure></div>

### Concepts used

- [Types](../getting-started/types/README.md) — a "Journal Entry" Type for daily notes
- [Templates](../getting-started/types/templates.md) — a Template with your preferred daily structure
- [Queries](../getting-started/sets/README.md) — to browse all entries sorted by date
- [Properties](../getting-started/types/relations.md) — Date property for sorting, optional Tags or Mood

### Step-by-step setup

1. **Create a "Journal Entry" Type.** Open Channel Settings > Content Model > Object Types > New. Name it "Journal Entry".
2. **Add Properties.** Add a **Date** property (this can be the creation date) and optionally a **Select** property for "Mood" or a **Multi-select** for "Tags".
3. **Create a Template.** Open the Journal Entry Type, click Templates, and create one. Structure it however you like — for example, headings for "Gratitude", "What happened today", and "Ideas". Enable name pre-fill with today's date if you prefer.
4. **Create a Query by Type.** Create a Query filtered to Type: Journal Entry. Sort by Date descending so the newest entry is always on top.
5. **Pin the Query to your sidebar.** Now you have a journaling dashboard one click away.
6. **Write your first entry.** Create a new Journal Entry Object. Your Template will be applied automatically. Start writing.

{% hint style="info" %}
**Tip:** Use @today in your entries to create date links. Over time, this lets you see everything connected to a specific date — journal entries, tasks completed, meetings held.
{% endhint %}

For more use cases, check out the [ANY Experience Gallery](../advanced/community/any-experience-gallery.md).
