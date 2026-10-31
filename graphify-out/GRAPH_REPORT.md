# Graph Report - find-a-barista  (2026-10-31)

## Corpus Check
- 6 files · ~8,822 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 119 nodes · 283 edges · 11 communities
- Extraction: 67% EXTRACTED · 33% INFERRED · 0% AMBIGUOUS · INFERRED: 94 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `0b5f3cbc`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]
- [[_COMMUNITY_Community 5|Community 5]]
- [[_COMMUNITY_Community 6|Community 6]]
- [[_COMMUNITY_Community 7|Community 7]]
- [[_COMMUNITY_Community 8|Community 8]]
- [[_COMMUNITY_Community 9|Community 9]]
- [[_COMMUNITY_Community 11|Community 11]]

## God Nodes (most connected - your core abstractions)
1. `render()` - 21 edges
2. `escapeHTML()` - 20 edges
3. `renderFullProfile()` - 14 edges
4. `$()` - 12 edges
5. `renderBookingDetail()` - 11 edges
6. `modal()` - 10 edges
7. `showBaristaApplication()` - 10 edges
8. `showApproval()` - 10 edges
9. `showOwnShiftForm()` - 9 edges
10. `renderProfileWorkspace()` - 9 edges

## Surprising Connections (you probably didn't know these)
- `locationCard()` --calls--> `escapeHTML()`  [INFERRED]
  experience.js → app.js
- `apply()` --calls--> `showBaristaApplication()`  [INFERRED]
  app.js → experience.js
- `invite()` --calls--> `showProfileInvite()`  [INFERRED]
  app.js → profiles.js
- `closeTour()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `showOwnShiftForm()` --calls--> `$()`  [INFERRED]
  experience.js → app.js

## Import Cycles
- None detected.

## Communities (11 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.38
Nodes (15): escapeHTML(), formatDate(), getShift(), hours(), invoice(), modal(), pounds(), shiftCard() (+7 more)

### Community 1 - "Community 1"
Cohesion: 0.18
Nodes (9): Agreed service rules, Community, Explore, FAB — Find a Barista ✳, Licence, Reviewer release, Run locally, What needs a backend before real use (+1 more)

### Community 2 - "Community 2"
Cohesion: 0.14
Nodes (20): renderBookings(), BOOKING_LABELS, locationCard(), nextBookingStep(), ownBookingActionAllowed(), ownCafeShifts(), renderCafeDashboard(), renderFeedback() (+12 more)

### Community 3 - "Community 3"
Cohesion: 0.28
Nodes (6): LONDON_AREAS, profileAvatar(), profileCard(), ratingText(), SAMPLE_CAFE_DETAILS, sampleReviews

### Community 4 - "Community 4"
Cohesion: 0.29
Nodes (6): A small central core, with optional personal storage, Feedback ownership, Identity is separate from experience, Keep large files out of the core, Keeping FAB inexpensive without weakening trust, Start with fewer paid services

### Community 5 - "Community 5"
Cohesion: 0.32
Nodes (8): currentMonth(), experienceLabel(), experienceMonths(), connectionsCard(), invitationsCard(), refreshConnections(), renderProfileWorkspace(), sectionCard()

### Community 6 - "Community 6"
Cohesion: 0.11
Nodes (27): allShifts(), apply(), baristas, cancellation(), filterShifts(), initialShifts, invite(), main (+19 more)

### Community 7 - "Community 7"
Cohesion: 0.40
Nodes (5): experienceYears(), cafeForShift(), findProfile(), profileList(), showProfileInvite()

### Community 8 - "Community 8"
Cohesion: 0.40
Nodes (5): galleryMarkup(), isHidden(), profileLinks(), renderFullProfile(), renderMyModeProfile()

### Community 9 - "Community 9"
Cohesion: 0.67
Nodes (3): modeConnections(), calendarEntries(), renderCalendarPreview()

### Community 11 - "Community 11"
Cohesion: 0.33
Nodes (6): dateIn(), post(), ensureDemoWorkspace(), showOwnShiftForm(), inputField(), locationFields()

## Knowledge Gaps
- **25 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `WORKSPACE_ROUTES` (+20 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `render()` connect `Community 6` to `Community 0`, `Community 2`, `Community 5`, `Community 8`, `Community 9`?**
  _High betweenness centrality (0.098) - this node is a cross-community bridge._
- **Why does `escapeHTML()` connect `Community 0` to `Community 2`, `Community 3`, `Community 5`, `Community 6`, `Community 7`, `Community 8`, `Community 11`?**
  _High betweenness centrality (0.078) - this node is a cross-community bridge._
- **Why does `renderFullProfile()` connect `Community 8` to `Community 0`, `Community 3`, `Community 5`, `Community 6`, `Community 7`, `Community 9`?**
  _High betweenness centrality (0.049) - this node is a cross-community bridge._
- **Are the 16 inferred relationships involving `render()` (e.g. with `renderBookingDetail()` and `renderCafeDashboard()`) actually correct?**
  _`render()` has 16 INFERRED edges - model-reasoned connections that need verification._
- **Are the 16 inferred relationships involving `escapeHTML()` (e.g. with `bookingLinkCard()` and `locationCard()`) actually correct?**
  _`escapeHTML()` has 16 INFERRED edges - model-reasoned connections that need verification._
- **Are the 6 inferred relationships involving `renderFullProfile()` (e.g. with `render()` and `allShifts()`) actually correct?**
  _`renderFullProfile()` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Are the 7 inferred relationships involving `$()` (e.g. with `closeTour()` and `renderWorkspaceNavigation()`) actually correct?**
  _`$()` has 7 INFERRED edges - model-reasoned connections that need verification._