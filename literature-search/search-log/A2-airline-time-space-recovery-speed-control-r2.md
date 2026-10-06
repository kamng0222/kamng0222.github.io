# Facet A2-airline-time-space-recovery-speed-control (round 2)

Date: 2026-10-06. Agent: facet airline-time-space-recovery-speed-control (r2).
Overall topic: Topic A - Regional Air Mobility (RAM) air traffic flow management, OR methodology lineage.
Facet scope: airline schedule planning and disruption recovery as the time-space-network methodology a RAM flow
model inherits: fleet assignment and aircraft routing with ground arcs and flight strings; recovery models that
reschedule, swap, cancel and speed up flights; special weight on cruise-speed control as a flow lever.
Venues in scope: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## STATUS: NO SEARCH COULD BE EXECUTED IN ROUND 2 (SAME FAILURE AS ROUND 1) - 4 PASS-THROUGH CANDIDATES ONLY

The per-turn WebSearch budget (200 calls, shared by every agent in this workflow turn) was already exhausted
when this agent issued its first batch of eight queries. All eight were refused with "Web search was not
performed: this turn's web search budget is used up". WebSearch is the only route to the internet here
(WebFetch, curl, wget, pip are blocked by the egress proxy) and the budget notice forbids working around the
limit, so no further query was attempted. Round 1 of this facet (A2-airline-schedule-recovery-r1.md) failed the
same way and recorded zero candidates, so after two rounds the facet still has NO independently corroborated
item from its own searches.

