# Facet A1: equity-cdm-slots — Equity, fairness, CDM, slot allocation and market mechanisms in ATFM / airport demand management (round 1)

Date: 2026-10-06. Agent: facet equity-cdm-slots. Venues in scope: Operations Research, Transportation Science, TR Part B, TR Part C.

## STATUS: NO WEB SEARCHES COULD BE EXECUTED THIS ROUND

WebSearch is the only route to the internet in this environment. The per-turn WebSearch budget
(200 calls, shared by every agent in the turn) was already exhausted by sibling agents before this
agent's first batch of eight queries ran; all eight were refused with "web search budget is used up".
No workaround was attempted (curl/wget/proxies are blocked and forbidden).

Fallback used instead of searching (local reads only, no internet):
- Repository /home/user/kamng0222.github.io: no bibliography/.bib files and no hits for
  "10.1287/trsc", "10.1287/opre", "10.1016/j.trb", "10.1016/j.trc", "ground delay", "slot allocation",
  "ration-by", "collaborative decision".
- Sibling round-1 notes in this folder (A1-deterministic-atfm-r1.md, A1-stochastic-robust-atfm-r1.md,
  A1-large-scale-solution-methods-r1.md, A2-airport-runway-terminal-r1.md, A2-uam-aam-ram-r1.md,
  B2-time-windows-periodic-launch-r1.md). Those agents DID execute WebSearch queries for several papers that
  belong to this facet (their queries 17-20, 37-38, 42-47 in A1-deterministic; 9-15, 30-31 in A1-stochastic;
  17 in A2-airport; 25-26 in B2-time-windows) and recorded the publisher/DOI/index URL they saw.

RULE APPLIED: a paper is recorded below ONLY if a sibling agent's executed search result corroborated title +
venue (publisher page, DOI shown in URL/snippet, or reputable index such as IDEAS/RePEc, IAOR, institutional
repository). Nothing is recorded from memory. Because this agent did not itself see any result page, every
confidence level is capped at "medium" (publisher/DOI page seen by sibling) or set to "low" (sibling saw only a
repository/index page without DOI). The downstream verifier should re-check every DOI.

Coverage: 22 candidates recorded against a target of 25-45. Missing entirely (no corroboration anywhere in the
sibling notes): Jacquillat & Vaze inter-airline equity (TS 2018), Vaze & Barnhart frequency competition (TS 2012),
Fairbrother-Zografos-Glazebrook slot mechanism (TS 2020), Zografos & Jiang / Jiang & Zografos fairness models
(TR-C 2019/2021), Katsigiannis et al. (TR-C 2021/2023), Ribeiro-Jacquillat-Antunes LNS (TS 2019), Benlic (TR-C 2018),
Swaroop-Zou-Ball-Hansen slot controls (TR-B 2012), the TR-B 2010 airport congestion-pricing issue (Basso & Zhang,
Czerny, Verhoef, Sieg, Fukui), Bertsimas-Farias-Trichakis price of fairness (OR 2011), Bard & Mohan slot
reallocation (TR-B 2008), Manley & Sherry GDP equity (TR-C 2010), Evans-Vaze-Barnhart (TS 2016), Kim & Hansen
collaborative en-route allocation (TR-C 2013), Castelli-Labbé-Violin airspace pricing (TR-C 2013), Montlaur &
Delgado (TR-C 2017), Wang & Jacquillat (OR 2020), and all 2021-2026 fairness/UAM-equity items. A ROUND 2 IS
REQUIRED; the query plan is below.

## Queries submitted this round — all REFUSED (budget exhausted), none executed
1. Vossen Ball "Slot trading opportunities in collaborative ground delay programs" Transportation Science
2. Ball Hoffman Mukherjee "Ground delay program planning under uncertainty based on the ration-by-distance principle"
3. Barnhart Bertsimas Caramanis Fearing "Equitable and efficient coordination in traffic flow management"
4. Bertsimas Gupta "Fairness and collaboration in network air traffic flow management" Transportation Science
5. Jacquillat Vaze "Interairline equity in airport scheduling interventions" Transportation Science
6. Jacquillat Odoni "An integrated scheduling and operations approach to airport congestion mitigation" Operations Research
7. Kotnyek Richetta "Equitable models for the stochastic ground-holding problem under collaborative decision making"
8. Pyrgiotis Odoni "On the impact of scheduling limits" Newark Transportation Science

