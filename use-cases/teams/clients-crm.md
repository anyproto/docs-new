# Clients / CRM

### What you'll build

A simple CRM (Customer Relationship Management) setup for tracking clients, contacts, interactions, and deal status.

{% hint style="info" %}Screenshot needed: clients/CRM view from your team space{% endhint %}

### Concepts used

- [Types](../../getting-started/types/README.md) — Types for Client, Contact, and Interaction
- [Properties](../../getting-started/types/relations.md) — to track deal stage, contact info, and relationships
- [Queries](../../getting-started/sets/README.md) — filtered views of your pipeline
- [Links](../../getting-started/object-editor/linking-objects.md) — to connect contacts to their company and interactions

### Step-by-step setup

1. **Create a "Client" Type** (represents a company or organization). Add Properties:
   - **Select:** "Stage" (Lead, Active, Closed Won, Closed Lost)
   - **Text:** "Industry"
   - **Object:** "Primary Contact"
2. **Create a "Contact" Type** (represents a person). Add Properties:
   - **Email:** "Email"
   - **Phone:** "Phone"
   - **Object:** "Company" (links back to a Client)
   - **Text:** "Role"
3. **Create an "Interaction" Type** (meetings, calls, emails). Add Properties:
   - **Date:** "Date"
   - **Select:** "Type" (Call, Meeting, Email)
   - **Object:** "Client" and "Contact" (links to the relevant records)
4. **Create a Pipeline Query.** Filter by Type: Client. Use Board view grouped by Stage to see your sales pipeline. Grid view works well for a spreadsheet-style overview with all Properties visible.
5. **Create a Recent Interactions Query.** Filter by Type: Interaction, sorted by Date descending. This gives you a timeline of all client touchpoints.
6. **Link everything together.** When you log an Interaction, link it to the Client and Contact. Over time, each Client Object's backlinks will show a full history of interactions.

{% hint style="info" %}
**Tip:** Use the Graph view to visualize relationships between Clients, Contacts, and Interactions — it's a natural fit for CRM data.
{% endhint %}

For more templates, check out the [ANY Experience Gallery](../../advanced/community/any-experience-gallery.md).
