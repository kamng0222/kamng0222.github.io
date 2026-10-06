# Facet A1 — Large-scale solution methods for ATFM and flight-level optimization (round 1)

Date: 2026-10-06. Agent: facet large-scale-solution-methods.

## STATUS AND PROVENANCE (read first)

ZERO WebSearch queries could be executed for this facet. The per-turn WebSearch budget (200 calls, shared by
every agent in the turn) was already exhausted by sibling agents when my first batch of six queries was
submitted; all six were refused ("web search budget is used up"). WebFetch/curl/wget are blocked by the egress
proxy and the harness forbids working around the limit, so no further attempts were made.

Fallback used: the sibling facet notes already in this directory (A1-deterministic-atfm-r1.md,
A1-stochastic-robust-atfm-r1.md, A2-airport-runway-terminal-r1.md) log publisher/DOI/index URLs that THEIR
executed searches returned. For papers that fall squarely in this facet's methodological lens I re-use those
logged sightings as a SECONDARY source. Consequences:
- Every candidate below is corroborated only second-hand (sibling search log), never by a page I saw myself.
  Confidence is therefore capped at "medium" (or "low" where the sibling saw no publisher page / DOI).
- DOIs are copied exactly as logged by the sibling; where the sibling saw none, the DOI is "".
- No paper is recorded from memory alone. Facet-named works that no sibling corroborated (Rios & Ross
  parallel Dantzig-Wolfe; Agustín et al. in-scope versions; column-generation / Benders ATFM papers) are
  listed as gaps, not candidates.
- The added value of this file is the large-scale-methods lens (what is decomposed/aggregated, why the
  relaxation is strong, how it scales) rather than new sightings. The downstream verifier should re-check
  every entry against the publisher page.

## Queries submitted — all REFUSED (budget exhausted), none executed
1. Bertsimas Stock Patterson 2000 "Traffic Flow Management Rerouting Problem" Transportation Science
2. Bertsimas Lulli Odoni 2011 "An Integer Optimization Approach to Large-Scale Air Traffic Flow Management" Operations Research
3. Lulli Odoni 2007 "The European Air Traffic Flow Management Problem" Transportation Science
4. Rios Ross dual decomposition Lagrangian relaxation air traffic flow management parallel
5. Sherali Smith Trani "airspace planning model" Operations Research Lagrangian
6. Agustín Alonso-Ayuso Escudero Pizarro air traffic flow management rerouting Transportation Research Part C

## Round-2 query plan (NOT executed; 32 queries)
(a) methodology phrases
7.  "Lagrangian relaxation" "air traffic flow management" "Transportation Science" OR "Operations Research"
8.  "column generation" OR "branch-and-price" air traffic flow management trajectories "Transportation Science"
9.  "Benders decomposition" air traffic flow management OR ground delay program "Transportation Research Part B" OR "Transportation Research Part C"
10. "facet-defining" OR "convex hull" air traffic flow management integer programming time-indexed
11. aggregate OR Eulerian air traffic flow model disaggregation flights "Transportation Research Part C"
12. rolling horizon air traffic flow management trajectory-based operations "Transportation Research Part C" 2023 2024
13. parallel OR distributed OR decentralized air traffic flow management optimization "Transportation Research Part C" 2024 2025
14. matheuristic flight scheduling OR aircraft sequencing "Transportation Research Part C" 2022 2023
15. time-indexed formulation scheduling Lagrangian relaxation "Operations Research" van den Akker OR Sousa
16. "dynamic programming" exact runway sequencing constrained position shifting "Transportation Science" 2021 2022
(b) problem phrases
17. network air traffic flow management rerouting speed control integer programming 2023 2024 "Transportation Science"
18. demand capacity balancing trajectory options large-scale optimization 2024 2025 "Transportation Research Part C"
19. collaborative trajectory options program optimization "Transportation Research Part C" OR "Transportation Science"
20. flight level assignment OR cruise level allocation conflict optimization "Transportation Research Part C"
(c) authors
21. Rios Ross "Dantzig-Wolfe" traffic flow scheduling (venue check; expected AIAA JACIC, out of scope)
22. Sherali Staats Trani airspace planning collaborative decision making Part II computations
23. Agustín Alonso-Ayuso Escudero Pizarro "Transportation Research Part C" OR "Transportation Science" stochastic ATFM rerouting
24. Lulli Dell'Olmo dynamic programming ATFM "Transportation Research Part B"
25. Balakrishnan Chandran scheduling runway operations dynamic programming "Operations Research" 2010
26. Bertsimas Gupta Lulli "An Integer Optimization Approach to Large-Scale Air Traffic Flow Management" follow-ups 2016 2017 TS
27. Zhu Wei strong formulation stochastic ATFM reroutes journal venue
(d)+(e) venue / DOI-prefix sweeps
28. "10.1287/trsc" air traffic flow management decomposition OR Lagrangian OR heuristic 2021 2022 2023 2024 2025
29. "10.1287/opre" air traffic flow management OR ground holding integer programming 2021 2022 2023 2024 2025 2026
30. "10.1016/j.trb" air traffic flow management OR trajectory optimization integer programming 2021 2022 2023 2024
31. "10.1016/j.trc" air traffic flow management large-scale OR heuristic OR decomposition 2023 2024 2025 2026
32. site:pubsonline.informs.org "ground-holding" OR "ground holding" 1990 1991 1992 1993 1994 1995 (pre-2005 classics)
33. "Transportation Science" air traffic 1987 1993 1998 2000 ground holding algorithms (pre-2005)
34. "Operations Research" INFORMS air traffic control flow management 1993 1994 1998 2000 (pre-2005)
35. Terrab Odoni 1993 heuristics stochastic ground holding "Operations Research" (pre-2005)
36. urban air mobility OR regional air mobility traffic flow management decomposition OR rolling horizon "Transportation Research Part C" 2024 2025 2026
37. eVTOL OR electric aircraft flight scheduling charging constraints time-space network integer programming "Transportation Research Part C" 2025 2026
38. "Transportation Research Part B" 2025 2026 air traffic integer programming capacity rerouting