## Round-2 query plan (prepared, NOT executed; ~45 queries in the mix the task asks for)
(a)/(c) seminal and author queries
9.  Vaze Barnhart "Modeling airline frequency competition for airport congestion mitigation" Transportation Science
10. Ribeiro Jacquillat Antunes "large-scale neighborhood search" airport slot allocation Transportation Science 2019
11. Zografos Jiang "bi-objective efficiency-fairness model" slots congested airports Transportation Research Part C
12. Jiang Zografos "fairness in allocating slots" capacity-constrained airports Transportation Research Part C 2021
13. Katsigiannis Zografos Fairbrother "airport slot-scheduling problem" multi-objective multi-level Transportation Research Part C
14. Fairbrother Zografos Glazebrook "slot-scheduling mechanism at congested airports" efficiency fairness airline preferences Transportation Science
15. Manley Sherry "Analysis of performance and equity in ground delay programs" Transportation Research Part C
16. Benlic "heuristic search for allocation of slots at network level" Transportation Research Part C
17. Swaroop Zou Ball Hansen "Do more US airports need slot controls" Transportation Research Part B
18. Bard Mohan "Reallocating arrival slots during a ground delay program" Transportation Research Part B
19. Evans Vaze Barnhart "airline-driven performance-based air traffic management" game theoretic Transportation Science
20. Kim Hansen "collaborative en route resource allocation" Transportation Research Part C
21. Montlaur Delgado "flight and passenger delay assignment optimization strategies" Transportation Research Part C
22. Wang Jacquillat "stochastic integer programming approach to air traffic scheduling and operations" Operations Research
23. Bertsimas Farias Trichakis "The price of fairness" Operations Research
24. Jacquillat Odoni "endogenous control of service rates" queuing airport congestion Transportation Research Part C
25. Mukherjee Hansen "dynamic stochastic model for the single airport ground holding problem" Transportation Science (CDM slot framing)
(congestion pricing / auctions)
26. Basso Zhang "Pricing vs. slot policies when airport profits matter" Transportation Research Part B
27. Czerny "Airport congestion management under uncertainty" Transportation Research Part B 2010
28. Verhoef "Congestion pricing, slot sales and slot trading in aviation" Transportation Research Part B
29. Sieg "Grandfather rights in the market for airport slots" Transportation Research Part B
30. Fukui "empirical analysis of airport slot trading" Transportation Research Part B
31. airport slot auction combinatorial "Transportation Research Part B" OR "Transportation Science"
32. Castelli Labbé Violin network pricing air navigation service providers Transportation Research Part C
(venue / DOI-prefix sweeps, 2021-2026)
33. "10.1287/trsc" ground delay program equity 2023 OR 2024 OR 2025
34. air traffic flow management fairness equity optimization "Transportation Research Part C" 2024
35. airport slot allocation fairness 2025 "Transportation Research Part B" OR "Transportation Science"
36. collaborative decision making ATFM slot swapping optimization 2023 2024 "10.1016/j.trc"
37. Katsigiannis Zografos "multi-objective airport slot scheduling" operational delays multi-stakeholder 2023 Transportation Research Part C
38. urban air mobility fairness equitable scheduling vertiport "Transportation Research Part C" 2024 2025
39. UDPP user driven prioritisation process ATFM optimization "Transportation Research Part C"
40. "collaborative trajectory options program" CTOP optimization "Transportation Research Part C" OR "Transportation Science"
41. Keskin Zografos "network-wide adjustments of initial airport slot allocations" doi 10.1016/j.trb 2023
42. "10.1287/opre" airport demand management slot 2022 2023 2024
(classic pre-2005)
43. Ball Hoffman Odoni Rifkin "stochastic integer program with dual network structure" ground-holding Operations Research 2003 (CDM/RBS basis)
44. Hoffman Ball "single-airport ground-holding problem with banking constraints" Operations Research 2000
45. Richetta Odoni "static ground-holding policy problem" Transportation Science 1993
46. Sherali Smith Trani "airspace planning model" equity "Transportation Science" 2002
47. Andreatta Romanin-Jacur "Aircraft flow management under congestion" Transportation Science 1987

