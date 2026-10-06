# Facet B2: time-windows-periodic-launch (round 1)

Scheduling of shared capacity with time windows and periodic constraints, as analogs for launch windows,
orbital phasing, pad/hub capacity and reusable-vehicle turnaround in spaceport-to-orbit feeder network design.

NOTE ON COVERAGE: 30 WebSearch queries were completed. A further 8 queries were issued but NOT executed because
the turn-wide WebSearch budget (shared across all agents) was exhausted. Those 8 are listed at the end as
"not executed" and the leads they were meant to confirm are listed as gaps. Only WebSearch reaches the internet
in this environment; nothing was fetched from publisher pages, so DOIs are recorded only when they appeared
literally in a result URL or snippet.

## Queries run (30 executed)
1. "space logistics" network design "Operations Research" OR "Transportation Science" INFORMS
2. "periodic event scheduling" "Transportation Science" Liebchen
3. Nachtigall Voget periodic timetabling "Transportation Research Part B"
4. Kroon Peeters cyclic railway timetabling "Transportation Science"
5. "spaceport" "Transportation Research Part C"
6. Bierwirth Meisel berth allocation survey "Transportation Research Part B" OR "Transportation Science"
7. "10.1287/trsc.1070.0213"
8. "Integrated Periodic Timetabling and Vehicle Circulation Scheduling" Transportation Science 2021 authors
9. Ho de Weck Shishko "space logistics" time-expanded network optimization
10. Taylor Song Klabjan de Weck "interplanetary logistics" mathematical model
11. satellite scheduling "Operations Research" INFORMS 10.1287/opre
12. Imai Nishimura Papadimitriou "dynamic berth allocation problem" "Transportation Research Part B"
13. Cordeau Laporte Legato Moccia "berth-allocation problem" tabu search "Transportation Science"
14. Odijk 1996 "constraint generation algorithm" periodic railway timetables "Transportation Research Part B"
15. "space shuttle" OR "launch" scheduling "Operations Research" INFORMS mission launch times
16. Chen Ho "space logistics" "Journal of Spacecraft and Rockets" mixed-integer nonlinear programming
17. Zhang Klabjan "gate re-assignment" "Transportation Research Part B" 2017
18. Drexl "Synchronization in Vehicle Routing" survey "Transportation Science" 2012
19. Polinder Breugem Dollevoet Maróti adjustable robust periodic timetabling "Transportation Research Part B"
20. Ibarra-Rojas Rios-Solis "synchronization of bus timetabling" "Transportation Research Part B"
21. Boland Hewitt Marshall Savelsbergh "continuous-time service network design" "Operations Research"
22. Imai Nishimura Papadimitriou "berth allocation with service priority" OR "continuous location space" "Transportation Research Part B"
23. "periodic timetabling" "Transportation Science" 2023 OR 2024 OR 2025
24. satellite OR orbit OR "space transportation" "Transportation Research Part C" 2024 OR 2025 optimization
25. Zografos Salouras Madas airport slot allocation "Transportation Research Part C" 2012
26. Ribeiro Jacquillat Antunes Odoni airport slot allocation IATA "Transportation Research Part B" 2018
27. Zhu Crainic Gendreau "scheduled service network design" freight rail "Operations Research" 2014
28. Sparing Goverde "cycle time optimization" stable periodic railway timetables "Transportation Research Part B" 2017
29. Jagannatha Ho "event-driven network model" space mission optimization "Journal of Spacecraft and Rockets"
30. "berth allocation" "Transportation Science" 2022 OR 2023 OR 2024 uncertainty

