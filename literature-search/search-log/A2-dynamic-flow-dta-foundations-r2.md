# Facet A2 dynamic-flow-dta-foundations (round 2): dynamic network flows and system-optimum DTA foundations of time-expanded ATFM / UAM traffic assignment

Date: 2026-10-06. Agent: facet dynamic-flow-dta-foundations, round 2.
In-scope venues: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc), TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## STATUS: NO SEARCH COULD BE EXECUTED IN THIS ROUND EITHER

All six WebSearch queries submitted by this agent were refused with "this turn's web search budget is used up
(limit: 200 WebSearch calls per turn, shared by every agent in it)". The same happened to round 1 of this facet
(A2-dynamic-flows-theory-r1.md). WebFetch/curl/wget are egress-blocked and the harness forbids working around the
limit, so zero fresh results exist for this facet after two rounds.

Consequences for the record below:
- NOTHING is recorded from memory alone. Every candidate is a pass-through of a paper that a SIBLING facet agent in
  this run corroborated with an executed search (URL logged in its notes file) and that falls inside this facet's
  methodology (time-expanded / time-indexed flow IPs for ATFM, dynamic discretization discovery, quasi-dynamic
  traffic assignment for UAM, time-expanded space logistics).
- Confidence is downgraded one notch relative to the sibling (publisher page seen by sibling -> medium here;
  sibling medium or venue not shown -> low here) because this agent did not see any page.
- DOIs are carried ONLY where the sibling saw the DOI string in a result URL or snippet. In particular the DOI that a
  verifier attached to Boland et al. 2017 (10.1287/opre.2017.1624) was explicitly "filled from recollection", so it
  is NOT carried here (doi = "").
