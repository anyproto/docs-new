---
description: Upload images, videos, audio, and files as standalone Objects.
---

# Files & Media

### What are File Objects?

In Anytype, files aren't just attachments — they're **Objects**. When you upload an image, video, audio file, or generic file, it becomes a standalone Object you can find, link, organize, and reference like anything else in your Channel.

This means a photo isn't trapped inside the page where you uploaded it. It exists as its own Object, can appear in a Query of all your photos, can be linked from multiple places, and shows up in the Graph alongside the rest of your knowledge.

### Why it matters

Most apps treat files as second-class — buried in folders, hard to find again, disconnected from your other work. Anytype treats them like everything else: searchable, linkable, taggable, and surfaced in Queries.

This is especially powerful for:

* **Visual collections** — a Query of all images tagged "design inspiration"
* **Audio notes** — voice memos that can be tagged, linked to projects, and transcribed in their description
* **Reference files** — PDFs that can be referenced from multiple projects without duplicating
* **Media libraries** — a Channel-wide view of every video you've uploaded

### File Types

There are four built-in file Types in Anytype:

| Type      | Use for                                      | Default layout              |
| --------- | -------------------------------------------- | --------------------------- |
| **Image** | Photos, screenshots, graphics, illustrations | Image preview at top        |
| **Video** | Recorded video, screen recordings            | Embedded player             |
| **Audio** | Voice memos, music, podcasts                 | Embedded player             |
| **File**  | PDFs, documents, archives, anything else     | Download link with metadata |

Each Type has its own default Properties (size, file format, dimensions for images, duration for audio/video) and its own dedicated layout optimized for the content.

### Creating File Objects

#### From the Create menu

1. In the sidebar, click the **+** dropdown.
2. Choose **Image**, **Video**, **Audio**, or **File**.
3. Pick the file from your disk.

The file is uploaded, the Object is created with the right Type, and it opens in the editor.

#### Drag and drop

Drag any file from your operating system onto:

* **A Type page in the sidebar** — creates a new Object of that Type
* **A widget** — same behavior
* **An open Object's editor** — embeds the file as a block _and_ creates a standalone Object

#### Paste from clipboard

If you've copied an image from a screenshot tool or another app, paste it directly with Cmd/Ctrl + V into:

* The sidebar — creates a new Image Object
* An open Object — embeds inline (and creates the Object behind the scenes)
* A Chat — sends as an attachment (and creates the Object)

#### Drop a folder

Drop a folder of files onto the sidebar and Anytype converts it into a **Collection** that mirrors the folder structure. Files inside the folder become individual File Objects, with the Collection acting as a parent grouping.

This is the fastest way to bring a large library — a photo archive, a music collection, a project's reference materials — into your Channel.

### File Block vs. File Object

When you embed a file inline in an editor, you can choose how it's displayed:

* **As a preview** — the file is shown inline (image visible, video player embedded, etc.)
* **As a link** — a compact link that opens the file when clicked

The default is set in **Vault Settings > Application > Editor Personalization > File block default style**.

Either way, the file exists as an Object you can find through Queries and the sidebar.

### Working with File Objects

#### Finding files

Files appear in the Objects section of your sidebar, grouped by Type. Click **Image** to see all your images, **Audio** to see all your audio files, etc.

You can also create a Query by Type for finer control — filter to only files larger than 10MB, or only files uploaded this week.

#### Adding metadata

Like any Object, a File can have:

* **Tags** — for categorization
* **Description** — typed by you (useful for transcribing voice notes or describing image content)
* **Object links** — link a screenshot to the project it documents
* **Custom Properties** — add anything you'd track

#### Previewing files

* **Images** — click to open in fullscreen. Click outside or press Esc to close. Double-click to zoom.
* **Audio/Video** — click to play in the embedded player.
* **Files** — click to download (or open in the default app on desktop).

#### Copying images

You can copy images directly to your clipboard:

* From a block in the editor (right-click > Copy)
* From the Object menu when an image is open in fullscreen

This makes it easy to paste the same image into another Object or external tool.

### Storage and limits

Files contribute to your Channel's storage usage. Owners can monitor this in **Channel Settings > Remote Storage**, where they see per-member storage breakdowns and total Channel usage.

#### Configurable download size limit

In shared Channels, large files can eat up bandwidth on every device. To prevent this, Owners can set a **maximum file size for automatic downloads** in Channel Settings.

Files larger than the limit won't be fetched automatically — they're listed but stay on the network until a member explicitly opens them. This keeps storage manageable on devices with limited disk space.

To change the limit:

1. Open **Channel Settings > Remote Storage**.
2. Find **Auto-download size limit**.
3. Set a value in MB (or "No limit").

Members can always manually download files above the limit by clicking **Download** on the File Object.

### Tips

{% hint style="info" %}
**Use the Description field as a transcript.** For voice notes and screen recordings, type or paste a short summary into the Description. This makes the file findable through search by content, not just filename.
{% endhint %}

{% hint style="info" %}
**Tag at upload time.** When you create a File Object, the editor opens immediately — add Tags right away. It takes ten seconds and saves you a future hunt.
{% endhint %}

{% hint style="warning" %}
**Files in shared Channels download automatically by default.** On devices with small disks, set a download size limit to avoid surprises. Members will still see the files exist — they just won't take up local space until opened.
{% endhint %}
