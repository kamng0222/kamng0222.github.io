# Facet A2 dynamic-flows-theory: Dynamic network flows / flows-over-time with transportation applications (round 1 notes)

Date: 2026-10-06. Agent: facet dynamic-flows-theory. Venues in scope: Operations Research (10.1287/opre),
Transportation Science (10.1287/trsc), TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## IMPORTANT LIMITATION: no search was executed in this round

The shared per-turn WebSearch budget (200 calls across every agent in the workflow) was already exhausted when
this agent started. All five queries submitted were refused with "web search budget is used up"; no further
queries were attempted (the harness forbids working around the limit with curl/wget/proxies, and every direct
HTTP route is egress-blocked anyway). Consequently:

- NOTHING below was recorded from memory alone. The only candidates returned are papers that sibling facet
  agents in this same run corroborated with a URL from an executed search and that fall squarely inside this
  facet's methodology (dynamic/time-expanded multicommodity flow, time-indexed 0-1 IP, dynamic discretization
  discovery, dynamic/quasi-dynamic traffic assignment for air traffic, time-expanded space logistics).
- Those candidates are duplicates of entries in the sibling files named in the provenance column; the merge step
  dedups by DOI/title, so the value added here is the dynamic-flows methodological reading in the summaries.
- Confidence was deliberately downgraded one notch relative to the sibling's (publisher page seen by sibling ->
  "medium"; sibling medium or venue not visible -> "low") because this agent did not see the pages itself.
- The core of this facet (flows-over-time theory, Eulerian/aggregate ATFM models, dynamic network loading and
  DTA in TR-B, flow corridors, capacity-constrained flow scheduling over time) has ZERO coverage so far.
  A round 2 with a fresh budget is required; the full query plan is at the bottom.

## Queries submitted in this round (all REFUSED, budget exhausted, nothing returned)

1. "dynamic discretization discovery" continuous-time service network design "Transportation Science" Boland Hewitt Marshall Savelsbergh  (standard)
2. "flows over time" earliest arrival quickest flow "Operations Research" INFORMS 10.1287/opre  (standard)
3. Menon Sweriduk Bilimoria Eulerian model air traffic flow "Transportation Research Part C" OR "Journal of Guidance"  (standard)
4. Sun Bayen "Transportation Research Part C" air traffic flow Eulerian large-capacity cell transmission model  (standard)
5. "dynamic network loading" "Transportation Research Part B" time-expanded formulation  (standard)

## Candidates returned (corroborated by sibling-facet search results in this run; re-verify downstream)

