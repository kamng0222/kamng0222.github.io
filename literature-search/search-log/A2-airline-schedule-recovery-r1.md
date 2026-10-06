# Facet A2: airline-schedule-recovery (round 1)

Date: 2026-10-06. Agent: facet airline-schedule-recovery.
Scope: airline schedule design, fleet assignment, aircraft routing and disruption
recovery as time-space network methodology (TS, OR, TR-B, TR-C only).

## STATUS: NO SEARCHES COULD BE EXECUTED — ZERO CANDIDATES RECORDED

The WebSearch tool is the only route to the internet in this environment. The
per-turn WebSearch budget (200 calls, shared by every agent in the turn) was
already exhausted by sibling agents before this agent's first query ran. All six
queries submitted in the first batch were refused with "web search budget is used
up". No further attempts were made (the harness forbids working around the limit
via curl/wget/proxies).

Fallback checks performed (no internet needed):
- Repository /home/user/kamng0222.github.io: no .bib/.ris/bibliography files; grep for
  "fleet assignment", "10.1287/trsc", "10.1287/opre", "10.1016/j.trb", "10.1016/j.trc",
  "Barnhart", "aircraft recovery" returned nothing.
- Sibling notes in this folder (A2-uam-aam-ram-r1.md, B2-network-design-uncertainty-r1.md,
  B2-time-windows-periodic-launch-r1.md): no corroborated item on airline fleet
  assignment, aircraft routing, flight retiming, delay propagation or airline
  disruption recovery. The only loosely related corroborated sighting is
  Zhang & Klabjan, "Optimization for gate re-assignment", TR-B 95:260-284 (2017),
  DOI 10.1016/j.trb.2016.11.006 (recorded by facet B2-time-windows). It is an
  airport-side disruption-recovery model, not airline aircraft recovery, and is
  already captured by that facet, so it is NOT duplicated here.

Per the task rules ("never record a paper from memory alone"), no candidates are
listed. The candidate array in the structured output is empty. A ROUND 2 IS
REQUIRED for this facet; the plan below is ready to execute.

## Queries submitted but REFUSED (budget exhausted) — 6
1. Hane Barnhart Johnson Marsten Nemhauser Sigismondi fleet assignment problem time-space network 1995
2. Rexing Barnhart Kniker fleet assignment time windows "Transportation Science"
3. Sherali Bish Zhu airline fleet assignment demand-driven re-fleeting "Transportation Science"
4. Lohatepanont Barnhart integrated schedule design fleet assignment "Transportation Science" 2004
5. Thengvall Bard Yu aircraft recovery disruption "Transportation Science" multiple fleets
6. Rosenberger Johnson Nemhauser rerouting aircraft airline recovery "Transportation Science" 2003

## Round-2 search plan (not executed; 34 queries, grouped by the task's mix)

### (a)+(c) Seminal / classic (pre-2005) — fleet assignment and routing
7.  "fleet assignment problem" "Operations Research" INFORMS Hane 1995 10.1287/opre
8.  Barnhart Boland Clarke Johnson Nemhauser Shenoi "flight string" fleet assignment aircraft routing "Transportation Science" 1998
9.  Clarke Johnson Nemhauser Zhu aircraft rotation problem maintenance 10.1287/trsc
10. Desaulniers Desrosiers Dumas Solomon Soumis daily aircraft routing scheduling "Operations Research" 1997
11. Abara fleet assignment Interfaces (expect out of scope; identify only) / Subramanian Scheff Quillinan Wiper Marsten "Coldstart" fleet assignment (likely Interfaces -> out of scope; confirm)
12. Rushmeier Kontogiorgis advances in fleet assignment "Operations Research" 1997 10.1287/opre
13. Rexing Barnhart Kniker Jarrah Krishnamurthy "airline fleet assignment with time windows" Transportation Science 2000
14. Sherali Bish Zhu "airline fleet assignment concepts, models, and algorithms" (survey; check venue — may be EJOR, out of scope)
15. Sherali Bish Zhu "polyhedral analysis and algorithms for a demand-driven refleeting model" Operations Research 2005
16. Barnhart Kniker Lohatepanont itinerary-based fleet assignment "Transportation Science" 2002
17. Lohatepanont Barnhart "airline schedule planning: integrated models and algorithms for schedule design and fleet assignment" Transportation Science 2004 10.1287/trsc

