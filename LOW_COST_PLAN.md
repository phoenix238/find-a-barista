# Keeping FAB inexpensive without weakening trust

This is a design proposal, not a deployed backend or a promise of permanently free hosting. The current marketplace is a GitHub Pages demo, with fictional records saved in each visitor's browser. Google sign-in and calendar connections are simulations. The external Google Form is the only live response collection.

## A small central core, with optional personal storage

Keep the website static. Put the minimum shared records in a small backend: profile summaries, businesses and location IDs, shifts, applications, confirmed bookings, blocked relationships, moderation decisions, invoice states and review eligibility. These records need one agreed version and server-side permissions; a user must not be able to edit their own rating, erase an unpaid booking or overwrite another person's confirmation.

Cloudflare D1 offers a free allocation, with usage limits and free-plan behaviour documented in its [pricing](https://developers.cloudflare.com/d1/platform/pricing/). A small pilot could fit within that allocation, but usage should be measured. Stay conservative with indexed searches, pagination and limited uploads. Put registration limits before adding charges; don't abandon existing bookings or unpaid invoices when a limit is reached.

Personal Google Drive is a useful optional destination for profile exports, original portfolio photos and invoice backups, with a user-selected access flow. It is a poor sole source for public searchable profiles and shared booking state: permissions can change, files can be edited or removed, and both parties need a consistent record. Google's private [application data folder](https://developers.google.com/workspace/drive/api/guides/appdata) cannot share its contents, and users can delete it. That makes it suitable for private preferences/backups rather than the shared marketplace database.

## Keep large files out of the core

- Save only small compressed public thumbnails, with a strict count and size cap.
- Let people link optional portfolios and CVs instead of uploading large originals.
- Generate invoice PDFs on demand rather than retaining duplicate files.
- Offer an optional export to the user's Drive later, with permission separate from sign-in.
- Never store personal profiles, invoices, emails or bank details in the public GitHub repository.

## Start with fewer paid services

Begin with on-site status checks and optional calendar integration, without SMS. The feedback/interest Google Form requires no custom message-sending service. Publish actual running costs and proposed contributions before introducing fees. A later transparent café contribution could be based on completed bookings, rather than taking a percentage of barista pay.

## Identity is separate from experience

Google sign-in is the intended future account entry, but it is not implemented here. It verifies account control, not professional ability. Social/portfolio links stay explicitly self-provided; completed shifts and mutual reviews build work history. Companies House collection is intentionally excluded following the owner's decision. No business registration or identity document is requested by the demo.

## Feedback ownership

The feedback Form has optional email and a separate contact choice. Response summaries and owner email notifications are off, and editor access should stay restricted. Responses are real personal information if an email is supplied. Review them through Google Forms' Responses tab; do not commit exports to this repository. Delete old feedback/contact data when no longer needed, and keep launch contact limited to people who opted in.
