# Facet A2-aam-network-planning-airspace-capacity (round 2) — Strategic network planning and airspace-capacity modelling for advanced and regional air mobility

Date: 2026-10-06. Agent: facet aam-network-planning-airspace-capacity (round 2).
Overall topic: Topic A — Regional Air Mobility (RAM) air traffic flow management, OR methodology lineage.
Facet scope (from brief): airline / RAM network and fleet planning with demand-supply interaction (Birolini, Jacquillat,
Cattaneo, Antunes TR-B 2021; Vaze & Barnhart TS 2012; Barnhart, Fearing, Vaze OR 2014); vertiport / skyport location,
fleet sizing and demand estimation for UAM/RAM in TR-C and TR-B (Garrow, German, Leonard TR-C 2021; citing papers of
Willey & Salmon TR-C 2021 on vertiport capacity and network design 2022-2026; Rajendran; Rath & Chow; Rimjha/Trani);
airspace structure and capacity for low-altitude operations (Sunil, Ellerbroek, Hoekstra et al. TR-C 2018 and the
Delft Metropolis line; Doole, Ellerbroek, Hoekstra constrained urban airspace); UTM strategic deconfliction and
demand-capacity balancing with fairness (Chin, Gopalakrishnan, Balakrishnan, Egorov, Evans) where it appears in TR-C.

## STATUS: NO SEARCHES COULD BE EXECUTED

Every WebSearch call issued by this agent (6 queries, listed below) was refused with:
"Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn, shared
by every agent in it)."

