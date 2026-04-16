---
description: >-
  One place to keep your course schedule, syllabus, study notes, assignments,
  and tasks.
---

# Study Notes

{% hint style="info" %}
**Shortcut:** You can import this use case directly into your Channel using this [gallery link](https://gallery.any.coop/?experience=study_hub). The walkthrough below explains how to build it from scratch.
{% endhint %}

### What you'll build

A study hub that organizes your courses, lecture notes, assignments, and resources — all linked together.

<div><figure><img src="../.gitbook/assets/screenshot-1 (2).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/screenshot-2 (1).png" alt=""><figcaption></figcaption></figure></div>

### Concepts used

- [Types](../getting-started/types/README.md) — Types for Course, Lecture Note, and Assignment
- [Properties](../getting-started/types/relations.md) — to link notes to courses and track due dates
- [Collections](../getting-started/sets/collections.md) — to group everything for a specific course
- [Templates](../getting-started/types/templates.md) — for consistent note-taking structure

### Step-by-step setup

1. **Create your Types.** Create three Types: "Course" (for each subject), "Lecture Note" (for class notes), and "Assignment" (for homework and projects).
2. **Add Properties.** Add an **Object** property called "Course" to both Lecture Note and Assignment Types — this links each note and assignment back to its course. Add a **Date** property for due dates on Assignments. Add a **Select** property for Status (To Do, In Progress, Done) on Assignments.
3. **Create a Template for Lecture Notes.** Include headings like "Key Concepts", "Details", and "Questions to Review". This gives you a consistent structure each class.
4. **Create a Collection per course.** For each course (e.g., "Biology 101"), create a Collection. Add the Course Object, its Lecture Notes, Assignments, and any reference materials. This gives you one place to see everything for that subject.
5. **Create an Assignments Query.** Create a Query by Type: Assignment, sorted by Due Date. Filter by Status to focus on what's upcoming. Pin it to your sidebar.

For more use cases, check out the [ANY Experience Gallery](../advanced/community/any-experience-gallery.md).