### Recovery / disruption management
18. Thengvall Bard Yu "balancing user preferences for aircraft schedule recovery during irregular operations" IIE / "multiple fleet aircraft schedule recovery following hub closures" Transportation Research Part A (confirm venue; only TS/OR/TRB/TRC in scope)
19. Bard Yu Argüello "optimizing aircraft routings in response to groundings and delays" IIE Transactions (venue check) 
20. Rosenberger Johnson Nemhauser "rerouting aircraft for airline recovery" "Transportation Science" 37(4) 2003 10.1287/trsc
21. Rosenberger Schaefer Goldsman Johnson Kleywegt Nemhauser SimAir stochastic simulation airline operations (venue check)
22. Petersen Sölveling Clarke Johnson Shebalov "an optimization approach to airline integrated recovery" Transportation Science 2012 10.1287/trsc
23. Marla Vaaben Barnhart "integrated disruption management and flight planning to trade off delays and fuel burn" Transportation Science 2017 10.1287/trsc
24. Maher "solving the integrated airline recovery problem using column-and-row generation" Transportation Science 2016
25. Vink Santos Verhagen Medeiros Filho Barnhart "dynamic aircraft recovery problem" Transportation Research Part C 2020
26. Lee Marla Jacquillat "dynamic disruption management in airline networks under airport operating uncertainty" Transportation Science 2020
27. Bratu Barnhart "flight operations recovery: new approaches considering passenger recovery" (check venue; JOS likely out of scope) ; Jafari Zegordi "simultaneous recovery model for aircraft and passengers" (venue check)
28. airline integrated aircraft passenger recovery "Transportation Research Part C" 2023 2024 column generation

### Robust routing / delay propagation / retiming
29. Lan Clarke Barnhart "planning for robust airline operations: optimizing aircraft routings and flight departure times to minimize passenger disruptions" Transportation Science 2006 10.1287/trsc
30. Dunbar Froyland Wu "robust airline schedule planning: minimizing propagated delay in an integrated routing and crewing framework" Transportation Science 2012
31. Dunbar Froyland Wu "an integrated scenario-based approach for robust aircraft routing, crew pairing and re-timing" Computers & OR (venue check) 
32. Froyland Maher Wu "the recoverable robust tail assignment problem" Transportation Science 2014 10.1287/trsc
33. Yan Kung "robust aircraft routing" Transportation Science 2018 ; Ahmadbeygi Cohn Lapp "decreasing airline delay propagation by re-allocating scheduled slack" IIE (venue check)
34. Weide Ryan Ehrgott "an iterative approach to robust and integrated aircraft routing and crew scheduling" Computers & OR (venue check) ; Cacchiani Salazar-González integrated airline planning "Transportation Science" 2017
35. flight retiming "Transportation Research Part B" aircraft routing 2020 2021 2022 ; Jiang Barnhart "dynamic airline scheduling" Transportation Science 2009 10.1287/trsc

### Airline network design with hub capacity / schedule design
36. airline network design hub capacity frequency "Transportation Science" 10.1287/trsc ; Lederer Nambimadom airline network design "Operations Research" 1998
37. Jacquillat Odoni "endogenous control of service rates in stochastic and dynamic queuing models of airport congestion" / "an integrated scheduling and operations approach to airport congestion mitigation" Operations Research 2015 10.1287/opre
38. Birolini Jacquillat Cattaneo Antunes airline network planning integrated frequency fleet assignment "Transportation Research Part B" 2021 2022
39. Wei Vaze Jacquillat airline timetable development fleet assignment "Transportation Science" 2020 2021 ; Pita Barnhart Antunes integrated flight scheduling and fleet assignment under airport congestion Transportation Science 2013