| # | Title | Authors | Year | Venue | DOI | URL where the sibling saw it | Provenance (sibling file) | Conf. here |
|---|-------|---------|------|-------|-----|------------------------------|---------------------------|------------|
| 1 | The Traffic Flow Management Rerouting Problem in Air Traffic Control: A Dynamic Network Flow Approach | Bertsimas, Stock Patterson | 2000 | Transportation Science 34(3) 239-255 | 10.1287/trsc.34.3.239.12300 | https://pubsonline.informs.org/doi/references/10.1287/trsc.34.3.239.12300 | A1-deterministic-atfm-r1.md #4 (publisher page) | medium |
| 2 | The Air Traffic Flow Management Problem with Enroute Capacities | Bertsimas, Stock Patterson | 1998 | Operations Research 46(3) 406-422 | 10.1287/opre.46.3.406 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.46.3.406 | A1-deterministic-atfm-r1.md #3 (publisher page) | medium |
| 3 | An Integer Optimization Approach to Large-Scale Air Traffic Flow Management | Bertsimas, Lulli, Odoni | 2011 | Operations Research 59(1) 211-227 | 10.1287/opre.1100.0899 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.1100.0899 | A1-deterministic-atfm-r1.md #5 (publisher page) | medium |
| 4 | A dynamic rerouting model for air traffic flow management | Mukherjee, Hansen | 2009 | Transportation Research Part B 43(1) 159-171 | 10.1016/j.trb.2008.05.011 | https://its.berkeley.edu/publications/dynamic-rerouting-model-air-traffic-flow-management | A1-deterministic-atfm-r1.md #15 (ITS Berkeley page, DOI recorded) | medium |
| 5 | The Continuous-Time Service Network Design Problem | Boland, Hewitt, Marshall, Savelsbergh | 2017 | Operations Research 65(5) 1303-1321 | (not seen) | https://scholars.luc.edu/en/publications/the-continuous-time-service-network-design-problem/ | B2-time-windows-periodic-launch-r1.md #18 (Loyola index, medium); B1-service-network-design-r1.md #5 (indirect, low) | medium |
| 6 | Interval-Based Dynamic Discretization Discovery for Solving the Continuous-Time Service Network Design Problem | Marshall, Boland, Savelsbergh, Hewitt | 2021 | Transportation Science 55(1) 29-51 | (not seen) | https://par.nsf.gov/biblio/10226533 | B1-service-network-design-r1.md #3 (NSF PAR, medium) | medium |
| 7 | Dynamic Discretization Discovery for Solving the Time-Dependent Traveling Salesman Problem with Time Windows | Vu, Hewitt, Boland, Savelsbergh | 2020 | Transportation Science | (not seen) | https://scholars.luc.edu/en/publications/dynamic-discretization-discovery-for-solving-the-time-dependent-t/ | B1-service-network-design-r1.md #4 (venue/year NOT visible in snippet) | low |
| 8 | Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility operations | Wang, Delahaye, Farges, Alam | 2022 | Transportation Research Part C (believed; NOT shown) | (not seen) | https://hal-enac.archives-ouvertes.fr/hal-03701655 | A2-uam-aam-ram-r1.md C5 (venue low) | low |
| 9 | A quasi-dynamic air traffic assignment model for mitigating air traffic complexity and congestion for high-density UAM operations | Wang, Delahaye, Farges, Alam | 2023 | Transportation Research Part C (believed; NOT shown) | (not seen) | (search summary only; see A2-uam-aam-ram-r1.md query 9) | A2-uam-aam-ram-r1.md C6 (venue low) | low |
| S1 | Dynamic modeling and optimization for space logistics using time-expanded networks | Ho, de Weck, Hoffman, Shishko | 2014 | Acta Astronautica (adjacent-venue) | (not seen) | https://experts.illinois.edu/en/publications/dynamic-modeling-and-optimization-for-space-logistics-using-time-/ | B2-time-windows-periodic-launch-r1.md A1 | medium |
| S2 | Event-Driven Network Model for Space Mission Optimization with High-Thrust and Low-Thrust Spacecraft | Jagannatha, Ho | 2020 | Journal of Spacecraft and Rockets 57(3) 446-463 (adjacent-venue) | (not seen) | https://arxiv.org/abs/1904.09364 | B2-time-windows-periodic-launch-r1.md A3 | medium |

Why these belong to the dynamic-flows facet (methodological reading):
- #1 is the canonical "ATFM as a dynamic multicommodity integer network flow on a time-expanded airspace network"
  paper, solved by Lagrangian relaxation with aggregate flows disaggregated into flight schedules; #2 is the
  canonical time-indexed cumulative ("by-time") 0-1 IP whose strong LP relaxation is the reason time-expanded
  ATFM models scale; #3 is its large-scale extension with rerouting and speed control (still time-indexed).
- #4 puts time-indexed rerouting decisions on a scenario tree (dynamic decisions revised as capacity scenarios
  unfold) - the stochastic flows-over-time variant.
- #5-#7 are the dynamic discretization discovery (DDD) lineage: partially time-expanded networks whose time
  points are discovered iteratively, giving exact continuous-time optima without a full time grid.
- #8-#9 are macroscopic / quasi-dynamic traffic assignment for UAM flows: the aggregate (DTA-style) side of the
  facet applied to small-aircraft air mobility.
- S1-S2 are time-expanded generalized multicommodity flow for space logistics (S1 uniform grid, S2 event-driven
  non-uniform discretization): the spaceport-to-orbit analogue of the discretization question in this facet.

