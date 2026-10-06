# Facet B1 liner-feeder-core-ts-trb — round 2 notes (re-run of liner shipping / feeder network design, TS and TR-B focus)

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet brief: re-run the liner shipping and feeder network design facet (round 1 returned nothing), targeting
Transportation Science (10.1287/trsc) and Transportation Research Part B (10.1016/j.trb, 0191-2615). For each paper
record how cyclic rotations, vessel capacity, transshipment at hubs and transit-time limits are modelled, since these
map to launch cadence, vehicle capacity, orbital-hub transfer and phasing windows.
Date: 2026-10-06. Agent: literature-search subagent (round 2).

## STATUS: NO SEARCHES COULD BE EXECUTED IN ROUND 2 EITHER — ZERO CORROBORATED CANDIDATES

Every WebSearch call issued by this agent (6 queries, first batch) was refused with:
"Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn,
shared by every agent in it). Continue with the information already gathered instead of searching again ...
do not work around the limit by querying search engines with curl or wget ... or through a third-party reader,
proxy or archive service."

WebFetch, curl, wget and all direct HTTP paths are blocked by the egress proxy in any case. The budget notice
forbids work-arounds, so none were attempted.

Local fallbacks checked (all negative for this facet):
- Repository /home/user/kamng0222.github.io: contains only .git — no bibliography.
- Sibling notes in this directory (20 files): the only maritime items corroborated by any sibling search are three
  berth-allocation papers (Imai, Nishimura, Papadimitriou TR-B 2001; Imai, Sun, Nishimura, Papadimitriou TR-B 2005;
  Meisel & Bierwirth TS 2013), recorded by the time-windows facet. They are port-operations papers, not liner
  shipping network design or feeder network design, so they are NOT re-recorded here.
