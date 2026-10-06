# Facet A2: Airport, runway and terminal-area operations (OR / TS / TR-B / TR-C)

Round 1 notes. Only WebSearch was available; no page fetches. The per-turn WebSearch budget (shared by all agents)
ran out after 24 completed queries, so 6 planned queries were refused and the sweep stopped early
(see "Queries that could not be run"). Candidates below are recorded only where a search result (publisher page,
DOI link, IDEAS/RePEc, TRID, institutional repository) corroborated title + venue. Where only a venue/volume/page
index entry was seen and the title is inferred, the entry is marked LOW confidence and flagged.

## Queries run (24 completed)
1. Beasley "scheduling aircraft landings" Transportation Science
2. Balakrishnan Chandran "constrained position shifting" runway scheduling Operations Research
3. Bennell Mesgarpour Potts airport runway scheduling dynamic programming Transportation Science
4. Pyrgiotis Malone Odoni queueing network airport delays "Transportation Research Part C"
5. Jacquillat Odoni airport congestion mitigation dynamic programming "Operations Research" OR "Transportation Science"
6. Lieder Stolletz runway scheduling "Transportation Research Part" dynamic programming
7. Furini Kidd Persiani Toth runway sequencing "Transportation Research Part C" rolling horizon
8. Sama D'Ariano Pacciarelli terminal control area aircraft scheduling "Transportation Research Part C"
9. Briskorn Stolletz aircraft landing problem runway "Transportation Science" OR "Operations Research" OR "Transportation Research Part B"
10. Richetta Odoni "ground-holding" stochastic "Transportation Science" 1993
11. ground delay program stochastic integer program Ball Hoffman Odoni Rifkin "Operations Research" 2003
12. aircraft taxi scheduling surface movement optimization "Transportation Research Part C" mixed integer
13. Simaiakis Balakrishnan "queuing model of the airport departure process" Transportation Science 10.1287/trsc
14. Jacquillat Odoni Simaiakis "runway configurations" dynamic control "Transportation Science" 2017
15. Terrab Odoni "strategic flow management" air traffic control "Operations Research" 1993
16. Hoffman Ball "ground-holding problem" banking constraints "Operations Research" 2000
17. airport slot allocation scheduling optimization "Transportation Research Part B" Zografos OR Jacquillat OR Pellegrini
18. airport capacity envelope arrival departure tradeoff Gilbo "Transportation Research" OR "Transportation Science"
19. "10.1287/trsc" runway sequencing aircraft arrivals departures
20. "10.1016/j.trb" runway scheduling aircraft landing mixed integer
21. "10.1016/j.trc" aircraft arrival sequencing terminal airspace 2024
22. Nikoleris Hansen "queueing models for trajectory-based aircraft operations" Transportation Science
23. metroplex multi-airport terminal airspace scheduling optimization "Transportation Research Part C"
24. eVTOL vertiport scheduling arrival sequencing optimization "Transportation Research Part C" 2024 OR 2025

## Queries that could not be run (budget exhausted)
- Bertsimas Frankovich Odoni "optimal selection of airport runway configurations" Operations Research 2011
- Frankovich Bertsimas "unified optimization of traffic flows through airports" Transportation Science
- Avella Boccia Mannino Vasilyev "time-indexed formulations for the runway scheduling problem" Transportation Science
- Venkatakrishnan Barnett Odoni "Landings at Logan Airport" Transportation Science 1993
- Psaraftis "dynamic programming approach for sequencing groups of identical jobs" Operations Research 1980
- Mukherjee Hansen "dynamic stochastic model for the single airport ground holding problem" Transportation Science 2007
Further planned but not reached: Ball-Hoffman-Mukherjee ration-by-distance (TS 2010); Liu-Hansen-Mukherjee scenario-based ATFM (TR-B 2008);
Kuhn and Glover-Ball GDP equity (TR-C 2013); Vossen-Ball slot trading (TS 2006); Estes-Ball (TS 2020); Jones-Lovell-Ball (TS 2018);
Jacquillat passenger-centric GDP (TS 2022); Jacquillat-Vaze interairline equity (TS); Pyrgiotis-Odoni scheduling limits (TS 2016);
Vaze-Barnhart frequency competition (TS 2012); Ribeiro-Jacquillat-Antunes LNS slot allocation (TS 2019); Pellegrini et al. SOSTA (TR-C 2017);
Sama et al. 2014 (TR-C); Liang-Delahaye-Marechal (TR-C 2017); Toratani (TR-C 2019); Khassiba et al. (TS 2020 / TR-C 2022);
Prakash-Piplani-Desai (TR-C 2018); Weiszer-Chen ground movement (TR-C); Yin et al. apron-runway (TR-B 2022);
Justin-Payan-Mavris electric aircraft battery swap (TR-C 2020); vertiport capacity (TR-C 2023-2025); Kim-Hansen deconstructing delay (TR-B 2013);
Richetta 1995 (OR); Andreatta-Romanin-Jacur 1987 (TS); Nikoleris-Hansen runway occupancy (TR-B 2015); departure metering (TS/TR-C);
Yan-Vaze-Barnhart airline-driven GDP (TR-C 2018); Zografos-Salouras-Madas (TR-C 2012); Ma-Delahaye TMA+airport (TR-C 2019).
These are leads for a round 2, not recorded candidates.

