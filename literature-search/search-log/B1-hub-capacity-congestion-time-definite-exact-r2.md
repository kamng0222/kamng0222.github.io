# Facet B1 — Hub location: capacitated/congested hubs, time-definite & incomplete hub networks, exact large-scale methods (round 2)

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Venues in scope: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## Status / important caveat (read first)

ZERO WebSearch queries could be executed in this round. Every call returned
"web search budget is used up (limit: 200 WebSearch calls per turn, shared by every agent in it)".
Per the task constraints no workaround (curl, wget, proxies, archives, third-party readers) was attempted,
and WebFetch/curl are blocked by the egress proxy anyway. Round 1 of this facet (B1-hub-location-r1.md)
ran only 8 queries before hitting the same limit, so the hub-location facet has been searched with 8 queries
in total across two rounds.

Consequence for this file:
- The candidate table below contains ONLY papers that some agent in this run saw in an executed search
  result (publisher DOI page, RePEc/IDEAS, TRID, IAOR, university repository). They are PASS-THROUGH records:
  I did not see the pages myself; the evidence URL is the one the sibling recorded. Confidence follows the
  evidence type (publisher/DOI page -> high; index/repository -> medium).
- The facet's own anchor papers (Correia/Nickel/Saldanha-da-Gama 2010; Taherkhani/Alumur/Hosseini 2020;
  de Camargo/Miranda/Luna 2009; Yaman/Kara/Tansel 2007; Alumur/Kara/Karasan 2009; O'Kelly & Bryan 1998;
  Aykin 1995; Racunica & Wynter 2005; Wandelt/Dai/Zhang/Sun 2022; Maheo/Kilby/Van Hentenryck 2019;
  Rostami/Chitsaz/Arslan/Laporte/Lodi 2022) have NO search sighting anywhere in this run. Following the rule
  "never record a paper from memory alone", they are NOT in the candidate list; they are in the verification
  queue (Section 5) with ready-to-run queries, each marked "recollection — verify before use".
- Sub-topic (1) "queueing-congestion hub models in TS/TR-B" and sub-topic (2) "time-definite / incomplete hub
  networks" therefore have NO corroborated entries at all after two rounds. This is a coverage gap of the run,
  not evidence that the literature is thin.

