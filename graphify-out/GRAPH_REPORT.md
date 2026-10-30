# Graph Report - find-a-barista  (2026-10-30)

## Corpus Check
- 3 files · ~5,546 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 70 nodes · 155 edges · 10 communities
- Extraction: 83% EXTRACTED · 17% INFERRED · 0% AMBIGUOUS · INFERRED: 27 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `70e1cecb`
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
- [[_COMMUNITY_Community 8|Community 8]]
- [[_COMMUNITY_Community 9|Community 9]]
- [[_COMMUNITY_Community 11|Community 11]]

## God Nodes (most connected - your core abstractions)
1. `escapeHTML()` - 13 edges
2. `render()` - 13 edges
3. `renderFullProfile()` - 11 edges
4. `modal()` - 9 edges
5. `$()` - 8 edges
6. `showShift()` - 8 edges
7. `invoice()` - 8 edges
8. `setAppMode()` - 8 edges
9. `renderProfileWorkspace()` - 7 edges
10. `showProfileInvite()` - 7 edges

## Surprising Connections (you probably didn't know these)
- `render()` --calls--> `renderPeopleDirectory()`  [INFERRED]
  app.js → profiles.js
- `refreshConnections()` --calls--> `$()`  [INFERRED]
  profiles.js → app.js
- `renderFullProfile()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js
- `renderModeNavigation()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js
- `renderProfileWorkspace()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js

## Import Cycles
- None detected.

## Communities (10 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.39
Nodes (8): formatDate(), getShift(), hours(), invoice(), pounds(), shiftCard(), showShift(), submitHours()

### Community 1 - "Community 1"
Cohesion: 0.25
Nodes (7): Agreed service rules, Community, Explore, FAB — Find a Barista ✳, Licence, Run locally, What needs a backend before real use

### Community 2 - "Community 2"
Cohesion: 0.29
Nodes (9): apply(), baristas, cancellation(), dateIn(), initialShifts, main, modal(), now (+1 more)

### Community 3 - "Community 3"
Cohesion: 0.21
Nodes (9): cafeForShift(), calendarEntries(), findProfile(), LONDON_AREAS, profileList(), renderCalendarPreview(), renderPeopleDirectory(), SAMPLE_CAFE_DETAILS (+1 more)

### Community 4 - "Community 4"
Cohesion: 0.50
Nodes (4): render(), renderBookings(), renderCommunity(), renderPermanent()

### Community 5 - "Community 5"
Cohesion: 0.40
Nodes (5): allShifts(), filterShifts(), invite(), renderShifts(), showProfileInvite()

### Community 6 - "Community 6"
Cohesion: 0.38
Nodes (7): profile(), save(), toast(), persistProfileState(), renderModeNavigation(), setAppMode(), $()

### Community 8 - "Community 8"
Cohesion: 0.60
Nodes (5): connectionsCard(), invitationsCard(), refreshConnections(), renderProfileWorkspace(), sectionCard()

### Community 9 - "Community 9"
Cohesion: 0.40
Nodes (5): galleryMarkup(), isHidden(), profileLinks(), renderFullProfile(), renderMyModeProfile()

### Community 11 - "Community 11"
Cohesion: 0.40
Nodes (6): escapeHTML(), inputField(), locationFields(), profileAvatar(), profileCard(), ratingText()

## Knowledge Gaps
- **13 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `LONDON_AREAS` (+8 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `render()` connect `Community 4` to `Community 2`, `Community 3`, `Community 5`, `Community 6`, `Community 8`, `Community 9`?**
  _High betweenness centrality (0.101) - this node is a cross-community bridge._
- **Why does `escapeHTML()` connect `Community 11` to `Community 0`, `Community 2`, `Community 5`, `Community 6`, `Community 8`, `Community 9`?**
  _High betweenness centrality (0.098) - this node is a cross-community bridge._
- **Why does `renderFullProfile()` connect `Community 9` to `Community 3`, `Community 4`, `Community 5`, `Community 8`, `Community 11`?**
  _High betweenness centrality (0.059) - this node is a cross-community bridge._
- **Are the 7 inferred relationships involving `escapeHTML()` (e.g. with `inputField()` and `profileAvatar()`) actually correct?**
  _`escapeHTML()` has 7 INFERRED edges - model-reasoned connections that need verification._
- **Are the 7 inferred relationships involving `render()` (e.g. with `renderCalendarPreview()` and `renderFullProfile()`) actually correct?**
  _`render()` has 7 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `renderFullProfile()` (e.g. with `render()` and `allShifts()`) actually correct?**
  _`renderFullProfile()` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `$()` (e.g. with `refreshConnections()` and `renderModeNavigation()`) actually correct?**
  _`$()` has 3 INFERRED edges - model-reasoned connections that need verification._