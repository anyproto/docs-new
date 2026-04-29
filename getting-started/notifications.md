---
description: Stay informed without being overwhelmed.
---

# Notifications

Anytype's notification system is designed around two principles: notifications should be **specific** (you control what you hear about) and **layered** (you can set a default, then override it per Channel, per Chat, or per Object).

This page covers everything you can configure.

### What you'll be notified about

By default, Anytype notifies you about:

- New messages in Chats and Direct Channels you belong to
- @-mentions of you in messages, posts, or Object content
- Replies to your messages or Discussion posts
- Reactions to your messages
- New members joining a Channel you're in
- Access requests for shared Channels (if you're an Owner)

Each of these can be turned on or off, individually or in groups.

### Three levels of notification settings

| Level | Set in | What it controls |
|---|---|---|
| **Global** | Vault Settings > Notifications | System-wide defaults for all Channels |
| **Per Channel** | Channel Settings > Preferences > Collaboration | All Chats, Discussions, and mentions inside that Channel |
| **Per Chat / Object** | Three-dot menu inside a Chat or Discussion | That specific conversation only |

The most specific setting wins. If you've muted a single Chat but kept Channel-level notifications on, you'll still get notifications from other Chats in that Channel — just not the muted one.

### Notification modes

For Chats and Discussions, you have three modes:

- **Enable all** — every new message produces a notification
- **Mentions only** — only @-mentions of you trigger a notification
- **Disable all** — no notifications, but the unread counter still updates

**Mentions only** is the most common compromise — it keeps you in the loop for things addressed to you without flooding you with every message in busy channels.

### Configuring notifications per Chat

1. Right-click the Chat in your sidebar, **or** click the three-dot menu inside the Chat.
2. Choose **Notification preferences**.
3. Pick **Enable all**, **Mentions only**, or **Disable all**.

This setting persists across devices.

### Configuring notifications per Channel

1. Open **Channel Settings > Preferences**.
2. Scroll to **Collaboration**.
3. Set the default notification mode for the Channel.

Per-Chat settings override this default.

### Configuring notifications per Object Discussion

For Objects with a Discussion thread:

1. Open the Object.
2. Click the three-dot menu in the Discussion tab.
3. Choose **Enable all**, **Mentions only**, or **Disable all**.

### Visual indicators

Even when notifications are disabled, you'll still see:

- **Unread counters** on Channels, Chats, and pinned items in the Vault and sidebar
- **Mention indicators** (a small dot or @ icon) when you've been specifically mentioned
- **A red dot in the sidebar** when there's a system notice to review (like a sync issue or invitation request)

In the **Compact Vault** stripe view, only the unread counter is shown, and mention indicators are hidden to keep the layout clean.

### Reaction notifications

When someone reacts to your message with an emoji, you'll receive a notification by default. To disable this:

1. Open **Vault Settings > Notifications**.
2. Toggle off **Notify on reactions**.

This setting applies globally — there's no per-Channel override for reactions.

### Notification sound

The desktop app uses a single notification sound for all incoming messages. To turn it off:

1. Open **Vault Settings > Notifications**.
2. Toggle off **Sound**.

You can also rely entirely on your operating system's notification settings — if you mute Anytype at the OS level, no in-app sound or system notification will appear.

### Sync status and system notices

Some notifications aren't about messages — they're about the app itself:

- **Sync issues** — when your device can't reach the network, the sync status icon at the top of the sidebar shows a warning
- **Channel invitations** — when someone invites you to a Channel, you'll see a notice in the Vault
- **Access requests** — Owners receive notices when members request access to a Channel

These appear as a red dot on the sidebar — click it to see the queue of notices.

### Mobile vs. desktop

Notifications work the same way on both, but:

- **Desktop** uses your OS notification system (Windows, macOS, Linux). System tray and dock notifications respect your OS-level Do Not Disturb.
- **Mobile** uses push notifications through your device's notification center. You can grant or revoke notification permission for Anytype in your phone's settings.

Per-Channel and per-Chat preferences sync across devices, so muting a Chat on desktop also mutes it on mobile.

### Tips

{% hint style="info" %}
**Set high-volume Channels to "Mentions only".** A team Channel with frequent chat traffic doesn't need to ping you for every message — but you still want to know when someone tags you.
{% endhint %}

{% hint style="info" %}
**Pin important Chats** even if you've muted them. The unread counter still updates, so you can glance at the sidebar to see if anything's happened, without active interruption.
{% endhint %}

{% hint style="warning" %}
If notifications stop working entirely, check both Anytype's notification settings *and* your OS's permission for Anytype to send notifications. The two work in series — if either says no, no notification appears.
{% endhint %}
