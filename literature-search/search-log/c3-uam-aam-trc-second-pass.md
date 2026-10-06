# c3-uam-aam-trc-second-pass — notes (Topic A, facet: UAM/AAM/RAM operations in TR-C/TR-B/TS/OR, second pass)

Quota: 28 WebSearch calls. Running count after each query is in brackets.

## Queries

1. [1] `"10.1016/j.trc" "urban air mobility"` — poor: TR-A/TR-E/arXiv hits only. No in-scope URLs.
2. [2] `"10.1016/j.trc" vertiport` — snippet mentions Willey & Salmon TR-C April 2021 (hub location / subgraph isomorphism) but no publisher URL; rest TR-A / JATM / arXiv.
3. [3] `site:sciencedirect.com "Transportation Research Part C" eVTOL` — no sciencedirect results; snippet mentions a TR-B paper on "eVTOL package delivery systems" (no title/URL) and TR-A vertiport location.
4. [4] `"10.1016/j.trc" "air taxi"` — snippet (citing reference lists) gives: Garrow, German, Leonard 2021 TR-C 132, DOI 10.1016/j.trc.2021.103377; Haan, Garrow, Marzuoli, Roy, Bierlaire 2021 TR-C DOI 10.1016/j.trc.2021.103392 (air-taxi commuter demand). No publisher URLs -> medium.
5. [5] `"10.1016/j.trc" "unmanned aircraft" traffic management capacity` — no in-scope URLs; snippet mentions Jiang, Geller, Ni, Collura UTM ConOps paper and Bulusu/Sengupta capacity work (venue not corroborated).
6. [6] `"10.1016/j.trc" "advanced air mobility"` — arXiv/UC ITS only.
7. [7] `"10.1016/j.trb" "urban air mobility"` — TRID 1904541 "Passenger-centric Urban Air Mobility: Fairness trade-offs and operational efficiency" (venue not shown); rest TR-A/TR-E/TR-D.
8. [8] `ideas.repec.org transc "urban air mobility"` — only TR-A/TR-E/JATM/ITS Berkeley working papers on IDEAS. No transc hits.

Lesson: quoting the DOI prefix does not work with this engine. Switching to allowed_domains restriction (sciencedirect.com / ideas.repec.org / pubsonline.informs.org).