## Candidates (in scope)

### Runway scheduling / aircraft sequencing
- Beasley, Krishnamoorthy, Sharaiha, Abramson (2000) "Scheduling Aircraft Landings—The Static Case", Transportation Science 34(2):180-197.
  DOI 10.1287/trsc.34.2.180.12302. https://pubsonline.informs.org/doi/fpi/10.1287/trsc.34.2.180.12302 ; https://people.brunel.ac.uk/~mastjjb/jeb/static.html  [HIGH]
- Balakrishnan, Chandran (2010) "Algorithms for Scheduling Runway Operations Under Constrained Position Shifting", Operations Research 58(6):1650-1665.
  https://ideas.repec.org/a/inm/oropre/v58y2010i6p1650-1665.html ; https://www.mit.edu/~hamsa/pubs/BalakrishnanChandranOR.pdf  [MEDIUM; DOI not seen]
- De Maere, Atkin, Burke (2018) "Pruning Rules for Optimal Runway Sequencing", Transportation Science 52(4):898-916.
  https://ideas.repec.org/a/inm/ortrsc/v52y2018i4p898-916.html  [MEDIUM; DOI not seen]
- Solak et al. (2018) "Stochastic Runway Scheduling", Transportation Science 52(4):917-940. Snippet named only "Senay Solak and colleagues".
  https://ideas.repec.org/a/inm/ortrsc/v52y2018i4p917-940.html  [MEDIUM; DOI not seen]
- (LOW, title inferred) TS 27(3):211-227 (1993) index entry seen at https://ideas.repec.org/a/inm/ortrsc/v27y1993i3p211-227.html ;
  believed to be Venkatakrishnan, Barnett, Odoni "Landings at Logan Airport: Describing and Increasing Airport Capacity". Title NOT shown in result.

### Terminal-area / arrival management
- Sama, D'Ariano, Corman, Pacciarelli (2017) "Metaheuristics for efficient aircraft scheduling and re-routing at busy terminal control areas", TR-C.
  https://iris.uniroma3.it/handle/11590/313776  [MEDIUM; DOI not seen]
- Ng, Ribeiro, Jorge (2024) "An optimization approach for the terminal airspace scheduling problem", TR-C 169:104856. DOI 10.1016/j.trc.2024.104856.
  https://repository.sutd.edu.sg/esploro/outputs/journalArticle/An-optimization-approach-for-the-terminal/9912336109846  [MEDIUM]
- Sidiropoulos, Han, Majumdar, Ochieng (2017) "Robust identification of air traffic flow patterns in Metroplex terminal areas under demand uncertainty", TR-C 75:212-227.
  https://spiral.imperial.ac.uk/entities/publication/dbb76848-c0f8-4168-a24b-298b30a3e60e  [MEDIUM; DOI not seen]
- Nikoleris, Hansen (2012) "Queueing Models for Trajectory-Based Aircraft Operations", Transportation Science 46(4):501-511. DOI 10.1287/trsc.1120.0411.
  https://ideas.repec.org/a/inm/ortrsc/v46y2012i4p501-511.html ; https://its.berkeley.edu/publications/queueing-models-trajectory-based-aircraft-operations  [MEDIUM]
