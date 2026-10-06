# Facet B2-drone-uam-emerging-network-design (round 2) — Drone, truck-drone and UAM network design in OR / TS / TR-B / TR-C

Date: 2026-10-06. Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet scope: range-limited, recharge/turnaround-constrained vehicles serving hub networks: truck-drone TSP/VRP (TR-C, TS, TR-B), drone hub and recharging-station location with range constraints, UAM vertiport / skyport hub location, integrated UAM network design and demand, 2022-2026 TR-C vertiport/eVTOL fleet scheduling. Emphasis: how range/energy windows, charging turnaround and hub capacity are modelled (maps onto launch windows, vehicle refurbishment, orbital-hub docking capacity).

## STATUS: NO SEARCHES COULD BE EXECUTED (second consecutive round)

Every WebSearch call issued by this agent returned:
"Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn, shared by every agent in it)."

The budget was consumed by other facet agents before this facet started. WebFetch, curl and all other HTTP paths are blocked by the egress proxy, and the task rules forbid recording any paper from memory alone or inventing DOIs. Round 1 of this facet (`B2-emerging-tech-network-design-r1.md`) hit the identical block and recorded zero candidates. **This facet therefore still has no independently corroborated candidates after two rounds.** This is a coverage gap in the run, not evidence that the literature is thin: every anchor paper named in the facet brief is a well-known item in TR-C / TS / TR-B and should be trivially corroborated once search budget exists.

Remedy: re-run this facet in a fresh turn (or raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION), ideally scheduling it BEFORE the A-facets so it is not starved again. The query plan below is ready to execute.

## Queries attempted this round (all BLOCKED — budget exhausted, zero results returned)

1. Murray Chu 2015 "flying sidekick traveling salesman problem" Transportation Research Part C
2. Chauhan Unnikrishnan Figliozzi "maximum coverage capacitated facility location problem with range constrained drones"
3. Hong Kuby Murray "range-restricted recharging station coverage model for drone delivery service planning"
4. Willey Salmon "urban air mobility network design using hub location and subgraph isomorphism"
5. Rath Chow "air taxi skyport location problem" single-allocation elastic demand airport access
6. Wu Zhang "integrated network design and demand forecast for on-demand urban air mobility"

## Planned queries NOT run (for the follow-up round; 25-40 target, mixed by type)

Anchor papers (author + title)
7. Agatz Bouman Schmidt "optimization approaches for the traveling salesman problem with drone" Transportation Science
8. Dayarian Savelsbergh Clarke "same-day delivery with drone resupply" Transportation Science
9. Poikonen Golden "multi-visit drone routing problem" Transportation Science OR Operations Research
10. Roberti Ruthmair "exact methods for the traveling salesman problem with drone" Transportation Science
11. Wang Sheu "vehicle routing problem with drones" Transportation Research Part B
12. Dukkanci Kara Bektas "minimizing energy and cost in range-limited drone deliveries with speed optimization" Transportation Research Part B
13. Cheng Adulyasak Rousseau "drone routing with energy function" Transportation Research Part B

Methodology / problem phrases + venue restrictor
14. drone hub location range constraint recharging "Transportation Research Part C"
15. vertiport location hub "Transportation Research Part C"
16. eVTOL fleet scheduling turnaround charging network "Transportation Research Part C"
17. drone delivery network design battery swap station "Transportation Research Part B"
18. truck-drone synchronization time windows "Transportation Science"
19. drone resupply hub capacity "Operations Research" INFORMS
20. urban air mobility hub-and-spoke network design "Transportation Research Part B"

DOI-prefix strings
21. "10.1016/j.trc" vertiport eVTOL scheduling charging
22. "10.1016/j.trc" drone delivery hub location
23. "10.1287/trsc" drone routing
24. "10.1016/j.trb" drone energy range
25. "10.1287/opre" drone OR UAV delivery

Recent (2021-2026) targeted
26. vertiport eVTOL fleet scheduling charging "Transportation Research Part C" 2023
27. urban air mobility network design "Transportation Research Part C" 2024
28. drone hub location recharging "Transportation Research Part C" 2025
29. truck-drone routing "Transportation Science" 2024 OR 2025
30. eVTOL vertiport capacity queueing "Transportation Research Part B" 2025
31. advanced air mobility network design "10.1016/j.trc" 2026

