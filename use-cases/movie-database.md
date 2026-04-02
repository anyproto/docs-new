---
description: >-
  Create a personal encyclopaedia for movies, books, or any hobby. Track what
  you've watched, rate it, and discover patterns.
---

# Movie Database

{% hint style="info" %}
**Shortcut:** You can import this use case directly into your Channel using this [gallery link](https://gallery.any.coop/?experience=movie_database). The walkthrough below explains how to build it from scratch.
{% endhint %}

### What you'll build

A personal movie database where you track films you've watched, rate them, and filter by genre, director, or rating.

<div><figure><img src="../.gitbook/assets/screenshot-1 (3).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/screenshot-2 (2).png" alt=""><figcaption></figcaption></figure></div>

### Concepts used

- [Types](../getting-started/types/README.md) — a "Movie" Type
- [Properties](../getting-started/types/relations.md) — for Genre, Director, Rating, Status
- [Queries](../getting-started/sets/README.md) — to browse your movies with filters and views
- [Templates](../getting-started/types/templates.md) — for a consistent structure when adding a new movie

### Step-by-step setup

1. **Create a "Movie" Type.** Open Channel Settings > Content Model > Object Types > New.
2. **Add Properties.** Add:
   - **Multi-select:** "Genre" (Action, Comedy, Drama, Sci-Fi, etc.)
   - **Text:** "Director"
   - **Number:** "Rating" (1-10)
   - **Select:** "Status" (Want to Watch, Watched)
   - **Date:** "Date Watched"
3. **Create a Template.** Open the Movie Type, add a Template with sections for "My Take" (your review) and "Notes". This gives each movie a consistent layout.
4. **Add your first movies.** Create a few Movie Objects. Fill in the Properties and write a short review in the body.
5. **Create a Query by Type: Movie.** Switch to Grid view to see your movies as a sortable table. Sort by Rating to see your favorites, or filter by Genre to browse.
6. **Try Gallery view.** Switch the Query layout to Gallery — if your Movies have cover images, you'll get a visual grid of your collection.

{% hint style="info" %}
**Tip:** This same pattern works for any collection-based hobby — books, video games, recipes, wine, vinyl records. Create a Type, add the Properties that matter to you, and build your personal database.
{% endhint %}

For more use cases, check out the [ANY Experience Gallery](../advanced/community/any-experience-gallery.md).
