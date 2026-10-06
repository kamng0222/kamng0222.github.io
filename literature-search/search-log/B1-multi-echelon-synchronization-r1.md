# Facet B1 — Multi-echelon distribution, two-echelon LRP/VRP, consolidation and synchronization — round 1 notes

Agent: literature-search subagent (facet multi-echelon-synchronization). Date: 2026-10-06.
Overall topic: Topic B — spaceport-to-orbit feeder network design, OR methodology analogs.
In-scope venues: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## IMPORTANT caveat on coverage — ZERO searches executed

The shared per-turn WebSearch budget (200 calls, shared by every agent in this workflow run) was
already exhausted when this agent started. All six queries submitted in the first batch were refused
by the tool ("Web search was not performed: this turn's web search budget is used up"). No other
internet-reaching tool is available (WebFetch/curl are egress-blocked), and the task forbids
working around the limit, so this facet has NOT been searched in round 1.

Per the task rules (never record a paper from memory alone; never invent a DOI), the candidate list
below contains ONLY two items whose title/venue/URL were corroborated by search results that sibling
agents recorded in this same run (their notes files sit in this directory). Both are flagged with
their provenance and downgraded confidence. Everything else for this facet must wait for a second
round (r2); the full query plan is given below so r2 can start immediately.

Remedy: re-run this facet in a follow-up turn, or raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION.

## Queries submitted and REFUSED (budget exhausted) — 6

1. `Drexl "synchronization in vehicle routing" survey Transportation Science 2012` (standard)
2. `Perboli Tadei Vigo "two-echelon capacitated vehicle routing problem" Transportation Science` (standard)
3. `Cuda Guastaroba Speranza two-echelon routing problems survey` (standard)
4. `Crainic Ricciardi Storchi "two-echelon" city logistics Transportation Science 2009` (standard)
5. `Hemmelmayr Cordeau Crainic adaptive large neighborhood search two-echelon vehicle routing city logistics` (standard)
6. `Breunig Baldacci Hartl Vidal "two-echelon" electric vehicle routing Transportation Science 2019` (standard)

## Query plan for r2 (not yet attempted) — 34 queries

Methodology / problem phrases with venue restrictors
7. `"two-echelon" "location-routing" "Transportation Research Part B"`
8. `"two-echelon vehicle routing" "Transportation Science" exact branch-and-cut`
9. `"two-echelon" "city logistics" "Transportation Research Part C"`
10. `"multi-echelon" distribution network design "Operations Research" INFORMS`
11. `"vehicle routing" "synchronization constraints" "Transportation Science"`
12. `"pickup and delivery" transshipment OR transfers "Transportation Science"`
13. `"pickup and delivery problem with transfers" "Transportation Research Part B"`
14. `"cross-docking" scheduling "Transportation Research Part B" OR "Transportation Science"`
15. `"timed transfer" OR "transfer synchronization" hub "Transportation Research Part B"`
16. `"hub" "consolidation" "time windows" freight "Transportation Science"`
17. `"two-echelon" "time windows" satellites synchronization "Transportation Research Part C"`
18. `"location-routing" "Transportation Science" exact algorithm`
19. `"multimodal" "transfer coordination" OR "timed transfers" hub "Transportation Research Part C"`
Author surnames
20. `Cortes Matamala Rey "pickup and delivery problem with transfers" Transportation Science`
21. `Rais Alvelos Carvalho "pickup and delivery" transshipment "Transportation Research Part B"`
22. `Masson Lehuede Peton "pickup and delivery problem with transfers" adaptive large neighborhood search`
23. `Mitrovic-Minic Laporte "pickup and delivery problem with time windows and transshipment"`
24. `Crainic Perboli Mancini Tadei "two-echelon" satellites "Transportation Research Part C"`
25. `Baldacci Mingozzi Roberti Wolfler Calvo "two-echelon capacitated vehicle routing" exact "Operations Research"`
26. `Contardo Hemmelmayr Crainic "two-echelon location-routing" branch-and-cut`
27. `Dellaert Dashty Saridarq Van Woensel Crainic "two-echelon" "time windows" "Transportation Science"`
28. `Mancini Gansterer two-echelon vehicle routing synchronization "Transportation Research Part C"`
29. `Anderluh Hemmelmayr Nolz "synchronizing vans and cargo bikes" two-echelon city logistics`
DOI-prefix strings
30. `"10.1287/trsc" "two-echelon"`
31. `"10.1016/j.trb" "two-echelon" OR "multi-echelon"`
32. `"10.1016/j.trc" "two-echelon" OR "transfers" "pickup and delivery"`
33. `"10.1287/opre" "location-routing" OR "two-echelon"`
Recent (2021-2026)
34. `"two-echelon" vehicle routing 2023 OR 2024 OR 2025 "Transportation Science"`
35. `"two-echelon" "location-routing" 2024 OR 2025 "Transportation Research Part B"`
36. `"synchronization" routing drones trucks 2022 OR 2023 OR 2024 "Transportation Research Part C"`
37. `"pickup and delivery" transfers 2023 OR 2024 OR 2025 "Transportation Science" exact`
38. `"two-echelon" stochastic OR robust 2023 OR 2024 OR 2025 "Transportation Research Part B"`
39. `"multi-echelon" network design 2024 OR 2025 OR 2026 "Operations Research" INFORMS`
Classics (pre-2005)
40. `Jacobsen Madsen "two-level" location routing newspaper 1980 "European Journal" OR "Transportation Science"`
41. `Laporte Nobert Taillefer "location-routing" "Transportation Science" 1988`
42. `Daganzo "one-to-many" distribution transshipment "Transportation Science" 1980s`
43. `Hall "consolidation" terminal "Transportation Research Part B" 1987`