WebFetch, curl, wget and every other HTTP path are blocked by the egress proxy, and the task rules forbid recording any
paper from memory alone or inventing DOIs. Consequently this facet has ZERO independently corroborated candidates in
round 2. The run-wide picture is the same: facets A1-trajectory-airspace (r1), A2-ram-demand-network-planning (r1),
A2-on-demand-aviation-and-electric-fleet-ops (r2) and B2-drone-uam-emerging-network-design (r1 and r2) all report the
identical block. Of the anchors named in THIS facet's brief, NONE was corroborated by any executed search anywhere in
the run (checked by grepping every notes file and every verified/*.ndjson record for: Birolini, Cattaneo, "network
planning", Vaze & Barnhart "frequency competition", Fearing "passenger travel", Garrow, German, Leonard, Sunil,
Ellerbroek, Hoekstra, Doole, Metropolis, Chin, Gopalakrishnan, Egorov, Rajendran, Rath, Chow, Rimjha, Trani — hits are
only planned-query lines or "expected venue" remarks, never a search result).

This is a coverage gap of the run, not evidence that the literature is thin: the brief's anchors are well-known items
in TR-B / TS / OR / TR-C and should be trivially corroborated once search budget exists.

Remedy: re-run this facet in a fresh turn, or raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION, and schedule the A2
AAM/RAM facets BEFORE the A1 ATFM facets so they are not starved again. The query plan below is ready to execute.

## Queries attempted this round (ALL REFUSED — budget exhausted; zero results returned)

1. Birolini Jacquillat Cattaneo Antunes "Airline network planning" mixed-integer non-convex demand-supply interactions Transportation Research Part B  (standard)
2. Vaze Barnhart "Modeling airline frequency competition for airport congestion mitigation" Transportation Science  (standard)
3. Barnhart Fearing Vaze "Modeling passenger travel and delays in the National Air Transportation System" Operations Research  (standard)
4. Garrow German Leonard urban air mobility review Transportation Research Part C 2021  (standard)
5. Willey Salmon vertiport network design Transportation Research Part C 2021  (standard)
6. Sunil Ellerbroek Hoekstra "Three-dimensional conflict count models for unstructured and layered airspace designs" Transportation Research Part C  (standard)

## Planned queries NOT run (round-3 plan; 25-40 target, mixed by type as the brief requires)

Anchor papers via DOI-prefix / venue restrictor (verify title, venue, DOI)
7.  "10.1016/j.trb" Birolini Jacquillat Cattaneo Antunes airline network planning demand-supply interactions 2021
8.  "10.1287/trsc" Vaze Barnhart airline frequency competition airport congestion mitigation 2012
9.  "10.1287/opre" Barnhart Fearing Vaze passenger travel delays National Air Transportation System 2014
10. "10.1016/j.trc" Garrow German Leonard urban air mobility review 2021
11. Willey Salmon "urban air mobility network design" hub location subgraph isomorphism "10.1016/j.trc"
12. "10.1016/j.trc" Sunil Ellerbroek Hoekstra layered airspace conflict count models 2018
13. Doole Ellerbroek Hoekstra constrained urban airspace drone capacity "Transportation Research Part C"
14. Hoekstra Ellerbroek Metropolis airspace structure very low level "Transportation Research Part C"
15. Chin Gopalakrishnan Balakrishnan Egorov Evans UTM fairness demand capacity balancing "Transportation Research Part C"
16. Balakrishnan unmanned aircraft system traffic management strategic deconfliction "10.1016/j.trc"

Problem / methodology phrases with venue restrictors (the brief's example queries first)
17. vertiport location fleet size "Transportation Research Part C"
18. urban air mobility demand estimation "Transportation Research Part B"
19. layered airspace capacity conflict count model
20. Rath Chow "air taxi skyport location" elastic demand airport access "Transportation Research Part C"
21. Rajendran Zack air taxi infrastructure location clustering "Transportation Research Part C" OR "Transportation Research Part B"
22. Rimjha Trani "regional air mobility" OR "urban air mobility" demand "Transportation Research Part C"
23. Wu Zhang "integrated network design and demand forecast" on-demand urban air mobility "Transportation Research Part C"
24. vertiport capacity network design citing Willey Salmon 2022 2023 "Transportation Research Part C"
25. Jacquillat Vaze vertiport OR "urban air mobility" "Transportation Science" OR "Operations Research"
26. airline network planning frequency fleet passenger choice "Transportation Research Part B" Jacquillat Antunes
27. airport congestion frequency competition game "Transportation Science" Vaze
28. passenger-centric delay metrics itinerary disruption "Operations Research" Barnhart

Recent (2021-2026) targeted — at least six as the brief requires
29. "advanced air mobility" network design "10.1016/j.trc" 2024
30. "advanced air mobility" vertiport capacity "10.1016/j.trc" 2025
31. "urban air mobility" vertiport location "Transportation Research Part B" 2024 2025
32. "regional air mobility" electric aircraft network airports "Transportation Research Part C" 2026
33. UTM OR U-space demand capacity balancing strategic deconfliction "Transportation Research Part C" 2023
34. eVTOL fleet sizing vertiport location stochastic programming "Transportation Research Part C" 2025
35. "10.1287/trsc" "urban air mobility" OR eVTOL OR vertiport 2023 2024
36. "10.1287/opre" "urban air mobility" OR "air taxi" 2024

Classics before 2005 — at least four as the brief requires
37. "free flight" airspace capacity conflict model "Transportation Science" 1998 2001
38. airline network design hub-and-spoke frequency "Transportation Science" 1990s Jaillet Song Yu
39. Lederer Nambimadom "Airline network design" "Operations Research" 1998
40. en route sector capacity controller workload model "Transportation Research Part B" 1990s
41. Dobson Lederer airline scheduling routing hub-and-spoke competition "Transportation Science" 1993

Author sweeps (UAM scalability / capacity lines)
42. Vascik Hansman urban air mobility scalability constraints "Transportation Research Part C"
43. Shihab Wei "urban air mobility" network scalability capacity "Transportation Research Part C"
44. Cummings Mahmassani urban air mobility congestion simulation "Transportation Research Part C"

## Overlap check against existing verified records (scratchpad/verified/*.ndjson, 185 records)

In-scope items already verified by sibling facets that fall inside THIS facet's domain (all recorded by facets
A2-uam-aam-ram r1, A2-airport-runway-terminal r1, or A1-deterministic-atfm r1; all pass-throughs below):
- Willey, Salmon (2021) TR-C 125, art. 102997 — UAM network design via hub location + subgraph isomorphism.
- Shao, Shao, Lu (2021) TR-C 132, art. 103385 — terminal-area control rules + eVTOL adaptive scheduling, multi-vertiport.
- Song, Yeo (2021) TR-C 128, art. 103181 — approach-control / scheduling strategies for multicopter VTOL.
- Tang, Zhang, Mohmoodian, Charkhgard (2021) TR-C 131 — automated conflict-free flight planning, high-density UAM, layered semi-structured airspace.
- Wang, Delahaye, Farges, Alam (2022) TR-C — complexity-optimal UAM traffic assignment on multilayer network (venue LOW in r1).
- Wang, Delahaye, Farges, Alam (2023) TR-C — quasi-dynamic traffic assignment for high-density UAM (venue LOW in r1).
- Waltz, Okhrin, Schultz (2024) TR-C 167, art. 104806 — self-organized free-flight UAM arrival.
- Kinene, Birolini (co-authors unconfirmed) (2024) TR-B — subsidised regional air network optimisation with electric aircraft (venue LOW).
- Adjacent: Wang (Kai), Jacquillat, Vaze (2022) M&SOM 10.1287/msom.2022.1148 — vertiport planning, adaptive discretization (DOI seen in URL).
- Adjacent: Kleinbekman, Mitici, Wei (2020) JAIS — rolling-horizon eVTOL arrival scheduling, MILP with battery constraints.
- status not_found in verified/: "On-demand ridesharing based on dynamic scheduling in urban air mobility" (2025, TR-C per one portal snippet, authors not captured) — NOT recorded here.

Nothing in verified/ covers: airline network planning with demand-supply interaction (Birolini et al. TR-B 2021), airline
frequency competition (Vaze & Barnhart TS 2012), passenger-centric NAS delay modelling (Barnhart, Fearing, Vaze OR 2014),
the UAM review (Garrow, German, Leonard TR-C 2021), skyport/vertiport location with demand (Rath & Chow; Rajendran; Wu &
Zhang), UAM demand estimation (Rimjha/Trani), airspace structure and conflict-count capacity models (Sunil et al. TR-C
2018; Doole et al.; Metropolis), or UTM strategic deconfliction / DCB with fairness (Chin et al.).

## Candidates recorded this round

No candidate in this file was corroborated by a search executed by THIS agent. The items below are pass-throughs from
search results that SIBLING agents executed earlier in this run and documented with URLs in their notes files (cited per
item). They are recorded so the merge step can attach this facet's label to them; confidence is the sibling's grade or
lower, never higher. Author lists are given as surnames only, because the sibling notes and the verifier records disagree
on some first names (e.g. Tang et al.) and I could not re-check.

### P1. Willey, Salmon (2021) — A method for urban air mobility network design using hub location and subgraph isomorphism
- Venue: Transportation Research Part C 125, art. 102997. DOI not seen -> "".
- Evidence (sibling A2-uam-aam-ram r1, query 11): search summary gave title, authors, TR-C vol 125 art 102997, 2021; seen
  cited at https://pubsonline.informs.org/doi/references/10.1287/msom.2022.1148 ; preprint
  https://optimization-online.org/wp-content/uploads/2021/10/8656.pdf . Confidence: medium.
- Method (from title and snippets): hub-location formulation on candidate vertiport sites, with subgraph isomorphism used
  to embed a desired network topology in the candidate graph. Relevance: both (strategic network on which a RAM flow model
  assigns departures/routes/holds; hub selection for a feeder network).

### P2. Shao, Shao, Lu (2021) — Terminal area control rules and eVTOL adaptive scheduling model for multi-vertiport system in urban air mobility
- Venue: TR-C 132, art. 103385. DOI not seen -> "". Evidence: sibling A2-uam-aam-ram r1 query 8 search summary (title,
  authors, venue, volume, article number); no direct publisher URL was captured -> url "". Confidence: medium.
- Method (from title/snippets): terminal-area structure and control rules for a vertiport cluster plus an adaptive
  (integer) scheduling model for eVTOL arrival/departure sequencing under pad capacity; evaluated by simulation.

### P3. Song, Yeo (2021) — Development of optimal scheduling strategy and approach control model of multicopter VTOL aircrafts for urban air mobility (UAM) operation
- Venue: TR-C 128, art. 103181. DOI not seen -> "". Evidence: KAIST pages https://dspace.kaist.ac.kr/handle/10203/286733 ,
  https://smartcity.kaist.ac.kr/2021/07/an-article-development-of-optimal.html (sibling A2-uam-aam-ram r1 queries 7, 12). Confidence: medium.
- Method (from snippets): three approach-control/scheduling strategies (branch queuing, sequence-based, sequence-based with
  moving circles) compared by simulation on punctuality and loss-of-separation risk.

### P4. Tang, Zhang, Mohmoodian, Charkhgard (2021) — Automated flight planning of high-density urban air mobility
- Venue: TR-C 131 (Oct 2021). DOI not seen -> "". Evidence: sibling A2-uam-aam-ram r1 query 10 search summary; supporting
  USF dissertation page https://digitalcommons.usf.edu/etd/10410 . Confidence: medium.
- Method (from snippets): semi-structured layered airspace with direct routes between entry/exit points; conflict-free 4D
  trajectory generation for medium-to-high-density UAM.

### P5. Wang, Delahaye, Farges, Alam (2022) — Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility operations
- Venue: TR-C 2022 (believed; NOT shown in snippet). DOI not seen -> "". Evidence: sibling A2-uam-aam-ram r1 query 9
  (model described in search summary); HAL page https://hal-enac.archives-ouvertes.fr/hal-03701655 . Confidence: LOW.
- Method (from summary): macroscopic traffic assignment on a multilayer network with a linear-dynamical-system complexity
  metric, solved by a two-step Dafermos-type algorithm.

### P6. Wang, Delahaye, Farges, Alam (2023) — A quasi-dynamic air traffic assignment model for mitigating air traffic complexity and congestion for high-density UAM operations
- Venue: TR-C 2023 (believed; NOT shown). DOI not seen -> "". No URL captured -> "". Evidence: sibling A2-uam-aam-ram r1
  query 9 summary. Confidence: LOW.
- Method (from summary): quasi-dynamic assignment of flows to routes over a planning horizon with complexity + congestion
  objective; centralised strategic planning.

### P7. Waltz, Okhrin, Schultz (2024) — Self-organized free-flight arrival for urban air mobility
- Venue: TR-C 167, art. 104806. DOI not seen -> "". Evidence: sibling A2-airport-runway-terminal r1,
  https://www.unibw.de/lvk-en/publications/2024_self-organized_free-flight_uam_arrival . Confidence: medium.
- Method (from title/sibling note): decentralised, self-organising arrival management for UAM in free-flight airspace,
  evaluated by simulation.

### P8. Kinene, Birolini (co-authors unconfirmed) (2024) — Optimization of subsidized air transport networks using electric aircraft
- Venue: Transportation Research Part B (from repository metadata as relayed). DOI not seen -> "". Evidence: sibling
  A1-deterministic-atfm r1 item 42, https://aisberg.unibg.it/handle/10446/283949 . Confidence: LOW.
- Method (from title/sibling notes): MILP route/frequency/fleet choice for subsidised regional routes with electric aircraft
  range and charging constraints. Relevance: both.

### Adjacent-venue pass-throughs (tag adjacent-venue)
- S1. Wang (Kai), Jacquillat, Vaze (2022) — Vertiport Planning for Urban Aerial Mobility: An Adaptive Discretization
  Approach — Manufacturing & Service Operations Management, DOI 10.1287/msom.2022.1148 (seen in URL
  https://pubsonline.informs.org/doi/references/10.1287/msom.2022.1148 by sibling A2-uam-aam-ram r1). Confidence: high.
- S2. Kleinbekman, Mitici, Wei (2020) — Rolling-horizon electric vertical takeoff and landing arrival scheduling for
  on-demand urban air mobility — Journal of Aerospace Information Systems;
  https://research.tudelft.nl/en/publications/rolling-horizon-electric-vertical-takeoff-and-landing-arrival-sch (sibling
  A2-uam-aam-ram r1 queries 5, 8). MILP assigning required times of arrival under pad and battery constraints, rolling
  horizon. Confidence: medium.

## Coverage assessment and gaps (all unsearched in this facet)
- Airline / RAM network planning with demand-supply interaction (Birolini et al. TR-B 2021; Vaze & Barnhart TS 2012;
  Barnhart, Fearing, Vaze OR 2014): 0 corroborated.
- UAM/RAM review and demand estimation (Garrow, German, Leonard TR-C 2021; Rimjha/Trani): 0 corroborated.
- Vertiport / skyport location, fleet sizing, citing papers of Willey & Salmon 2022-2026 (Rath & Chow; Rajendran; Wu &
  Zhang): 0 corroborated beyond Willey & Salmon itself.
- Airspace structure and capacity (Sunil et al. TR-C 2018; Doole et al.; Metropolis line): 0 corroborated.
- UTM strategic deconfliction / DCB with fairness (Chin et al.) in TR-C: 0 corroborated.
- Pre-2005 classics (free-flight airspace capacity; hub-and-spoke airline network design in TS/OR): 0 corroborated.

## Note for the report writer
Nothing in this file may be cited as corroborated by this facet. P1-P8, S1, S2 were corroborated by siblings' executed
searches (URLs above) and are already in scratchpad/verified/; they are repeated here only so the facet label attaches
to them in the merge. The anchor list in the facet brief is an orchestrator-supplied plan, not a search result; do not
promote those items to the verified table without a successful search in a follow-up run.
