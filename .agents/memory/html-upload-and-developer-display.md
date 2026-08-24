---
name: HTML uploads and developer display
description: User wants a mobile-first site with an admin-editable developer identity and text-only HTML storage.
---

The product must be mobile-first, show the developer identity on the homepage, and let the admin replace that homepage section through an HTML upload. The developer Discord ID is configured separately and the bot fetches that member's avatar from the configured Discord server. Owner-only profile rings are private by default; users receive them only through an explicit manual grant or a giveaway entitlement. Giveaway winners can receive a ring automatically until an admin-selected expiry date, after which access and the active ring are revoked. Every HTML upload anywhere in the admin must be read as text, sanitized, and saved as text in Firestore; the original file must not be persisted as a file. Each uploaded ring/design must receive a shareable property URL whose metadata renders an automatic preview wherever the URL is pasted on the website.

**Why:** The user explicitly wants phone optimization, a customizable developer ID section, and Firebase-friendly text-only HTML storage.

**How to apply:** Keep the developer Discord ID/config separate from owner permissions when needed, render the saved HTML in a sandboxed safe area, and use the same upload-to-text pipeline for rings, badges, profiles, announcements, and homepage content.
