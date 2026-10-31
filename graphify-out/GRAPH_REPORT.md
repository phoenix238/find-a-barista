# Graph Report - find-a-barista  (2026-10-31)

## Corpus Check
- 5 files · ~8,342 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 110 nodes · 267 edges · 9 communities
- Extraction: 67% EXTRACTED · 33% INFERRED · 0% AMBIGUOUS · INFERRED: 87 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `c8274b89`
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
- [[_COMMUNITY_Community 11|Community 11]]

## God Nodes (most connected - your core abstractions)
1. `render()` - 21 edges
2. `escapeHTML()` - 20 edges
3. `renderFullProfile()` - 13 edges
4. `$()` - 12 edges
5. `renderBookingDetail()` - 11 edges
6. `modal()` - 10 edges
7. `showBaristaApplication()` - 10 edges
8. `showApproval()` - 10 edges
9. `showOwnShiftForm()` - 9 edges
10. `renderProfileWorkspace()` - 9 edges

## Surprising Connections (you probably didn't know these)
- `apply()` --calls--> `showBaristaApplication()`  [INFERRED]
  app.js → experience.js
- `post()` --calls--> `showOwnShiftForm()`  [INFERRED]
  app.js → experience.js
- `closeTour()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `renderWorkspaceNavigation()` --calls--> `$()`  [INFERRED]
  experience.js → app.js
- `showOwnShiftForm()` --calls--> `$()`  [INFERRED]
  experience.js → app.js

## Import Cycles
- None detected.

## Communities (9 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.33
Nodes (14): formatDate(), getShift(), hours(), invoice(), modal(), pounds(), shiftCard(), showShift() (+6 more)

### Community 1 - "Community 1"
Cohesion: 0.22
Nodes (8): Agreed service rules, Community, Explore, FAB — Find a Barista ✳, Licence, Reviewer release, Run locally, What needs a backend before real use

### Community 2 - "Community 2"
Cohesion: 0.24
Nodes (14): BOOKING_LABELS, bookingScope(), nextBookingStep(), ownCafeShifts(), renderBookingDetail(), renderCafeDashboard(), renderFeedback(), renderLocationProfile() (+6 more)

### Community 3 - "Community 3"
Cohesion: 0.13
Nodes (23): invite(), experienceLabel(), experienceMonths(), experienceYears(), calendarEntries(), connectionsCard(), findProfile(), galleryMarkup() (+15 more)

### Community 4 - "Community 4"
Cohesion: 0.29
Nodes (6): A small central core, with optional personal storage, Feedback ownership, Identity is separate from experience, Keep large files out of the core, Keeping FAB inexpensive without weakening trust, Start with fewer paid services

### Community 5 - "Community 5"
Cohesion: 0.24
Nodes (10): render(), renderBookings(), renderCommunity(), renderPermanent(), save(), renderDemoWelcome(), renderWorkspaceNavigation(), renderModeNavigation() (+2 more)

### Community 6 - "Community 6"
Cohesion: 0.22
Nodes (10): allShifts(), apply(), baristas, cancellation(), filterShifts(), initialShifts, main, now (+2 more)

### Community 7 - "Community 7"
Cohesion: 0.29
Nodes (7): profile(), toast(), closeTour(), routeTo(), showTourStep(), persistProfileState(), $()

### Community 11 - "Community 11"
Cohesion: 0.29
Nodes (10): dateIn(), escapeHTML(), currentMonth(), ensureDemoWorkspace(), locationCard(), showOwnShiftForm(), inputField(), invitationsCard() (+2 more)

## Knowledge Gaps
- **21 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `BOOKING_LABELS` (+16 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `render()` connect `Community 5` to `Community 2`, `Community 3`, `Community 6`, `Community 7`, `Community 11`?**
  _High betweenness centrality (0.113) - this node is a cross-community bridge._
- **Why does `escapeHTML()` connect `Community 11` to `Community 0`, `Community 2`, `Community 3`, `Community 5`, `Community 6`?**
  _High betweenness centrality (0.090) - this node is a cross-community bridge._
- **Why does `renderFullProfile()` connect `Community 3` to `Community 11`, `Community 5`, `Community 6`?**
  _High betweenness centrality (0.050) - this node is a cross-community bridge._
- **Are the 15 inferred relationships involving `render()` (e.g. with `renderBookingDetail()` and `renderCafeDashboard()`) actually correct?**
  _`render()` has 15 INFERRED edges - model-reasoned connections that need verification._
- **Are the 16 inferred relationships involving `escapeHTML()` (e.g. with `bookingLinkCard()` and `locationCard()`) actually correct?**
  _`escapeHTML()` has 16 INFERRED edges - model-reasoned connections that need verification._
- **Are the 5 inferred relationships involving `renderFullProfile()` (e.g. with `render()` and `allShifts()`) actually correct?**
  _`renderFullProfile()` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 7 inferred relationships involving `$()` (e.g. with `closeTour()` and `renderWorkspaceNavigation()`) actually correct?**
  _`$()` has 7 INFERRED edges - model-reasoned connections that need verification._