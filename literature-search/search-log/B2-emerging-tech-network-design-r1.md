# Facet B2-emerging-tech-network-design (round 1) — Emerging-technology transport network design in OR / TS / TR-B / TR-C

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet scope: drone/UAV delivery network and hub design; truck-drone systems; drone-station and charging-hub location; air taxi / UAM vertiport location and network design; hyperloop and high-speed network design; space transportation / spaceport / launch logistics; autonomous mobility hubs; EV charging network design (hub-with-capacity analog); hydrogen / alternative-fuel station location.

## STATUS: NO SEARCHES COULD BE EXECUTED

Every WebSearch call issued by this agent returned:
"Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn, shared by every agent in it)."

The budget was consumed by the other facet agents in this run before this facet started. WebFetch, curl and other HTTP paths are blocked by the egress proxy, and the task instructions forbid recording any paper from memory alone or inventing DOIs. Therefore **zero candidates are recorded for this facet in round 1**. This is a coverage gap, not evidence that the literature is empty: the facet's named anchors (Murray & Chu TR-C 2015; Agatz, Bouman & Schmidt TS 2018; Poikonen & Golden; Wang & Sheu TR-B; Mak, Rong & Shen OR; He, Yin & Zhou TR-B; Chen & Kockelman; Rajendran; Willey & Salmon; Wu & Zhang; Shihab) are all well known and should be straightforward to corroborate once search budget is available.

Recommended remedy: re-run this facet in a follow-up turn (or raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION) using the query plan below.

## Queries attempted (all BLOCKED — budget exhausted, no results returned)

1. Murray Chu "flying sidekick traveling salesman problem" Transportation Research Part C 2015
2. Agatz Bouman Schmidt "traveling salesman problem with drone" Transportation Science 2018
3. Poikonen Golden drone routing "Transportation Science" OR "Operations Research" INFORMS
4. Wang Sheu "vehicle routing problem with drones" Transportation Research Part B
5. Carlsson Song "coordinated logistics with a truck and a drone" Management Science
6. drone delivery hub location network design "Transportation Research Part C"
7. vertiport location urban air mobility network design "Transportation Research Part C"
8. Rajendran air taxi "Transportation Research Part C" OR "Transportation Research Part E"

## Planned queries NOT yet run (for the follow-up round)

Truck-drone / drone delivery / drone hubs
9. drone charging station location "Transportation Research Part B" OR "Transportation Science"
10. "10.1016/j.trc" drone delivery network hub location
11. "10.1287/trsc" drone OR UAV routing OR network design
12. drone delivery network design 2024 OR 2025 "Transportation Science"
13. truck-drone 2025 OR 2026 "Transportation Research Part C"
14. UAV delivery hub 2026 "Transportation Research Part B"
15. drone resupply station location "Operations Research" INFORMS

UAM / air taxi / vertiport
16. Willey Salmon vertiport network design optimization
17. Wu Zhang vertiport "Transportation Research Part C"
18. Shihab urban air mobility network design optimization
19. UAM vertiport location 2025 "Transportation Research Part C"
20. air taxi fleet sizing network design "Transportation Research Part B" OR "Operations Research" 2023 2024
21. "10.1016/j.trc" "urban air mobility" vertiport

Space / launch logistics
22. spaceport launch logistics "Transportation Research Part C" OR "Transportation Science"
23. "space logistics" network design "Operations Research" OR "Transportation Science" INFORMS
24. "10.1287/opre" satellite OR launch OR orbital scheduling
25. reusable launch vehicle fleet scheduling operations research
26. space transportation network time-expanded "Transportation Research"

EV charging / hydrogen / alternative fuel (hub-with-capacity analogs)
27. Mak Rong Shen "infrastructure planning for electric vehicles with battery swapping" Operations Research
28. He Yin Zhou "deploying public charging stations" Transportation Research Part B
29. Chen Kockelman charging station location "Transportation Research" Part B OR C
30. EV charging network design robust OR stochastic "Transportation Research Part B" 2023 2024
31. "10.1016/j.trb" charging station location capacity
32. Kuby flow refueling location model "Transportation Research Part B" OR "Transportation Science"
33. hydrogen refueling station location "Transportation Research Part C" OR "Transportation Science"
34. alternative-fuel station location "Operations Research" INFORMS

Hyperloop / high-speed / mobility hubs
35. hyperloop network design "Transportation Research Part C" OR "Transportation Research Part B"
36. high-speed rail network design hub "Transportation Research Part B"
37. autonomous mobility hub location "Transportation Research Part C" 2024 2025
38. shared autonomous vehicle depot location "Transportation Research Part B" OR "Transportation Science"

Classics (pre-2005)
39. flow-capturing location model Hodgson "Transportation Science" 1990
40. refueling station location Kuby Lim 2005 "Socio-Economic Planning" OR "Transportation Science"
41. airline hub location Jaillet Song Yu 1996 "Transportation Science"
42. telecommunications OR air express hub network design "Operations Research" 1990s

## Candidates recorded

None (0). See STATUS above.

## Overlap with other facets (from existing notes files in this directory, for the merge step)

- `A2-uam-aam-ram-r1.md` already covers UAM / eVTOL vertiport scheduling and some vertiport planning items (e.g. "Vertiport Planning for Urban Aerial Mobility: An Adaptive Discretization Approach", MSOM 10.1287/msom.2022.1148 — out-of-scope venue; several TR-C vertiport scheduling papers). It lists venue sweeps still pending for TR-B + UAM, TS + air taxi, OR + UAM, and "10.1016/j.trc" + "advanced air mobility" 2024-2026.
- `B2-time-windows-periodic-launch-r1.md` already records the adjacent-venue space-logistics items (Ho, de Weck, Hoffman, Shishko 2014 Acta Astronautica time-expanded network; Chen & Ho 2018 JSR MINLP) and reports that no "spaceport"/"orbital" network design paper surfaced in TR-C/TR-B in its searches.
- `B1-hub-location-r1.md`, `B2-network-design-uncertainty-r1.md` touch hub location under uncertainty but not drone/EV/UAM network design.

Not covered anywhere in round 1 (true gaps): truck-drone routing (Murray & Chu; Agatz et al.; Poikonen & Golden; Wang & Sheu), drone hub / charging-station location, EV charging network design (Mak-Rong-Shen; He-Yin-Zhou; Chen-Kockelman), hydrogen / alt-fuel station location (Kuby; flow-refueling), hyperloop / high-speed network design, autonomous mobility hubs.