## Candidates (in-scope venues; ALL second-hand via sibling search logs; confidence <= medium)
Format: title | authors | year | venue | DOI | URL logged by sibling | sibling file | my confidence

1. The Air Traffic Flow Management Problem with Enroute Capacities | Bertsimas, Stock Patterson | 1998 | Operations Research 46(3) 406-422 | 10.1287/opre.46.3.406 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.46.3.406 | A1-det | medium
2. The Traffic Flow Management Rerouting Problem in Air Traffic Control: A Dynamic Network Flow Approach | Bertsimas, Stock Patterson | 2000 | Transportation Science 34(3) 239-255 | 10.1287/trsc.34.3.239.12300 | https://pubsonline.informs.org/doi/references/10.1287/trsc.34.3.239.12300 | A1-det | medium
3. An Integer Optimization Approach to Large-Scale Air Traffic Flow Management | Bertsimas, Lulli, Odoni | 2011 | Operations Research 59(1) 211-227 | 10.1287/opre.1100.0899 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.1100.0899 | A1-det | medium
4. The European Air Traffic Flow Management Problem | Lulli, Odoni | 2007 | Transportation Science 41(4) 431-443 | 10.1287/trsc.1070.0214 | https://pubsonline.informs.org/doi/10.1287/trsc.1070.0214 | A1-det | medium
5. The Multi-Airport Ground-Holding Problem in Air Traffic Control | Vranas, Bertsimas, Odoni | 1994 | Operations Research 42(2) 249-261 | 10.1287/opre.42.2.249 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.42.2.249 | A1-det | medium
6. Dynamic Ground-Holding Policies for a Network of Airports | Vranas, Bertsimas, Odoni | 1994 | Transportation Science 28(4) 275-291 | 10.1287/trsc.28.4.275 | https://pubsonline.informs.org/doi/10.1287/trsc.28.4.275 | A1-det, A1-stoch | medium
7. Optimal Algorithms and a Remarkably Efficient Heuristic for the Ground-Holding Problem in Air Traffic Control | Richetta | 1995 | Operations Research 43(5) 758-770 | 10.1287/opre.43.5.758 | https://pubsonline.informs.org/doi/10.1287/opre.43.5.758 | A1-stoch | medium
8. A Comparison of Formulations for the Single-Airport Ground-Holding Problem with Banking Constraints | Hoffman, Ball | 2000 | Operations Research 48(4) 578-590 | 10.1287/opre.48.4.578.12417 | https://pubsonline.informs.org/doi/pdf/10.1287/opre.48.4.578.12417 | A1-det | medium
9. The Multiple Connections Multi-Airport Ground Holding Problem: Models and Algorithms | Navazio, Romanin-Jacur | 1998 | Transportation Science 32(3) 268-276 | 10.1287/trsc.32.3.268 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.32.3.268 | A1-det | medium
10. A Stochastic Integer Program with Dual Network Structure and Its Application to the Ground-Holding Problem | Ball, Hoffman, Odoni, Rifkin | 2003 | Operations Research 51(1) 167-171 | 10.1287/opre.51.1.167.12795 | https://ideas.repec.org/a/inm/oropre/v51y2003i1p167-171.html | A1-det, A1-stoch | medium
11. A dynamic rerouting model for air traffic flow management | Mukherjee, Hansen | 2009 | Transportation Research Part B 43(1) 159-171 | 10.1016/j.trb.2008.05.011 | https://its.berkeley.edu/publications/dynamic-rerouting-model-air-traffic-flow-management | A1-det | medium
12. An Airspace Planning Model for Selecting Flight-plans Under Workload, Safety, and Equity Considerations | Sherali, Smith, Trani | 2002 | Transportation Science 36(4) 378-397 | 10.1287/trsc.36.4.378.546 | https://pubsonline.informs.org/doi/pdf/10.1287/trsc.36.4.378.546 | A1-det | medium (relevance both: SUA closures for space launches)
13. An Airspace Planning and Collaborative Decision-Making Model: Part I—Probabilistic Conflicts, Workload, and Equity Considerations | Sherali, Staats, Trani | 2003 | Transportation Science 37(4) 434-456 | 10.1287/trsc.37.4.434.23272 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.37.4.434.23272 | A1-det | medium
14. An Airspace-Planning and Collaborative Decision-Making Model: Part II—Cost Model, Data Considerations, and Computations | Sherali, Staats, Trani | 2006 | Transportation Science 40(2) 147-164 | 10.1287/trsc.1050.0141 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.1050.0141 | A1-det | medium
15. Equity and Strength in Stochastic Integer Programming Models for the Dynamic Single Airport Ground-Holding Problem | Estes, Ball | 2020 | Transportation Science 54(4) 944-955 | 10.1287/trsc.2020.0975 | https://pubsonline.informs.org/doi/pdf/10.1287/trsc.2020.0975 | A1-stoch | medium
16. An Integrated Scheduling and Operations Approach to Airport Congestion Mitigation | Jacquillat, Odoni | 2015 | Operations Research 63(6) 1390-1410 | 10.1287/opre.2015.1428 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.2015.1428 | A1-det, A2-airport | medium
17. Algorithms for Scheduling Runway Operations Under Constrained Position Shifting | Balakrishnan, Chandran | 2010 | Operations Research 58(6) 1650-1665 | 10.1287/opre.1100.0869 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.1100.0869 | A1-det, A2-airport | medium
18. Scheduling Aircraft Landings—The Static Case | Beasley, Krishnamoorthy, Sharaiha, Abramson | 2000 | Transportation Science 34(2) 180-197 | 10.1287/trsc.34.2.180.12302 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.34.2.180.12302 | A2-airport | medium
19. Pruning Rules for Optimal Runway Sequencing | De Maere, Atkin, Burke | 2018 | Transportation Science 52(4) 898-916 | "" | https://ideas.repec.org/a/inm/ortrsc/v52y2018i4p898-916.html | A2-airport | low (index page only)
20. Fairness and Collaboration in Network Air Traffic Flow Management: An Optimization Approach | Bertsimas, Gupta | 2016 | Transportation Science 50(1) 57-76 | 10.1287/trsc.2014.0567 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2014.0567 | A1-det | medium
21. Central Authority–Controlled Air Traffic Flow Management: An Optimization Approach | Hamdan, Cheaitou, Jouini, Andersson Granberg, Jemai, Alsyouf, Bettayeb, Josefsson | 2022 | Transportation Science 56(2) 299-321 | 10.1287/trsc.2021.1087 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2021.1087 | A1-det, A1-stoch | medium
22. Data-Driven Optimization for Air Traffic Flow Management with Trajectory Preferences | De Giovanni, Lancia, Lulli | 2024 | Transportation Science 58(2) 540-556 | 10.1287/trsc.2022.0309 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2022.0309 | A1-det | medium
23. Incorporating Stakeholders' priorities and preferences in 4D trajectory optimization | Dal Sasso, Djeumou Fomeni, Lulli, Zografos | 2018 | Transportation Research Part B 117 594-609 | 10.1016/j.trb.2018.09.009 | https://ideas.repec.org/a/eee/transb/v117y2018ipap594-609.html | A1-det | medium
24. Synchronised demand-capacity balancing in collaborative air traffic flow management | Xu, Prats, Delahaye | 2020 | Transportation Research Part C 114 359-376 | 10.1016/j.trc.2020.02.007 | https://hal-enac.archives-ouvertes.fr/hal-02508893 | A1-det | medium
25. Metaheuristics for efficient aircraft scheduling and re-routing at busy terminal control areas | Samà, D'Ariano, Corman, Pacciarelli | 2017 | Transportation Research Part C 80 485-511 (volume/pages from memory, NOT seen) | "" | https://iris.uniroma3.it/handle/11590/313776 | A2-airport | low (repository page; DOI not seen)

