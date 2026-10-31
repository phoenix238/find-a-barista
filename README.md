# FAB — Find a Barista ✳

An open-source, community-first project connecting London's freelance baristas with independent coffee shops and event cafés.

**This repository currently contains a static concept demo, not a live marketplace.** All people and initial listings are fictional. Interactions are simulated and saved only in the visitor's browser. Do not enter personal, financial or sensitive information.

## Run locally

No dependencies or build step. Serve this directory with any static web server, for example `python3 -m http.server 8080`, then open `http://localhost:8080`.

GitHub Actions publishes the demo to GitHub Pages when changes reach `main`.

## Explore

- Search and filter sample shifts by London area and café/event type; sort by date or rate.
- View sample barista profiles and simulate an invitation.
- Post a device-local shift with clear café cancellation acceptance.
- Try manual approval or rating-based automatic booking (three reviewed shifts minimum).
- Submit worked hours, simulate the 48-hour confirmation window, view/print sample invoices with 14-day payment terms.
- Simulate café cancellation compensation and overdue invoice posting restrictions.
- Hide sample profiles/cafés while retaining existing booking records.
- Read the community promise and browse sample permanent vacancies.
- Browse searchable barista and café directories and dedicated profile pages.
- Switch between persistent Barista and Café modes in the header. Each mode opens its own profile (or a create-profile prompt), with relevant navigation and booking actions. Profile editing is separate from viewing your own profile. Mode selection is a device-local demo preference, not an authorization boundary.
- Create and edit device-local barista and café profiles, with photos, links and contact visibility choices. Café profiles support multiple locations and managers; baristas have equipment, skills, languages and travel preferences.
- Preview separate Google sign-in and Google Calendar connections, both explicitly simulated. No OAuth request is made and no Google credentials or account data are collected.
- See approved bookings in a simulated calendar; pending and cancelled shifts stay off it. Invitations can be accepted or declined in the demo workspace.

Profile uploads are optional JPG/PNG/WebP images, at most 500 KB each and three gallery photos. They stay in local browser storage. CVs are optional HTTPS links, not file uploads. Social links are self-provided and never labelled verified. Demo reviews are fictional, and newly created profiles start with no ratings. Reports are saved locally without notifying anyone. Profile routes are device-local examples, not shareable user accounts.

## Agreed service rules

London only initially, 18+. Freelance cover is the primary focus; permanent roles have a separate section with employer application links/email. Cafés choose manual approval or an auto-book rating threshold. New baristas need three reviewed shifts before automatic booking. Invitations require acceptance.

Planned hourly floors: current London Living Wage; £16 within 48 hours, £17 within 24 hours, whichever is higher. **The official current Living Wage has not been verified or integrated.** Demo posting requires at least £16 for all shifts and £17 inside 24 hours. Real launch requires an authoritative, maintained rate source and an admin override.

Café cancellation within 24 hours owes 50% of booked paid hours, and after shift start owes 100%. Barista late cancellations have a separate reliability history. No-show reports show as under review and pause automatic bookings pending admin review. Reviews remain hidden until both submit or seven days pass. Reports must allow evidence and resolution.

Baristas submit actual hours and breaks. Cafés have 48 hours to confirm/dispute before invoicing. Payment is directly to the barista by bank transfer, due 14 days after invoice issue. Reported overdue invoices block café posts until paid or resolved. Blocking is mutually invisible for future opportunities, while existing records/disputes remain accessible. Café businesses may have multiple locations and managers.

## What needs a backend before real use

Authentication and age acceptance, café/business/location roles, durable shared records, secure uploads/CVs, email delivery and privacy controls, authoritative time-zone/rate handling, atomic overlap protection, real invitations, hours disputes and deadlines, scheduled invoicing, valid invoice issuer/tax/bank details, review publication, reliability flags, moderation, mutual blocking, admin controls, overdue evidence and resolution, export/deletion and privacy processes. The demo's role simulations are **not access controls**. The overdue demo flag pauses posting globally on that device; the real service must scope it to the responsible café business.

Distance-from-place search, availability calendars and production background automation are not implemented. Area filters work in the demo. No real email messages or invoices are sent; printing generates a visibly marked sample.

## Community

Be kind, be honest, turn up when you commit, and pay people when you owe them. Tester feedback and early interest are collected through the private-response Google Form linked from the website. GitHub Issues are for public code contributions, not private user feedback. No booking fees in this demo. Future infrastructure costs and any proposed café contributions should be published transparently before charges are introduced.

## Licence

AGPL-3.0-or-later. See [LICENSE](LICENSE). Code is open source; this does not grant permission to disclose users' personal information. External fonts are loaded from Google Fonts and are subject to their own licences.


## Reviewer release

The main menu is separated by role. Baristas see Find a shift, My bookings and Permanent jobs, plus their profile. Cafés see My café (their own business dashboard), Find baristas and Bookings. Café mode has no directory of other café owners. All branch profiles link back to the main business workspace. Mode routing is only a demo UI boundary, not production authorization.

Each new browser gets fictional role-specific profiles, shifts and applications to explore. Existing demo profiles and records are retained and migrated. Legacy numeric experience is converted to an estimated start month with a prompt to correct it. Experience is recalculated by calendar month in Europe/London. Specialist equipment is optional. Location IDs remain stable across edits.

The booking manager separates requests/invitations from confirmation, hours, invoices and payment. Manual café approval requires explicit acceptance of terms. Baristas can use a clearly labelled demo helper to simulate the other café approving their own application. No requests are sent to real people. Role-specific tours are available in the mode bar and footer.

Feedback is the one live collection: an external Google Form, configured for anyone with the link, no automatic email collection, no one-response sign-in restriction and no response-summary sharing. The optional email question is separate from the contact choice. Owner response-email notifications are off. The form owner should access the Responses tab in Google Forms to review feedback. No form responses, interest emails, Google credentials or tokens are stored in this public repository.

Run meaningful demo logic checks with `node --test tests/workspaces.test.cjs`.