- verified/*.ndjson (round-1 verified records): same three berth-allocation items only; no liner-shipping network
  design, fleet deployment, cargo routing, empty-repositioning or feeder-network paper.
- Session tool-results folder: contains no saved WebSearch result blocks from any agent that mention liner shipping.
- The round-1 note B1-liner-feeder-shipping-r1.md records zero candidates and a memory-only seed list that it
  explicitly marks UNVERIFIED; nothing there is corroborated by a search result, so nothing is borrowed.

Consequence: the structured output for this facet again has an EMPTY candidates list. This is a tooling-coverage
gap, not evidence that the literature is thin: the liner-shipping network design literature in TS and TR-B is
large, well-cited and directly relevant. The task rules (never record a paper from memory alone; never invent a
DOI; a wrong venue or invented paper is worse than a missing one) make an empty list the only defensible output.

Recommended remedy: run this facet in a fresh turn (r3) with an un-shared or reset WebSearch budget, or raise
CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION, and give the liner-shipping facet first call on the budget since it has
now failed twice.

## Queries issued in round 2 (all REFUSED — budget exhausted; none returned results)

1. Agarwal Ergun "Ship scheduling and network design for cargo routing in liner shipping" Transportation Science 2008 (standard) — NOT EXECUTED
2. Brouer Alvarez Plum Pisinger Sigurd "A Base Integer Programming Model and Benchmark Suite for Liner-Shipping Network Design" Transportation Science (standard) — NOT EXECUTED
3. Meng Wang Andersson Thun "Containership Routing and Scheduling in Liner Shipping: Overview and Future Research Directions" Transportation Science 2014 (standard) — NOT EXECUTED
4. Koza Desaulniers Ropke "Integrated liner shipping network design and scheduling" Transportation Science 2020 (standard) — NOT EXECUTED
5. Tierney Askelsdottir Jensen Pisinger "Solving the liner shipping fleet repositioning problem with cargo flows" Transportation Science 2015 (standard) — NOT EXECUTED
6. Karsten Ropke Pisinger "Simultaneous optimization of container ship sailing speed and container routing with transit time restrictions" Transportation Science 2018 (standard) — NOT EXECUTED

## Query programme for round 3 (planned, not run) — ordered by priority

Named-paper corroboration (TS / TR-B), one query each:
7.  Song Dong "Cargo routing and empty container repositioning in multiple shipping service routes" "Transportation Research Part B" 2012
8.  Wang Meng "Robust schedule design for liner shipping services" OR "liner ship schedule design" port time uncertainty "Transportation Research Part B" 2012
9.  Wang Liu Meng "Segment-based alteration" liner shipping network design "Transportation Research Part B" 2015
10. Zhen Hu Wang Laporte Wu "Fleet deployment and demand fulfillment" liner shipping "Transportation Research Part B" 2019
11. "10.1287/trsc" liner shipping network design
12. "10.1016/j.trb" liner shipping fleet deployment
13. "10.1016/j.trb" container routing transit time liner
14. "10.1287/opre" container shipping network OR empty container repositioning
15. "10.1016/j.trc" liner shipping OR container shipping network design

Methodology / problem phrases with venue restrictors:
16. liner shipping network design "Transportation Science"
17. feeder network design hub-and-spoke container shipping "Transportation Research Part B"
18. vessel repositioning cargo flows "Transportation Science"
19. "liner shipping" "column generation" OR "branch-and-price" "Transportation Science"
20. "liner shipping" "Benders" OR "Lagrangian" "Transportation Research Part B"
21. transshipment hub port liner shipping network design "Transportation Research Part B"
22. "transit time" constraints liner shipping cargo routing "Transportation Science"
23. containership schedule design port time uncertainty stochastic "Transportation Research Part B"
24. liner ship fleet deployment stochastic demand "Transportation Research Part B"
25. empty container repositioning stochastic "Operations Research" INFORMS
26. speed optimization bunker liner shipping "Transportation Research Part B"
27. liner shipping service frequency weekly rotation number of vessels "Transportation Science"
28. LINER-LIB benchmark liner shipping network design results

Recent (2021-2026):
29. liner shipping network design 2023 "Transportation Science"
30. liner shipping network design 2024 "Transportation Research Part B"
31. container shipping network design 2025 "Transportation Research Part B" OR "Transportation Science"
32. liner shipping schedule recovery disruption 2023 "Transportation Research Part B"
33. feeder network design container 2024 "Transportation Research Part C" OR "Transportation Science"
34. liner shipping decarbonization network design 2025 2026 "Transportation Research Part B"

Classics (pre-2005):
35. Christiansen Fagerholt Ronen "Ship routing and scheduling: status and perspectives" "Transportation Science" 2004
36. Rana Vickson "Routing container ships using Lagrangean relaxation and decomposition" "Transportation Science" 1991
37. Cheung Chen "two-stage stochastic network model" "empty container allocation" "Transportation Science" 1998
38. Crainic Gendreau Dejax "allocation of empty containers" "Operations Research" 1993
39. Christiansen "Decomposition of a combined inventory and time constrained ship routing problem" "Transportation Science" 1999
40. "0191-2615" containership OR liner shipping fleet deployment

## Recording template for round 3 (what to capture per paper, per the facet brief)

For each corroborated paper record, in method_summary, how the paper models:
- Cyclic rotations: closed loop of port calls with weekly (or fixed-period) frequency; number of vessels = round-trip
  time / headway; whether rotations are given (cargo routing/fleet deployment) or designed (network design).
  -> analogue: launch cadence and reusable-vehicle turnaround (vehicles per route = cycle time / cadence).
- Vessel capacity: TEU capacity per vessel class, per-leg capacity = vessel capacity x frequency; whether
  capacity is a hard constraint, has demand rejection/penalty, or is uncertain.
  -> analogue: payload mass/volume per launch vehicle; per-window lift capacity; demand rejection.
- Transshipment at hubs: whether cargo paths may change rotation at a port (transshipment cost/time, hub
  capacity, path-based vs arc-based multicommodity flow, transshipment counted or limited).
  -> analogue: payload transfer at orbital depot/station; hub docking/handling capacity.
- Transit-time limits: origin-destination transit-time (level-of-service) constraints on cargo paths, sailing
  speed/time trade-offs, time-space or time-expanded network representation, schedule/berth time windows.
  -> analogue: orbital-phasing / rendezvous windows and maximum time-to-orbit for payloads or crew.
Also record the solution approach (IP, column generation, Benders, matheuristic, heuristic, stochastic/robust
programming) and what was shown (benchmarks such as LINER-LIB, case studies).

## Verification targets (from the facet brief) — UNVERIFIED, NOT recorded as candidates, NO DOIs given

These titles/venues/years come from the facet brief and the round-1 seed list, not from any search result.
They are search targets only and must be corroborated before being recorded:

Transportation Science targets
- Agarwal & Ergun (2008) — ship scheduling and network design for cargo routing in liner shipping
- Brouer, Alvarez, Plum, Pisinger & Sigurd (2014) — base IP model and benchmark suite (LINER-LIB)
- Meng, Wang, Andersson & Thun (2014) — containership routing and scheduling overview
- Tierney, Askelsdottir, Jensen & Pisinger (2015) — fleet repositioning with cargo flows
- Karsten, Ropke & Pisinger (2018) — sailing speed and container routing with transit time restrictions
- Koza, Desaulniers & Ropke (2020) — integrated network design and scheduling with transit-time windows
- Christiansen, Fagerholt & Ronen (2004) — ship routing and scheduling: status and perspectives
- Rana & Vickson (1991); Cheung & Chen (1998); Christiansen (1999) — classics

Transportation Research Part B targets
- Song & Dong (2012) — cargo routing and empty container repositioning in multiple service routes
- Wang & Meng (2012) — schedule design under port-time uncertainty
- Wang, Liu & Meng (2015) — segment-based alteration for liner shipping network design
- Zhen, Hu, Wang, Laporte & Wu (2019) — fleet deployment and demand fulfilment
- Meng & Wang (2011) — intermodal hub-and-spoke network design with multi-type containers (also hub-location facet)
- Ng (2015) — container vessel fleet deployment with stochastic dependencies in demand (venue to confirm)

Operations Research targets
- Crainic, Gendreau & Dejax (1993) — dynamic and stochastic allocation of empty containers
- Erera, Morales & Savelsbergh (2009) — robust optimization for empty repositioning (venue to confirm)

Adjacent-venue (secondary) targets, only if space-logistics relevance is argued: none specific to this facet;
feeder-network papers in EJOR / TR-E / Maritime Economics & Logistics (Santini-Plum-Ropke; Polat-Günther-Kulak;
Msakni et al.; Gelareh-Nickel-Pisinger; Imai-Shintani-Papadimitriou) are OUT of scope for the primary list.

## Corroborated in-scope candidates (0)

None. See Status above.

## Secondary / adjacent-venue candidates (0)

None.

## Gaps

- Entire facet unsearched for a second consecutive round: liner shipping network design (TS), cargo routing and
  fleet deployment (TR-B), empty container repositioning (OR/TS/TR-B), feeder network design and hub-port
  transshipment, schedule design under uncertainty, transit-time-constrained routing, 2021-2026 recent work and
  pre-2005 classics.
- No transfer statement in this facet is sourced; the recording template above is the facet brief's mapping,
  restated for the round-3 agent, not a finding.