## Round-2 search plan (35 queries, NONE executed yet). Mode: standard first, extended for pre-2005 and niche items.

(a) Methodology phrases
1. "dynamic network flow" "time-expanded" multicommodity "Transportation Science"
2. "flows over time" OR "dynamic flows" quickest flow earliest arrival "Operations Research" INFORMS
3. "time-expanded network" integer programming scheduling capacity "Operations Research" 10.1287/opre
4. "partially time-expanded network" OR "dynamic discretization discovery" Transportation Science 2022 2023 2024
5. "dynamic discretization discovery" "Transportation Research Part B" 2020 2023
6. "continuous-time" versus "discrete-time" network flow formulation "Transportation Research Part B"
7. "dynamic network loading" "Transportation Research Part B" formulation properties
8. "cell transmission model" Daganzo "Transportation Research Part B" 1994 1995
9. "system optimum dynamic traffic assignment" linear programming cell transmission "Transportation Science" Ziliaskopoulos
10. "dynamic traffic assignment" "Operations Research" Friesz variational inequality continuous time 1989 1993
11. Merchant Nemhauser "dynamic traffic assignment" "Transportation Science" 1978
12. Carey "optimal time-varying flows on congested networks" "Operations Research" 1987
13. Ford Fulkerson "constructing maximal dynamic flows from static flows" "Operations Research" 1958
14. "Lagrangian relaxation" time-expanded "train timetabling" "Operations Research" OR "Transportation Science" (capacity-constrained flow scheduling over time analogue)
(b) Problem phrases
15. "air traffic flow" Eulerian OR aggregate OR "cell-based" model "Transportation Research Part C"
16. "air traffic flow management" "dynamic network flow" OR "time-space network" "Transportation Science"
17. "flow corridor" OR "flow corridors" air traffic "Transportation Research Part C" Yousefi
18. "Lagrangian-Eulerian" OR "Eulerian-Lagrangian" air traffic model "Transportation Research Part C"
19. "link transmission model" air traffic flow management journal
20. "dynamic traffic assignment" air traffic OR airspace "Transportation Research Part C" 2023 2024 2025
21. "regional air mobility" OR "advanced air mobility" flow "time-expanded" OR "time-space network" "Transportation Research Part C" 2024 2025 2026
(c) Author sweeps
22. Menon Sweriduk Bilimoria "Eulerian" air traffic flow model journal (check whether any venue is TR-C; expect JGCD = out of scope)
23. Sun Bayen "large-capacity cell transmission model" air traffic (check venue; expect JGCD/NHM = out of scope)
24. Sridhar Soni Sheth Chatterji "aggregate flow model" air traffic management (check venue)
25. Work Bayen "convex formulations of air traffic flow optimization" (check venue; expect Proc. IEEE = out)
26. Boland Hewitt Savelsbergh Lagos "continuous-time inventory routing" "Transportation Science" 2020
27. Hewitt "enhanced dynamic discretization discovery" load plan "Transportation Science" 2019
28. Scherr Hewitt Neumann Saavedra Mattfeld "mixed autonomous fleets" "Transportation Research Part B" 2020
29. Hewitt Lehuede "new formulations for the scheduled service network design problem" "Transportation Research Part B" 2023
(d) Venue restrictors with 2021-2026 targets
30. "Transportation Science" "time-expanded" OR "time-indexed" 2024 2025 flow scheduling capacity
31. "Operations Research" INFORMS "flows over time" OR "dynamic flow" 2021 2022 2023 2024
32. "Transportation Research Part B" "dynamic network loading" OR "dynamic user equilibrium" 2022 2023 2024 2025
(e) DOI-prefix strings
33. "10.1287/trsc" "time-expanded network" multicommodity
34. "10.1016/j.trb" "dynamic network loading" OR "cell transmission"
35. "10.1016/j.trc" "air traffic flow" aggregate OR Eulerian OR "traffic assignment"