Local sources checked instead of the web (all read-only):
- /home/user/kamng0222.github.io : contains only .git — no bibliography, .bib, notes.
- scratchpad/research_notes/RAM ATFM and spaceport feeder literature/*.md (26 sibling notes, r1 and r2).
- scratchpad/verified/*.ndjson (A1, A2, B1, B2 verified records built by the orchestrator from r1 notes).

## 1. Queries attempted this round (6; ALL refused by the budget limit, none executed)

1. capacitated hub location Benders "Transportation Science"  (standard) — NOT EXECUTED
2. hub location congestion queue "Transportation Research Part B"  (standard) — NOT EXECUTED
3. Correia Nickel Saldanha-da-Gama single-assignment hub location problems multiple capacity levels Transportation Research Part B 2010 — NOT EXECUTED
4. Taherkhani Alumur Hosseini Benders decomposition profit maximizing capacitated hub location multiple demand classes Transportation Science — NOT EXECUTED
5. de Camargo Miranda Luna Benders decomposition hub location problems economies of scale Transportation Science 2009 — NOT EXECUTED
6. Contreras Cordeau Laporte Benders decomposition large-scale uncapacitated hub location Operations Research 2011 — NOT EXECUTED

## 2. Candidates recorded (pass-through from sibling agents' executed searches)

Sub-topic key: (1) capacitated/modular/congested/uncertain hubs; (2) time-definite & incomplete hub networks;
(3) exact large-scale methods & benchmarks; (S) seminal/survey; (E) emerging-technology hub networks.

| # | Paper | Venue, year | DOI | Evidence URL (as recorded by sibling) | Sibling file | Conf. | Sub-topic |
|---|-------|-------------|-----|----------------------------------------|--------------|-------|-----------|
| 1 | Contreras, Cordeau, Laporte — Benders Decomposition for Large-Scale Uncapacitated Hub Location | Operations Research 59(6):1477-1490, 2011 | 10.1287/opre.1110.0965 | https://pubsonline.informs.org/doi/10.1287/opre.1110.0965 ; https://researchportal.bath.ac.uk/en/publications/benders-decomposition-for-large-scale-uncapacitated-hub-location/ ; https://www.cirrelt.ca/DocumentsTravail/CIRRELT-2010-26.pdf | B2-network-design-uncertainty-r1; verified/B2 | high | (3) |
| 2 | Contreras, Cordeau, Laporte — The Dynamic Uncapacitated Hub Location Problem | Transportation Science 45(1):18-32, 2011 | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v45y2011i1p18-32.html (index shows TS 45(1) 2011 pp. 18-32; sibling flagged title/authors "from recollection", matched to index) | B1-hub-location-r1 | medium | (1)/(3) |
| 3 | Taherkhani, Alumur, Hosseini — Robust Stochastic Models for Profit-Maximizing Hub Location Problems | Transportation Science 55(6):1322-1350, 2021 | 10.1287/trsc.2021.1064 | https://pubsonline.informs.org/doi/10.1287/trsc.2021.1064 ; https://ideas.repec.org/a/inm/ortrsc/v55y2021i6p1322-1350.html | B1-hub-location-r1 | high | (1)/(3) |
| 4 | Wang, Chen, Liu — Distributionally Robust Hub Location | Transportation Science, 2020 | 10.1287/trsc.2019.0948 | https://pubsonline.informs.org/doi/10.1287/trsc.2019.0948 | B2-network-design-uncertainty-r1 | high | (1) |
| 5 | Zetina, Contreras, Cordeau, Nikbakhsh — Robust uncapacitated hub location | Transportation Research Part B 106:393-410, 2017 | (not seen) | https://ideas.repec.org/a/eee/transb/v106y2017icp393-410.html | B2-network-design-uncertainty-r1 | medium | (1)/(3) |
| 6 | Alumur, Nickel, Saldanha-da-Gama — Hub location under uncertainty | Transportation Research Part B 46(4):529-543, 2012 | 10.1016/j.trb.2011.11.006 | https://ideas.repec.org/a/eee/transb/v46y2012i4p529-543.html ; https://uwaterloo.ca/scholar/salumura/node/10433 ; https://iaorifors.com/paper/77618 | B1-hub-location-r1; B2-network-design-uncertainty-r1 | medium | (1) |
| 7 | An, Zhang, Zeng — The reliable hub-and-spoke design problem: Models and algorithms | Transportation Research Part B 77:103-122, 2015 | 10.1016/j.trb.2015.02.006 (as displayed on the RePEc index per sibling) | https://ideas.repec.org/a/eee/transb/v77y2015icp103-122.html ; https://trid.trb.org/view/1354344 | B1-hub-location-r1; B2-network-design-uncertainty-r1 | medium | (1) |
| 8 | Campbell — Hub Location and the p-Hub Median Problem | Operations Research 44(6):923-935, 1996 | 10.1287/opre.44.6.923 | https://pubsonline.informs.org/doi/10.1287/opre.44.6.923 | B1-hub-location-r1 | high | (S) |
| 9 | O'Kelly — The Location of Interacting Hub Facilities | Transportation Science 20(2):92-106, 1986 | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v20y1986i2p92-106.html | B1-hub-location-r1 | medium | (S) |
| 10 | Aykin — On the Location of Hub Facilities | Transportation Science 22(2):155-157, 1988 | (not seen) | https://trid.trb.org/View/318813 ; https://ideas.repec.org/a/inm/ortrsc/v22y1988i2p155-157.html | B1-hub-location-r1 | medium | (S) |
| 11 | Campbell, O'Kelly — Twenty-Five Years of Hub Location Research | Transportation Science 46(2):153-169, 2012 | 10.1287/trsc.1120.0410 | https://pubsonline.informs.org/doi/10.1287/trsc.1120.0410 | B1-hub-location-r1 | high | (S) |
| 12 | Campbell — Continuous and discrete demand hub location problems | Transportation Research Part B 27(6):473-482, 1993 | (not seen) | https://iaorifors.com/paper/11858 | B1-hub-location-r1 | medium | (S) |
| 13 | Yildiz, Yaman, Karasan — Hub Location, Routing, and Route Dimensioning: Strategic and Tactical Intermodal Transportation Hub Network Design | Transportation Science 55(6):1351-1369, 2021 | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v55y2021i6p1351-1369.html (authors from sibling recollection matched to index) | B1-hub-location-r1 | medium | (1)/(2) |
| 14 | Meier, Clausen — Solving Single Allocation Hub Location Problems on Euclidean Data | Transportation Science 52(5), 2018 | 10.1287/trsc.2017.0751 | https://pubsonline.informs.org/doi/references/10.1287/trsc.2017.0751 | B1-hub-location-r1 | high | (3) |
| 15 | Puerto, Ramos, Rodriguez-Chia, Sanchez-Gil — Ordered median hub location problems with capacity constraints | Transportation Research Part C 70:142-156, 2016 | (not seen) | https://produccioncientifica.uca.es/documentos/600ef0faf179b17b49334307?lang=fr ; preprint https://arxiv.org/pdf/1503.04468 | B1-hub-location-r1 | medium | (1) |
| 16 | (authors not captured) — Demand-Driven Hub Network Design Under Uncertainty for Less-Than-Truckload Carriers | Transportation Science, 2025 | 10.1287/trsc.2025.0180 | https://pubsonline.informs.org/doi/10.1287/trsc.2025.0180 | B2-network-design-uncertainty-r1 | medium | (1) |
| 17 | (authors not captured) — Budget-Driven Multiperiod Hub Location: A Robust Time-Series Approach | Operations Research 73(2):613-631, 2025 | (not seen) | https://ideas.repec.org/a/inm/oropre/v73y2025i2p613-631.html ; https://academicnewsletter.sufe.edu.cn/info/401695 | B2-network-design-uncertainty-r1 | medium | (1) |
| 18 | Willey, Salmon — A method for urban air mobility network design using hub location and subgraph isomorphism | Transportation Research Part C 125 (art. 102997), 2021 | (not seen) | https://pubsonline.informs.org/doi/references/10.1287/msom.2022.1148 (cited in reference list) ; https://optimization-online.org/wp-content/uploads/2021/10/8656.pdf | A1-deterministic-atfm-r1; A2-uam-aam-ram-r1; B2-drone-uam-r2 | medium | (E) |
| 19 | Crainic, Hewitt, Maggioni, Rei — Partial Benders Decomposition: General Methodology and Application to Stochastic Network Design | Transportation Science 55(2), 2021 | 10.1287/trsc.2020.1022 | https://pubsonline.informs.org/doi/10.1287/trsc.2020.1022 | B2-network-design-uncertainty-r1 | high | (3) |
| 20 | Rahmaniani, Ahmed, Crainic, Gendreau, Rei — The Benders Dual Decomposition Method | Operations Research 68(3), 2020 | (not seen) | https://publications.polymtl.ca/45344 | B2-network-design-uncertainty-r1 | medium | (3) |

Secondary (adjacent venue, space logistics; pass-through):

| S1 | Chen, Ho — Integrated space logistics mission planning and spacecraft design with mixed-integer nonlinear programming | Journal of Spacecraft and Rockets 55(2), 2018 | (not seen) | https://researchwith.stevens.edu/en/publications/integrated-space-logistics-mission-planning-and-spacecraft-design/ | B2-time-windows-periodic-launch-r1 | medium |

Cross-references already in the pipeline and NOT duplicated here (different facet): Snyder & Daskin TS 2005 and
Cui/Ouyang/Shen OR 2010 (reliable facility location), Peng/Snyder/Lim/Liu TR-B 2011, Hewitt/Crainic/Nowak/Rei
TR-B 2019, Boland/Hewitt/Marshall/Savelsbergh OR 2017, Andreatta & Romanin-Jacur TS 1987 (single congested
hub, ATFM facet).

## 3. Seen by siblings but OUT of scope (not recorded)

- Campbell, Ernst, Krishnamoorthy — Hub Arc Location Problems I/II, Management Science 2005 (10.1287/mnsc.1050.0406).
- Contreras, Cordeau, Laporte — Stochastic uncapacitated hub location, EJOR 212(3) 2011.
- "Hub location with congestion and time-sensitive demand", EJOR 316(3):828-844, 2024 (arXiv 2401.07280) — the only
  congestion-hub sighting in the whole run, and it is EJOR.
- "Exact solution method for stochastic single-allocation hub location problems", TR Part E 202, 2025.
- "Distributionally Robust Chance-Constrained p-Hub Center Problem", INFORMS J. Computing (10.1287/ijoc.2022.0113).
- Elhedhli & Hu 2005 (C&OR), Elhedhli & Wu 2010 (IJOC), Alumur et al. 2018 (Appl. Math. Modelling) — congestion hub
  models in out-of-scope venues; Alumur & Kara 2008 and Alumur et al. 2021 (EJOR surveys).

## 4. Leads seen but venue NOT corroborated (do not record until verified)

- Bayram, Yildiz, Farham (2023) — hub network design with capacity, congestion and stochastic demand (believed TS).
- "Hub Network Design Problem with Capacity, Congestion and Heterogeneous Economies of Scale" — arXiv 2404.03521.
- "Multi-period hub-and-spoke network design considering flow-dependent economies of scale" — venue not shown.
- "Branch & Solve for Hub Location" — arXiv 2508.02665 (2025 preprint).

## 5. Verification queue for round 3 — facet anchors and classics (RECOLLECTION ONLY; verify before use)

Everything below is from memory of the literature, NOT from a search result in this run. Bibliographic details
may be wrong; DOIs deliberately omitted. One query each should settle them.

Sub-topic (1) capacitated / modular / congested hubs
- Correia, Nickel, Saldanha-da-Gama — "Single-assignment hub location problems with multiple capacity levels", TR-B 44(8-9), 2010.
  Query: Correia Nickel Saldanha-da-Gama "multiple capacity levels" "10.1016/j.trb"
- Taherkhani, Alumur, Hosseini — "Benders decomposition for the profit maximizing capacitated hub location problem with multiple demand classes", TS 54(6), 2020.
  Query: "profit maximizing capacitated hub location" "demand classes" "10.1287/trsc"
- de Camargo, de Miranda, Luna — "Benders decomposition for hub location problems with economies of scale", TS 43(1), 2009.
  Query: Camargo Miranda Luna "economies of scale" hub Benders "Transportation Science" 2009
- Serper, Alumur — "The design of capacitated intermodal hub networks with different vehicle types", TR-B 86, 2016.
  Query: Serper Alumur "intermodal hub networks" "different vehicle types" "Transportation Research Part B"
- Meng, Wang — "Intermodal hub-and-spoke network design: Incorporating multiple stakeholders and multi-type containers", TR-B 45(4), 2011.
  Query: Meng Wang "multi-type containers" hub-and-spoke "Transportation Research Part B"
- Merakli, Yaman — "Robust intermodal hub location under polyhedral demand uncertainty", TR-B 86, 2016.
  Query: Merakli Yaman "polyhedral demand uncertainty" hub "Transportation Research Part B"
- Alkaabneh, Diabat, Elhedhli — "A Lagrangian heuristic and GRASP for the hub-and-spoke network system with economies-of-scale and congestion", TR-C 102, 2019.
  Query: Alkaabneh Diabat Elhedhli congestion hub "Transportation Research Part C"
- Queueing-congestion location roots (facet asked for Elhedhli / Marianov-Serra style models "wherever they appear in TS or TR-B"):
  Berman, Larson, Parkan — "The stochastic queue p-median problem", TS 21(3), 1987. Query: "stochastic queue p-median" "Transportation Science"
  Berman, Larson, Chiu — "Optimal server location on a network operating as an M/G/1 queue", OR 33(4), 1985. Query: "M/G/1 queue" server location "Operations Research" 1985
  Marianov & Serra 2003 (C&OR) and Elhedhli & Hu 2005 (C&OR) are out of scope; search "hub" "congestion" "10.1016/j.trb" and "10.1287/trsc" to find any in-scope successor.

Sub-topic (2) time-definite and incomplete hub networks
- Yaman, Kara, Tansel — "The latest arrival hub location problem for cargo delivery systems with stopovers", TR-B 41(8), 2007.
  Query: "latest arrival hub location" stopovers "Transportation Research Part B"
- Alumur, Kara, Karasan — "The design of single allocation incomplete hub networks", TR-B 43(10), 2009.
  Query: "incomplete hub networks" single allocation "Transportation Research Part B" 2009
- Yaman — "The hierarchical hub median problem with single assignment", TR-B 43(6), 2009.
  Query: Yaman "hierarchical hub median" "Transportation Research Part B"
- O'Kelly, Bryan — "Hub location with flow economies of scale", TR-B 32(8), 1998.
  Query: O'Kelly Bryan "flow economies of scale" "10.1016/S0191-2615"
- Aykin — "Networking policies for hub-and-spoke systems with application to the air transportation system", TS 29(3), 1995.
  Query: Aykin "networking policies" hub-and-spoke "Transportation Science" 1995
- Racunica, Wynter — "Optimal location of intermodal freight hubs", TR-B 39(5), 2005.
  Query: Racunica Wynter "intermodal freight hubs" "Transportation Research Part B"
- Lin, Chen — "The hierarchical network design problem for time-definite express common carriers", TR-B 38(3), 2004; Lin — "The freight routing problem of time-definite freight delivery common carriers", TR-B 35(6), 2001.
  Query: Lin Chen "time-definite" express "hierarchical network design" "Transportation Research Part B"
- Martins de Sa, Contreras, Cordeau, de Camargo, de Miranda — "The hub line location problem", TS 49(3), 2015.
  Query: "hub line location problem" "Transportation Science"
- Classics on terminal/consolidation economics: Daganzo — "The break-bulk role of terminals in many-to-many logistic networks", OR 35(4), 1987; Hall — "Direct versus terminal freight routing on a network with concave costs", TR-B 21(4), 1987; Campbell — "Freight consolidation and routing with transportation economies of scale", TR-B 24(5), 1990.
  Queries: Daganzo "break-bulk" terminals "Operations Research" 1987 ; Hall "direct versus terminal" concave "Transportation Research Part B" ; Campbell "freight consolidation" "economies of scale" "Transportation Research Part B" 1990
- Airline hub-and-spoke design: Lederer, Nambimadom — "Airline network design", OR 46(6), 1998; Dobson, Lederer — "Airline scheduling and routing in a hub-and-spoke system", TS 27(3), 1993; Adler — "Hub-spoke network choice under competition with an application to Western Europe", TS 39(1), 2005.
  Queries: Lederer Nambimadom "airline network design" "Operations Research" ; Dobson Lederer hub-and-spoke "Transportation Science" 1993 ; Adler "hub-spoke network choice" "Transportation Science"

Sub-topic (3) exact large-scale methods and benchmarks
- Wandelt, Dai, Zhang, Sun — "Toward a reference experimental benchmark for solving hub location problems", TS 56(2), 2022.
  Query: Wandelt Dai Zhang Sun "benchmark" hub location "Transportation Science" 2022
- Maheo, Kilby, Van Hentenryck — "Benders decomposition for the design of a hub and shuttle public transit system", TS 53(1), 2019.
  Query: Maheo Kilby "Van Hentenryck" "hub and shuttle" "Transportation Science"
- Rostami, Chitsaz, Arslan, Laporte, Lodi — "Single allocation hub location with heterogeneous economies of scale", OR 70(2), 2022.
  Query: Rostami Chitsaz Arslan Laporte Lodi "heterogeneous economies of scale" "Operations Research"
- Ghaffarinasab, Cavus, Kara — "A mean-CVaR approach to the risk-averse single allocation hub location problem with flow-dependent economies of scale", TR-B 167, 2023; Ghaffarinasab, Kara, Campbell — "The stratified p-hub center and p-hub maximal covering problems", TR-B 157, 2022.
  Queries: Ghaffarinasab Kara "mean-CVaR" hub "Transportation Research Part B" ; Ghaffarinasab Kara Campbell "stratified p-hub" "Transportation Research Part B"
- Zetina, Contreras, Cordeau — "Profit-oriented fixed-charge network design with elastic demand", TR-B 127, 2019.
  Query: Zetina Contreras Cordeau "elastic demand" fixed-charge network design "Transportation Research Part B"
- Recency sweeps: "10.1287/trsc" hub location 2024 2025 2026 ; "10.1287/opre" hub location 2023 2024 2025 ; "10.1016/j.trb" hub location 2024 2025 ; "10.1016/j.trc" hub location vertiport 2023 2024 2025.

## 6. Transfer notes for the report writer (apply once the queue is verified)

- Capacitated / modular hubs (Correia et al. 2010; Taherkhani et al. 2020/2021; Puerto et al. 2016): discrete capacity
  levels at a hub = berthing/docking slots or propellant/payload storage modules at an orbital depot; demand classes with
  different revenues = payload classes (crew, priority cargo, bulk) with different willingness-to-pay; profit-maximizing
  variants let the model drop unprofitable spokes (spaceports) rather than serving all demand.
- Congestion (queueing-based) hubs: hub throughput as an M/M/c or M/D/c server maps directly to orbital-hub
  rendezvous/docking service rates; the convex delay term is the analog of phasing/waiting penalties for vehicles
  queued at a station. No in-scope corroborated paper yet — flag as gap.
- Time-definite and incomplete networks (Yaman et al. 2007; Alumur et al. 2009; Lin & Chen 2004): latest-arrival
  objectives with stopovers = delivery deadlines through intermediate transfer orbits; incomplete inter-hub graphs =
  only a subset of orbital transfer arcs (plane changes) are affordable; hierarchical designs = spaceport -> LEO depot
  -> higher-energy hub.
- Economies of scale on inter-hub arcs (O'Kelly & Bryan 1998; de Camargo et al. 2009; Rostami et al. 2022): piecewise
  concave arc costs = larger/consolidated transfer vehicles between depots being cheaper per kg.
- Exact methods (Contreras et al. 2011 OR; Benders dual decomposition; partial Benders; Euclidean cuts; Wandelt et al.
  benchmark): the Benders master (open hubs, assignments) / subproblem (O-D flows) split is the natural decomposition
  for a spaceport-to-orbit design with hundreds of spoke-hub-period combinations; benchmark instance sets (CAB, AP, TR)
  are the obvious templates for a public spaceport-feeder instance library.
- Uncertainty (Alumur et al. 2012; Zetina et al. 2017; Wang et al. 2020; An et al. 2015; the 2025 TS/OR items): demand
  and set-up-cost uncertainty, budgeted/polyhedral/moment-based ambiguity, and hub failure with backup routing map onto
  uncertain launch demand, cost overruns, and loss of a depot or launch site.
