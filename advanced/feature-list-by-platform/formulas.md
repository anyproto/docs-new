---
description: Aggregations and counts in Grid view.
---

# Formulas

### What are Formulas?

**Formulas** let you summarize and aggregate Property values across the Objects in a Query or Collection. When you're looking at your data in Grid view, you can show counts, sums, averages, minimums, maximums, and other calculations at the bottom of any column.

The result is a row of summary values right under your data — useful for things like:

- Total hours estimated across all tasks in a sprint
- Average rating across all books in your reading list
- Number of in-progress tasks per assignee
- Sum of expenses per category
- Count of Objects of each type

### Why it matters

Without formulas, summarizing requires either exporting your data or counting by hand. Formulas put the summary inside Anytype, live and updating — change a Property value and the formula recalculates instantly.

This makes Anytype usable for lightweight tracking that you'd otherwise need a spreadsheet for: project hours, simple budgets, reading stats, habit counts.

### Where Formulas appear

Formulas live at the **bottom of each column in Grid view**. Each column gets its own formula, so different columns can show different calculations.

To open the formula menu:

1. Open a Query or Collection in **Grid view**.
2. Hover over the bottom edge of any column.
3. Click the formula indicator (or the column footer) that appears.
4. Pick a formula from the list.

The result displays in the column footer and updates as your data changes.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

### Available formulas

The formulas available depend on the Property type of the column. Here's the full list:

#### For all Property types

| Formula | What it calculates |
|---|---|
| **None** | No formula (default) |
| **Count All** | Total number of Objects in the column |
| **Count Values** | Number of Objects with a non-empty value in this column |
| **Count Unique** | Number of distinct values |
| **Count Empty** | Number of Objects with no value in this column |
| **Count Not Empty** | Same as Count Values |
| **Percent Empty** | % of Objects with no value |
| **Percent Not Empty** | % of Objects with a value |

#### For Number Properties

| Formula | What it calculates |
|---|---|
| **Sum** | Total of all values |
| **Average** | Mean value |
| **Median** | Middle value when sorted |
| **Minimum** | Smallest value |
| **Maximum** | Largest value |
| **Range** | Maximum − Minimum |

#### For Date Properties

| Formula | What it calculates |
|---|---|
| **Earliest** | The earliest date in the column |
| **Latest** | The latest date in the column |
| **Range** | The number of days between earliest and latest |

#### For Select / Multi-select / Checkbox Properties

| Formula | What it calculates |
|---|---|
| **Count Checked** (Checkbox only) | Number of true values |
| **Count Unchecked** (Checkbox only) | Number of false values |
| **Percent Checked** (Checkbox only) | % of true values |
| **Count by Option** (Select) | Count of each option (shown in the footer as a breakdown) |

### Formulas update with filters

If your view has filters applied, formulas operate on the **filtered set**, not the full Channel. Change the filter and every formula recalculates.

This makes them powerful for slicing:

- Filter to "Status: In Progress" → see how many active tasks you have
- Filter to "Assignee: Alex" → see total hours estimated for Alex
- Filter to "Created this week" → see how many Objects you've made this week

### Formulas across grouped Views

In Grid view with grouping (for example, grouping Tasks by Assignee), formulas show:

- A subtotal under each group
- A grand total at the bottom of the Grid

This is the closest equivalent to a pivot table inside Anytype — and it's free, since you're already looking at your data.

### Limitations

- **Formulas are visual only** — they're shown in the column footer but you can't reference them in another Object or use them in filters
- **No custom expressions** — you choose from the list of available formulas; there's no way to write `column1 + column2`
- **Grid view only** — other layouts (List, Gallery, Board) don't show formulas
- **Per-View** — each View remembers its own formula choice, so a Grid View and a List View of the same Query don't share formulas

For more complex calculations, export the data to CSV and process it externally — or use the [Anytype Agents Skill](../../getting-started/anytype-agents-skill.md) to run scripts against your data.

### Common patterns

#### Sprint hours estimate

```
Query: Tasks
Filter: Sprint = "Sprint 14"
Property: Estimated Hours (Number)
Formula: Sum
```

You see the total estimated hours for the current sprint, updating as you add or change tasks.

#### Reading stats

```
Query: Books
Property 1: Rating (Number) → Formula: Average
Property 2: Pages (Number) → Formula: Sum
Property 3: Status (Select) → Formula: Count by Option
```

Three columns, three formulas, instant reading dashboard.

#### Habit completion rate

```
Query: Habit Logs
Filter: Date = This Week
Property: Done (Checkbox)
Formula: Percent Checked
```

You see your weekly habit completion percentage at the bottom of the column.

#### Project portfolio

```
Query: Projects
Group by: Status
Property: Budget (Number) → Formula: Sum (per group)
```

A subtotal of budget per project status (Planning, Active, On Hold, Done) plus a grand total.

### Tips

{% hint style="info" %}
**Add a formula to your Type's default View.** When you open the Type page, you see all Objects of that Type — adding a formula to a key column makes the page act as a quick stats dashboard.
{% endhint %}

{% hint style="info" %}
**Use Count All to verify filters.** A quick way to confirm "how many Objects am I looking at right now" — set Count All on the Title column. Useful when iterating filters.
{% endhint %}

{% hint style="info" %}
**Combine with grouping for pivot-style summaries.** Group by Assignee, sum Estimated Hours — instant team workload chart, no spreadsheet needed.
{% endhint %}