### Venue / DOI-prefix sweeps targeting 2021-2026
40. "10.1287/trsc" aircraft recovery 2023 ; "10.1287/trsc" fleet assignment 2024
41. "10.1016/j.trc" aircraft recovery disruption 2023 2024 2025 ; "10.1016/j.trc" flight rescheduling eVTOL fleet recovery 2025 2026
42. "10.1016/j.trb" airline schedule design fleet assignment 2022 2023 ; "10.1016/j.trb" airline disruption recovery 2024
43. site:pubsonline.informs.org "Operations Research" airline schedule recovery 2022 2023 2024
44. electric aircraft fleet assignment charging turnaround "Transportation Research Part C" 2024 2025 (bridge to RAM: battery/charging-constrained time-space network)

## Leads (FROM MEMORY ONLY — NOT VERIFIED, NOT RECORDED AS CANDIDATES)
These are the papers the round-2 queries above are designed to corroborate. Treat
every entry as a hypothesis until a publisher/DOI/index page is seen; venues in
particular must be checked, since several classic recovery papers appeared in
IIE Transactions, TR-A, JOS or EJOR (out of scope).
- Hane, Barnhart, Johnson, Marsten, Nemhauser, Sigismondi (1995) fleet assignment on a time-space network (expected: Mathematical Programming — may be OUT of scope; verify).
- Rushmeier, Kontogiorgis (1997) fleet assignment advances (expected OR).
- Barnhart, Boland, Clarke, Johnson, Nemhauser, Shenoi (1998) flight-string fleet assignment + routing (expected TS).
- Rexing, Barnhart, Kniker, Jarrah, Krishnamurthy (2000) fleet assignment with time windows (expected TS).
- Lohatepanont, Barnhart (2004) integrated schedule design and fleet assignment (expected TS).
- Sherali, Bish, Zhu (2005) demand-driven re-fleeting polyhedral analysis (expected OR).
- Rosenberger, Johnson, Nemhauser (2003) rerouting aircraft for recovery (expected TS).
- Lan, Clarke, Barnhart (2006) robust routing + departure retiming for passenger disruption (expected TS).
- Jiang, Barnhart (2009) dynamic airline scheduling (expected TS).
- Dunbar, Froyland, Wu (2012) integrated routing/crewing propagated delay (expected TS).
- Petersen, Sölveling, Clarke, Johnson, Shebalov (2012) integrated airline recovery (expected TS).
- Froyland, Maher, Wu (2014) recoverable robust tail assignment (expected TS).
- Jacquillat, Odoni (2015) integrated airport scheduling/operations (expected OR).
- Maher (2016) integrated recovery via column-and-row generation (expected TS).
- Marla, Vaaben, Barnhart (2017) disruption management + flight planning (expected TS).
- Lee, Marla, Jacquillat (2020) dynamic disruption management under airport uncertainty (expected TS).
- Vink et al. (2020) dynamic aircraft recovery (expected TR-C).

## Transfer notes for the RAM flow problem (methodological, independent of any specific citation)
- Fleet assignment and aircraft routing on a time-space (connection) network is the
  same representation the RAM flow problem needs: nodes = (airport, time), arcs =
  flight legs, ground arcs carry aircraft between legs with turnaround/charging
  minima; aircraft-count/balance constraints map directly to small-fleet eVTOL
  rotations; "flight-string" / column-generation formulations handle maintenance
  and battery-cycle side constraints the way they handle maintenance checks.
- Recovery models (re-timing, cancellation, swap arcs on a time-band network;
  rolling-horizon re-solve) give the operational layer of RAM demand-capacity
  balancing when weather or charger outages hit; integrated aircraft-passenger
  recovery supplies passenger-centric delay costs for on-demand RAM.
- Robust routing / delay-propagation models supply the slack-allocation logic
  (where to place buffer in a rotation) that a RAM pre-departure scheduler needs
  given tight charging windows.
- For the spaceport feeder problem (facet B): fleet assignment + retiming with
  time windows is the natural model for assigning reusable launch vehicles to
  periodic windows with pad turnaround constraints; recovery models cover
  scrub/slip rescheduling.

## Gaps
- Entire facet uncorroborated this round (0 of 25-45 target). Round 2 should run
  queries 7-44 above, starting with the DOI-prefix and venue-restricted sweeps
  (fewest calls per corroborated hit), then author-name queries for classics.