## Candidates recorded (22) — all corroborated by a SIBLING agent's executed search; provenance in last column
| # | Title | Authors | Year | Venue | DOI (as seen by sibling) | URL seen by sibling | Conf. | Sibling file |
|---|---|---|---|---|---|---|---|---|
| 1 | Slot Trading Opportunities in Collaborative Ground Delay Programs | Vossen, Ball | 2006 | Transportation Science 40(1) 29-43 | 10.1287/trsc.1050.0121 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.1050.0121 | medium | A1-deterministic q19 |
| 2 | Ground Delay Program Planning Under Uncertainty Based on the Ration-by-Distance Principle | Ball, Hoffman, Mukherjee | 2010 | Transportation Science 44(1) 1-14 | 10.1287/trsc.1090.0289 | https://pubsonline.informs.org/doi/epdf/10.1287/trsc.1090.0289 | medium | A1-deterministic q20; A1-stochastic q9 |
| 3 | Equitable and Efficient Coordination in Traffic Flow Management | Barnhart, Bertsimas, Caramanis, Fearing | 2012 | Transportation Science 46(2) 262-280 | 10.1287/trsc.1110.0393 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.1110.0393 | medium | A1-deterministic q18 |
| 4 | Fairness and Collaboration in Network Air Traffic Flow Management: An Optimization Approach | Bertsimas, Gupta | 2016 | Transportation Science 50(1) 57-76 | 10.1287/trsc.2014.0567 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2014.0567 | medium | A1-deterministic q17 |
| 5 | Equitable Models for the Stochastic Ground-Holding Problem Under Collaborative Decision Making | Kotnyek, Richetta | 2006 | Transportation Science 40(2) 133-146 | 10.1287/trsc.1050.0129 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.1050.0129 | medium | A1-deterministic q37; A1-stochastic |
| 6 | Equity and Strength in Stochastic Integer Programming Models for the Dynamic Single Airport Ground-Holding Problem | Estes, Ball | 2020 | Transportation Science 54(4) 944-955 | 10.1287/trsc.2020.0975 | https://pubsonline.informs.org/doi/pdf/10.1287/trsc.2020.0975 | medium | A1-stochastic q10 |
| 7 | Stochastic optimization models for ground delay program planning with equity-efficiency tradeoffs | Glover, Ball | 2013 | Transportation Research Part C 33 196-202 | (not seen) | https://www.sciencedirect.com/science/article/abs/pii/S0968090X11001653 | medium | A1-stochastic q12/13/21/30 |
| 8 | Ground delay program planning: Delay, equity, and computational complexity | Kuhn | 2013 | Transportation Research Part C 35 193-203 | 10.1016/j.trc.2013.07.008 | https://www.sciencedirect.com/science/article/abs/pii/S0968090X13001617 | medium | A1-stochastic q14/31 |
| 9 | The design of a market mechanism to allocate Air Traffic Flow Management slots | Castelli, Pesenti, Ranieri | 2011 | Transportation Research Part C 19(5) 931-943 | (not seen) | https://iaorifors.com/paper/72955 | low | A1-deterministic q38 |
| 10 | The time slot allocation problem under uncertain capacity | Corolli, Lulli, Ntaimo | 2014 | Transportation Research Part C 46 16-29 | 10.1016/j.trc.2014.05.004 | https://boa.unimib.it/handle/10281/56796 | medium | A1-deterministic q42; A1-stochastic q15 |
| 11 | Dealing with the efficient allocation of scarce resources at congested airports | Zografos, Salouras, Madas | 2012 | Transportation Research Part C 21(1) 244-256 | (not seen) | https://eprints.lancs.ac.uk/id/eprint/64630 | low | B2-time-windows q25 |
| 12 | An optimization approach for airport slot allocation under IATA guidelines | Ribeiro, Jacquillat, Antunes, Odoni, Pita | 2018 | Transportation Research Part B 112 132-156 | 10.1016/j.trb.2018.04.005 | https://www.sciencedirect.com/science/article/pii/S0191261517304538 | medium | A1-deterministic q47; A2-airport q17; B2-time-windows q26 |
| 13 | An Integrated Scheduling and Operations Approach to Airport Congestion Mitigation | Jacquillat, Odoni | 2015 | Operations Research 63(6) 1390-1410 | 10.1287/opre.2015.1428 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.2015.1428 | medium | A1-deterministic q16; A2-airport q5 |
| 14 | On the Impact of Scheduling Limits: A Case Study at Newark Liberty International Airport | Pyrgiotis, Odoni | 2016 | Transportation Science 50(1) 150-165 | 10.1287/trsc.2014.0564 | https://pubsonline.informs.org/doi/10.1287/trsc.2014.0564 | medium | A1-deterministic q45 |
| 15 | Predictive and Prescriptive Analytics Toward Passenger-Centric Ground Delay Programs | Jacquillat | 2022 | Transportation Science 56(2) 265-298 | 10.1287/trsc.2021.1081 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2021.1081 | medium | A1-deterministic q44; A1-stochastic q46 |
| 16 | Optimal network-wide adjustments of initial airport slot allocations with connectivity and fairness objectives | Keskin, Zografos | 2023 | Transportation Research Part B | (not seen) | https://eprints.whiterose.ac.uk/id/eprint/205144/ | low | A2-airport q17 |
| 17 | Incorporating Stakeholders' priorities and preferences in 4D trajectory optimization | Dal Sasso, Djeumou Fomeni, Lulli, Zografos | 2018 | Transportation Research Part B 117 594-609 | 10.1016/j.trb.2018.09.009 | https://ideas.repec.org/a/eee/transb/v117y2018ipap594-609.html | medium | A1-deterministic q27/31 |
| 18 | Synchronised demand-capacity balancing in collaborative air traffic flow management | Xu, Prats, Delahaye | 2020 | Transportation Research Part C 114 359-376 | 10.1016/j.trc.2020.02.007 | https://hal-enac.archives-ouvertes.fr/hal-02508893 | medium | A1-deterministic q28/32 |
| 19 | An Airspace Planning Model for Selecting Flight-plans Under Workload, Safety, and Equity Considerations | Sherali, Smith, Trani | 2002 | Transportation Science 36(4) 378-397 | 10.1287/trsc.36.4.378.546 | https://pubsonline.informs.org/doi/pdf/10.1287/trsc.36.4.378.546 | medium | A1-deterministic q14/33 |
| 20 | An Airspace Planning and Collaborative Decision-Making Model: Part I—Probabilistic Conflicts, Workload, and Equity Considerations | Sherali, Staats, Trani | 2003 | Transportation Science 37(4) 434-456 | 10.1287/trsc.37.4.434.23272 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.37.4.434.23272 | medium | A1-deterministic q33 |
| 21 | An Airspace-Planning and Collaborative Decision-Making Model: Part II—Cost Model, Data Considerations, and Computations | Sherali, Staats, Trani | 2006 | Transportation Science 40(2) 147-164 | 10.1287/trsc.1050.0141 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.1050.0141 | medium | A1-deterministic q22 |
| 22 | The European Air Traffic Flow Management Problem | Lulli, Odoni | 2007 | Transportation Science 41(4) 431-443 | 10.1287/trsc.1070.0214 | https://pubsonline.informs.org/doi/10.1287/trsc.1070.0214 | medium | A1-deterministic q6 |