- Lead not recorded: LiU/Polishchuk group "TRC_Entry_time_2021.pdf" (https://itn-web.it.liu.se/~tatpo46/pps/TRC_Entry_time_2021.pdf) is a TR-C 2021 paper on TMA entry-time / arrival sequencing; title not seen.

### Airport congestion, queueing, runway configuration, capacity utilisation
- Pyrgiotis, Malone, Odoni (2013) "Modelling delay propagation within an airport network", TR-C 27. https://trid.trb.org/view/1245698  [MEDIUM]
- Simaiakis, Balakrishnan (2016) "A Queuing Model of the Airport Departure Process", Transportation Science 50(1):94-109. DOI 10.1287/trsc.2015.0603.
  https://pubsonline.informs.org/doi/references/10.1287/trsc.2015.0603  [HIGH]
- Jacquillat, Odoni (2015) "An Integrated Scheduling and Operations Approach to Airport Congestion Mitigation", Operations Research.
  https://academicnewsletter.sufe.edu.cn/info/383735 ; https://dspace.mit.edu/handle/1721.1/99331  [MEDIUM; DOI not seen]
- Jacquillat, Odoni, Webster (2017) "Dynamic Control of Runway Configurations and of Arrival and Departure Service Rates at JFK Airport Under Stochastic Queue Conditions",
  Transportation Science 51(1):155-176. https://ideas.repec.org/a/inm/ortrsc/v51y2017i1p155-176.html ; a pubsonline link 10.1287/trsc.2015.0644 appeared in the
  same result set and is believed to be this paper (association inferred).  [MEDIUM]
- (LOW, title inferred) OR 59(6):1407-1419 (2011) index entry seen at https://ideas.repec.org/a/inm/oropre/v59y2011i6p1407-1419.html ;
  believed to be Bertsimas, Frankovich, Odoni "Optimal Selection of Airport Runway Configurations". Title NOT shown.
- (LOW, title inferred) TS 50(1):77-93 (2016) index entry seen at https://ideas.repec.org/a/inm/ortrsc/v50y2016i1p77-93.html ;
  believed to be Bertsimas, Frankovich "Unified Optimization of Traffic Flows Through Airports". Title NOT shown.
- (LOW, title inferred) OR 43(6):995-1011 (1995) index entry seen at https://ideas.repec.org/a/inm/oropre/v43y1995i6p995-1011.html ;
  believed to be Peterson, Bertsimas, Odoni "Decomposition Algorithms for Analyzing Transient Phenomena in Multiclass Queueing Networks, with an Application to Air Transportation". Title NOT shown.

### Ground holding / ground delay programs (airport-side ATFM)
- Terrab, Odoni (1993) "Strategic Flow Management for Air Traffic Control", Operations Research 41(1):138-152. https://ideas.repec.org/a/inm/oropre/v41y1993i1p138-152.html  [MEDIUM]
- Richetta, Odoni (1993) "Solving Optimally the Static Ground-Holding Policy Problem in Air Traffic Control", Transportation Science 27(3):228-238.
  https://ideas.repec.org/a/inm/ortrsc/v27y1993i3p228-238.html ; https://trid.trb.org/View/382715  [MEDIUM]
- Hoffman, Ball (2000) "A Comparison of Formulations for the Single-Airport Ground-Holding Problem with Banking Constraints", Operations Research 48(4):578-590.
  https://ideas.repec.org/a/inm/oropre/v48y2000i4p578-590.html  [MEDIUM]
- Ball, Hoffman, Odoni, Rifkin (2003) "A Stochastic Integer Program with Dual Network Structure and Its Application to the Ground-Holding Problem", Operations Research 51(1):167-171.
  DOI 10.1287/opre.51.1.167.12795 (shown in snippet). https://ideas.repec.org/a/inm/oropre/v51y2003i1p167-171.html  [MEDIUM]
- Navazio, Romanin-Jacur (1998) "The Multiple Connections Multi-Airport Ground Holding Problem: Models and Algorithms", Transportation Science 32(3):268-.
  DOI 10.1287/trsc.32.3.268. https://pubsonline.informs.org/doi/references/10.1287/trsc.32.3.268 (title + DOI seen; authors not displayed in result, taken from memory)  [MEDIUM]
- (LOW, title inferred) TS 40(2):133-146 (2006) index entry seen at https://ideas.repec.org/a/inm/ortrsc/v40y2006i2p133-146.html ;
  believed to be Kotnyek, Richetta "Equitable Models for the Stochastic Ground-Holding Problem Under Collaborative Decision Making". Title NOT shown.

### Slot allocation / demand management
- Ribeiro, Jacquillat, et al. (2018) "An optimization approach for airport slot allocation under IATA guidelines", TR-B.
  https://repository.sutd.edu.sg/esploro/outputs/journalArticle/An-optimization-approach-for-airport-slot/9912335909846  [MEDIUM]
- Keskin, Zografos (2023) "Optimal network-wide adjustments of initial airport slot allocations with connectivity and fairness objectives", TR-B.
  https://eprints.whiterose.ac.uk/id/eprint/205144/  [MEDIUM]

### Surface movement / taxi
- Evertse, Visser (2017?) TR-C paper on real-time surface movement planning minimising emissions with timed taxi routes via MILP; snippet confirmed authors, venue and
  method but NOT the title or year. Believed title: "Real-time airport surface movement planning: Minimizing aircraft emissions".
  https://repository.tudelft.nl/file/File_daa82b50-710d-48b7-8382-77854e35eb1b?preview=1  [LOW]

### UAM / vertiport
- Waltz, Okhrin, Schultz (2024) "Self-organized free-flight arrival for urban air mobility", TR-C 167:104806.
  https://www.unibw.de/lvk-en/publications/2024_self-organized_free-flight_uam_arrival  [MEDIUM; DOI not seen]

## Seen but OUT of scope (for the record)
- Bennell, Mesgarpour, Potts (2013) "Airport runway scheduling" (4OR 2011 / Annals of OR 2013) and (2017) "Dynamic scheduling of aircraft landings" EJOR 258(1).
- Lieder, Stolletz (2016) interdependent/heterogeneous runways, TR-E 88; Lieder, Briskorn, Stolletz (2015) DP for ALP with aircraft classes, EJOR 243.
- Furini, Kidd, Persiani, Toth (2015) improved rolling horizon for aircraft sequencing, Journal of Scheduling.
- Ghoniem, Sherali, Baik (2014) "Enhanced Models for a Mixed Arrival-Departure Aircraft Sequencing Problem", INFORMS J. Computing (10.1287/ijoc.2013.0581).
- Kleinbekman, Mitici, Wei eVTOL arrival sequencing/scheduling (DASC conference; JAIS) - venue not in scope; not recorded.
- arXiv 2502.12196 metroplex bi-level sequencing - preprint.
