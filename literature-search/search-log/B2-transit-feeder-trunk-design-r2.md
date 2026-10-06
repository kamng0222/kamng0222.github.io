# Facet B2 transit-feeder-trunk-design — round 2 notes

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet: trunk-and-feeder / hierarchical transit network design in which many low-capacity feeder services
deliver passengers to a few high-capacity trunk stations or hubs (structural analog of spaceports feeding
orbital hubs). Co-optimization of feeder frequency, stop spacing and transfer coordination.
Venues in scope: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## Status / important caveat (round 2 — SAME FAILURE AS ROUND 1)

ZERO WebSearch queries could be executed in this round either. The first batch of six queries was refused
with: "web search budget is used up (limit: 200 WebSearch calls per turn, shared by every agent in it)".
Sibling agents consumed the pooled per-turn budget before this agent started. Per the task constraints no
workaround (curl, wget, WebFetch, proxies, archive or reader services) was attempted.

Consequence: this facet still has NO newly corroborated candidates. The procedure forbids recording any
paper from memory alone, so no feeder-bus / hierarchical-transit paper is recorded here. Two items that
sibling facets had ALREADY corroborated from their own search results and that sit squarely on this facet's
"transfer coordination" theme are cross-referenced below (not new finds; de-duplicate at merge).

A third round (fresh WebSearch budget, ideally run while no sibling agents share the turn) is required.
The full query plan below is ready to run verbatim.

## Queries attempted this round (6) — ALL REFUSED, NOT EXECUTED

1. Kuah Perl 1988 "Optimization of feeder bus routes and bus-stop spacing" Transportation Research Part B (standard) — REFUSED
2. Daganzo 2010 "Structure of competitive transit networks" Transportation Research Part B (standard) — REFUSED
3. Ouyang Nourbakhsh Cassidy 2014 "Continuum approximation approach to bus network design under spatially heterogeneous demand" (standard) — REFUSED
4. Nourbakhsh Ouyang 2012 "A structured flexible transit system for low demand areas" Transportation Research Part B (standard) — REFUSED
5. Quadrifoglio Li 2009 "critical demand density" feeder transit Transportation Research Part B (standard) — REFUSED
6. Li Quadrifoglio 2010 "Feeder transit services: choosing between fixed and demand responsive policy" Transportation Research Part C (standard) — REFUSED

## Query plan for round 3 (not yet run; 40 queries, ordered by priority)

Named seed papers (facet brief)
7.  Chen Nie 2017 "Connecting e-hailing to mass transit platform" "Transportation Research Part B"
8.  Ibarra-Rojas Delgado Giesen Muñoz 2015 "Planning, operation, and control of bus transport systems: A literature review" "Transportation Research Part B"
9.  Pinto Hyland Mahmassani Verbas 2020 "Joint design of multimodal transit networks and shared autonomous mobility fleets" "Transportation Research Part C"
10. Current ReVelle Cohon 1986 "The hierarchical network design problem" "Transportation Science" OR "European Journal of Operational Research" (venue check: brief says TS; confirm)
11. Steiner Irnich 2018 "Schedule-based integrated intercity bus line planning via branch-and-cut" "Transportation Science"
12. Bertsimas Ng Yan 2021 "Data-driven transit network design at scale" "Operations Research"
13. Li Quadrifoglio 2010 feeder transit fixed vs demand responsive "Transportation Research Part C" OR "Transportation Science" (venue check)
14. Quadrifoglio Li 2009 "A methodology to derive the critical demand density for designing and operating feeder transit services" "Transportation Research Part B"

Methodology / problem phrases with venue restrictors
15. feeder bus network design rail station "Transportation Research Part B"
16. trunk feeder transit continuum approximation hub "Transportation Research Part B"
17. timed transfer coordination feeder trunk schedule "Transportation Science"
18. hierarchical transit network design trunk feeder "Transportation Research Part C"
19. "transit network design" frequency setting "Operations Research" INFORMS
20. first-mile last-mile feeder shared autonomous vehicles rail station "Transportation Research Part C"
21. demand responsive connector feeder design analytical "Transportation Research Part B"
22. integrated fixed-route flexible transit Kim Schonfeld "Transportation Research Part B"
23. zonal express bus service design "Transportation Research Part B"
24. park-and-ride location feeder "Transportation Research Part B"
25. Estrada Roca-Riu Badia Robusté Daganzo hybrid transit network design "Transportation Research Part C" 2011
26. Badia Estrada Robusté hub-and-spoke radial transit network design "Transportation Research Part B"
27. Chien Schonfeld joint optimization rail line feeder bus "Transportation Research Part B"
28. Wirasinghe feeder bus rail "Transportation Research Part B"
29. Sivakumaran Li Cassidy Madanat "Cost-saving properties of schedule coordination in a simple trunk-and-feeder transit system" "Transportation Research Part A" (venue check — likely OUT)
30. Fan Machemehl transit network design "Transportation Research Part B" OR "Transportation Science"

Recent (2021-2026)
31. feeder bus network design 2023 "Transportation Research Part C"
32. first-mile feeder autonomous shuttle 2024 "Transportation Research Part B"
33. trunk feeder hierarchical transit network design 2025 "Transportation Research Part C"
34. transit network design large-scale 2024 "Transportation Science"
35. demand responsive feeder transit 2023 "Transportation Research Part B"
36. microtransit feeder rail integration 2025 2026 "Transportation Research Part C"

