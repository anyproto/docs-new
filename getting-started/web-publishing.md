---
description: Publish Objects as static webpages on your personal subdomain.
---

# Publish

### What is Web Publishing?

**Web Publishing** lets you turn any Object into a public webpage at a URL anyone can visit. Pick an Object, click Publish, and Anytype generates a static HTML page hosted on your personal subdomain at `<your-id>.any.coop/<slug>`.

This is for content you want **publicly readable** — blog posts, public profiles, documentation, recipes, anything you'd otherwise put on a personal website. Published pages are unencrypted (so search engines can index them) but limited to specific Objects you've explicitly chosen to share.

### Why it matters

Most people who keep notes also occasionally want to share something — an article, a how-to, a portfolio piece, a public version of a research note. Without Web Publishing, that means copying content into another tool (a blog, Notion, a static site generator).

With Web Publishing, the Object you've already written is the published page. Update the Object, republish, and the public page updates. No second platform to maintain.

This is useful for:

- Personal blog posts and essays
- Documentation visible to people without an Anytype account
- Public profiles and bios
- Recipes, guides, manuals
- Portfolio pages
- Anything you want a permanent URL for

<figure><img src="../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

### Prerequisites

To publish, you need:

- **An ANY ID** — a custom handle that becomes the subdomain for your published pages. ANY IDs are included with paid memberships (Builder, Co-Creator, Ultra). See [Memberships](../advanced/monetization/README.md).
- **The Object you want to publish**, finished or close to it.

If you don't have an ANY ID yet, you'll be prompted to set one up the first time you click Publish.

### Publishing an Object

1. Open the Object you want to publish.
2. Click the three-dot menu in the top-right corner.
3. Choose **Publish**.
4. Review the publish dialog:
   - **URL slug** — the path after your subdomain. Defaults to a slugified version of the title. Edit it if you want a different URL.
   - **Visible Properties** — choose which Properties show on the public page (defaults are usually fine).
   - **SEO settings** — title and description for search engines (defaults pulled from your Object).
5. Click **Publish**.

Within a few seconds, your Object is live at `<your-any-id>.any.coop/<slug>`. Copy the URL or share directly from the dialog.

### Updating a published page

Edit the Object normally. Your edits don't auto-publish — you have to republish to push changes:

1. Open the Object.
2. Click the three-dot menu.
3. Choose **Update published version** (the menu item changes to this when an Object is already published).

The page is regenerated. Visitors see the latest version on next page load.

If you want to make several edits before republishing, just keep editing. Anytype tracks which Objects have unpublished changes — open Vault Settings > My Sites to see a list.

### What's supported, what isn't

Web Publishing is still developing. Currently:

#### Supported in published pages

- **All text formatting** — paragraphs, headings, lists, callouts, quotes
- **Images and image blocks** — included as part of the published page
- **Code blocks** with syntax highlighting
- **LaTeX math** — rendered as static MathML
- **Embeds** that work in static contexts — YouTube, Vimeo, Mermaid diagrams (rendered server-side), images
- **Custom Object icon and cover** — appears at the top of the page
- **Visible Properties** — chosen Properties appear in the page metadata or sidebar
- **Toggle blocks** — collapsed by default in published view, expandable on click

#### Not yet supported

- **Linked Objects** — links to other Objects in your Channel point to a "page not published" placeholder unless those Objects are also published
- **Inline Queries and Collections** — these don't render in published pages
- **Chats and Discussions** — not exposed publicly
- **Multi-page sites** — you can publish many Objects but they're independent pages, not a connected site (multi-page is on the roadmap)
- **Custom themes or styling** — published pages use a default Anytype style
- **Custom domains** — published pages live on `<your-id>.any.coop`; pointing a custom domain is on the roadmap

For multi-page sites and custom domains, watch for updates in the Anytype changelog.

### Encryption and privacy

Anytype's core value is end-to-end encryption — and Web Publishing intentionally breaks that for the published Object only.

When you publish:

- The Object is **decrypted locally** on your device
- The decrypted content is uploaded to Anytype's web publishing server in **AnyBlock format**
- The server **renders and caches** the page server-side and serves it as plain HTML
- **Anyone** who knows the URL can read the page (including search engine crawlers, by design)

**Other Objects in your Channel remain encrypted**. Only the specific Objects you publish are exposed.

#### Why upload unencrypted?

Anytype's design intentionally publishes unencrypted because:

- Users explicitly choose what to publish — there's no accidental leakage
- Search engine indexability requires plaintext
- Decryption-in-browser via URL keys works poorly for multi-Object exports
- Server-side rendering and caching keeps the published pages fast

#### File encryption keys

If your Object includes file blocks (images, attachments), Anytype includes the encryption keys for those specific files in the published page so visitors can view them. **Each file has a unique locally-generated encryption key** — including a file's key in a published page does not compromise your Vault, your Channel, or any other content.

### Unpublishing

To take a published page offline:

1. Open the Object.
2. Click the three-dot menu.
3. Choose **Unpublish**.

The page is removed from the server immediately. The URL returns 404 to visitors. Your Object stays in your Channel — only the public version is removed.

You can also unpublish from **Vault Settings > My Sites**, which lists every published Object across all your Channels:

1. Open **Vault Settings > My Sites**.
2. Find the Object in the list.
3. Click the three-dot menu next to it.
4. Choose **Unpublish**.

### Managing your published pages

**Vault Settings > My Sites** is the central management screen for everything you've published:

- See a list of every published Object with title, URL, last published date
- See which Objects have unpublished changes
- Click any URL to open the live page in a browser
- Bulk republish or unpublish from this screen

### SEO and discoverability

Published pages include the metadata most search engines need:

- `<title>` from your Object's title (or custom override)
- `<meta description>` from a Property or custom override
- Open Graph tags for link previews on social media
- Structured data based on the Object's Type

For private "share via link only" content, there's no obfuscation — anyone with the URL can find it. If you want to make a page hard to discover, use a long random slug (or unpublish when you're done sharing).

### Tips

{% hint style="info" %}
**Use Web Publishing for one-off public documents, not as a CMS.** It's great for "publish this article" or "share this guide". For a content site you'll update frequently with many cross-linked pages, you'll want a dedicated CMS — at least until multi-page Web Publishing arrives.
{% endhint %}

{% hint style="info" %}
**Republish after major edits.** Small typo fixes can wait, but if you've meaningfully updated the content, republish so visitors see the new version. The URL stays the same.
{% endhint %}

{% hint style="warning" %}
**Don't publish Objects with sensitive Properties.** Properties like internal status, private notes, and personal information are uploaded too unless you exclude them in the publish dialog. Review what's visible before clicking Publish.
{% endhint %}

{% hint style="warning" %}
**Anyone with the URL can see a published page** — including web archivers, search engines, and screenshot tools. Treat the URL as effectively public, even if you don't share it widely.
{% endhint %}
