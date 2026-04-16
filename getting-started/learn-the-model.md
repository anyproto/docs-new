# Learn the Model

Before diving into individual features, here's a quick map of how Anytype is organized. Understanding these six concepts and how they relate to each other will make everything else in the docs click.

### Vault

Your **Vault** is the starting point. It's an encrypted container stored on your device that holds everything you create in Anytype. Think of it like the app itself on your device — one Vault per person, secured with a cryptographic key that only you have.

Inside your Vault, you'll find one or more **Channels**.

### Channels

A **Channel** is a workspace within your Vault. Each Channel has its own set of Objects, its own sidebar, and its own sharing settings. You might have one Channel for personal notes and another shared with your team.

Channels are how you separate different areas of your life or work, and control who has access to what.

### Objects

Everything you create inside a Channel is an **Object**. A page is an Object. A task is an Object. A note, a bookmark, an image — all Objects.

This is the core idea in Anytype: instead of files in folders, you have Objects in a graph. Every Object can link to any other Object, regardless of where it lives.

### Types

Every Object has a **Type** that describes what kind of thing it is — a Note, a Task, a Person, a Book. Types help you categorize your Objects so you can find, filter, and display them in useful ways.

Anytype comes with built-in Types, and you can create your own to match how you think about your information.

### Properties

**Properties** are the details attached to an Object. A Task might have properties like Status, Priority, and Due Date. A Book might have Author, Rating, and Genre.

Properties serve two purposes: they **describe** an Object (like a due date), and they **connect** Objects to each other (like linking a Task to a Project).

### Queries & Collections

Once you have Objects with Types and Properties, you need ways to find and view them.

A **Query** is a live filter across your entire Channel. You define criteria — like "all Tasks where Status is In Progress" — and the Query automatically shows matching Objects. When you create or update an Object that matches, it appears in the Query automatically.

A **Collection** is a manual grouping. You add specific Objects to it by hand. Unlike a Query, a Collection can hold Objects of different Types together — for example, a project Collection might contain tasks, notes, and documents side by side.

### How it all fits together

```
Vault
└── Channel (personal, shared, or team)
    ├── Objects (everything you create)
    │   ├── each has a Type (Note, Task, Book...)
    │   └── each has Properties (Status, Due Date, Author...)
    ├── Queries (live filters to find Objects)
    └── Collections (manual groupings of Objects)
```

You don't need to set all of this up before you start — most people begin by creating Objects and gradually add structure as they need it. The rest of the docs cover each concept in detail.