## Queries issued but NOT executed (budget exhausted)
31. "Integrated berth and yard space allocation under uncertainty" "Transportation Research Part B" 2022 authors
32. Xu Zhang Xiao Wang "robust approach to airport gate assignment" solution-dependent uncertainty budget "Transportation Research Part B"
33. Bookbinder Désilets "transfer optimization in a transit network" "Transportation Science" 1992
34. "satellite constellation" OR "space debris" OR "in-space" optimization "Operations Research" INFORMS 2023 OR 2024 OR 2025
35. "service network design" "departure time" choice "Transportation Research Part C" OR "Transportation Science"
36. Zhen Liang Zhuge Lee Chew "daily berth planning" tidal port channel "Transportation Research Part B" 2017
37. Dorndorf Jaehn Pesch "robust flight-gate scheduling" clique partitioning "Transportation Science" 2008
38. reusable launch vehicle fleet scheduling turnaround launch manifest optimization "Acta Astronautica" OR "Journal of Spacecraft and Rockets" 2023 OR 2024

## Key observations
- No paper with "spaceport" in TRC, nor "orbital"/"satellite" network design in TRB/TRC, surfaced in the executed
  queries (query 5 and 24 returned only journal-description pages and non-venue items). The space-logistics OR
  literature (Ho group, de Weck group) sits in Acta Astronautica / Journal of Spacecraft and Rockets / arXiv,
  not in the four target venues. INFORMS is only now (IFORS 2026) opening an "OR in Space" stream.
- The one genuinely in-venue launch-scheduling paper found is Fisher & Jaikumar (1978, Operations Research):
  NASA shuttle mission launch-time selection with earliest-start and resource constraints.
- PESP/periodic timetabling in TS and TRB is well represented (Odijk 1996; Kroon & Peeters 2003; Liebchen 2008;
  Kroon et al. 2014; Sparing & Goverde 2017; Polinder et al. 2019; Van Lieshout 2021). Recent (2023-2025) PESP
  work found is in ATMOS, Operations Research Forum and Mathematical Programming, i.e. out of scope.
- Berth allocation (Imai 2001/2003/2005 TRB; Cordeau et al. 2005 TS; Meisel & Bierwirth 2013 TS; Agra &
  Rodrigues 2022 TRB) and gate (re)assignment (Zhang & Klabjan 2017 TRB) give the "time-windowed shared
  resource" analog for pads/docking ports.
- Airport slot allocation (Zografos et al. 2012 TRC; Ribeiro et al. 2018 TRB) is the closest analog for
  allocating scarce launch slots among competing users under declared capacity.

## Candidates (in-scope venues)

