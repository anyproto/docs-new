---
description: >-
  Put everything you need for a trip in one place, so you don't need to fuss
  over wifi while traveling.
---

# Travel Wiki

{% hint style="info" %}
**Shortcut:** You can import this use case directly into your Channel using this [gallery link](https://gallery.any.coop/?experience=trip_planner). The walkthrough below explains how to build it from scratch.
{% endhint %}

### What you'll build

A travel planner where each trip is an Object containing your itinerary, accommodations, bookings, and local tips — all accessible offline.

<div><figure><img src="../.gitbook/assets/screenshot-1 (4).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/screenshot-2 (3).png" alt=""><figcaption></figcaption></figure></div>

### Concepts used

- [Types](../getting-started/types/README.md) — a "Trip" Type and optionally "Place" and "Booking" Types
- [Properties](../getting-started/types/relations.md) — dates, locations, and links between trips and places
- [Collections](../getting-started/sets/collections.md) — to group all items for a specific trip
- [Blocks](../getting-started/object-editor/blocks.md) — for embedding maps, adding checklists, and organizing content

### Step-by-step setup

1. **Create a "Trip" Type.** Add Properties: **Date** (start/end), **Text** for "Destination", and **Select** for Status (Planning, Upcoming, Completed).
2. **Create a Trip Object.** Name it after your destination — e.g., "Tokyo 2026". Fill in the dates and destination.
3. **Add your itinerary as Blocks.** Inside the Trip Object, use headings for each day. Add checklists for packing lists, text blocks for restaurant recommendations, and embed Google Maps for key locations.
4. **Create linked Objects for details.** For complex trips, create separate Objects for Accommodations, Flights, and Activities. Link them to your Trip using an **Object** property.
5. **Create a Collection for the trip.** Add the Trip Object and all related Objects (bookings, places, notes) into one Collection. This is your trip dashboard.
6. **Create a "My Trips" Query.** Filter by Type: Trip, sorted by Date. Pin it to your sidebar to see all your trips at a glance.

{% hint style="info" %}
**Tip:** Since Anytype works offline, all your travel info is available without wifi. Just make sure your device has synced before you travel.
{% endhint %}

For more use cases, check out the [ANY Experience Gallery](../advanced/community/any-experience-gallery.md).