9. [9] allowed_domains=sciencedirect.com `"urban air mobility" "Transportation Research Part C: Emerging Technologies"` — HIT: S0968090X21003788 Garrow/German/Leonard 2021 review. Rest TR-E (S1366554525003576, UAM network design in urban agglomeration, out of scope), TR-A, JATM.
10. [10] allowed_domains=ideas.repec.org,econpapers `urban air mobility eVTOL vertiport` — only transa / transe / jaitra / ormsom / Springer chapter hits (TR-E 2026 S1366554525005769 rolling-horizon UAM w/ shared riding, vertiport-airspace capacity, recharge — out of scope; MSOM 2022 vertiport planning — out of scope).
11. [11] sciencedirect `vertiport eVTOL scheduling capacity Transportation Research Part C` — HIT: S0968090X21003843 Shao/Shao/Lu 2021 terminal area control rules + eVTOL adaptive scheduling. Others TR-E (S1366554526002425 vertiport siting MILP 2026), TR-A, Journal of the Air Transport Research Society (vertiport airside capacity DES).
12. [12] sciencedirect `unmanned aircraft drone traffic management low-altitude airspace capacity Transportation Research Part C` — HIT: S0968090X22002339 "Traffic management and resource allocation for UAV-based parcel delivery in low-altitude urban space" (TR-C Oct 2022). Rest arXiv / TR-A.
13. [13] ideas/econpapers `"air taxi" network vertiport Transportation Research Part C` — snippets mention TR-C 131 (2021) "Identification and prediction of urban airspace availability for emerging air mobility operations" and TR-C 132 (2021) commuter air-taxi 40-city study (Haan et al.) — no URLs (medium). IJOC 2022 scalable vertiport hub location (out of scope).
14. [14] sciencedirect `electric aircraft regional air mobility charging network scheduling Transportation Research Part C` — HITS: S0968090X22000158 "Integrated fleet assignment and scheduling for environmentally friendly electrified regional air mobility" (TR-C 2022; Justin/Payan/Mavris per brief); S0968090X23003029 "Optimizing the battery charging and swapping infrastructure for electric short-haul aircraft—The case of electric flight in Norway" (TR-C 2023).
15. [15] ideas/econpapers `unmanned aerial vehicle airspace traffic flow management corridor transc` — patents/arXiv only. Nothing.
16. [16] allowed_domains=pubsonline.informs.org `urban air mobility OR eVTOL OR vertiport OR "unmanned aircraft" trsc` — only msom.2022.1148 and ijoc.2021.1109 (out of scope). No TS/OR hits.
17. [17] sciencedirect `Transportation Research Part C urban air mobility 2025 eVTOL fleet operations scheduling optimization` — HIT: S0968090X25001159 "On-demand ridesharing based on dynamic scheduling in urban air mobility" (TR-C 175, 2025). Rest TR-E 2025/2026 (S1366554526000980 UAM site selection + route operation; S1366554525003576; S1366554525005769; S1366554526002425) — out of scope.
18. [18] sciencedirect `"air taxi" Transportation Research Part C strategic network infrastructure locations Rajendran` — Rajendran & Zack 2019 is TR-E (S1366554519300407) -> OUT of scope; removed from wanted list.
19. [19] sciencedirect `Transportation Research Part C unmanned aircraft system traffic management strategic deconfliction flight planning` — HITS: S0968090X24000688 "Chance-constrained UAM traffic flow optimization with fast disruption recovery under uncertain waypoint occupancy time" (TR-C 2024); S0968090X25002803 "Conflict probability based strategic conflict resolution for UAS traffic management considering Reasonable-Time-To-Act principle" (TR-C 2025). TR-E 2025 S1366554525003679 collaborative UAM traffic flow optimization (out of scope).
20. [20] sciencedirect `Transportation Research Part C drone urban airspace capacity layered airspace conflict traffic density` — snippet: "Capacity of a constrained urban airspace: Influencing factors, analytical modelling and simulations", TR-C 2023 (no URL -> medium). JATM traffic-density paper (out).
21. [21] sciencedirect `Transportation Research Part C urban air mobility demand capacity vertiport ridesharing pooling passengers` — JATM reviews, arXiv only; snippet mentions "hierarchical vertiport network design for on-demand multi-modal UAM" (venue not shown).
22. [22] ideas.repec.org `"Emerging Technologies" eVTOL OR "urban air mobility" OR "air taxi" OR "unmanned aircraft"` — nothing in scope (Sustainability, JATM).
23. [23] sciencedirect `"Transportation Research Part B" eVTOL OR "urban air mobility" OR drone airspace network design` — no TR-B hits; TR-E, Control Eng. Practice, TR Interdisciplinary Perspectives. Snippet mentions "Designing airspace for urban air mobility: a review of concepts and approaches" (venue not shown).
24. [24] sciencedirect `Transportation Research Part C air traffic assignment urban air mobility complexity congestion Delahaye OR Mahmassani` — HITS: S0968090X23002681 Wang/Delahaye/Farges/Alam 2023 (TR-C 154, 104279); S0968090X22002054 Wang/Delahaye/Farges/Alam 2022 (TR-C 142, 103776); S0968090X25004814 "Real-time traffic simulation and management for large-scale urban air mobility: Integrating route guidance and collision avoidance" (TR-C 2025). Snippet: Cummings & Mahmassani 2024 "Airspace congestion, flow relations, and 4-d fundamental diagrams for advanced urban air mobility", TR-C 159, 104467 (no URL -> medium). TR-E 2024 S1366554524004502 air-corridor planning (out of scope).
25. [25] sciencedirect `Transportation Research Part C 2026 urban air mobility OR eVTOL OR vertiport OR "unmanned aircraft" optimization` — only repeats + TR-A 2026 S0965856426000984 (vertiport location under demand uncertainty, out of scope).
26. [26] pubsonline `"Transportation Science" unmanned aerial vehicles OR drones Levin Rey branch-and-price urban airspace` — HIT: 10.1287/trsc.2022.1175 Levin & Rey 2023. Also TS drone-routing papers trsc.2017.0791, trsc.2020.1017, trsc.2019.0944 (TSP-with-drone / drone resupply — not relevant to either topic; not recorded).
27. [27] sciencedirect `"Transportation Research Part B" electric aircraft subsidized air transport networks Kinene Birolini` — HIT: S0191261524001899 Kinene & Birolini 2024 TR-B 190 (time-space-energy network + fleet planning). By-catch: S0968090X22004107 TR-C 2022 space–time–energy flow IP for regional SAEV system + charging network. EJOR 2023 electric aircraft charging network design (out of scope).
28. [28] sciencedirect `Transportation Research Part C urban air mobility automated flight planning trajectory high-density 2021 Tang Bulusu Sengupta` — HITS: S0968090X21003302 Tang/Zhang/Mohmoodian/Charkhgard 2021 (TR-C 131, 103324); S0968090X26003797 "Pre-planned air routes or dynamic 4D trajectories? A comparative study of UTM ConOps" (TR-C 2026). TR-E 2022 S1366554522002526 route network planning for urban air delivery (out of scope).

QUOTA REACHED (28/28). Searching stopped.

## Candidates recorded (see JSON)

