# Graph Report - find-a-barista  (2026-10-31)

## Corpus Check
- 7 files · ~9,736 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 128 nodes · 311 edges · 8 communities
- Extraction: 66% EXTRACTED · 34% INFERRED · 0% AMBIGUOUS · INFERRED: 107 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `9b7e33e2`
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
- [[_COMMUNITY_Community 11|Community 11]]

## God Nodes (most connected - your core abstractions)
1. `render()` - 22 edges
2. `escapeHTML()` - 20 edges
3. `renderFullProfile()` - 14 edges
4. `$()` - 12 edges
5. `renderBookingDetail()` - 12 edges
6. `modal()` - 11 edges
7. `showBaristaApplication()` - 10 edges
8. `showApproval()` - 10 edges
9. `reviewDeputyImport()` - 9 edges
10. `workspaceTitle()` - 9 edges

## Surprising Connections (you probably didn't know these)
- `locationCard()` --calls--> `escapeHTML()`  [INFERRED]
  experience.js → app.js
- `apply()` --calls--> `showBaristaApplication()`  [INFERRED]
  app.js → experience.js
- `closeTour()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `showOwnShiftForm()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `renderCafeDashboard()` --calls--> `escapeHTML()`  [INFERRED]
  experience.js → app.js

## Import Cycles
- None detected.

## Communities (8 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.38
Nodes (15): escapeHTML(), formatDate(), getShift(), hours(), invoice(), modal(), pounds(), shiftCard() (+7 more)

### Community 1 - "Community 1"
Cohesion: 0.17
Nodes (10): Agreed service rules, Community, Deputy demo, Explore, FAB — Find a Barista ✳, Licence, Reviewer release, Run locally (+2 more)

### Community 2 - "Community 2"
Cohesion: 0.15
Nodes (20): BOOKING_LABELS, bookingScope(), locationCard(), nextBookingStep(), ownBookingActionAllowed(), ownCafeShifts(), renderCafeDashboard(), renderFeedback() (+12 more)

### Community 3 - "Community 3"
Cohesion: 0.13
Nodes (25): experienceLabel(), experienceMonths(), experienceYears(), modeConnections(), calendarEntries(), connectionsCard(), findProfile(), galleryMarkup() (+17 more)

### Community 4 - "Community 4"
Cohesion: 0.29
Nodes (6): A small central core, with optional personal storage, Feedback ownership, Identity is separate from experience, Keep large files out of the core, Keeping FAB inexpensive without weakening trust, Start with fewer paid services

### Community 5 - "Community 5"
Cohesion: 0.44
Nodes (8): dateIn(), deputyDashboardCard(), deputyRosterPreview(), deputySamples(), deputyState(), importedDeputyShift(), renderDeputyDemo(), reviewDeputyImport()

### Community 6 - "Community 6"
Cohesion: 0.12
Nodes (25): allShifts(), apply(), baristas, cancellation(), filterShifts(), initialShifts, main, now (+17 more)

### Community 11 - "Community 11"
Cohesion: 0.22
Nodes (9): invite(), post(), save(), toast(), currentMonth(), ensureDemoWorkspace(), showOwnShiftForm(), persistProfileState() (+1 more)

## Knowledge Gaps
- **26 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `WORKSPACE_ROUTES` (+21 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `render()` connect `Community 6` to `Community 0`, `Community 2`, `Community 3`, `Community 5`?**
  _High betweenness centrality (0.103) - this node is a cross-community bridge._
- **Why does `escapeHTML()` connect `Community 0` to `Community 3`, `Community 2`, `Community 11`, `Community 6`?**
  _High betweenness centrality (0.073) - this node is a cross-community bridge._
- **Why does `renderFullProfile()` connect `Community 3` to `Community 0`, `Community 6`?**
  _High betweenness centrality (0.045) - this node is a cross-community bridge._
- **Are the 17 inferred relationships involving `render()` (e.g. with `renderDeputyDemo()` and `renderBookingDetail()`) actually correct?**
  _`render()` has 17 INFERRED edges - model-reasoned connections that need verification._
- **Are the 16 inferred relationships involving `escapeHTML()` (e.g. with `bookingLinkCard()` and `locationCard()`) actually correct?**
  _`escapeHTML()` has 16 INFERRED edges - model-reasoned connections that need verification._
- **Are the 6 inferred relationships involving `renderFullProfile()` (e.g. with `render()` and `allShifts()`) actually correct?**
  _`renderFullProfile()` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Are the 7 inferred relationships involving `$()` (e.g. with `closeTour()` and `renderWorkspaceNavigation()`) actually correct?**
  _`$()` has 7 INFERRED edges - model-reasoned connections that need verification._