| # | Title | Authors | Year | Venue | DOI (seen) | URL where seen | Conf. |
|---|-------|---------|------|-------|-----------|----------------|-------|
| 1 | An Algorithm for the Space-Shuttle Scheduling Problem | Fisher, Jaikumar | 1978 | Operations Research 26(1):166-182 | 10.1287/opre.26.1.166 | https://pubsonline.informs.org/doi/fpi/10.1287/opre.26.1.166 | high |
| 2 | A constraint generation algorithm for the construction of periodic railway timetables | Odijk | 1996 | TRB 30(6):455-464 | | https://ideas.repec.org/a/eee/transb/v30y1996i6p455-464.html ; https://trid.trb.org/View/468296 | medium |
| 3 | A Variable Trip Time Model for Cyclic Railway Timetabling | Kroon, Peeters | 2003 | TS 37(2):198-212 | | https://ideas.repec.org/a/inm/ortrsc/v37y2003i2p198-212.html | medium |
| 4 | Flexible connections in PESP models for cyclic passenger railway timetabling | Kroon, Peeters, Wagenaar, Zuidwijk | 2014 | TS 48(1):136-154 | | https://repub.eur.nl/pub/76844 | medium |
| 5 | The First Optimized Railway Timetable in Practice | Liebchen | 2008 | TS 42(4) | 10.1287/trsc.1080.0240 | https://pubsonline.informs.org/doi/references/10.1287/trsc.1080.0240 | high |
| 6 | Optimizing Timetable Synchronization for Rail Mass Transit | Wong, Yuen, Fung, Leung | 2008 | TS 42(1) | 10.1287/trsc.1070.0200 | https://pubsonline.informs.org/doi/references/10.1287/trsc.1070.0200 | high |
| 7 | Integrated Periodic Timetabling and Vehicle Circulation Scheduling | Van Lieshout | 2021 | TS 55(3):768-790 | 10.1287/trsc.2020.1024 | https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2020.1024 | high |
| 8 | A cycle time optimization model for generating stable periodic railway timetables | Sparing, Goverde | 2017 | TRB 98:198-223 | | https://ideas.repec.org/a/eee/transb/v98y2017icp198-223.html ; https://research.tudelft.nl/en/publications/a-cycle-time-optimization-model-for-generating-stable-periodic-ra | medium |
| 9 | An adjustable robust optimization approach for periodic timetabling | Polinder, Breugem, Dollevoet, Maróti | 2019 | TRB 128:50-68 | | https://ideas.repec.org/a/eee/transb/v128y2019icp50-68.html | medium |
| 10 | Synchronization of bus timetabling | Ibarra-Rojas, Rios-Solis | 2012 | TRB 46(5):599-614 | | https://www.worldtransitresearch.info/research/4228 | medium |
| 11 | The dynamic berth allocation problem for a container port | Imai, Nishimura, Papadimitriou | 2001 | TRB 35(4):401-417 | | https://ideas.repec.org/a/eee/transb/v35y2001i4p401-417.html | medium |
| 12 | Berth allocation with service priority | Imai, Nishimura, Papadimitriou | 2003 | TRB 37(5):437-457 | | https://ideas.repec.org/a/eee/transb/v37y2003i5p437-457.html | medium |
| 13 | Berth allocation in a container port: using a continuous location space approach | Imai, Sun, Nishimura, Papadimitriou | 2005 | TRB 39(3):199-221 | | https://ideas.repec.org/a/eee/transb/v39y2005i3p199-221.html | medium |
| 14 | Models and Tabu Search Heuristics for the Berth-Allocation Problem | Cordeau, Laporte, Legato, Moccia | 2005 | TS 39(4):526-538 | | https://ideas.repec.org/a/inm/ortrsc/v39y2005i4p526-538.html | medium |
| 15 | A Framework for Integrated Berth Allocation and Crane Operations Planning in Seaport Container Terminals | Meisel, Bierwirth | 2013 | TS 47(2):131-147 | | https://prodlog.wiwi.uni-halle.de/team/ehemalige_mitarbeiter/meisel | medium |
| 16 | Optimization for gate re-assignment | Zhang, Klabjan | 2017 | TRB 95:260-284 | 10.1016/j.trb.2016.11.006 | https://ideas.repec.org/a/eee/transb/v95y2017icp260-284.html | medium |
| 17 | Synchronization in Vehicle Routing—A Survey of VRPs with Multiple Synchronization Constraints | Drexl | 2012 | TS 46(3):297-316 | | https://ideas.repec.org/a/inm/ortrsc/v46y2012i3p297-316.html | medium |
| 18 | The Continuous-Time Service Network Design Problem | Boland, Hewitt, Marshall, Savelsbergh | 2017 | Operations Research 65(5):1303-1321 | | https://scholars.luc.edu/en/publications/the-continuous-time-service-network-design-problem/ | medium |
| 19 | Scheduled Service Network Design for Freight Rail Transportation | Zhu, Crainic, Gendreau | 2014 | Operations Research 62(2):383-400 | 10.1287/opre.2013.1254 | https://pubsonline.informs.org/doi/suppl/10.1287/opre.2013.1254 | high |
| 20 | Dealing with the efficient allocation of scarce resources at congested airports | Zografos, Salouras, Madas | 2012 | TRC 21(1):244-256 | | https://eprints.lancs.ac.uk/id/eprint/64630 | medium |
| 21 | An optimization approach for airport slot allocation under IATA guidelines | Ribeiro, Jacquillat, Antunes, Odoni, Pita | 2018 | TRB 112:132-156 | 10.1016/j.trb.2018.04.005 | https://ideas.repec.org/a/eee/transb/v112y2018icp132-156.html | medium |
| 22 | Distributionally robust optimization for the berth allocation problem under uncertainty | Agra, Rodrigues | 2022 | TRB 164:1-24 | | https://ideas.repec.org/a/eee/transb/v164y2022icp1-24.html | medium |
| 23 | Integrated berth and yard space allocation under uncertainty | (authors not shown in snippet; PolyU-affiliated) | 2022 | TRB 162 | | https://research.polyu.edu.hk/en/publications/integrated-berth-and-yard-space-allocation-under-uncertainty/ | low |