## Candidates (in-scope venues) — reused from sibling notes, NOT searched by this agent

| # | Title | Authors | Year | Venue | DOI (seen) | URL where seen | Conf. | Provenance |
|---|-------|---------|------|-------|-----------|----------------|-------|------------|
| 1 | Synchronization in Vehicle Routing—A Survey of VRPs with Multiple Synchronization Constraints | Drexl | 2012 | Transportation Science 46(3):297-316 | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v46y2012i3p297-316.html | medium | Row 17 of B2-time-windows-periodic-launch-r1.md (sibling saw it on a RePEc index page). |
| 2 | Reliable Location-Routing Design Under Probabilistic Facility Disruptions | Xie, Ouyang, Wong | 2016 | Transportation Science 50(3):1128-1138 | 10.1287/trsc.2015.0630 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2015.0630 ; https://ideas.repec.org/a/inm/ortrsc/v50y2016i3p1128-1138.html | medium (sibling: high on publisher page; downgraded here because this agent did not see the page itself) | Row 15 of B2-network-design-uncertainty-r1.md. |

Method notes (limited to what the titles/venues support; model details beyond the title are not
corroborated by any snippet seen in this run and are marked as such):
- Drexl 2012 (TS): a survey and classification of VRP variants whose routes are interdependent through
  synchronization constraints (the title states this; the standard taxonomy of task / operation /
  movement / load / resource synchronization is general knowledge, not snippet-corroborated).
  Transfer: the spaceport-to-orbit feeder has launch-vehicle / orbital-hub rendezvous timing
  (operation and movement synchronization), payload transfer between vehicles at hubs (load
  synchronization) and shared hub docking slots (resource synchronization) - exactly the classes
  the survey organises; it also warns that route interdependence breaks standard local search.
- Xie, Ouyang & Wong 2016 (TS): location-routing design where facilities can fail with given
  probabilities and routes must remain reliable. Transfer: orbital hubs/depots that may be
  unavailable (phasing, outage) with spokes re-assigned to surviving hubs.

## Overlap pointers to sibling facets (do not re-record; for the merge/dedup step)
- Zhu, Crainic, Gendreau 2014 OR (scheduled SND, freight rail) and Boland et al. 2017 OR (continuous-time SND)
  are in B1-service-network-design / B2-time-windows notes.
- Ibarra-Rojas & Rios-Solis 2012 TRB and Wong et al. 2008 TS (timetable synchronization) are in B2-time-windows notes.
- Lium, Crainic, Wallace 2009 TS; Hewitt et al. 2019 TRB; Bai et al. 2014 TRB (stochastic SND) are in
  B2-network-design-uncertainty notes.

## Gaps (everything in the facet brief is uncorroborated in r1)
- Two-echelon VRP/LRP core (Perboli-Tadei-Vigo TS 2011; Crainic-Ricciardi-Storchi TS 2009; Baldacci et al. OR 2013;
  Hemmelmayr et al.; Breunig et al. TS 2019; Cuda et al. survey; Contardo et al.; Dellaert et al. TS 2019/2021).
- Pickup-and-delivery with transfers/transshipment (Cortes-Matamala-Rey; Rais-Alvelos-Carvalho; Masson et al.;
  Mitrovic-Minic & Laporte).
- Cross-docking scheduling, timed transfers in hubs, truck-drone synchronization in TR-C, 2021-2026 recent work,
  pre-2005 classics (Laporte-Nobert-Taillefer, Daganzo, Hall).
- No spaceport / space-logistics papers checked for this facet.