Classics (pre-2005) — range-limited vehicle and refuelling-hub precursors
32. Hodgson "flow-capturing location-allocation model" 1990 Geographical Analysis OR "Transportation Science"
33. Kuby Lim flow refueling location model 2005
34. airline hub location range limited aircraft "Transportation Science" 1990s
35. helicopter OR air taxi fleet routing scheduling "Transportation Science" before 2000
36. electric vehicle recharging station location "Transportation Research Part B" 2000 OR 2001 OR 2002

Secondary (adjacent venues, at most 8)
37. drone delivery network hub location "Transportation Research Part E" range
38. urban air mobility vertiport location "European Journal of Operational Research" OR Omega
39. space logistics network design launch vehicle reuse "Acta Astronautica" OR "Journal of Spacecraft and Rockets"

## Candidates recorded this round

### Carried over (NOT independently re-verified this round — corroborated in round 1 by sibling facet A2-uam-aam-ram, query 11)
- Willey, L. C.; Salmon, J. L. (2021). "A method for urban air mobility network design using hub location and subgraph isomorphism." Transportation Research Part C 125, art. 102997.
  - URLs seen in round-1 search results: https://pubsonline.informs.org/doi/references/10.1287/msom.2022.1148 (listed in the reference list of Wang, Jacquillat & Vaze MSOM 2022) and https://optimization-online.org/wp-content/uploads/2021/10/8656.pdf (preprint). DOI not displayed -> "".
  - Also present in `verified/` ndjson from round 1. Recorded here only so this facet's structured output is non-empty for the merge step; confidence downgraded to medium.

### New candidates
None (0). See STATUS above.

## Overlap check against existing round-1 verified records (`scratchpad/verified/*.ndjson`, 170 records)
In-scope items already verified by sibling facets that touch this facet's domain (all UAM traffic management, relevance A, recorded by facet A2-uam-aam-ram; none are drone/hub network design):
- Shao, Shao, Lu (2021) TR-C 132 — eVTOL adaptive scheduling, multi-vertiport terminal area.
- Song, Yeo (2021) TR-C 128 — multicopter VTOL approach-control scheduling strategies.
- Tang, Zhang, Mohmoodian, Charkhgard (2021) TR-C 131 — automated 4D flight planning, high-density UAM.
- Wang, Delahaye, Farges, Alam (2022) TR-C — complexity-optimal UAM traffic assignment (venue low-confidence in r1).
- "On-demand ridesharing based on dynamic scheduling in urban air mobility" (2025) TR-C — authors not captured.
- Waltz, Okhrin, Schultz (2024) TR-C — self-organized free-flight UAM arrival.
- Adjacent: Kleinbekman, Mitici, Wei (2020) JAIS; Wang, Jacquillat, Vaze (2022) MSOM 10.1287/msom.2022.1148 (vertiport planning, adaptive discretization).

## True gaps remaining for this facet (never searched in either round)
- Truck-drone routing: Murray & Chu 2015 (TR-C); Agatz, Bouman & Schmidt 2018 (TS); Roberti & Ruthmair 2021 (TS); Poikonen & Golden 2020 (TS); Dayarian, Savelsbergh & Clarke 2020 (TS); Wang & Sheu 2019 (TR-B).
- Energy/range modelling in drone routing: Dukkanci, Kara & Bektas 2021 (TR-B); Cheng, Adulyasak & Rousseau 2020 (TR-B).
- Drone hub / recharging-station location with range constraints: Chauhan, Unnikrishnan & Figliozzi 2019 (TR-C); Hong, Kuby & Murray 2018 (TR-C).
- UAM hub / skyport location and integrated design-demand: Rath & Chow 2022 (TR-C); Wu & Zhang 2021 (TR-C).
- 2022-2026 TR-C vertiport / eVTOL fleet scheduling with charging turnaround and pad capacity.
- Pre-2005 precursors (flow-capturing / flow-refuelling location, range-limited fleet routing).

## Note for the report writer
Nothing in this file beyond the single carried-over Willey & Salmon entry may be cited as corroborated by this facet. The anchor-paper list in the facet brief is an orchestrator-supplied plan, not a search result; do not promote those items to the verified table without a successful search in a follow-up run.