## Candidates (adjacent venues, tag "adjacent-venue")

| # | Title | Authors | Year | Venue | URL where seen | Conf. |
|---|-------|---------|------|-------|----------------|-------|
| A1 | Dynamic modeling and optimization for space logistics using time-expanded networks | Ho, de Weck, Hoffman, Shishko | 2014 | Acta Astronautica | https://experts.illinois.edu/en/publications/dynamic-modeling-and-optimization-for-space-logistics-using-time-/ | medium |
| A2 | Integrated space logistics mission planning and spacecraft design with mixed-integer nonlinear programming | Chen, Ho | 2018 | Journal of Spacecraft and Rockets 55(2) | https://researchwith.stevens.edu/en/publications/integrated-space-logistics-mission-planning-and-spacecraft-design/ | medium |
| A3 | Event-Driven Network Model for Space Mission Optimization with High-Thrust and Low-Thrust Spacecraft | Jagannatha, Ho | 2020 | Journal of Spacecraft and Rockets 57(3):446-463 | https://arxiv.org/abs/1904.09364 | medium |
| A4 | Modeling interplanetary logistics: A mathematical model for mission planning | Taylor, Song, Klabjan, de Weck, Simchi-Levi | 2007 | Logistics Spectrum 41(1):23-33 | https://research.polyu.edu.hk/en/publications/modeling-interplanetary-logistics-a-mathematical-model-for-missio/ | low |

## Leads seen but NOT recorded (venue/title/authors unconfirmed)
- "Multi-periodic train timetabling using a period-type-based Lagrangian relaxation decomposition" (worldtransitresearch.info/research/6742) - venue not shown.
- ideas.repec.org/a/eee/transb/v125y2019icp52-75 (a TRB 2019 timetabling paper, title not shown).
- Isaji, Takubo, Ho "Multidisciplinary Design Optimization Approach to Integrated Space Mission Planning and Spacecraft Design" (arXiv 2110.07323; journal version not confirmed).
- "Generalizing Space Logistics Network Optimization with Integrated Machine Learning and Mathematical Programming" (arXiv 2404.18770; venue not confirmed).
- 2023-2025 PESP work (Lindner, Masing, Bortoletto, Liebchen, Schöbel, Grafe) is in ATMOS / OR Forum / Math. Programming - out of scope.
- Bierwirth & Meisel BAP surveys (EJOR 2010, 2015) - out of scope.
- Nachtigall & Voget 1996 (Computers & OR) - out of scope.
- Fisher & Jaikumar is the only in-venue launch-scheduling paper found; a 1988 Interfaces satellite-support paper (Kennedy, Parnell, Rowell) is out of scope.

## Gaps (searches that could not be run)
- Confirmation of Xu et al. 2017 TRB robust gate assignment; Dorndorf, Jaehn, Pesch 2008 TS robust flight-gate scheduling.
- Bookbinder & Désilets 1992 TS transfer optimization (classic synchronization).
- Zhen et al. 2017 TRB daily berth planning in tidal port (channel time windows).
- Time-dependent SND with departure-time choice in TS/TRC; rendezvous/synchronized-arrival scheduling in TRB.
- Any 2021-2026 OR/TS paper on satellite constellations, in-space servicing or launch logistics (query 34 not executed; query 24 found none in TRC).
- Reusable-launch-vehicle fleet/turnaround scheduling in Acta Astronautica / JSR (adjacent).