## Leads for round 2 (FROM MEMORY ONLY, NOT corroborated here, NO DOIs; do NOT cite until a search confirms title+venue)

Likely in-scope venue (verify): Ford & Fulkerson 1958 maximal dynamic flows (OR); Merchant & Nemhauser 1978 two DTA
papers (TS); Carey 1987 optimal time-varying flows (OR); Carey 1992 nonconvexity of DTA (TR-B); Friesz, Luque, Tobin,
Wie 1989 DTA as continuous-time optimal control (OR); Friesz, Bernstein, Smith, Tobin, Wie 1993 VI formulation of
dynamic user equilibrium (OR); Ran, Boyce, LeBlanc 1993 instantaneous dynamic user-optimal DTA (OR); Daganzo 1994/1995
cell transmission model (TR-B); Ziliaskopoulos 2000 single-destination SO-DTA LP (TS); Lo & Szeto 2002 cell-based VI
DUO (TR-B); Carey & Subrahmanian 2000 time-varying flows on congested networks (TR-B); Carey & McCartney 2002 whole-link
travel time model (TR-B); Nie 2011 cell-based Merchant-Nemhauser SO-DTA (TR-B); Long, Gao, Szeto 2011 discretised link
travel time models (TR-B); Han, Friesz, Yao 2013 simultaneous route and departure DUE (TR-B); Brannlund, Lindberg, Nou,
Nilsson 1998 railway timetabling by Lagrangian relaxation on a time-discretised network (TS); Caprara, Fischetti, Toth
2002 train timetabling on a time-expanded graph (OR); Cacchiani, Caprara, Toth 2010 extra freight trains (TR-B);
Harrod 2011 hypergraph network transition constraints (TS); Hewitt 2019 enhanced DDD load plan (TS); Lagos, Boland,
Savelsbergh 2020 continuous-time inventory routing (TS); Scherr et al. 2020 DDD mixed autonomous fleets (TR-B);
Hewitt & Lehuede 2023 scheduled SND formulations (TR-B); Yousefi & Zadeh 2013 dynamic allocation of flow corridors
(TR-C?).
Likely OUT of scope venue (list only so the writer knows the lineage exists): Menon, Sweriduk, Bilimoria 2004 and
Menon et al. 2006 Eulerian ATFM models (J. Guidance, Control, and Dynamics); Sun & Bayen 2008 multicommodity
Eulerian-Lagrangian large-capacity CTM (JGCD); Sun, Strub, Bayen 2007 comparison of four Eulerian models (Networks
and Heterogeneous Media); Bayen, Raffard, Tomlin 2006 adjoint control of Eulerian model (IEEE TCST); Work & Bayen
2008 convex formulations (Proc. IEEE); Sridhar, Soni, Sheth, Chatterji 2006 aggregate flow model (JGCD); Cao & Sun
2011 link transmission model for ATFM (JGCD); Hoppe & Tardos 2000 quickest transshipment (Math OR); Fleischer &
Skutella 2007 quickest flows over time (SIAM J Comput); Baumann & Skutella 2009 earliest arrival flows (Math OR);
Aronson 1989 dynamic network flow survey (Annals OR); Boland, Hewitt, Marshall, Savelsbergh 2019 price of
discretizing time (EURO J Transp Logist); He, Boland, Nemhauser, Savelsbergh 2022 DDD for time-dependent shortest
paths (IJOC); Boland & Savelsbergh 2019 perspectives on IP for time-dependent models (TOP).

## Gaps (all facet sub-areas; nothing could be searched)
- Flows-over-time theory in OR/TS: none corroborated.
- Eulerian/aggregate ATFM models: none corroborated; venue for the whole lineage must be checked (most are JGCD/IEEE).
- Dynamic network loading / DTA in TR-B sharing time-expanded machinery: none corroborated.
- Flow-corridor models in TR-C: none corroborated.
- 2021-2026 dynamic-flow papers in the four venues: none corroborated beyond the DDD items carried from facet B1.
- Pre-2005 classics: only Bertsimas & Stock Patterson 1998/2000 carried from facet A1.
