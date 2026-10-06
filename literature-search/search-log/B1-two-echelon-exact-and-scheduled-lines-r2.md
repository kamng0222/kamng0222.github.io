# Facet B1 two-echelon-exact-and-scheduled-lines — round 2 notes

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet brief: fill the near-empty multi-echelon facet with the exact / branch-and-price two-echelon literature
(2E-CVRP, 2E-VRPTW, CLRP, two-tier city logistics) in OR and TS, plus the feeder-to-scheduled-trunk
synchronization stream (PDPTW with scheduled lines, PDP with transfers, TRB/TS). Note how satellite
synchronization and scheduled-line capacity constraints are formulated, since spaceports act as satellites
feeding fixed launch slots.
In-scope venues: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).
Agent: literature-search subagent (round 2). Date: 2026-10-06 (07:22 UTC).

## STATUS: NO SEARCH COULD BE EXECUTED IN ROUND 2 — FACET REMAINS UNSEARCHED

The first batch of five WebSearch queries (listed below) was refused in full with:
"Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn,
shared by every agent in it). Continue with the information already gathered instead of searching again ...
do not work around the limit by querying search engines with curl or wget from Bash, or by searching or
fetching through a third-party reader, proxy or archive service."

WebSearch is the only internet path in this environment (WebFetch, curl, wget, pip are egress-blocked), and the
budget notice forbids work-arounds, so none was attempted. Round 1 of this facet
(B1-multi-echelon-synchronization-r1.md) failed the same way, so after two rounds NONE of the facet's named
targets has been seen in any search result in this workflow run:
Perboli-Tadei-Vigo TS 2011; Baldacci-Mingozzi-Roberti-Wolfler Calvo OR 2013; Baldacci-Mingozzi-Wolfler Calvo
OR 2011; Jepsen-Spoorendonk-Ropke TS 2013; Santos-Mateus-da Cunha TS 2015; Dellaert-Dashty Saridarq-Van
Woensel-Crainic TS 2019; Mhamedi-Andersson-Cherkesly-Desaulniers TS 2022; Schneider-Loffler TS 2019;
Crainic-Ricciardi-Storchi TS 2009 and TRC 2004; Crainic-Errico-Rei-Ricciardi TS 2016; Ghilas-Demir-Van Woensel
TRB 2016; Ghilas-Cordeau-Demir-Van Woensel TS 2018; Masson-Lehuede-Peton TS 2013; Fatnassi-Chaouachi-Klibi
TRB 2015.

Per the task rules (never record a paper from memory alone; never invent a DOI; a wrong venue or invented paper
is worse than a missing one), these targets are NOT recorded. The structured output carries only two
pass-through items whose title and venue were corroborated by search results that sibling agents logged earlier
in this run (see "Candidates" below), both flagged with provenance and downgraded confidence.

Remedy: run this facet in a fresh turn (r3) with a reset or un-shared WebSearch budget, or raise
CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION. The r3 query plan below is ready to run as-is; the facet has now
failed twice and should get first call on the next budget.

## Queries submitted this round — ALL REFUSED (budget exhausted) — 5

1. `Perboli Tadei Vigo two-echelon capacitated vehicle routing problem Transportation Science 2011` (standard) — REFUSED
2. `Baldacci Mingozzi Roberti Wolfler Calvo exact algorithm two-echelon capacitated vehicle routing Operations Research 2013` (standard) — REFUSED
3. `Baldacci Mingozzi Wolfler Calvo exact method capacitated location-routing problem Operations Research 2011` (standard) — REFUSED
4. `Jepsen Spoorendonk Ropke branch-and-cut two-echelon capacitated vehicle routing Transportation Science 2013` (standard) — REFUSED
5. `Santos Mateus da Cunha branch-and-cut-and-price two-echelon capacitated vehicle routing Transportation Science 2015` (standard) — REFUSED

## Local fallbacks checked (no internet needed)