Classic (pre-2005)
37. "0191-2615" feeder bus routes bus-stop spacing 1988
38. Kuah Perl 1989 "The feeder-bus network-design problem" (expect J. Oper. Res. Soc. — OUT; confirm) 
39. "Transportation Science" 1986 "hierarchical network design problem" Current ReVelle Cohon
40. "Transportation Research Part B" 1990s feeder bus route rail station design

DOI-prefix queries
41. "10.1287/trsc" feeder bus transit network design
42. "10.1016/j.trb" feeder transit continuum approximation
43. "10.1016/j.trc" first-mile feeder autonomous rail
44. "10.1287/opre" transit network design
45. "10.1016/0191-2615" feeder bus
46. "10.1016/S0968-090X" feeder transit

## Cross-referenced in-scope items ALREADY corroborated by sibling facets (NOT new finds — dedupe at merge)

Both sit on this facet's "transfer coordination / hub-arrival synchronization" theme. Evidence URLs are those
the sibling agent (B2-time-windows-periodic-launch-r1) saw in actual search results; this agent did not view
them, hence confidence is capped at medium here.

| # | Title | Authors | Year | Venue | DOI | Evidence URL | Conf. | Origin |
|---|-------|---------|------|-------|-----|--------------|-------|--------|
| X1 | Optimizing Timetable Synchronization for Rail Mass Transit | Wong, Yuen, Fung, Leung | 2008 | Transportation Science 42(1) | 10.1287/trsc.1070.0200 | https://pubsonline.informs.org/doi/10.1287/trsc.1070.0200 | medium (sibling: high) | B2-time-windows-periodic-launch-r1.md row 6 |
| X2 | Synchronization of bus timetabling | Ibarra-Rojas, Rios-Solis | 2012 | Transportation Research Part B 46(5) | (not seen) | https://www.worldtransitresearch.info/research/4228 | medium | B2-time-windows-periodic-launch-r1.md row 10 |

Facet-specific transfer notes for X1/X2:
- X1 (Wong et al. 2008, TS): non-periodic MIP choosing run times, dwell times, headways and dispatch offsets on
  all lines to minimise total transfer waiting time under safety headways; optimisation-based heuristic with
  iterative variable fixing; Hong Kong MTR. Transfer: synchronising feeder-launch arrivals at an orbital hub
  with onward hub departures is the same transfer-synchronisation MIP, with pad / docking separation playing
  the role of headway.
- X2 (Ibarra-Rojas & Rios-Solis 2012, TR-B): 0-1 IP maximising the number of synchronised arrivals at transfer
  nodes while keeping departures in almost-evenly-spaced headway windows; NP-hard; multistart iterated local
  search for Monterrey-scale instances. Transfer: coordinating departures from many spaceports so payloads
  arrive at a hub within common windows, with cadence (headway) windows per pad, is this problem.

Other sibling-corroborated items adjacent to this facet (already recorded elsewhere; NOT repeated):
Kroon, Peeters, Wagenaar & Zuidwijk 2014 TS (PESP flexible connections); Van Lieshout 2021 TS (integrated
periodic timetabling and vehicle circulation); Drexl 2012 TS (synchronisation in VRP survey).

## Newly corroborated in-scope candidates this round (0)

None. See Status above.

## Secondary / adjacent-venue candidates (0)

None.

## Gaps (entire facet remains unsearched after two rounds)

- Classic feeder-bus design: Kuah & Perl (TR-B 1988; JORS 1989), Chien & Schonfeld, Wirasinghe, Chang & Schonfeld.
- Continuum-approximation trunk/feeder design: Daganzo 2010 TR-B; Estrada et al. 2011 TR-C; Nourbakhsh & Ouyang
  2012 TR-B; Ouyang, Nourbakhsh & Cassidy 2014 TR-B; Badia et al.; Sivakumaran et al. (venue check).
- Fixed vs demand-responsive feeder policy: Quadrifoglio & Li 2009 TR-B; Li & Quadrifoglio 2010 (venue check);
  Kim & Schonfeld TR-B; Chen & Nie 2017 TR-B.
- Reviews: Ibarra-Rojas, Delgado, Giesen & Muñoz 2015 TR-B.
- First/last-mile with SAVs: Pinto, Hyland, Mahmassani & Verbas 2020 TR-C and 2021-2026 TR-C follow-ups.
- OR / TS transit network design: Current, ReVelle & Cohon 1986 (venue check); Steiner & Irnich 2018 TS;
  Bertsimas, Ng & Yan 2021 OR.
- Methodological transfer note for the writer (independent of any citation): the facet's three co-optimised
  levers — feeder frequency (-> launch cadence), stop/route spacing and catchment (-> spaceport catchment and
  number of active pads), and transfer coordination at the trunk station (-> hub-arrival synchronisation under
  orbital-phasing windows) — are exactly the quantities a spaceport-to-orbit feeder model must jointly set, and
  continuum-approximation models give closed-form first-cut sizing while synchronisation IPs give the exact
  timetable layer.
