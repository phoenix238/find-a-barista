# Graph Report - find-a-barista  (2026-10-30)

## Corpus Check
- 3 files · ~5,247 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 67 nodes · 139 edges · 12 communities (10 shown, 2 thin omitted)
- Extraction: 87% EXTRACTED · 13% INFERRED · 0% AMBIGUOUS · INFERRED: 18 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `32f892c6`
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
- [[_COMMUNITY_Community 10|Community 10]]
- [[_COMMUNITY_Community 11|Community 11]]

## God Nodes (most connected - your core abstractions)
1. `escapeHTML()` - 12 edges
2. `renderFullProfile()` - 10 edges
3. `modal()` - 9 edges
4. `render()` - 9 edges
5. `showShift()` - 8 edges
6. `invoice()` - 8 edges
7. `renderProfileWorkspace()` - 7 edges
8. `FAB — Find a Barista ✳` - 7 edges
9. `$()` - 6 edges
10. `showProfileInvite()` - 6 edges

## Surprising Connections (you probably didn't know these)
- `render()` --calls--> `renderPeopleDirectory()`  [INFERRED]
  app.js → profiles.js
- `inputField()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js
- `profileAvatar()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js
- `profileCard()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js
- `renderFullProfile()` --calls--> `escapeHTML()`  [INFERRED]
  profiles.js → app.js

## Import Cycles
- None detected.

## Communities (12 total, 2 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.29
Nodes (14): apply(), dateIn(), escapeHTML(), formatDate(), getShift(), hours(), invoice(), modal() (+6 more)

### Community 1 - "Community 1"
Cohesion: 0.25
Nodes (7): Agreed service rules, Community, Explore, FAB — Find a Barista ✳, Licence, Run locally, What needs a backend before real use

### Community 2 - "Community 2"
Cohesion: 0.33
Nodes (5): baristas, cancellation(), initialShifts, main, now

### Community 3 - "Community 3"
Cohesion: 0.21
Nodes (9): calendarEntries(), LONDON_AREAS, profileAvatar(), profileCard(), ratingText(), renderCalendarPreview(), renderPeopleDirectory(), SAMPLE_CAFE_DETAILS (+1 more)

### Community 4 - "Community 4"
Cohesion: 0.50
Nodes (4): render(), renderBookings(), renderCommunity(), renderPermanent()

### Community 5 - "Community 5"
Cohesion: 0.67
Nodes (3): allShifts(), filterShifts(), renderShifts()

### Community 6 - "Community 6"
Cohesion: 0.67
Nodes (3): save(), toast(), persistProfileState()

### Community 8 - "Community 8"
Cohesion: 0.83
Nodes (4): connectionsCard(), invitationsCard(), renderProfileWorkspace(), sectionCard()

### Community 9 - "Community 9"
Cohesion: 0.33
Nodes (6): findProfile(), galleryMarkup(), isHidden(), profileLinks(), profileList(), renderFullProfile()

### Community 10 - "Community 10"
Cohesion: 0.67
Nodes (3): profile(), refreshConnections(), $()

## Knowledge Gaps
- **13 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `LONDON_AREAS` (+8 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `escapeHTML()` connect `Community 0` to `Community 2`, `Community 3`, `Community 7`, `Community 8`, `Community 9`, `Community 11`?**
  _High betweenness centrality (0.118) - this node is a cross-community bridge._
- **Why does `render()` connect `Community 4` to `Community 2`, `Community 3`, `Community 5`, `Community 8`, `Community 9`?**
  _High betweenness centrality (0.088) - this node is a cross-community bridge._
- **Why does `renderFullProfile()` connect `Community 9` to `Community 0`, `Community 3`, `Community 4`, `Community 5`, `Community 8`?**
  _High betweenness centrality (0.069) - this node is a cross-community bridge._
- **Are the 6 inferred relationships involving `escapeHTML()` (e.g. with `inputField()` and `profileAvatar()`) actually correct?**
  _`escapeHTML()` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `renderFullProfile()` (e.g. with `render()` and `allShifts()`) actually correct?**
  _`renderFullProfile()` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 4 inferred relationships involving `render()` (e.g. with `renderCalendarPreview()` and `renderFullProfile()`) actually correct?**
  _`render()` has 4 INFERRED edges - model-reasoned connections that need verification._
- **What connects `now`, `initialShifts`, `baristas` to the rest of the system?**
  _13 weakly-connected nodes found - possible documentation gaps or missing edges._