Notes on inclusion decisions
- #22 Lulli & Odoni is primarily a deterministic network model (owned by the deterministic facet) but is listed here
  because its equity analysis (optimal total-delay solutions assign delay inequitably; equity terms added) is a
  standard reference point for the network-fairness lineage (#3, #4).
- #13, #14 are scheduling-level demand management (airport caps / schedule displacement) which the facet
  definition includes; #17, #18 are TBO/collaborative DCB models with explicit airspace-user preference or
  equity terms; #19-21 are the Sherali CDM/equity airspace-planning models (inter-airline equity in flight-plan
  selection) and are marked relevance "both" because the 2002 model is motivated by SUA closures for space launches.
- Hamdan et al. (2022, TS, 10.1287/trsc.2021.1087) and De Giovanni-Lancia-Lulli (2024, TS) were corroborated by
  siblings but are NOT claimed for this facet: the snippets did not show a fairness/CDM component.
- Liu & Hansen (2016, TS, predictability in GDP cost optimization) corroborated by A1-stochastic; GDP planning
  but no equity/CDM component shown -> left to that facet.

## Method summaries and transfer to the RAM flow problem (for the writer)
- RBS / compression / slot trading (#1, #2, #5, #6, #7, #8, #15): the CDM machinery is a flight-to-slot assignment
  on a single-resource time line (arrival slots at one airport). RBS = proportional (schedule-order) allocation;
  compression / mediated bartering = assignment or network-flow IP that re-optimises within airline-declared
  substitutions; equity is measured as deviation from the RBS order or from each airline's RBS share. For RAM the
  same structure applies to departure/arrival slots and charger slots at small regional airports or vertiports;
  multiple operators (scheduled + on-demand) make the mediated-exchange and ration-by-distance ideas directly
  reusable (short electric legs can absorb late information; long legs get priority).
- Network fairness (#3, #4, #22): fairness metric embedded in the Bertsimas-Stock Patterson 0-1 IP on a time-expanded
  sector/airport network (reversals/overtaking penalties, time-order deviation); #4 adds an airline-collaboration
  stage. A RAM flow model that assigns departure times and holds on a time-expanded network can import these
  constraints verbatim, replacing sectors by corridor/airspace-block capacities.
- Inter-airline equity in rerouting / flight-plan selection (#19-21, #17, #18): 0-1 IP choosing one trajectory per
  flight with per-operator relative-cost bounds or priority weights; transfers to multi-operator RAM route choice
  under weather or launch-related airspace closures.
- Slot allocation and scheduling-level demand management (#10, #11, #12, #13, #14, #16): IP minimising schedule
  displacement under declared capacity on rolling windows, with IATA priority classes (lexicographic), series-of-slots
  regularity, network connectivity and inter-airline fairness; #10 adds two-stage stochastic recourse for capacity;
  #13/#14 couple the displacement IP with stochastic queuing models to size the caps. For RAM this is the strategic
  layer (seasonal schedule coordination at capacity-constrained regional airports / vertiports) ahead of the tactical
  flow problem; for the spaceport feeder problem it is the closest analog to allocating scarce launch windows / pad
  slots among competing users under declared capacity (noted also by the B2-time-windows sibling).
- Market mechanisms (#9): credit-based combinatorial exchange of ATFM slots solved as an IP with budget-balance;
  template for pricing or trading charger/slot capacity among RAM operators.

## Leads FROM MEMORY ONLY — NOT corroborated, NOT recorded (targets for the round-2 queries above)
Jacquillat & Vaze (2018) TS 52(4) interairline equity in airport scheduling interventions; Vaze & Barnhart (2012) TS 46(4)
frequency competition; Ribeiro, Jacquillat & Antunes (2019) TS 53(6) LNS slot allocation; Fairbrother, Zografos &
Glazebrook (2020) TS 54(1) slot-scheduling mechanism; Zografos & Jiang (2019) TR-C 102 bi-objective efficiency-fairness;
Jiang & Zografos (2021) TR-C 126 fairness framework; Katsigiannis, Zografos & Fairbrother (2021) TR-C 124; Katsigiannis &
Zografos (2023) TR-C; Benlic (2018) TR-C 86 network-level slots; Swaroop, Zou, Ball & Hansen (2012) TR-B 46(9) slot
controls; Basso & Zhang (2010), Czerny (2010), Verhoef (2010), Sieg (2010), Fukui (2010) TR-B 44 airport congestion
pricing/slots; Bertsimas, Farias & Trichakis (2011) OR 59(1) price of fairness; Bard & Mohan (2008) TR-B 42(2) slot
reallocation in GDP; Manley & Sherry (2010) TR-C 18 GDP equity; Evans, Vaze & Barnhart (2016) TS 50(1) airline-driven
PBATM; Kim & Hansen (2013) TR-C 33 collaborative en-route allocation; Castelli, Labbé & Violin (2013) TR-C 33 ANSP network
pricing; Montlaur & Delgado (2017) TR-C 81 flight/passenger delay assignment; Wang & Jacquillat (2020) OR 68(5) stochastic
IP for air traffic scheduling and operations; Mukherjee & Hansen (2007) TS 41(4) dynamic stochastic GHP (CDM slot framing).
Venues/years above are hypotheses to be checked; several equity/slot papers by these authors are in TR-A, TR-E, EJOR or
J. Air Transport Management (out of scope) and must not be assumed in scope.

## Gaps
- Zero own searches executed; 22 of 25-45 target candidates, all second-hand corroborated, none at "high" confidence.
- No 2021-2026 fairness/slot-market work beyond Jacquillat 2022 (TS) and Keskin & Zografos 2023 (TR-B, DOI not seen).
- No congestion-pricing / auction paper in TR-B or OR corroborated at all.
- No UAM/RAM-specific equity or slot-market paper corroborated.
- DOIs missing for #7, #9, #11, #16.