## Facet-named or expected works NOT recorded (no sibling sighting, or out-of-scope venue)
- Rios & Ross, massively parallel Dantzig-Wolfe / dual decomposition for traffic flow scheduling — no sighting; believed AIAA JACIC / conference (out of scope). Query 21 planned.
- Agustín, Alonso-Ayuso, Escudero, Pizarro (2012) "On air traffic flow management with rerouting. Part I: Deterministic case" and Part II (stochastic) — sibling A1-det saw only EJOR 219(1) (https://ideas.repec.org/a/eee/ejores/v219y2012i1p156-166.html). EJOR is out of scope and not UAM/spaceport, so not recorded even as adjacent-venue.
- Column-generation / branch-and-price / Benders papers for ATFM in TS/OR/TR-B/TR-C — none sighted by any sibling; queries 7-9 planned.
- Eulerian / aggregate flow models (Menon, Sweriduk, Bilimoria; Sun, Bayen) — expected AIAA / IEEE venues; not searched.
- Khassiba, Bastin, Cafieri, Gendron, Mongeau (2020) TS two-stage stochastic arrival management — sighted by A1-stoch but decomposition method not confirmed in snippets; left to the stochastic facet.
- "An Efficient Algorithm for Solving an Air Traffic Management Model of the National Airspace System" — INFORMS J. Computing 10(4) (out of scope; sighted by A1-det).
- Zhu & Wei "A Strong Formulation for Stochastic Multiple Constrained Resources ATFM with Reroutes" — arXiv only; venue unverified.
- Ng, Ribeiro, Jorge (2024) TR-C terminal airspace scheduling (DOI 10.1016/j.trc.2024.104856, sighted by A2-airport) — solution method not visible in snippets; not claimed for this facet.

## Methodological lens for the writer (what transfers to the RAM flow problem)
- Cumulative time-indexed "by" variables (candidates 1, 3, 4, 20): capacity constraints become differences of cumulative variables; the resulting 0-1 formulation has very strong LP relaxations (many constraints facet-defining; LP often integral), which is why NAS/ECAC-scale instances solve with a commercial MIP solver. A RAM time-space model with airport, sector/corridor and charger capacities can inherit this exactly; charging/turnaround minima are connectivity constraints of the same type.
- Aggregation/disaggregation + Lagrangian relaxation (candidate 2): aggregate flights into O-D/aircraft-type commodities on a dynamic network, solve a Lagrangian relaxation, then disaggregate to flight-level schedules. For RAM with many thin O-D pairs and few aircraft types this is the natural scalability path.
- Rolling-horizon / dynamic re-solve (candidates 6, 11): re-solve as capacity forecasts update; reroute decisions on a scenario tree.
- Formulation strength comparisons and dual-network structure (candidates 8, 10, 15): guidance on which GHP/slot formulations are integral or tight — important when RAM slot allocation at small airports with banking/connection constraints is embedded in the flow model.
- Flight-plan selection models with workload/conflict side constraints (candidates 12-14): one-plan-per-flight assignment IP with model strengthening; explicitly handles special-use-airspace closures from space launches (relevance both).
- Heuristic decomposition between planning and operations (candidate 16), exact DP for sequencing (17-19), and metaheuristics for TMA scheduling (24-25): the tactical layer of RAM (vertiport/regional-airport arrival sequencing) and the strategic layer (network DCB) can be coupled the way Jacquillat & Odoni alternate between an IP and a stochastic queue model.

## Gaps
- Entire facet unsearched first-hand; all candidates second-hand (sibling logs) — verifier must re-check.
- No in-scope column-generation, branch-and-price, Benders or parallel/distributed ATFM paper corroborated.
- 2021-2026 sweeps of OR/TS/TR-B/TR-C for decomposition-based ATFM not run.
- UAM/RAM-specific large-scale methods (rolling-horizon DCB, charging-constrained time-space networks) not run.
