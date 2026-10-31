# Graph Report - find-a-barista  (2026-10-31)

## Corpus Check
- 4 files · ~7,751 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 102 nodes · 259 edges · 6 communities
- Extraction: 66% EXTRACTED · 34% INFERRED · 0% AMBIGUOUS · INFERRED: 87 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `cb6a32b8`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 6|Community 6]]
- [[_COMMUNITY_Community 11|Community 11]]

## God Nodes (most connected - your core abstractions)
1. `render()` - 21 edges
2. `escapeHTML()` - 20 edges
3. `renderFullProfile()` - 13 edges
4. `$()` - 12 edges
5. `renderBookingDetail()` - 11 edges
6. `modal()` - 10 edges
7. `showApproval()` - 10 edges
8. `showOwnShiftForm()` - 9 edges
9. `showBaristaApplication()` - 9 edges
10. `renderProfileWorkspace()` - 9 edges

## Surprising Connections (you probably didn't know these)
- `closeTour()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `showOwnShiftForm()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `refreshConnections()` --calls--> `$()`  [INFERRED]
  profiles.js → app.js
- `bookingLinkCard()` --calls--> `escapeHTML()`  [INFERRED]
  experience.js → app.js
- `locationCard()` --calls--> `escapeHTML()`  [INFERRED]
  experience.js → app.js

## Import Cycles
- None detected.

## Communities (6 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.22
Nodes (19): apply(), cancellation(), formatDate(), getShift(), hours(), invite(), invoice(), modal() (+11 more)

### Community 1 - "Community 1"
Cohesion: 0.22
Nodes (8): Agreed service rules, Community, Explore, FAB — Find a Barista ✳, Licence, Reviewer release, Run locally, What needs a backend before real use

### Community 2 - "Community 2"
Cohesion: 0.24
Nodes (14): BOOKING_LABELS, bookingScope(), nextBookingStep(), ownCafeShifts(), renderBookingDetail(), renderCafeDashboard(), renderFeedback(), renderLocationProfile() (+6 more)

### Community 3 - "Community 3"
Cohesion: 0.14
Nodes (21): experienceLabel(), experienceMonths(), experienceYears(), calendarEntries(), connectionsCard(), galleryMarkup(), invitationsCard(), isHidden() (+13 more)

### Community 6 - "Community 6"
Cohesion: 0.14
Nodes (24): allShifts(), baristas, filterShifts(), initialShifts, main, now, profile(), render() (+16 more)

### Community 11 - "Community 11"
Cohesion: 0.28
Nodes (9): dateIn(), escapeHTML(), post(), currentMonth(), ensureDemoWorkspace(), locationCard(), showOwnShiftForm(), inputField() (+1 more)

## Knowledge Gaps
- **16 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `BOOKING_LABELS` (+11 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `render()` connect `Community 6` to `Community 2`, `Community 3`?**
  _High betweenness centrality (0.130) - this node is a cross-community bridge._
- **Why does `escapeHTML()` connect `Community 11` to `Community 0`, `Community 2`, `Community 3`, `Community 6`?**
  _High betweenness centrality (0.103) - this node is a cross-community bridge._
- **Why does `renderFullProfile()` connect `Community 3` to `Community 0`, `Community 11`, `Community 6`?**
  _High betweenness centrality (0.057) - this node is a cross-community bridge._
- **Are the 15 inferred relationships involving `render()` (e.g. with `renderBookingDetail()` and `renderCafeDashboard()`) actually correct?**
  _`render()` has 15 INFERRED edges - model-reasoned connections that need verification._
- **Are the 16 inferred relationships involving `escapeHTML()` (e.g. with `bookingLinkCard()` and `locationCard()`) actually correct?**
  _`escapeHTML()` has 16 INFERRED edges - model-reasoned connections that need verification._
- **Are the 5 inferred relationships involving `renderFullProfile()` (e.g. with `render()` and `allShifts()`) actually correct?**
  _`renderFullProfile()` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 7 inferred relationships involving `$()` (e.g. with `closeTour()` and `renderWorkspaceNavigation()`) actually correct?**
  _`$()` has 7 INFERRED edges - model-reasoned connections that need verification._