High (publisher URL seen):
- H1 Garrow, German, Leonard 2021 TR-C — UAM comprehensive review — https://www.sciencedirect.com/science/article/pii/S0968090X21003788 (DOI 10.1016/j.trc.2021.103377 from snippet)
- H2 Shao, Shao, Lu 2021 TR-C — Terminal area control rules and eVTOL adaptive scheduling model for multi-vertiport system — https://www.sciencedirect.com/science/article/abs/pii/S0968090X21003843
- H3 Tang, Zhang, Mohmoodian, Charkhgard 2021 TR-C 131:103324 — Automated flight planning of high-density UAM — https://www.sciencedirect.com/science/article/pii/S0968090X21003302
- H4 Wang, Delahaye, Farges, Alam 2022 TR-C 142:103776 — Complexity optimal air traffic assignment in multi-layer transport network for UAM — https://www.sciencedirect.com/science/article/abs/pii/S0968090X22002054
- H5 Wang, Delahaye, Farges, Alam 2023 TR-C 154:104279 — Quasi-dynamic air traffic assignment model ... high-density UAM — https://www.sciencedirect.com/science/article/abs/pii/S0968090X23002681
- H6 (authors not shown) 2022 TR-C — Traffic management and resource allocation for UAV-based parcel delivery in low-altitude urban space — https://www.sciencedirect.com/science/article/pii/S0968090X22002339
- H7 (authors not shown) 2024 TR-C — Chance-constrained UAM traffic flow optimization with fast disruption recovery under uncertain waypoint occupancy time — https://www.sciencedirect.com/science/article/abs/pii/S0968090X24000688
- H8 (authors not shown) 2025 TR-C — Conflict probability based strategic conflict resolution for UAS traffic management considering Reasonable-Time-To-Act principle — https://www.sciencedirect.com/science/article/abs/pii/S0968090X25002803
- H9 (authors not shown) 2025 TR-C 175 — On-demand ridesharing based on dynamic scheduling in urban air mobility — https://www.sciencedirect.com/science/article/pii/S0968090X25001159
- H10 (authors not shown) 2025 TR-C — Real-time traffic simulation and management for large-scale UAM: integrating route guidance and collision avoidance — https://www.sciencedirect.com/science/article/abs/pii/S0968090X25004814
- H11 (authors not shown) 2026 TR-C — Pre-planned air routes or dynamic 4D trajectories? A comparative study of UTM ConOps — https://www.sciencedirect.com/science/article/pii/S0968090X26003797
- H12 Justin, Payan, Mavris (per brief) 2022 TR-C — Integrated fleet assignment and scheduling for environmentally friendly electrified regional air mobility — https://www.sciencedirect.com/science/article/abs/pii/S0968090X22000158
- H13 (authors not shown) 2023 TR-C — Optimizing the battery charging and swapping infrastructure for electric short-haul aircraft—The case of electric flight in Norway — https://www.sciencedirect.com/science/article/pii/S0968090X23003029
- H14 (authors not shown) 2022 TR-C — Space–time-energy flow-based IP model to design and operate a regional SAEV system and charging network (by-catch) — https://www.sciencedirect.com/science/article/pii/S0968090X22004107
- H15 Kinene, Birolini 2024 TR-B 190 — Optimization of subsidized air transport networks using electric aircraft — https://www.sciencedirect.com/science/article/pii/S0191261524001899
- H16 Levin, Rey 2023 TS 57(4) — Branch-and-Price for Drone Delivery Service Planning in Urban Airspace — https://pubsonline.informs.org/doi/10.1287/trsc.2022.1175

Medium (venue in snippet, no publisher URL):
- M1 Haan, Garrow, Marzuoli, Roy, Bierlaire 2021 TR-C 132 — commuter air-taxi 40-US-city study — DOI 10.1016/j.trc.2021.103392 (snippet); exact title not displayed.
- M2 Cummings, Mahmassani 2024 TR-C 159:104467 — Airspace congestion, flow relations, and 4-d fundamental diagrams for advanced urban air mobility.
- M3 (authors not shown) 2023 TR-C — Capacity of a constrained urban airspace: Influencing factors, analytical modelling and simulations.
- M4 (authors not shown) 2021 TR-C 131 — Identification and prediction of urban airspace availability for emerging air mobility operations.
- M5 Willey, Salmon 2021 TR-C — A method for urban air mobility network design using hub location and subgraph isomorphism.

Out-of-scope items seen (for the record, NOT recorded): Rajendran & Zack 2019 (TR-E); UAM network design in urban agglomeration (TR-E 2025); rolling-horizon UAM w/ shared riding & recharge (TR-E 2026); vertiport siting MILP (TR-E 2026); UAM site selection & route operation (TR-E 2026); air corridor planning for urban drone delivery (TR-E 2024); collaborative UAM traffic flow optimization w/ mission preferences (TR-E 2025); route network planning for urban air delivery (TR-E 2022); vertiport planning adaptive discretization (MSOM 2022); scalable vertiport hub location (IJOC 2022); vertiport location under demand uncertainty (TR-A 2026); vertiport location Beijing (TR-A 2025); electric aircraft charging network design kernel search (EJOR 2023); TS TSP-with-drone papers (not topical).

Note: medium-confidence entries have url="" in the JSON because the venue evidence came only from the engine's snippet text (query number given in method_summary), not from a specific result URL.

Totals: 28/28 searches; 21 candidates (16 high, 5 medium); 9 wanted_not_seen.
