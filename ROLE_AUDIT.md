# Public pages and role workflow audit

The site has one public homepage. The public homepage introduces FAB and offers two explicit demo entry choices. It has no personal profile, employer posting button, role switch or workplace navigation. The logo returns to that homepage. The About/community promise and private-feedback link are shared information pages.

| Function | Public | Barista workspace | Café workspace |
| --- | --- | --- | --- |
| Introduction and role choice | Homepage | Logo returns here | Logo returns here |
| Find cover shifts / apply | — | Search, inspect, request | — |
| Employer and branch profile | — | Read from relevant shift | Own business and branches only |
| Find baristas / invite | — | — | Browse people; invite to own open shifts |
| Deputy import / mock rota | — | — | Own business simulation only |
| Post shifts | — | — | Own locations only |
| Applications / bookings | — | Own work only | Own business only |
| Confirm / decline applicants | — | Labelled other-party demo helper only | Own applications, with terms acceptance |
| Accept invitations | — | Invitations addressed to this barista | Labelled other-party demo helper only |
| Submit / correct worked hours | — | Own confirmed work | — |
| Confirm hours / request correction | — | Labelled other-party demo helper only | Own business bookings |
| Invoice view and sample print | — | Own work | Own business |
| Report overdue invoice | — | Own invoice | — |
| Mark invoice paid | — | — | Own business invoice |
| Café cancellation compensation | — | Read status / invoice | Cancel own booking |
| Permanent job opportunities | — | Browse and inspect | — |
| Edit profile | — | Own barista profile | Own business and locations |
| Specialist equipment | — | Optional barista skill | Location's setup |
| Google / calendar demo | — | Separate role settings, own shifts | Separate role settings, own bookings |
| Hide/report a counterpart | — | Café counterpart | Barista counterpart |
| Tour | Choose which role tour | Barista tour | Café tour |
| Feedback / community promise | Shared | Shared | Shared |

No ordinary action or old deep link silently changes persona. Unsupported routes return to the current role's starting page. Explicit role controls and the public entry choices are the only mode changes. The barista shift finder is a search workspace without a promotional hero, employer CTA or cross-role landing content.

Route, action and record-scoping checks are demo UX boundaries. A real service still requires server-side authentication, authorization and shared transactional records. No production security claim is made by these client-side checks.