- The core of the facet - Ford & Fulkerson 1958 (OR), Merchant & Nemhauser 1978 (TS, two papers), Carey 1986 (TS)
  and 1987 (OR), Friesz-Bernstein-Smith-Tobin-Wie 1993 (OR), Daganzo 1994/1995 CTM (TR-B), Ziliaskopoulos 2000 (TS),
  Lo & Szeto 2002 (TR-B), Hewitt 2019 (TS) and the Boland-Hewitt-Marshall-Savelsbergh discretization-error line -
  was corroborated by NO executed search anywhere in this run (confirmed by grepping all 29 sibling notes files and
  all verified/*.ndjson records for Fulkerson, Merchant, Carey, Friesz, Daganzo, "cell transmission", Ziliaskopoulos,
  Szeto, "dynamic traffic assignment", "dynamic network loading", "flows over time"). Zero hits other than planned
  query lines. These items therefore appear ONLY in the "leads" section, without DOIs, and must not be cited until a
  search confirms title and venue.

## Queries submitted this round (all REFUSED, budget exhausted, nothing returned)

1. Ford Fulkerson "Constructing maximal dynamic flows from static flows" Operations Research 1958  (standard)
2. Merchant Nemhauser "A model and an algorithm for the dynamic traffic assignment problems" Transportation Science 1978  (standard)
3. Carey "Optimal time-varying flows on congested networks" Operations Research 1987  (standard)
4. Carey "A constraint qualification for a dynamic traffic assignment model" Transportation Science 1986  (standard)
5. Friesz Bernstein Smith Tobin Wie "A variational inequality formulation of the dynamic network user equilibrium problem" Operations Research 1993  (standard)
6. Ziliaskopoulos "A linear programming model for the single destination system optimum dynamic traffic assignment problem" Transportation Science 2000  (standard)

No further queries were attempted after the refusal (the tool asks not to retry or work around the limit).

## Local evidence consulted instead (no internet)

- research_notes/.../A2-dynamic-flows-theory-r1.md (round 1 of this facet; also zero searches).
- research_notes/.../A1-deterministic-atfm-r1.md (51 executed searches; publisher pages for the Bertsimas papers).
- research_notes/.../A2-uam-aam-ram-r1.md (12 executed searches; Wang-Delahaye UAM assignment papers).
- research_notes/.../B1-service-network-design-r1.md and B2-time-windows-periodic-launch-r1.md (DDD lineage, space logistics).
- research_notes/.../A2-on-demand-aviation-and-electric-fleet-ops-r2.md (Kinene-Birolini pass-through provenance).
- verified/*.ndjson (verifier records and their correction notes on which DOIs were seen vs recalled).

## Candidates (pass-through; corroborated by sibling-executed searches; re-verify on publisher pages before citing)

| # | Title | Authors | Year | Venue | DOI (seen by sibling) | URL where the sibling saw it | Provenance | Conf. here |
|---|-------|---------|------|-------|-----------------------|------------------------------|------------|------------|
| 1 | The Air Traffic Flow Management Problem with Enroute Capacities | Bertsimas, Stock Patterson | 1998 | Operations Research 46(3) 406-422 | 10.1287/opre.46.3.406 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.46.3.406 | A1-deterministic-atfm-r1 #3 (publisher page) | medium |
| 2 | The Traffic Flow Management Rerouting Problem in Air Traffic Control: A Dynamic Network Flow Approach | Bertsimas, Stock Patterson | 2000 | Transportation Science 34(3) 239-255 | 10.1287/trsc.34.3.239.12300 | https://pubsonline.informs.org/doi/references/10.1287/trsc.34.3.239.12300 | A1-deterministic-atfm-r1 #4 (publisher page) | medium |
| 3 | An Integer Optimization Approach to Large-Scale Air Traffic Flow Management | Bertsimas, Lulli, Odoni | 2011 | Operations Research 59(1) 211-227 | 10.1287/opre.1100.0899 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.1100.0899 | A1-deterministic-atfm-r1 #5 (publisher page) | medium |
| 4 | A dynamic rerouting model for air traffic flow management | Mukherjee, Hansen | 2009 | Transportation Research Part B 43(1) 159-171 | 10.1016/j.trb.2008.05.011 | https://its.berkeley.edu/publications/dynamic-rerouting-model-air-traffic-flow-management | A1-deterministic-atfm-r1 #15 (ITS Berkeley page with DOI) | medium |
| 5 | Synchronised demand-capacity balancing in collaborative air traffic flow management | Xu, Prats, Delahaye | 2020 | Transportation Research Part C 114 359-376 | 10.1016/j.trc.2020.02.007 | https://hal-enac.archives-ouvertes.fr/hal-02508893 | A1-deterministic-atfm-r1 #29 (HAL page; DOI recorded from result) | medium |
| 6 | The Continuous-Time Service Network Design Problem | Boland, Hewitt, Marshall, Savelsbergh | 2017 | Operations Research 65(5) 1303-1321 | "" (verifier's DOI was from recollection; not seen) | https://scholars.luc.edu/en/publications/the-continuous-time-service-network-design-problem/ | B2-time-windows-periodic-launch-r1 #18 (Loyola index page shows venue) | medium |
| 7 | Interval-Based Dynamic Discretization Discovery for Solving the Continuous-Time Service Network Design Problem | Marshall, Boland, Savelsbergh, Hewitt | 2021 | Transportation Science 55(1) 29-51 | "" | https://par.nsf.gov/biblio/10226533 | B1-service-network-design-r1 #3 (NSF PAR record) | medium |
| 8 | Dynamic Discretization Discovery for Solving the Time-Dependent Traveling Salesman Problem with Time Windows | Vu, Hewitt, Boland, Savelsbergh | 2020 | Transportation Science | "" | https://scholars.luc.edu/en/publications/dynamic-discretization-discovery-for-solving-the-time-dependent-t/ | B1-service-network-design-r1 #4 (venue/year NOT visible in snippet) | low |
| 9 | Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility operations | Wang, Delahaye, Farges, Alam | 2022 | Transportation Research Part C (believed; NOT shown in snippet) | "" | https://hal-enac.archives-ouvertes.fr/hal-03701655 | A2-uam-aam-ram-r1 C5 | low |
| 10 | A quasi-dynamic air traffic assignment model for mitigating air traffic complexity and congestion for high-density UAM operations | Wang, Delahaye, Farges, Alam | 2023 | Transportation Research Part C (believed; NOT shown) | "" | (no page seen; search summary only, A2-uam-aam-ram-r1 query 9) | A2-uam-aam-ram-r1 C6 | low |
| 11 | Optimization of subsidized air transport networks using electric aircraft | Kinene, Birolini (co-authors not confirmed) | 2024 | Transportation Research Part B (per repository metadata relayed by sibling) | "" | https://aisberg.unibg.it/handle/10446/283949 | A1-deterministic-atfm-r1 #42; A2-on-demand r2 P1 | low |
| S1 | Dynamic modeling and optimization for space logistics using time-expanded networks | Ho, de Weck, Hoffman, Shishko | 2014 | Acta Astronautica (adjacent-venue) | "" | https://experts.illinois.edu/en/publications/dynamic-modeling-and-optimization-for-space-logistics-using-time-/ | B2-time-windows-periodic-launch-r1 A1 | medium |
| S2 | Event-Driven Network Model for Space Mission Optimization with High-Thrust and Low-Thrust Spacecraft | Jagannatha, Ho | 2020 | Journal of Spacecraft and Rockets 57(3) 446-463 (adjacent-venue) | "" | https://arxiv.org/abs/1904.09364 | B2-time-windows-periodic-launch-r1 A3 | medium |

## Methodological reading for the report writer: how DTA machinery maps onto ATFM and UAM assignment

(The mapping below is methodological commentary on the corroborated papers; the classical DTA papers it refers to are
NOT corroborated in this run and are named only as lineage - see "leads".)

1. Holding-over-time arcs. In a time-expanded network a node (location i, period t) is joined to (i, t+1) by a
   holding arc. In SO-DTA (Merchant-Nemhauser / Carey / Ziliaskopoulos lineage) that arc carries vehicles queued on a
   link or held in a cell; in ATFM it is ground holding when i is the departure airport and airborne holding when i
   is a sector or the arrival airport. Bertsimas & Stock Patterson 1998 (#1) encode the same thing with cumulative
   "by-time" variables w(f,j,t) = 1 if flight f has reached sector j by t: the hold is w(f,j,t) - w(f,j,t-1) summed,
   and the cumulative encoding gives the facet-defining, near-integral LP relaxation. In a RAM model the holding arc
   at a regional airport doubles as the turnaround / charging arc, so the per-period capacity on that arc becomes
   stand or charger capacity.

2. FIFO / non-overtaking. DTA imposes FIFO on link exit (CTM sending/receiving functions, or the exit-flow function of
   Merchant-Nemhauser/Carey). ATFM flight-level IPs do not need FIFO because each flight is its own commodity with a
   fixed route segment order; the by-time connectivity constraints w(f,j+1,t) <= w(f,j,t - tau) play the role of
   link traversal time. Aggregate ATFM (Bertsimas & Stock Patterson 2000, #2) treats flows per origin-destination
   commodity and recovers flight identities afterwards, which is exactly where FIFO-type consistency has to be
   restored by the disaggregation step. The UAM quasi-dynamic assignment (#10) sits in between: flows are
   route-level rates per time slice, propagated across slices, with no per-vehicle FIFO.

3. Capacity-over-time. CTM/SO-DTA bound flow into each cell per period (sending <= receiving, capacity Q_i(t)). ATFM
   bounds the number of flights in sector j during period t and the departures/arrivals at airport k in period t
   (#1, #3), and Mukherjee & Hansen 2009 (#4) make those bounds scenario-dependent on a tree. Xu, Prats & Delahaye
   2020 (#5) make the capacity profile itself a decision (sector opening scheme per period), the airspace analogue of
   time-varying link capacity / signal control in DTA. For RAM the same constraint family covers low-altitude
   corridor throughput, small-airport arrival/departure slots and charging-slot availability per period.

4. Time discretization error. Full time expansion at the resolution needed for turnaround and charging durations is
   the scaling bottleneck for time-indexed ATFM/RAM IPs. The DDD line (#6, #7, #8) shows that an exact
   continuous-time optimum can be obtained on a partially time-expanded network whose arcs under-estimate durations
   (valid lower bound) and whose time points are refined only where the relaxed solution is time-infeasible.
   Interval-indexed nodes (#7) fit ground-hold windows naturally. S1/S2 are the spaceport-to-orbit analogue: a uniform
   time-expanded generalized multicommodity flow (S1) versus an event-driven, non-uniform discretization at launch /
   transfer events (S2).

5. Quasi-dynamic assignment for UAM (#9, #10). Static multilayer assignment with a congestion plus
   linear-dynamical-system complexity objective (#9), then time-sliced assignment with inter-slice flow propagation
   (#10). Relative to SO-DTA this is a semi-dynamic (quasi-dynamic) loading without spillback; relative to ATFM IPs it
   is the aggregate pre-balancing step before flight-level slot assignment.

## Leads for round 3 (FROM MEMORY ONLY; NOT corroborated by any search in this run; NO DOIs; do NOT cite until confirmed)

Likely in-scope venue (verify title + venue first): Ford & Fulkerson 1958 maximal dynamic flows (OR); Merchant &
Nemhauser 1978 "A model and an algorithm for the dynamic traffic assignment problems" and "Optimality conditions for a
dynamic traffic assignment model" (TS); Carey 1986 constraint qualification (TS); Carey 1987 optimal time-varying
flows (OR); Carey 1992 nonconvexity of DTA (TR-B); Friesz, Luque, Tobin, Wie 1989 (OR); Friesz, Bernstein, Smith,
Tobin, Wie 1993 VI formulation (OR); Ran, Boyce, LeBlanc 1993 (OR); Wie, Tobin, Friesz, Bernstein 1995 (TS); Daganzo
1994 CTM and 1995 network CTM (TR-B); Ziliaskopoulos 2000 single-destination SO-DTA LP (TS); Lo & Szeto 2002 cell-based
VI DUO (TR-B); Carey & Subrahmanian 2000 (TR-B); Kuwahara & Akamatsu 2001 (TR-B); Carey & Ge 2005 (TS); Waller &
Ziliaskopoulos 2006 chance-constrained SDTA (TR-C); Nie 2011 cell-based Merchant-Nemhauser (TR-B); Doan & Ukkusuri
2012 holding-back problem (TR-B); Ban, Pang, Liu, Ma 2012 point-queue (TR-B); Ma, Ban, Pang 2014 continuous-time DSO
(TR-B); Han, Friesz, Yao 2013 (TR-B); Levin 2017 SO route choice for SAVs with CTM LP (TR-C); Long, Wang, Szeto 2019
link-based SO-DTA (OR?); Hewitt 2019 enhanced DDD load plan (TS); Lagos, Boland, Savelsbergh 2020 (TS); Scherr, Hewitt,
Neumann Saavedra, Mattfeld 2020 DDD mixed autonomous fleets (TR-B); Hewitt 2022 flexible scheduled SND (TS); Hewitt &
Lehuede 2023 (TR-B); Lulli & Odoni 2007 (TS, already corroborated by A1 as an ATFM item).
Likely OUT of scope venue: Fleischer & Skutella 2007 (SIAM J Comput); Hoppe & Tardos 2000 (Math OR); Aronson 1989
(Annals OR); Peeta & Ziliaskopoulos 2001 (NSE); Peeta & Mahmassani 1995 (Annals OR); Li, Waller, Ziliaskopoulos 2003
(NSE); Ukkusuri & Waller 2008 (NSE); Boland, Hewitt, Marshall, Savelsbergh 2019 price of discretizing time (EJTL); He,
Boland, Nemhauser, Savelsbergh 2022 (IJOC); Boland & Savelsbergh 2019 (TOP).

## Round-3 query plan (not executed; 32 queries)
(a) Methodology: "system optimum dynamic traffic assignment" "Transportation Science" linear programming cell transmission;
"dynamic traffic assignment" "Operations Research" 1987 OR 1993 optimal control variational inequality; "flows over time"
OR "dynamic flows" "Operations Research" INFORMS; "cell transmission model" Daganzo "Transportation Research Part B" 1994
1995; "dynamic network loading" "Transportation Research Part B" FIFO exit flow; "time-expanded network" discretization
"Transportation Science"; "partially time-expanded" OR "dynamic discretization discovery" "Transportation Science" 2019
2021 2022 2023 2024; "dynamic discretization discovery" "Transportation Research Part B" 2020 2023; "holding back" cell
transmission system optimum "Transportation Research Part B"; "continuous-time" dynamic system optimum "Transportation
Research Part B" 2014.
(b) Problem: "air traffic flow management" "dynamic network flow" "Transportation Science"; air traffic "dynamic traffic
assignment" OR "quasi-dynamic" "Transportation Research Part C" 2022 2023; "urban air mobility" traffic assignment
complexity "Transportation Research Part C" Delahaye; "regional air mobility" OR "advanced air mobility" time-expanded
"Transportation Research Part C" 2024 2025 2026.
(c) Authors: Ford Fulkerson 1958 OR; Merchant Nemhauser 1978 TS (two titles); Carey 1986 TS, 1987 OR, 1992 TR-B; Friesz
Bernstein Smith Tobin Wie 1993 OR; Ran Boyce LeBlanc 1993 OR; Ziliaskopoulos 2000 TS; Lo Szeto 2002 TR-B; Nie 2011 TR-B;
Hewitt 2019 TS enhanced DDD; Marshall Boland Savelsbergh Hewitt 2021 TS (DOI check); Boland Hewitt Marshall Savelsbergh
2017 OR (DOI check); Vu Hewitt Boland Savelsbergh 2020 TS (venue check); Wang Delahaye Farges Alam 2022/2023 TR-C (DOI check).
(d) DOI prefixes: "10.1287/trsc" "dynamic traffic assignment"; "10.1287/opre" "dynamic traffic assignment" OR "dynamic
flows"; "10.1016/j.trb" "cell transmission" OR "dynamic network loading"; "10.1016/0191-2615" cell transmission 1994;
"10.1016/j.trc" "traffic assignment" "urban air mobility".

## Gaps
- Flows-over-time and SO-DTA classics in OR/TS/TR-B: zero corroborated after two rounds (budget).
- Discretization-error line (Hewitt 2019 TS; Boland et al. follow-ups): only the 2017 OR, 2021 TS and 2020 TS DDD
  papers carried, none with a seen DOI.
- 2021-2026 dynamic-flow / DTA papers in the four venues: none beyond the DDD and UAM items carried from siblings.
- Pre-2005 classics: only Bertsimas & Stock Patterson 1998/2000 carried.
- DOIs for the two Wang-Delahaye TR-C papers and the Boland/Marshall/Vu DDD papers were never seen in a result.