Fallback performed without internet: every notes file and every verified/*.ndjson record left by sibling agents
in this run was grepped for fleet assignment, aircraft routing, flight string, aircraft/airline recovery,
disruption management, cruise speed, speed control, retiming, tail assignment, block time, delay propagation,
robust airline, and for the surnames Barnhart, Lohatepanont, Rexing, Rosenberger, Jarrah, Petersen, Maher,
Marla, Lee, Liang, Sohoni, Arikan, Akturk, Gurel, Safak, Cacchiani, Lan, Clarke, Jiang, Dunbar, Froyland,
Cordeau, Klabjan, Berge, Hopperstad, Talluri, Hane, Sherali, Jacobs, Dumas, Rushmeier, Pita, Wei, Vaze,
Birolini, Justin, Vink, Evler, Wandelt. Result: NONE of the anchor papers named in the facet brief (Barnhart et
al. 1998; Rexing et al. 2000; Lohatepanont & Barnhart 2004; Lan, Clarke & Barnhart 2006; Cacchiani &
Salazar-Gonzalez 2017; Jarrah et al. 1993; Yan & Yang 1996; Rosenberger et al. 2003; Petersen et al. 2012;
Maher 2016; Lee, Marla & Jaillet 2020; Marla, Vaaben & Barnhart 2017; Liang et al. 2018; Akturk, Atamturk &
Gurel 2014; Arikan, Deshpande & Sohoni 2017; Gurkan, Gurel & Akturk 2016; Safak, Cavus & Akturk 2018; Sohoni,
Lee & Klabjan 2011) was corroborated by ANY executed search in this run, mine or a sibling's.

The only in-scope, search-corroborated items anywhere in the run that fall inside this facet's methodology are
four pass-throughs (below): three on cruise-speed reduction / delay transfer as a flow lever (ATFM side, not
airline-side rescheduling) and one on electric-aircraft fleet/network design on a time-space-energy network.
Each was corroborated by a SIBLING agent's executed search (URL logged), not by this agent, so confidence is
capped at medium (publisher page seen by sibling) or low (repository page only). All four are already in the
verified pipeline from other facets; the merge step deduplicates on DOI/title.

Per the facet rules ("never record a paper from memory alone"; "a wrong venue or an invented paper is worse than a
missing one"), nothing else is recorded. The StructuredOutput carries 4 candidates.

Remedy: a follow-up turn (fresh budget) or a higher CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION; the round-3 plan
below is ready to run as-is. Schedule this facet before the A1 ATFM facets so it is not starved a third time.

## Queries issued this round - ALL REFUSED (budget exhausted; none executed)

1. "Flight string models" fleet assignment aircraft routing Transportation Science Barnhart Boland 1998
2. Rexing Barnhart Kniker "Airline fleet assignment with time windows" Transportation Science 2000
3. Lohatepanont Barnhart "Airline schedule planning: integrated models and algorithms for schedule design and fleet assignment" Transportation Science
4. Lan Clarke Barnhart "Planning for robust airline operations" Transportation Science 2006 10.1287/trsc
5. Cacchiani Salazar-Gonzalez "Optimal solutions to a real-world integrated airline scheduling problem" Transportation Science 2017
6. Jarrah Yu Krishnamurthy Rakshit "decision support framework for airline flight cancellations and delays" Operations Research 1993
7. Yan Yang "decision support framework for handling schedule perturbation" Transportation Research Part B 1996
8. Rosenberger Johnson Nemhauser "Rerouting aircraft for airline recovery" Transportation Science 2003

## Candidates recorded (pass-throughs from sibling agents' executed searches)

### C1. Jones, Lovell, Ball (2018) - Stochastic Optimization Models for Transferring Delay Along Flight Trajectories to Reduce Fuel Usage
- Venue: Transportation Science 52(1) 134-149. DOI 10.1287/trsc.2016.0689 (seen in the publisher URL logged by
  facet A1-deterministic-atfm / A1-trajectory, verified record A1-verified-r1-3).
- Evidence URL: https://pubsonline.informs.org/doi/10.1287/trsc.2016.0689
- Method: two-stage stochastic integer program over GDP cancellation-time scenarios; each flight's assigned ground
  delay is partly converted into en-route speed reduction so that early GDP cancellation lets the flight accelerate
  and recover delay at no extra fuel relative to the ground-hold baseline; expected fuel vs expected delay traded on
  realistic GDP instances.
- Why in this facet: speed control used as a flow lever (the facet's special-weight theme) - the ATFM counterpart of
  the Akturk / Arikan cruise-speed rescheduling line.
- Relevance A: RAM flow model can treat airborne speed reduction as a continuous recourse that shifts delay from
  ground to air when charger/airport capacity recovers earlier than forecast.
- Confidence: medium (publisher page seen by sibling, not by me). Duplicate of A1 record.

### C2. Delgado, Prats, Sridhar (2013) - Cruise speed reduction for ground delay programs: A case study for San Francisco International Airport arrivals
- Venue: Transportation Research Part C 36, 83-96. DOI not seen -> "".
- Evidence URL (sibling A1-deterministic-atfm item 39): https://westminsterresearch.westminster.ac.uk/item/9x205/cruise-speed-reduction-for-ground-delay-programs-a-case-study-for-san-francisco-international-airport-arrivals
- Method: aircraft-performance / trajectory model computing the "equivalent cruise speed" (slower speed with the same
  fuel burn as nominal) so GDP delay is absorbed airborne and recoverable if the GDP ends early; recoverable delay
  quantified by flight length, aircraft type and GDP cancellation time on SFO arrivals.
- Relevance A: supplies the speed-vs-fuel feasibility envelope that a RAM flow model needs to price airborne delay
  absorption for small electric aircraft (energy-equivalent speed instead of fuel-equivalent speed).
- Confidence: low (university repository record only; not opened by me). Duplicate of A1 record.

### C3. Delgado, Prats (2014) - Operating cost based cruise speed reduction for ground delay programs: Effect of scope length
- Venue: Transportation Research Part C 48, 437-452. DOI not seen -> "".
- Evidence URL (sibling A1-deterministic-atfm item 40): https://results2021.ref.ac.uk/outputs/d9f582f0-4815-4d9d-8b16-c113fbfeb998?page=1
- Method: extends C2 with a cost-index (operating-cost) speed criterion and a parametric analysis of GDP scope length
  (which flights are included, hence how long they are airborne), trading controller commitment under uncertainty
  against airline cost.
- Relevance A: shows how the geographic scope of a flow-control programme interacts with speed control; for RAM, the
  analogue is which regional feeder legs are long enough to absorb delay airborne.
- Confidence: low (REF output record only). Duplicate of A1 record.

### C4. Kinene, Birolini (co-authors unconfirmed) (2024) - Optimization of subsidized air transport networks using electric aircraft
- Venue: Transportation Research Part B (from repository metadata as relayed by sibling A1-deterministic-atfm item 42). DOI not seen -> "".
- Evidence URL: https://aisberg.unibg.it/handle/10446/283949 (University of Bergamo repository).
- Method (per sibling verified record A1-verified-r1-4; abstract not seen by me): quadratic demand disaggregation,
  then a bi-objective MILP on a time-space-energy network choosing routes, frequencies and a mixed
  electric/conventional fleet while tracking battery energy along aircraft rotations under a subsidy budget.
- Why in this facet: the only corroborated item in the run from the fleet-assignment lineage (Birolini / Jacquillat
  airline network planning) and the only one that adds charging/range state to the time-space network the facet is
  about.
- Relevance both: (A) battery energy as a third coordinate of the time-expanded graph is the template for a RAM flow
  model where charging capacity is an ATFM-style resource; (B) subsidy-constrained route/frequency/fleet choice for
  range- and turnaround-limited vehicles mirrors the spaceport feeder question.
- Confidence: low (repository metadata only; author list and DOI unconfirmed). Already passed through by four
  sibling facets; merge step should keep one copy.

## Sightings in sibling notes that touch this facet but are NOT recorded here
- Pyrgiotis, Malone, Odoni (2013) TR-C 27, DOI 10.1016/j.trc.2011.05.017 (TRID record via A2-airport facet): airport-
  network delay-propagation queueing model. Related to the propagated-delay logic of robust routing but airport-side,
  not airline scheduling; already recorded by A2-airport.
- Pyrgiotis, Odoni (2016) TS 50(1), DOI 10.1287/trsc.2014.0564: IP schedule displacement under hourly caps, evaluated
  with queueing and delay propagation. Airport scheduling facet; already recorded by A1.
- Jacquillat, Odoni (2015) OR 63(6), DOI 10.1287/opre.2015.1428; Ribeiro et al. (2018) TR-B 112, DOI
  10.1016/j.trb.2018.04.005: airport-side; recorded by A1/A2/B2.
- Kleinbekman, Mitici, Wei (2020) JAIS (adjacent venue) eVTOL arrival scheduling with battery constraints; recorded by
  A2-on-demand-aviation.

## Round-3 query plan (40 queries; none run). Order: DOI-prefix sweeps first (most hits per call), then venue
## restrictors, then author-name queries for classics, then recency. Mix satisfies the task rule (>= 6 recency, >= 4 pre-2005).

### (e) DOI-prefix sweeps
1.  "10.1287/trsc" "fleet assignment" time-space network
2.  "10.1287/trsc" "aircraft recovery" OR "airline recovery" column generation
3.  "10.1287/trsc" "cruise speed" OR "speed control" airline
4.  "10.1287/opre" "aircraft rescheduling" OR "cruise speed control" OR "fleet assignment"
5.  "10.1016/j.trb" airline scheduling cruise speed OR aircraft recovery OR fleet assignment
6.  "10.1016/j.trc" airline recovery OR disruption management OR cruise speed OR electric aircraft fleet assignment

### (a)/(b) Methodology and problem phrases with venue restrictors
7.  time-space network fleet assignment ground arcs "Transportation Science"
8.  "flight string" aircraft routing fleeting "Transportation Science"
9.  aircraft recovery column generation "Transportation Science"
10. integrated airline recovery aircraft crew passengers "Transportation Science" column-and-row generation
11. cruise speed control rescheduling "Operations Research" INFORMS
12. airline schedule recovery "Transportation Research Part B" cancellation swap delay
13. airline disruption management flight planning fuel burn "Transportation Research Part C" OR "Transportation Science"
14. robust airline scheduling block time uncertainty "Transportation Science"
15. robust aircraft routing propagated delay "Transportation Science"
16. dynamic airline scheduling re-fleeting retiming "Transportation Science"
17. integrated flight scheduling fleet assignment airport congestion "Transportation Science"

### (c) Author surnames (classics pre-2005 and seminal)
18. Barnhart Boland Clarke Johnson Nemhauser Shenoi flight string "Transportation Science" 1998
19. Rexing Barnhart Kniker Jarrah Krishnamurthy fleet assignment time windows "Transportation Science" 2000
20. Lohatepanont Barnhart schedule design fleet assignment "Transportation Science" 2004 ; Barnhart Kniker Lohatepanont itinerary-based 2002
21. Jarrah Yu Krishnamurthy Rakshit flight cancellations delays "Operations Research" 1993 ; Berge Hopperstad demand driven dispatch "Operations Research" 1993
22. Yan Yang schedule perturbation "Transportation Research Part B" 1996 ; Talluri swapping fleet assignment "Transportation Science" 1996
23. Rosenberger Johnson Nemhauser rerouting aircraft "Transportation Science" 2003 ; Cordeau Stojkovic Soumis Desrosiers Benders routing crew "Transportation Science" 2001
24. Clarke Hane Johnson Nemhauser maintenance crew fleet assignment "Transportation Science" 1996 ; Rushmeier Kontogiorgis 1997
25. Lan Clarke Barnhart robust airline operations "Transportation Science" 2006 ; Jiang Barnhart dynamic airline scheduling 2009
26. Sohoni Lee Klabjan block-time uncertainty "Transportation Science" 2011 ; Dunbar Froyland Wu propagated delay 2012
27. Petersen Solveling Clarke Johnson Shebalov integrated airline recovery "Transportation Science" 2012
28. Akturk Atamturk Gurel "aircraft rescheduling with cruise speed control" "Operations Research" 2014
29. Froyland Maher Wu recoverable robust tail assignment "Transportation Science" 2014 ; Maher column-and-row generation 2016
30. Gurkan Gurel Akturk airline scheduling fleeting routing cruise speed control "Transportation Research Part C" 2016
31. Arikan Deshpande Sohoni flight network integrated airline recovery cruise speed control "Transportation Science" 2017
32. Marla Vaaben Barnhart integrated disruption management flight planning delays fuel burn 2017 (VENUE CHECK: brief says TR-C; memory says TS 51(1))
33. Cacchiani Salazar-Gonzalez integrated airline scheduling "Transportation Science" 2017 ; Yan Kung robust aircraft routing 2018
34. Safak Cavus Akturk multi-stage airline scheduling stochastic passenger demand non-cruise times "Transportation Research Part B" 2018
35. Liang Xiao Cui Chaovalitwongse Zhang aircraft recovery airport capacity maintenance flexibility "Transportation Research Part B" 2018
36. Lee Marla Jaillet dynamic disruption management airport operating uncertainty "Transportation Science" 2020

### (d) Recency 2021-2026 (>= 6 required)
37. aircraft recovery OR airline disruption recovery "Transportation Science" OR "Transportation Research Part B" 2023 2024
38. integrated airline recovery reinforcement learning OR machine learning "Transportation Research Part C" 2024 2025
39. airline integrated robust scheduling cruise speed "Transportation Research Part B" 2021 2022 (Xu Wandelt Sun)
40. electric aircraft OR eVTOL fleet assignment charging turnaround time-space network "Transportation Research Part C" 2024 2025 2026 ;
    Justin Payan Mavris integrated fleet assignment electrified regional air mobility "Transportation Research Part C" 2022 ;
    Birolini Jacquillat Cattaneo Antunes airline network planning "Transportation Research Part B" 2021 2023 ;
    Yan Barnhart Vaze choice-based schedule design fleet assignment "Transportation Science" 2022
    (SECONDARY, at most 8: eVTOL fleet recovery EJOR / Omega 2024-2025; airline recovery TR-E 2023-2025 venue identification only.)

## Leads FROM MEMORY ONLY - NOT VERIFIED, NOT RECORDED (hypotheses for round 3; no DOIs given on purpose)

Fleet assignment / routing on time-space networks (expected TS unless noted): Clarke, Hane, Johnson, Nemhauser 1996;
Talluri 1996 (swapping); Rushmeier & Kontogiorgis 1997; Barnhart, Boland, Clarke, Johnson, Nemhauser, Shenoi 1998
(flight strings); Rexing, Barnhart, Kniker, Jarrah, Krishnamurthy 2000; Cordeau, Stojkovic, Soumis, Desrosiers 2001
(Benders routing+crew); Barnhart, Kniker, Lohatepanont 2002; Klabjan et al. 2002 (crew with time windows and
plane-count); Cohn & Barnhart 2003 (expected OR); Lohatepanont & Barnhart 2004; Smith & Johnson 2006 (station purity);
Jacobs, Smith, Johnson 2008; Barnhart, Farahat, Lohatepanont 2009 (expected OR); Dumas, Aithnard, Soumis 2009
(expected TR-B); Jiang & Barnhart 2009 (dynamic scheduling); Liang et al. 2011 and Liang & Chaovalitwongse 2013
(rotation-tour maintenance routing); Haouari, Shao, Sherali 2013; Sherali, Bae, Haouari 2013; Pita, Barnhart,
Antunes 2013 (airport congestion); Froyland, Maher, Wu 2014; Liang et al. 2015 (robust weekly routing, expected TR-B);
Cadarso, Vaze, Barnhart, Marin 2017; Cacchiani & Salazar-Gonzalez 2017; Ruther, Boland, Engineer, Evans 2017; Yan &
Kung 2018; Wei, Vaze, Jacquillat 2020; Birolini, Jacquillat, Cattaneo, Antunes 2021 (expected TR-B); Yan, Barnhart,
Vaze 2022. Out of scope if found: Hane et al. 1995 (Mathematical Programming), Sherali-Bish-Zhu survey (EJOR).

Recovery: Jarrah, Yu, Krishnamurthy, Rakshit 1993 (expected OR); Berge & Hopperstad 1993 (expected OR; demand-driven
dispatch); Yan & Yang 1996 (expected TR-B); Lettovsky, Johnson, Nemhauser 2000 (crew recovery, expected TS);
Rosenberger, Johnson, Nemhauser 2003 (expected TS); Petersen, Solveling, Clarke, Johnson, Shebalov 2012 (expected
TS); Maher 2016 (expected TS); Marla, Vaaben, Barnhart 2017 (VENUE UNRESOLVED: brief says TR-C, memory says TS);
Liang, Xiao, Cui, Chaovalitwongse, Zhang 2018 (expected TR-B); Lee, Marla, Jaillet 2020 (expected TS); Vink et al.
2020 (expected TR-C); Evler et al. 2021 ground-operations recovery (expected TR-C); Xu, Wandelt, Sun 2021 (expected
TR-B); Ding, Wandelt et al. 2023 RL recovery (expected TR-C, uncertain). Out of scope if found: Thengvall-Bard-Yu
(IIE/TR-A), Bard-Yu-Arguello (IIE), Bratu & Barnhart (J. Scheduling), Clausen et al. review (C&OR), Eggenberg et al.
(C&OR), Hassan-Santos-Vink review (C&OR).

Cruise-speed control as a flow lever: Sohoni, Lee, Klabjan 2011 (expected TS); Akturk, Atamturk, Gurel 2014 (expected
OR); Gurkan, Gurel, Akturk 2016 (expected TR-C); Arikan, Deshpande, Sohoni 2017 (expected TS); Safak, Cavus, Akturk
2018 (expected TR-B); Safak, Atamturk, Akturk 2019 (new flights into existing schedule, expected TR-C); Duran, Gurel,
Akturk 2015 (IIE Trans, out); Safak, Gurel, Akturk 2017 (C&OR, out). ATFM-side speed control already corroborated by
siblings: Jones-Lovell-Ball TS 2018; Delgado et al. TR-C 2013/2014 (recorded above).

Electric / RAM fleet assignment: Justin, Payan, Briceno, German, Mavris 2020 and Justin, Payan, Mavris 2022 (expected
TR-C); Mitici et al. electric flight scheduling with battery swapping (EURO J Transp Logist, adjacent).

## Transfer notes for the RAM flow problem (methodological; independent of any citation)
- Fleet assignment / aircraft routing on a time-space (connection) network is the representation the RAM flow problem
  needs: nodes = (airport, time), arcs = flight legs, ground arcs carry aircraft with turnaround/charging minima,
  aircraft-count and balance constraints map to small eVTOL fleets; flight-string / column-generation formulations
  handle battery-cycle and maintenance side constraints as they handle maintenance checks.
- Recovery models (retiming, cancellation, swap arcs on a time-band network; rolling-horizon re-solve) are the
  operational layer of RAM demand-capacity balancing under weather or charger outages.
- Cruise-speed control (Akturk line, airline side; Jones-Lovell-Ball and Delgado lines, ATFM side) turns the discrete
  time-space model into a mixed-integer model with a continuous per-leg speed/energy variable: for electric aircraft
  the fuel-time trade-off becomes an energy-time trade-off bounded by battery state, so speed is a direct demand-
  capacity balancing lever between charging capacity and airspace/airport capacity.
- Robust scheduling under block-time uncertainty supplies the slack-allocation logic for tight charging windows.
- For facet B: fleet assignment + retiming with time windows models reusable launch vehicles against periodic launch
  windows with pad turnaround; recovery models cover scrub/slip rescheduling.

## Gaps
- Entire facet uncorroborated by its own searches after two rounds (0 of the 25-45 target; 4 pass-throughs from
  siblings, none airline-side). No DOI, publisher page or index page was seen for any fleet-assignment, routing,
  recovery or airline cruise-speed paper in this run.
- Venue of Marla, Vaaben & Barnhart 2017 must be checked in round 3 (brief says TR-C; memory says TS).
- No pre-2005 or 2021-2026 corroboration specific to this facet; no SECONDARY search possible.
