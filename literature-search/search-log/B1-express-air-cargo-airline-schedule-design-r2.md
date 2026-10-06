# Facet B1 — Express shipment, air cargo and airline schedule design (round 2, OR/TS focus)

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Venues in scope: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).
Agent: literature-search subagent, facet express-air-cargo-airline-schedule-design (r2). Date: 2026-10-06.

## STATUS: NO SEARCH COULD BE EXECUTED IN ROUND 2 EITHER — ONE PASS-THROUGH CANDIDATE ONLY

Round 2 of this facet was launched in the same workflow turn as round 1 and the other facets. The
per-turn WebSearch budget (200 calls, shared by every agent in the turn) was already exhausted when
this agent issued its first batch of six queries; all six were refused with "Web search was not
performed: this turn's web search budget is used up". WebSearch is the only route to the internet in
this environment (WebFetch, curl, wget and pip are blocked by the egress proxy) and the budget notice
forbids working around the limit, so no further query was attempted.

Fallback performed (no internet needed): every notes file and every verified/*.ndjson record left by
sibling agents in this run was grepped for express shipment, air cargo, fleet assignment, airline
schedule / network design, hub sortation, time-definite delivery and the author surnames named in the
facet brief (Barnhart, Armacost, Kim, Leung, Derigs, Lin, Lederer, Lohatepanont, Wei, Vaze, Jacquillat,
Birolini, Feng). Result: NONE of the eleven seminal targets named in the facet brief was corroborated by
any search result in this run. Exactly one in-scope sighting falls inside this facet's airline network
planning strand (Kinene & Birolini, TR-B 2024, seen by facet A1-deterministic-atfm on a University of
Bergamo repository page). It is passed through below at confidence LOW so the verifier re-checks it.

Per the facet rules ("never record a paper from memory alone", "a wrong venue or an invented paper is
worse than a missing one"), nothing else is recorded. The StructuredOutput carries 1 candidate.

Remedy: the user can send a follow-up message (new turn, fresh budget) or raise
CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION; the round-3 plan below is ready to run as-is.

## Queries issued this round — ALL REFUSED (budget exhausted; none executed)

1. Barnhart Schneur "Air network design for express shipment service" Operations Research 1996
2. Armacost Barnhart Ware "Composite variable formulations for express shipment service network design" Transportation Science
3. Kim Barnhart Ware Reinhardt "Multimodal express package delivery" Transportation Science 1999
4. Leung Van Hui Wang Chen 0-1 LP air cargo consolidation Operations Research 2009
5. Derigs Friederichs Schäfer "Air cargo scheduling" integrated models Transportation Science 2009
6. Lin Chen "hierarchical network design" time-definite express "Transportation Research Part B" 2004

## Candidate recorded (pass-through from a sibling agent's executed search; confidence LOW)

### C1. Kinene, Birolini (co-authors not confirmed) (2024) — Optimization of subsidized air transport networks using electric aircraft
- Venue: Transportation Research Part B, as stated by the search result logged by facet A1-deterministic-atfm
  (its item 42). DOI not seen -> "". Year 2024 per that result.
- Evidence URL: https://aisberg.unibg.it/handle/10446/283949 (University of Bergamo institutional repository).
- Why it is in this facet: it belongs to the Birolini / Jacquillat / Antunes airline-network-planning lineage
  named in the facet brief (Birolini et al. TR-B 2021 is the seminal target; this is the follow-on that adds
  electric-aircraft range, charging/turnaround and subsidy constraints to route-frequency-fleet network design).
- Method (from title and sibling snippet only; abstract not seen): MILP route / frequency / fleet network design
  for public-service-obligation (subsidised) regional air networks operated with electric aircraft, with
  aircraft range and charging-time constraints shaping which legs can be flown and how aircraft rotate.
- Relevance: both. (B) choosing which spoke-to-hub legs to serve at what frequency with a range-limited,
  turnaround-constrained vehicle class under a budget is exactly the spaceport-to-orbit feeder question;
  (A) its route/frequency output is the schedule input a RAM flow model consumes.
- Already recorded by facet A2-ram-demand-network-planning (its C2) at LOW confidence; the merge step should
  de-duplicate and keep the richer framing.

## Sightings in sibling notes that touch this facet but are NOT recorded here

- "Operations design for high-velocity intra-city package service", TR-B 161:150-168 (2022),
  https://ideas.repec.org/a/eee/transb/v161y2022icp150-168.html — express/parcel operations design with
  repeatable cyclic shuttle routes under capacity and timing requirements; authors not captured by the
  sibling snippet. Already recorded (LOW) by B1-service-network-design and B2-fleet-sizing; not duplicated.
- Jacquillat & Odoni, OR 63(6) 2015, 10.1287/opre.2015.1428 — airport scheduling interventions plus stochastic
  queue operations; recorded by three A facets. Airport-side, not airline schedule design; not duplicated.
- Ribeiro, Jacquillat, Antunes, Odoni, Pita, TR-B 112 2018, 10.1016/j.trb.2018.04.005 — airport slot allocation;
  recorded by A1/A2/B2 facets; not this facet.
- Barnhart, Bertsimas, Caramanis, Fearing, TS 46(2) 2012, 10.1287/trsc.1110.0393 — ATFM equity; A facet.
- Vaze & Barnhart TS 2012 (frequency competition), Jacquillat & Vaze TS 2018, Pita-Barnhart-Antunes TS 2013
  appear in sibling notes ONLY as unverified leads; no search result corroborated them.
- Aykin TS 1995 (networking policies for hub-and-spoke), Dobson & Lederer TS 1993, Adler TS 2005,
  Lederer & Nambimadom OR 1998, Lin & Chen TR-B 2004 appear in B1-hub-location-r1.md ONLY in its
  "verification queue" (not corroborated); the hub-location facet's corroborated set is pure hub location.

## Round-3 query plan (40 queries; none run). Order: DOI-prefix sweeps first (most hits per call), then venue
## restrictors, then author-name queries for classics, then recency.

### (e) DOI-prefix sweeps
1.  "10.1287/trsc" "express shipment" OR "express package" service network design
2.  "10.1287/opre" "express shipment" OR "air network design" Barnhart
3.  "10.1287/trsc" "air cargo" network OR fleet routing OR scheduling
4.  "10.1287/opre" "air cargo" consolidation OR revenue OR capacity
5.  "10.1016/j.trb" "air cargo" OR "time-definite" OR "express carrier" network design
6.  "10.1016/j.trc" "air cargo" review OR network OR freighter
7.  "10.1287/trsc" "fleet assignment" "schedule design" integrated
8.  "10.1287/opre" "fleet assignment" OR "aircraft routing" OR "maintenance routing"
9.  "10.1016/j.trb" airline network planning frequency fleet assignment demand-supply
10. "10.1016/j.trc" airline schedule design OR fleet assignment OR electric aircraft network

### (a)/(b) Methodology and problem phrases with venue restrictors
11. "express shipment service network design" "Operations Research" INFORMS
12. "composite variable" formulation express shipment "Transportation Science"
13. "air cargo network design" "Transportation Science"
14. "air cargo" consolidation 0-1 linear program "Operations Research" INFORMS
15. "airline schedule design" "fleet assignment" "Transportation Science"
16. "itinerary-based fleet assignment" OR "fleet assignment with time windows" "Transportation Science"
17. "aircraft maintenance routing" "Transportation Science" OR "Operations Research" rotation tour
18. "flight string" OR "aircraft rotation" fleeting routing "Transportation Science"
19. "hub-and-spoke" airline scheduling routing competition "Transportation Science"
20. "time-definite" express delivery network design "Transportation Research Part B"
21. "sortation" OR "sort" hub capacity parcel distribution "Transportation Science"
22. "less-than-truckload" load plan OR "service network design" "Transportation Science" OR "Operations Research"
23. passenger choice airline timetable fleet assignment "Transportation Science" spill recapture

### (c) Author surnames (classic, pre-2005 and seminal)
24. Barnhart Schneur express shipment "Operations Research" 1996
25. Armacost Barnhart Ware composite variables "Transportation Science" 2002
26. Kim Barnhart Ware Reinhardt multimodal express package "Transportation Science" 1999
27. Lederer Nambimadom "airline network design" "Operations Research" 1998
28. Dobson Lederer hub-and-spoke airline scheduling "Transportation Science" 1993 ; Daskin Panayotopoulos Lagrangian hub-and-spoke airline 1989
29. Lohatepanont Barnhart schedule design fleet assignment "Transportation Science" 2004 ; Rexing Barnhart Kniker Jarrah Krishnamurthy 2000
30. Barnhart Boland Clarke Johnson Nemhauser Shenoi flight string "Transportation Science" 1998 ; Rushmeier Kontogiorgis 1997
31. Leung Van Hui Wang Chen air cargo consolidation "Operations Research" 2009
32. Derigs Friederichs Schaefer air cargo network planning "Transportation Science" 2009
33. Lin Chen hierarchical time-definite express "Transportation Research Part B" 2004 ; Lin 2001 freight routing time-definite
34. Feng Li Shen air cargo operations literature review "Transportation Research Part C" 2015

### (d) Recency 2021-2026 (>= 6 required)
35. Wei Vaze Jacquillat airline timetable passenger choice "Transportation Science" 2020 2021
36. Birolini Jacquillat Cattaneo Antunes airline network planning demand-supply interactions "Transportation Research Part B" 2021
37. Yan Barnhart Vaze choice-based airline schedule design fleet assignment "Transportation Science" 2022 2023
38. "air cargo" network OR scheduling "Transportation Research Part C" 2023 2024 2025
39. "service network design" express OR parcel OR middle-mile "Transportation Science" OR "Transportation Research Part B" 2023 2024 2025
40. electric aircraft OR eVTOL fleet assignment turnaround charging network design "Transportation Research Part C" OR "Transportation Research Part B" 2024 2025 2026
    (SECONDARY, at most 8: "space logistics" time-expanded network Acta Astronautica / Journal of Spacecraft and Rockets 2021-2025;
    reusable launch vehicle fleet rotation turnaround optimization 2023-2026.)

## Leads FROM MEMORY ONLY — NOT VERIFIED, NOT RECORDED (hypotheses for round 3; no DOIs given on purpose)

Express shipment / parcel SND: Barnhart & Schneur 1996 (expected OR); Armacost, Barnhart & Ware 2002 (expected TS;
NOTE the facet brief says OR 2002 — venue must be checked, memory says Transportation Science 36(1));
Kim, Barnhart, Ware & Reinhardt 1999 (expected TS); Jarrah, Johnson & Neubert 2009 LTL SND (expected OR);
Erera, Hewitt, Savelsbergh & Zhang 2013 load plan design (expected TS); Lindsey, Erera & Savelsbergh 2016
(expected TS); Baubaid, Boland & Savelsbergh 2021/2023 (expected TS); Greening, Dahan & Erera 2023 middle-mile
consolidation (expected TR-B). Out-of-scope by venue if found: Armacost et al. 2004 (Interfaces), Kuby & Gray 1993
(TR-A), Barnhart, Krishnan, Kim & Ware 2002 (Comput. Optim. Appl.), Gruenert & Sebastian 2000 (EJOR).

Air cargo: Leung, Van Hui, Wang & Chen 2009 (expected OR); Derigs, Friederichs & Schaefer 2009 (expected TS);
Feng, Li & Shen 2015 review (expected TR-C). Out of scope if found: Yan, Chen & Chen 2006 (TR-E), Marsten & Muller
1980 (Management Science).

Airline schedule design / fleet assignment / rotation: Daskin & Panayotopoulos 1989 (TS); Dobson & Lederer 1993
(TS); Lederer & Nambimadom 1998 (OR); Rushmeier & Kontogiorgis 1997 (TS); Barnhart et al. 1998 flight strings
(TS); Rexing et al. 2000 (TS); Barnhart, Kniker & Lohatepanont 2002 (TS); Lohatepanont & Barnhart 2004 (TS);
Gopalan & Talluri 1998 (OR); Talluri 1998 (TS); Cordeau, Stojkovic, Soumis & Desrosiers 2001 (TS); Cohn &
Barnhart 2003 (OR); Jacobs, Smith & Johnson 2008 (TS); Barnhart, Farahat & Lohatepanont 2009 (OR); Dumas,
Aithnard & Soumis 2009 (TR-B); Sherali, Bae & Haouari 2010 and 2013 (TS); Liang et al. 2011, Liang &
Chaovalitwongse 2013, Haouari, Shao & Sherali 2013 (TS); Pita, Barnhart & Antunes 2013 (TS); Vaze & Barnhart
2012 (TS); Cadarso, Vaze, Barnhart & Marin 2017 (TS); Cacchiani & Salazar-Gonzalez 2017 (TS); Wei, Vaze &
Jacquillat 2020 (TS); Birolini, Jacquillat, Cattaneo & Antunes 2021 (TR-B); Yan, Barnhart & Vaze 2022 (TS).
Out of scope if found: Hane et al. 1995 (Mathematical Programming), Abara 1989 (Interfaces).

Hub economics / sortation / time-definite: Hansen 1990 and Hong & Harker 1992 (TR-B); Adler 2005 (TS);
Lin 2001, Lin, Lin & Chen 2004 (TR-B); Fedtke & Boysen 2017 sortation conveyors (TS); Pyrgiotis, Malone &
Odoni 2013 delay propagation (TR-C). Out of scope if found: Campbell 2009 (C&OR), Smilowitz & Daganzo 2007 (Networks).

## Transfer notes for spaceport-to-orbit feeder design (methodological; independent of any citation)

- Express-shipment SND (UPS/FedEx-type) is the closest structural analog to the feeder problem: many origins
  (spokes) feed a few hubs inside hard time windows (sort start / cut-off), aircraft routes are chosen from a
  candidate set on a time-space network, each route carries capacity, and aircraft count and balance (reusable
  asset cycles) are enforced. "Composite variables" that bundle a route with the demand it covers remove the
  weak route-capacity coupling and give strong LP bounds; this maps to launch-vehicle "mission" variables that
  bundle a spaceport, a launch window, a vehicle and the manifest it lifts to a given orbital hub.
- Hub sort capacity (packages per hour) maps to orbital-hub berthing / payload-transfer capacity per phasing
  window; banked schedules (waves of arrivals then departures) map to orbital phasing bands.
- Fleet assignment on a time-space network with ground arcs and turnaround minima gives the reusable-booster
  rotation model (pad turnaround, refurbishment as "maintenance checks"); flight-string / rotation-tour
  formulations handle cumulative-cycle limits exactly as they handle maintenance-interval limits.
- Integrated schedule design + fleet assignment (choose which legs to fly, then which vehicle type) is the
  natural model for choosing which launch windows to open and which vehicle class to assign, with
  spill/recapture logic transferring to payload deferral to a later window.
- Air-cargo consolidation 0-1 models (which shipments share which flight/ULD under weight-volume limits)
  transfer directly to payload-integration (rideshare manifesting) under mass-volume-cg limits.
- Time-definite delivery network design supplies lead-time-constrained routing for payloads with
  orbital-insertion deadlines; hub-and-spoke vs point-to-point economics frames how many orbital depots to run
  versus direct-to-target launches.

## Gaps

- All eleven seminal targets named in the facet brief remain uncorroborated after two rounds (0 of the 25-45
  target from executed searches; 1 LOW pass-through from a sibling). No DOI, publisher page or index page was seen
  for any express-shipment, air-cargo or fleet-assignment paper in this run.
- No 2021-2026 or pre-2005 corroboration specific to this facet; no SECONDARY (space logistics) search possible.
- Venue of Armacost, Barnhart & Ware 2002 must be checked in round 3 (facet brief says OR; memory says TS).