- Repository /home/user/kamng0222.github.io: no bibliography, no .bib/.ris, no DOI strings for the four venues.
- All 22 sibling notes files in this directory, grepped for the facet's author surnames and topic phrases
  (two-echelon, two-tier, scheduled line(s), transfers, location-routing, synchronization). Hits inside this
  facet's scope: Drexl 2012 TS (seen by facet B2-time-windows-periodic-launch on a RePEc inm/ortrsc index page)
  and Xie-Ouyang-Wong 2016 TS (seen by facet B2-network-design-uncertainty on the INFORMS publisher page with
  DOI in the URL). Other hits (Wong et al. 2008 TS; Ibarra-Rojas & Rios-Solis 2012 TRB; Hewitt & Lehuede TRB 2023
  mentioned only as a plan item) belong to the timetable-synchronization / SND facets and are not re-recorded.
- verified/*.ndjson (round-1 verifier output, 160 records): same two in-scope hits. Note that the verifier record
  B2-verified-r1-3 states the Drexl DOI 10.1287/trsc.1110.0400 was "filled from recollection", i.e. NOT seen in a
  search result; this agent therefore carries Drexl with an EMPTY doi. The Xie et al. DOI 10.1287/trsc.2015.0630
  appears inside the publisher URL recorded by the search agent, so it is carried.
- No saved WebSearch result blocks mentioning any facet target exist anywhere under 

## Candidates — pass-through only (NOT searched by this agent)

| # | Title | Authors | Year | Venue | DOI (seen) | URL where a sibling saw it | Conf. | Provenance |
|---|-------|---------|------|-------|-----------|----------------------------|-------|------------|
| 1 | Synchronization in Vehicle Routing—A Survey of VRPs with Multiple Synchronization Constraints | Drexl | 2012 | Transportation Science 46(3):297-316 | "" (not seen in any search result) | https://ideas.repec.org/a/inm/ortrsc/v46y2012i3p297-316.html | medium | B2-time-windows-periodic-launch-r1.md row 17; verified/B1-verified-r1-2.ndjson, verified/B2-verified-r1-3.ndjson |
| 2 | Reliable Location-Routing Design Under Probabilistic Facility Disruptions | Xie, Ouyang, Wong | 2016 | Transportation Science 50(3):1128-1138 | 10.1287/trsc.2015.0630 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2015.0630 ; https://ideas.repec.org/a/inm/ortrsc/v50y2016i3p1128-1138.html | medium | B2-network-design-uncertainty-r1.md row 15; verified/B2-verified-r1-1.ndjson, verified/B1-verified-r1-2.ndjson |

Method notes (restricted to what the corroborated title/venue supports; nothing beyond the title was seen in a
snippet in this run):
- Drexl 2012 (TS): survey and classification of VRPs whose routes are interdependent through synchronization
  constraints. Transfer to the facet: two-echelon satellite transfers (first-echelon truck must meet
  second-echelon vehicle at the satellite) and feeder-to-scheduled-line transfers are exactly the operation /
  movement / load synchronization classes this survey organizes; the spaceport-to-launch-slot problem is a
  movement-and-load synchronization of ground feeders with a fixed-schedule trunk service.
- Xie, Ouyang & Wong 2016 (TS): location-routing design with facilities that fail probabilistically. Transfer:
  orbital hubs / depots that may be unavailable, with spokes (spaceports) reassigned to surviving hubs.

## Checklist of formulation features to extract in r3 (per the facet brief; NOT findings)
- Satellite synchronization in 2E-VRP/2E-VRPTW: whether satellites are capacitated, whether first- and
  second-echelon arrivals are coupled by equality (no storage) or by time windows with storage, and how the
  coupling enters pricing (resource-constrained shortest path with satellite-visit resources) or branch-and-cut
  (satellite-capacity and flow-linking cuts).
- Scheduled-line capacity in PDPTW-SL: fixed timetable of trunk departures, per-departure capacity, transfer
  node time windows, and how demand uncertainty is handled (scenario-based recourse).
- Two-tier city logistics: time-dependent service network design over satellites, fleet synchronization, and
  the stochastic extension (demand uncertainty, scenario trees).
- Mapping to spaceport feeder design: spaceports = satellites; launch vehicles = second-echelon vehicles with
  fixed departure slots (scheduled lines); orbital hubs = depots/transfer orbits; turnaround = vehicle
  re-use constraints; launch-window capacity = scheduled-line capacity.

## Query plan for r3 — 36 queries, none attempted

Named targets (OR/TS exact two-echelon and CLRP)
1. `Perboli Tadei Vigo "two-echelon capacitated vehicle routing problem" "Transportation Science"`
2. `Baldacci Mingozzi Roberti "Wolfler Calvo" "two-echelon" exact "Operations Research"`
3. `Baldacci Mingozzi "Wolfler Calvo" "capacitated location-routing" exact "Operations Research" 2011`
4. `Jepsen Spoorendonk Ropke "two-echelon" branch-and-cut "Transportation Science" 2013`
5. `Santos Mateus "da Cunha" "two-echelon" branch-and-cut-and-price "Transportation Science" 2015`
6. `Dellaert "Dashty Saridarq" "Van Woensel" Crainic "two-echelon" "time windows" "Transportation Science"`
7. `Mhamedi Andersson Cherkesly Desaulniers "two-echelon" branch-price-and-cut "Transportation Science" 2022`
8. `Schneider Loffler "location-routing" tree-based search "Transportation Science" 2019`
9. `Crainic Ricciardi Storchi "two-tier" city logistics "Transportation Science" 2009`
10. `Crainic Ricciardi Storchi "city logistics" "Transportation Research Part C" 2004`
11. `Crainic Errico Rei Ricciardi "two-tier" city logistics uncertainty "Transportation Science" 2016`
Scheduled lines / transfers (TRB, TS)
12. `Ghilas Demir "Van Woensel" "scheduled lines" stochastic demand "Transportation Research Part B" 2016`
13. `Ghilas Cordeau Demir "Van Woensel" branch-and-price "scheduled lines" "Transportation Science" 2018`
14. `Masson Lehuede Peton "pickup and delivery problem with transfers" "Transportation Science" 2013`
15. `Fatnassi Chaouachi Klibi "Transportation Research Part B" 2015 personal rapid transit freight`
16. `"pickup and delivery" "scheduled lines" "Transportation Science"`
17. `"pickup and delivery" transfers OR transshipment "Transportation Research Part B"`
Methodology / problem phrases with venue restrictors (facet-mandated)
18. `two-echelon vehicle routing "Transportation Science" branch-and-price`
19. `pickup and delivery scheduled lines "Transportation Science"`
20. `two-tier city logistics "Transportation Science"`
21. `"two-echelon" "location-routing" "Transportation Research Part B"`
22. `"two-echelon" satellites synchronization "Transportation Research Part C"`
23. `"multi-echelon" distribution "Operations Research" INFORMS exact`
DOI-prefix strings
24. `"10.1287/trsc" "two-echelon"`
25. `"10.1287/opre" "two-echelon" OR "location-routing"`
26. `"10.1016/j.trb" "scheduled lines" OR "two-echelon"`
27. `"10.1016/j.trc" "two-echelon" OR "city logistics" synchronization`
Recent 2021-2026 (at least six)
28. `"two-echelon" vehicle routing 2023 "Transportation Science" exact`
29. `"two-echelon" "time windows" branch-price-and-cut 2024 "Transportation Science"`
30. `"two-echelon" location-routing 2024 OR 2025 "Transportation Research Part B"`
31. `"scheduled lines" OR "public transport" freight integration 2023 OR 2024 "Transportation Research Part C"`
32. `"two-echelon" stochastic OR robust 2025 "Transportation Research Part B" OR "Operations Research"`
33. `"pickup and delivery" transfers synchronization 2025 OR 2026 "Transportation Science"`
Classics before 2005 (at least four)
34. `Laporte Nobert Taillefer "location-routing" "Transportation Science" 1988`
35. `Jacobsen Madsen two-level location routing newspaper 1980`
36. `Daganzo "transshipment" OR "break-bulk" terminals "Transportation Science" OR "Operations Research" 1987`
37. `Hall "consolidation" terminals freight "Transportation Research Part B" 1987`

## Gaps
- Entire facet brief uncorroborated after two rounds: no 2E-CVRP / 2E-VRPTW exact paper, no CLRP exact paper,
  no two-tier city logistics paper, no PDPTW with scheduled lines or PDP with transfers paper, no 2021-2026 or
  pre-2005 item has been seen in a search result. This is a tooling gap (search budget), not evidence that the
  literature is thin.
- No spaceport / space-logistics adjacent-venue paper checked for this facet.
