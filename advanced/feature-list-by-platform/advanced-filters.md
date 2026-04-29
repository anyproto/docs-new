---
description: Build precise queries with AND/OR logic and grouped conditions.
---

# Advanced Filters

### What are Advanced Filters?

**Advanced Filters** let you combine multiple filter conditions with AND/OR logic and group them into nested rules — so you can express complex queries like:

> Show me all Tasks where (Priority is High **OR** Due Date is this week) **AND** Status is not Done

Without advanced filters, every condition is joined by AND and applied flatly. Advanced filters give you parentheses — you can express OR, you can group rules, and you can build precise queries that match how you actually think about your data.

### Why it matters

Most filtering needs are simple: "tasks assigned to me", "books I've read". A single condition handles those.

But once your data has any complexity, you start needing things like:

- "Tasks that are urgent **OR** overdue"
- "Notes from this quarter, **but not** the ones tagged 'archive'"
- "Books I've rated 4 or 5 stars **AND** haven't recommended yet"

Each of those needs at least two conditions, and the way they combine matters. Advanced filters make this expressible.

### How to add an Advanced Filter

Advanced filters live alongside basic filters in the filter bar of any Query or Collection.

1. Open a Query or Collection in any list-style view (Grid, List, Gallery, Board).
2. Click the filter icon (or use the **+** button next to the filter bar).
3. Choose **Add advanced filter**.
4. Define your conditions in the dedicated bar that appears.

The basic filter bar shows simple conditions joined by AND. The advanced filter bar shows your full logic — including OR groupings, nested rules, and visual indicators of how conditions combine.

<figure><img src="../../.gitbook/assets/unknown (1).png" alt=""><figcaption></figcaption></figure>

### Building conditions

Each condition has three parts:

- **Property** — which Property to filter by (Status, Priority, Tags, Due Date, etc.)
- **Operator** — how to compare (is, is not, is empty, contains, is greater than, etc.)
- **Value** — what to compare against (a specific value, a list, or a [dynamic value](#dynamic-filter-values))

Operators available depend on the Property type:

| Property type | Operators |
|---|---|
| **Text / Title** | is, is not, contains, doesn't contain, starts with, ends with, is empty, is not empty |
| **Number** | =, ≠, >, <, ≥, ≤, is empty, is not empty |
| **Date** | is, is before, is after, is between, is empty, is not empty, is today/this week/this month/etc. |
| **Select / Multi-select** | is, is not, includes any of, includes all of, is empty, is not empty |
| **Checkbox** | is checked, is not checked |
| **Object** | is, is not, includes any of, includes all of, is empty, is not empty |

### Combining with AND / OR

By default, multiple conditions are joined by **AND** — every condition must be true for an Object to match. Switch to **OR** between two conditions and only one of them needs to be true.

To toggle between AND and OR:

1. Click the operator label (AND / OR) between two conditions.
2. The label flips to the other operator.

Visually:

```
Condition A  AND  Condition B  AND  Condition C    → All three must be true
Condition A  OR   Condition B  AND  Condition C    → A is true, OR (B and C are both true)
```

### Grouping conditions

For more complex logic, use **groups** to control precedence — like parentheses in math:

```
(Priority is High  OR  Priority is Urgent)  AND  Status is not Done
```

Without parentheses, AND has higher precedence than OR by default — but this leads to subtle bugs. Always group when the logic isn't trivial.

To create a group:

1. Add the conditions you want to group.
2. Select multiple conditions (Shift + click their handles, or use the group toggle).
3. Click **Group** in the filter toolbar.

Grouped conditions are visually indented and bracketed in the filter bar. You can change the operator inside a group (AND or OR) independently of the operator joining groups.

To ungroup:

1. Click the group's handle.
2. Choose **Ungroup**.

### Dynamic filter values

Filters support **dynamic values** that change based on context:

| Dynamic value | Where it makes sense | Example |
|---|---|---|
| **Current User** | Object Property pointing to a Person | Tasks where Assignee = Current User |
| **This Object** | Inline Queries on Object Properties | Tasks where Project = This Object |
| **Today** | Date Property | Notes where Created = Today |
| **This Week** | Date Property | Tasks where Due Date is this week |
| **This Month** | Date Property | Reviews where Date is this month |

**Current User** is especially useful for shared Channels — every member sees their own personalized view of a Query without you having to maintain separate Queries per person.

**This Object** only works inside [Inline Queries](inline-queries.md) — it scopes the inline Query to whatever Object is hosting it. Move the inline Query to a different Object, and it filters by *that* Object instead.

### Auto-open value picker

When you select a Property in the filter menu, the value picker now opens automatically — saving you an extra click. Just pick the values you want and the filter is added.

### Active filter bar

Once you have filters configured, they appear in a **dedicated bar above your view**. Each active filter shows:

- The property name (e.g., "Status")
- The condition (e.g., "is not")
- The value (e.g., "Done")

Sort indicators sit alongside the filters, so you always see how your data is organized at a glance.

To edit any active filter, click it. To remove it, click the × on the filter chip. To clear everything in one click, use the **Clear all** button at the end of the bar.

### Filters per view, not per source

In a Query with multiple Views (List, Grid, Board), each View has its own filters. The Query itself has source-level filters that apply to every View, plus each View can layer additional filters on top.

This separation means you can have a single Query of "all Tasks" but with three Views:

- **Active** — filtered to Status: In Progress
- **My Tasks** — filtered to Assignee: Current User
- **Overdue** — filtered to Due Date: before Today

…all from the same Query. See [Queries](../../getting-started/sets/README.md) for how Views work.

### Common filter patterns

#### Tasks I'm working on right now

```
Status is In Progress  AND  Assignee is Current User
```

#### Notes from this week

```
Created is this week
```

#### Books I want to recommend

```
Rating ≥ 4  AND  Recommended-To is empty
```

#### Tasks that are blocked or stale

```
Status is Blocked  OR  (Status is In Progress  AND  Modified is before 7 days ago)
```

#### Items needing review

```
(Type is Document  OR  Type is Note)  AND  Reviewed is unchecked  AND  Created is before this week
```

### Tips

{% hint style="info" %}
**Always group OR conditions.** AND has higher default precedence — `A AND B OR C` may not mean what you think. Wrapping the OR in a group makes the intent explicit and unambiguous.
{% endhint %}

{% hint style="info" %}
**Save complex filters as separate Views.** If you've built a filter that's hard to recreate, save it as a View on your Query rather than rebuilding it each time. The Views menu makes them switchable in one click.
{% endhint %}

{% hint style="info" %}
**Use Current User in shared Channel templates.** A "My Tasks" Query in a team Channel works for everyone — each member sees their own tasks. No need to duplicate the Query per person.
{% endhint %}
