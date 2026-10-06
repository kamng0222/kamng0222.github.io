# Facet B2 fleet-sizing-empty-repositioning — round 2 notes

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet brief: fleet sizing, vehicle allocation and empty-asset repositioning on time-space networks with
stochastic demand and travel/turnaround times (the methodology for sizing a reusable launch-vehicle fleet
with refurbishment cycles). Record how cycle time (loaded leg + return + turnaround) drives fleet size and how
empty repositioning is handled.
In-scope venues: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).
Agent: literature-search subagent (round 2). Date: 2026-10-06.

## STATUS: NO SEARCH COULD BE EXECUTED IN ROUND 2 — FACET CORE STILL UNCORROBORATED (second consecutive round)

The first batch of six WebSearch queries (listed below) was refused in full with:
"Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn,
shared by every agent in it). Continue with the information already gathered instead of searching again ...
do not work around the limit by querying search engines with curl or wget from Bash, or by searching or
fetching through a third-party reader, proxy or archive service."

WebSearch is the only internet path in this environment (WebFetch, curl, wget, pip are egress-blocked) and the
budget notice forbids work-arounds, so none was attempted. Round 1 of this facet
(B2-fleet-sizing-capacity-expansion-r1.md) failed identically (0 of 8 queries executed).

Consequence: after two rounds, NONE of the facet's named anchors has been seen in any search result in this
workflow run: Turnquist & Jordan 1986; Beaujon & Turnquist 1991; Jordan & Turnquist 1983; Dejax & Crainic
1987; Cheung & Chen 1998; Powell & Carvalho 1998; Godfrey & Powell 2002 (I, II); Nair & Miller-Hooks 2011;
Crainic, Gendreau & Dejax 1993; Erera, Morales & Savelsbergh 2009; Song & Dong 2012; Fagnant & Kockelman 2014;
AMoD fleet-sizing papers in TR-B/TR-C. Per the task rules (never record a paper from memory alone; never invent
a DOI; a wrong venue or invented paper is worse than a missing one) they are NOT recorded.

What IS recorded: eight pass-through items whose title and venue were corroborated by search results logged by
sibling facet agents earlier in this run and that fall inside this facet's methodological core (fleet / asset
balance on cyclic time-space networks, fleet acquisition under uncertainty, vehicle circulation that fixes fleet
size from cycle time, cyclic shuttle operations, charging/turnaround-constrained electric-aircraft networks).
Each carries its provenance; confidence is capped at "medium" and set to "low" where the sibling flagged that
venue or authors were not visible in the snippet. The merge step should de-duplicate them against the B1/B2
sibling notes (several were also passed through by round 1 of this facet).

This is a tooling-coverage gap, not evidence that the literature is thin. Remedy: run this facet in a fresh
turn (r3) with a reset or un-shared WebSearch budget, or raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION; the
facet has now failed twice and should get first call on the next budget. The r3 query plan below is ready to
run verbatim.

