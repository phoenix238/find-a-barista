# Graph Report - find-a-barista  (2026-10-30)

## Corpus Check
- 2 files · ~3,090 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 40 nodes · 77 edges · 7 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `7aa2f30f`
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

## God Nodes (most connected - your core abstractions)
1. `modal()` - 10 edges
2. `invoice()` - 8 edges
3. `showShift()` - 7 edges
4. `FAB — Find a Barista ✳` - 7 edges
5. `render()` - 6 edges
6. `escapeHTML()` - 5 edges
7. `getShift()` - 5 edges
8. `apply()` - 5 edges
9. `$()` - 4 edges
10. `formatDate()` - 4 edges

## Surprising Connections (you probably didn't know these)
- `filterShifts()` --calls--> `$()`  [EXTRACTED]
  app.js → app.js  _Bridges community 6 → community 5_
- `modal()` --calls--> `$()`  [EXTRACTED]
  app.js → app.js  _Bridges community 6 → community 3_
- `invoice()` --calls--> `dateIn()`  [EXTRACTED]
  app.js → app.js  _Bridges community 3 → community 0_
- `apply()` --calls--> `toast()`  [EXTRACTED]
  app.js → app.js  _Bridges community 6 → community 0_
- `invite()` --calls--> `modal()`  [EXTRACTED]
  app.js → app.js  _Bridges community 3 → community 5_

## Import Cycles
- None detected.

## Communities (7 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.36
Nodes (10): apply(), escapeHTML(), formatDate(), getShift(), hours(), invoice(), pounds(), shiftCard() (+2 more)

### Community 1 - "Community 1"
Cohesion: 0.25
Nodes (7): Agreed service rules, Community, Explore, FAB — Find a Barista ✳, Licence, Run locally, What needs a backend before real use

### Community 2 - "Community 2"
Cohesion: 0.40
Nodes (4): baristas, initialShifts, main, now

### Community 3 - "Community 3"
Cohesion: 0.40
Nodes (5): cancellation(), dateIn(), modal(), post(), profile()

### Community 4 - "Community 4"
Cohesion: 0.40
Nodes (5): render(), renderBaristas(), renderBookings(), renderCommunity(), renderPermanent()

### Community 5 - "Community 5"
Cohesion: 0.50
Nodes (4): allShifts(), filterShifts(), invite(), renderShifts()

### Community 6 - "Community 6"
Cohesion: 0.67
Nodes (3): save(), toast(), $()

## Knowledge Gaps
- **10 isolated node(s):** `now`, `initialShifts`, `baristas`, `main`, `Run locally` (+5 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `modal()` connect `Community 3` to `Community 0`, `Community 2`, `Community 5`, `Community 6`?**
  _High betweenness centrality (0.022) - this node is a cross-community bridge._
- **Why does `invoice()` connect `Community 0` to `Community 2`, `Community 3`?**
  _High betweenness centrality (0.010) - this node is a cross-community bridge._
- **What connects `now`, `initialShifts`, `baristas` to the rest of the system?**
  _10 weakly-connected nodes found - possible documentation gaps or missing edges._