Local fallbacks checked (no internet needed):
- Repository /home/user/kamng0222.github.io: no bibliography.
- All 25 sibling notes files and all verified/*.ndjson records were grepped for fleet sizing, repositioning,
  empty containers/flows, vehicle sharing, AMoD, charging/turnaround and the facet's author surnames.
  Hits that are inside this facet are the eight items below; everything else was either out of facet
  (berth allocation, hub location, ATFM) or explicitly marked UNVERIFIED / memory-only by the sibling.
- The verifier records themselves state "NOT WEB-VERIFIED" for the same budget reason, so they add no
  independent corroboration beyond the original search-result URL.

## Queries issued this round (6) — ALL REFUSED, NOT EXECUTED

1. Turnquist Jordan "Fleet sizing under production cycles and uncertain travel times" Transportation Science (standard) — REFUSED
2. Beaujon Turnquist "A model for fleet sizing and vehicle allocation" Transportation Science 1991 (standard) — REFUSED
3. Jordan Turnquist "A stochastic, dynamic network model for railroad car distribution" Transportation Science 1983 (standard) — REFUSED
4. Dejax Crainic "A review of empty flows and fleet management models in freight transportation" Transportation Science 1987 (standard) — REFUSED
5. Cheung Chen "two-stage stochastic network model" "dynamic empty container allocation problem" Transportation Science 1998 (standard) — REFUSED
6. Powell Carvalho "Dynamic control of logistics queueing networks for large-scale fleet management" Transportation Science (standard) — REFUSED

## Round-3 query plan (NOT run; 40 queries, ordered by priority; at least 6 recency and 4 pre-2005)

Classics / named authors (pre-2005)
7.  Godfrey Powell "An Adaptive Dynamic Programming Algorithm for Dynamic Fleet Management" Transportation Science 2002 Part I ; Part II multiperiod travel times
8.  Powell 1986 "A Stochastic Model of the Dynamic Vehicle Allocation Problem" Transportation Science
9.  Powell 1987 "An Operational Planning Model for the Dynamic Vehicle Allocation Problem with Uncertain Demands" Transportation Research Part B
10. Frantzeskakis Powell 1990 "A Successive Linear Approximation Procedure for Stochastic, Dynamic Vehicle Allocation Problems" Transportation Science
11. Cheung Powell 1996 "An Algorithm for Multistage Dynamic Networks with Random Arc Capacities" Operations Research
12. Crainic Gendreau Dejax 1993 "Dynamic and Stochastic Models for the Allocation of Empty Containers" Operations Research
13. Holmberg Joborn Lundgren 1998 "Improved Empty Freight Car Distribution" Transportation Science ; Joborn Crainic Gendreau Holmberg Lundgren 2004 "Economies of Scale in Empty Freight Car Distribution in Scheduled Railways" Transportation Science
14. Powell Shapiro Simao 2002 "An Adaptive Dynamic Programming Algorithm for the Heterogeneous Resource Allocation Problem" Transportation Science
15. Spivey Powell 2004 "The Dynamic Assignment Problem" Transportation Science
16. Ceder Stern 1981 "Deficit Function Bus Scheduling with Deadheading Trip Insertions for Fleet Size Reduction" Transportation Science
17. Wu Hartman Wilson 2005 "An Integrated Model and Solution Approach for Fleet Sizing with Heterogeneous Assets" Transportation Science
18. Topaloglu Powell 2007 "Sensitivity Analysis of a Dynamic Fleet Management Model Using Approximate Dynamic Programming" Operations Research
19. Simao Day George Gifford Nienow Powell 2009 "An Approximate Dynamic Programming Algorithm for Large-Scale Fleet Management: A Case Application" Transportation Science
20. Erera Morales Savelsbergh 2009 "Robust Optimization for Empty Repositioning Problems" Operations Research
21. Nair Miller-Hooks 2011 "Fleet Management for Vehicle Sharing Operations" Transportation Science
22. Song Dong 2012 "Cargo routing and empty container repositioning in multiple shipping service routes" "Transportation Research Part B"
23. Bouzaiene-Ayari Cheng Das Fiorillo Powell 2016 "From Single Commodity to Multiattribute Models for Locomotive Optimization" Transportation Science
24. Tierney Askelsdottir Jensen Pisinger 2015 "Solving the Liner Shipping Fleet Repositioning Problem with Cargo Flows" Transportation Science

Methodology / problem phrases with venue restrictors and DOI prefixes
25. "fleet sizing" "time-space network" stochastic "Transportation Science"
26. "empty repositioning" OR "empty vehicle" two-stage stochastic "Transportation Science" OR "Operations Research"
27. "approximate dynamic programming" fleet management 10.1287/trsc
28. "fleet size" vehicle sharing OR carsharing relocation "Transportation Research Part B" (Boyaci Zografos Geroliminis 2017; Hu Liu 2016; Nourinejad Roorda)
29. "10.1016/j.trc" fleet sizing shared autonomous vehicles charging (Fagnant Kockelman 2014; Chen Kockelman Hanna 2016 is TR-A — out; Loeb Kockelman TR-C 2018/2019)
30. "autonomous mobility-on-demand" fleet sizing rebalancing "Transportation Research Part B" OR "Transportation Research Part C" (Zhang Pavone; Spieser et al.; Vosooghi et al.)
31. "10.1016/j.trb" fleet size cycle time turnaround vehicle scheduling
32. "10.1287/opre" fleet sizing stochastic demand vehicle allocation
33. design-balanced OR "asset-balance" service network design "Transportation Science" (Pedersen Crainic Madsen 2009; Chouman Crainic 2015)
34. "rotation" OR "vehicle circulation" fleet minimum periodic "Transportation Science" OR "Transportation Research Part B"

Recency (2021-2026)
35. "fleet sizing" OR "fleet size" electric vehicles charging "Transportation Research Part C" 2023 2024 2025
36. eVTOL OR "air taxi" fleet sizing turnaround charging "Transportation Research Part C" 2024 2025 2026
37. "approximate dynamic programming" OR "reinforcement learning" fleet repositioning rebalancing "Transportation Science" 2022 2023 2024
38. "empty container repositioning" OR "empty repositioning" "Transportation Research Part B" 2021 2022 2023
39. "10.1287/trsc" fleet management stochastic 2024 2025 2026
40. drone fleet sizing battery turnaround "Operations Research" OR "Transportation Science" 2022 2023 2024

Secondary / adjacent (space logistics; at most 8)
41. Ho de Weck Hoffman Shishko 2014 "Dynamic modeling and optimization for space logistics using time-expanded networks" Acta Astronautica
42. Chen Ho 2018 "Integrated Space Logistics Mission Planning and Spacecraft Design with Mixed-Integer Nonlinear Programming" Journal of Spacecraft and Rockets
43. Jagannatha Bui Ho 2019 "Generalized multicommodity network flow model for the Earth-Moon-Mars logistics system" Journal of Spacecraft and Rockets
44. reusable launch vehicle fleet size turnaround "launch cadence" optimization Acta Astronautica OR "Journal of Spacecraft and Rockets" 2022 2023 2024
45. Isaji Takubo Ho "multi-fidelity" OR "robust" space logistics network Journal of Spacecraft and Rockets 2022 2023
46. spaceport location OR "launch site selection" network optimization Acta Astronautica

## Candidates recorded (pass-through from sibling agents' corroborated search results; de-duplicate at merge)

| # | Paper | Venue / year | DOI | Where the sibling saw it | Sibling file | Confidence |
|---|-------|--------------|-----|--------------------------|--------------|------------|
| 1 | Andersen, Christiansen, Crainic, Grønhaug — Branch and Price for Service Network Design with Asset Management Constraints | Transportation Science 45(1):33-49, 2011 | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v45y2011i1p33-49.html (RePEc inm/ortrsc record; snippet mentions branch-and-price) | B1-service-network-design-r1.md | medium |
| 2 | Andersen, Crainic, Christiansen — Service network design with asset management: Formulations and comparative analyses | Transportation Research Part C 17(2), 2009 (journal venue NOT in snippet; seen as CIRRELT-2007-55 working paper) | (not seen) | https://www.cirrelt.ca/DocumentsTravail/CIRRELT-2007-55.pdf | B1-service-network-design-r1.md | low |
| 3 | Crainic, Hewitt, Toulouse, Vu — Service network design with resource constraints | Transportation Science 50(4), 2016 | (not seen) | https://scholars.luc.edu/en/publications/service-network-design-with-resource-constraints/ (Loyola research portal; co-authors beyond Crainic/Hewitt from sibling knowledge) | B1-service-network-design-r1.md | medium |
| 4 | Hewitt, Crainic, Nowak, Rei — Scheduled service network design with resource acquisition and management under uncertainty | Transportation Research Part B 128:324-343, 2019 | 10.1016/j.trb.2019.08.008 | https://ideas.repec.org/a/eee/transb/v128y2019icp324-343.html ; https://scholars.luc.edu/en/publications/scheduled-service-network-design-with-resource-acquisition-and-ma/ | B2-network-design-uncertainty-r1.md | medium |
| 5 | Zhu, Crainic, Gendreau — Scheduled Service Network Design for Freight Rail Transportation | Operations Research 62(2):383-400, 2014 | 10.1287/opre.2013.1254 | https://pubsonline.informs.org/doi/suppl/10.1287/opre.2013.1254 (publisher supplement page) | B2-time-windows-periodic-launch-r1.md | medium (sibling: high; downgraded as pass-through) |
| 6 | van Lieshout — Integrated Periodic Timetabling and Vehicle Circulation Scheduling | Transportation Science 55(3):768-790, 2021 | 10.1287/trsc.2020.1024 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2020.1024 (publisher page) | B2-time-windows-periodic-launch-r1.md | medium (sibling: high; downgraded as pass-through) |
| 7 | (authors not captured in snippet) — Operations design for high-velocity intra-city package service | Transportation Research Part B 161:150-168, 2022 | (not seen) | https://ideas.repec.org/a/eee/transb/v161y2022icp150-168.html (snippet: shuttle activities, rate-based repeatable cyclic routes with capacity/timing requirements) | B1-service-network-design-r1.md | low |
| 8 | Kinene, Birolini (full author list unconfirmed) — Optimization of subsidized air transport networks using electric aircraft | Transportation Research Part B, 2024 (venue from repository metadata) | (not seen) | https://aisberg.unibg.it/handle/10446/283949 (University of Bergamo repository) | A1-deterministic-atfm-r1.md ; A2-ram-demand-network-planning-r1.md | low |

### Why these belong to this facet and what they say about cycle time, fleet size and repositioning
- 1, 2 (asset-management / design-balanced SND): vehicles are modelled as flows on a cyclic time-space network
  with node-time balance constraints, so every vehicle follows a closed rotation; with cycle (rotation)
  variables, the count of selected cycles IS the fleet size and the rotation length (loaded legs + empty
  repositioning legs + dwell) is the cycle time. Empty repositioning appears as design arcs carrying no
  commodity but needed to close the rotation. Branch-and-price over cycles (1) and the arc/path/cycle
  formulation comparison (2) are the standard toolkit for sizing a small reusable fleet that must return to base.
  Transfer: a launch vehicle's ascent, orbital leg, return and pad refurbishment form one cycle; pricing rotations
  gives both fleet size and the schedule of empty (down-mass-less) return legs.
- 3 (resource-constrained SND): each vehicle anchored to a home terminal, bounded fleet per terminal, rotation
  must complete within the schedule period; column-generation / slope-scaling matheuristic. Transfer: bounded
  vehicles per spaceport with mandatory return to the home pad for refurbishment.
- 4 (resource acquisition under uncertainty): fleet acquisition is a first-stage decision in a two-stage
  stochastic scheduled SND with outsourcing recourse for unserved stochastic demand — the direct analogue of
  deciding how many launchers to procure before payload demand is known, with expendable/third-party launches
  as the recourse.
- 5 (scheduled SND for rail): multi-layer cyclic time-space network (services / blocks / cars) couples vehicle
  cycles with consolidated-load routing; large-scale matheuristic. Transfer: launchers carrying consolidated
  payload "blocks" to orbital hubs on a repeating cadence.
- 6 (periodic timetable + vehicle circulation): integrates PESP-type periodic timetabling with the vehicle
  circulation that operates it, so the number of vehicles required by the periodic schedule is optimised jointly
  with event times. Transfer: for a fixed launch cadence T, fleet = number of vehicles whose rotation
  (ascent + on-orbit + return + refurbishment) fits in the periodic circulation — the clearest cycle-time-to-fleet
  coupling corroborated in this run.
- 7 (high-velocity package shuttles): rate-based, repeatable cyclic vehicle routes with capacity and timing
  requirements — a template for fixed-cadence feeder shuttles whose fleet follows from route cycle time.
- 8 (electric-aircraft subsidised networks): range and charging/turnaround constraints shape which legs can be
  flown and how aircraft rotate in a subsidised regional network — the closest corroborated TR-B item to
  "fleet sizing with charging turnaround" (relevance both A and B).

## UNVERIFIED leads (memory-only; NOT recorded; seed list for round 3)
Turnquist & Jordan 1986 TS 20(4); Beaujon & Turnquist 1991 TS 25(1); Jordan & Turnquist 1983 TS 17(2);
Dejax & Crainic 1987 TS 21(4); Cheung & Chen 1998 TS 32(2); Powell & Carvalho 1998 TS 32(2); Godfrey & Powell
2002 TS 36(1) parts I-II; Nair & Miller-Hooks 2011 TS 45(4); Crainic, Gendreau & Dejax 1993 OR 41(1); Erera,
Morales & Savelsbergh 2009 OR 57(2); Song & Dong 2012 TR-B 46(10); Fagnant & Kockelman 2014 TR-C 40;
Powell 1986 TS / 1987 TR-B; Frantzeskakis & Powell 1990 TS; Cheung & Powell 1996 OR; Holmberg et al. 1998 TS;
Joborn et al. 2004 TS; Powell, Shapiro & Simao 2002 TS; Spivey & Powell 2004 TS; Topaloglu & Powell 2007 OR;
Simao et al. 2009 TS; Bouzaiene-Ayari et al. 2016 TS; Wu, Hartman & Wilson 2005 TS; Ceder & Stern 1981 TS;
Boyaci, Zografos & Geroliminis 2017 TR-B; Hu & Liu 2016 TR-B; Tierney et al. 2015 TS; Pedersen, Crainic &
Madsen 2009 TS; Chouman & Crainic 2015 TS. Out-of-venue items to NOT record even if found: Chen, Kockelman &
Hanna 2016 (TR-A); Meng & Wang empty-container SND (TR-E); Shintani et al. 2007 (TR-E); Topaloglu & Powell 2006
(IJOC); Ahmed, King & Parija 2003 (J. Global Optim.).
Secondary (adjacent): Ho, de Weck, Hoffman & Shishko 2014 Acta Astronautica; Chen & Ho 2018 JSR; Jagannatha,
Bui & Ho 2019 JSR; Chen, Gardner, Grogan & Ho 2021 JSR.

## Gaps
- Entire facet core (classic TS fleet sizing and vehicle allocation; ADP fleet management; empty container
  allocation OR/TS/TR-B; robust empty repositioning; vehicle-sharing fleet management; AMoD / SAV / eVTOL fleet
  sizing with charging turnaround in TR-B/TR-C; space-logistics secondary venues) remains uncorroborated after
  two rounds: 0 of the planned 25-40 searches ran in either round.
- No DOI captured for any item except Hewitt et al. 2019, Zhu et al. 2014 and van Lieshout 2021 (all via siblings).
- No pre-2005 classic corroborated for this facet; the only 2021-2026 items (6, 7, 8) are pass-throughs, two of
  them with uncaptured author lists or repository-only venue evidence.
