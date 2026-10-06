# Facet c1-liner-feeder-shipping — round 3 notes (Topic B)

Facet: liner shipping network design, feeder network design and hub ports, transshipment vs multi-port calling,
fleet deployment and speed optimization, schedule design with transit-time constraints, empty container
repositioning, containership routing/scheduling reviews, tramp/industrial shipping, port-hub location for feeders,
liner shipping with uncertain demand. Venues: TS, TR-B, OR, TR-C.
Rounds 1 and 2 (B1-liner-feeder-shipping-r1.md, B1-liner-feeder-core-ts-trb-r2.md) recorded ZERO candidates
because every WebSearch was refused (shared budget exhausted). This round starts from scratch. Quota: 28.

## Query log (running count after each call)

1. "10.1287/trsc" liner shipping network design (standard) — count 1. HITS: Brouer et al. 10.1287/trsc.2013.0471; Agarwal&Ergun 10.1287/trsc.1070.0205; Koza/Desaulniers/Ropke 10.1287/trsc.2018.0888; "Network Design and Capacity Exchange for Liner Alliances..." 10.1287/trsc.2014.0572; ideas oropre v73y2025i4p1825-1848 (OR 2025, title unknown).
2. "10.1016/j.trb" liner shipping fleet deployment schedule design (standard) — count 2. HITS: Zhang/Zheng/Teo 2022 TR-B 155:499-525 doi 10.1016/j.trb.2021.11.010; Wang&Meng 2012 TR-B 46(5):615-633 (ideas transb v46y2012i5p615-633, schedule design w/ sea+port time uncertainty); Zhen/Hu/Wang/Laporte/Wu 2019 TR-B 120:15-32 doi 10.1016/j.trb.2018.11.011. Out-of-scope seen: Mulder&Dekker (TR-E), fleet deployment overview (TR-E), week-dependent demand (EJOR).
3. Agarwal Ergun "Ship scheduling and network design..." TS (standard) — count 3. Confirms TS 42(2):175-196, 2008; MILP, weekly frequency, transshipment; greedy, column generation, 2-phase Benders; 20 ports/100 ships instances.
4. Brouer Alvarez Plum Pisinger Sigurd LINER-LIB (standard) — count 4. Confirms TS 48(2):281-312 2014; strongly NP-hard; tabu + heuristic column generation; github LINERLIB.
5. Meng Wang Andersson Thun overview (standard) — count 5. Confirms TS 48(2):265-280 2014, pubsonline 10.1287/trsc.2013.0461. Also saw Wang&Meng "Schedule design and container routing in liner shipping" (TRR, out of scope).
6. Christiansen Fagerholt Ronen status and perspectives (standard) — count 6. Confirms TS 38(1):1-18 2004 via ideas ortrsc v38y2004i1p1-18.
7. Song Dong cargo routing + empty repositioning TR-B (standard) — count 7. Confirms TR-B 46(10):1556-1575 2012 via ideas transb v46y2012i10p1556-1575.
8. "10.1287/opre" liner/container/empty container (standard) — count 8. HITS: Cheung&Chen TS 10.1287/trsc.32.2.142 (1998); Agarwal&Ergun 2010 OR 10.1287/opre.1100.0848 (carrier alliances network design + allocation); Crainic/Gendreau/Dejax 1993 OR 10.1287/opre.41.1.102; TS 10.1287/trsc.2014.0572 again.
9. "10.1016/j.trb" container routing "transit time" liner OR containership (standard) — count 9. HITS: Wang/Meng/Liu 2013 TR-B 54:68-83 doi 10.1016/j.trb.2013.04.003 (ideas transb v54y2013icp68-83); Akyuz&Lee 2016 TR-B 88:46-71 doi 10.1016/j.trb.2016.02.007; Meng&Lee 2016 TR-B 90:135-155 (ideas transb v90y2016icp135-155). TR-E items seen (out).
10. "10.1016/j.trc" liner shipping OR container shipping network design OR schedule (standard) — count 10. No TR-C hits; repeats of TS Agarwal&Ergun and Koza et al.; EJOR/TR-E items (out). TR-C appears thin for liner shipping.
11. Karsten Ropke Pisinger sailing speed + container routing + transit time TS (standard) — count 11. Confirms TS 52(4):769-787 2018, pubsonline 10.1287/trsc.2018.0818; Benders + column generation exact algorithm.
12. Tierney Askelsdottir Jensen Pisinger LSFRP TS (standard) — count 12. Confirms TS 49(3):652-674 2015 via ideas ortrsc v49y2015i3p652-674; graph-based model + simulated annealing; real Maersk data.
13. feeder network design hub port container shipping TR-B/TS/TR-C (standard) — count 13. HIT: "Feeder vessel routing and transshipment coordination at a congested hub port" (TR-B per snippet; SMU repository, authors not shown -> follow-up). Others: HIT "hub port location and routing for a single hub feeder network" (venue unknown), NTNU feeder design (TR-E), IGI chapter (out).
14. Rana Vickson 1991 TS (standard) — count 14. Confirms TS 25(3):201-214, pubsonline 10.1287/trsc.25.3.201. Also saw ideas ortrsc v22y1988i2p83-95 (TS 1988, title not shown — likely Rana&Vickson time-chartered containership, wanted_not_seen) and Christiansen 1999 10.1287/trsc.33.1.3; Chalmers "two-stage stochastic nonlinear IP slot allocation liner" (venue not shown).
15. Christiansen 1999 decomposition inventory + time constrained ship routing TS (standard) — count 15. Confirms TS 33(1):3-16, doi 10.1287/trsc.33.1.3; Dantzig-Wolfe + B&B, ammonia fleet, time windows.
16. liner shipping network design 2024 2025 TS/TR-B (standard) — count 16. HITS: Wang/Liu/Meng 2015 TR-B 72:128-145 segment-based alteration (ideas transb v72y2015icp128-145); OR 2025 "A Simultaneous Column-and-Row Generation Solution Method for Liner Shipping Network Design" pubsonline 10.1287/opre.2020.0458 (published online 22 Apr 2025; authors not shown -> follow-up; matches ideas oropre v73y2025i4p1825-1848 from q1). Wang&Meng "Systematic network design..." is TRR (out).
17. "Feeder vessel routing and transshipment coordination at a congested hub port" TR-B (standard) — count 17. Confirms Jin/Meng/Wang 2021 TR-B 151:1-21 via ideas transb v151y2021icp1-21; arc-based MILP + set partitioning; branch-and-price (30 ports) + CG heuristic; limited berthing slots at hub. Also saw SMU "Column generation approach for feeder vessel routing and synchronization at a congested transshipment port" (venue not shown).
18. "Simultaneous Column-and-Row Generation" LSND OR (standard) — count 18. Confirms Xia/Xu/Baldacci OR 73(4):1825-1848 July 2025, doi 10.1287/opre.2020.0458; set-partitioning-like formulation, SCRG inside branch-and-price, exact.
19. hub-and-spoke / multi-port calling / transshipment hub LSND TR-B/TS (standard) — count 19. Only TR-E hits (Imai/Shintani/Papadimitriou 2009; Meng&Wang 2011 TR-E 47(5):695-708; Zheng/Meng/Sun TR-E 75:32-48) — all OUT of scope; none recorded.
20. Norstad Fagerholt Laporte tramp + speed TR-C (standard) — count 20. TR-C 19(5):853-865, 2011 per snippet (SINTEF/IAOR pages, no publisher URL) -> medium.
21. liner fleet deployment stochastic/uncertain demand TR-B (standard) — count 21. HIT: TR-B 2025 PII S0191261525000852 (PolyU PDF "1-s2.0-S0191261525000852-main.pdf"): fleet deployment + slot allocation, two-stage data-driven robust chance-constrained / DRO; title/authors not shown -> follow-up. Also "Robust ship fleet deployment with shipping revenue management" (PolyU; venue not shown). Meng/Wang/Wang 2012 is EJOR (out).
22. liner schedule recovery/disruption TR-B/TR-C 2023 2024 (standard) — count 22. No in-scope hits (TR-E 2023, JMSE, TR-D) — none recorded.
23. Erera Morales Savelsbergh robust empty repositioning OR (standard) — count 23. Confirms OR 57(2):468-483 2009, pubsonline 10.1287/opre.1080.0650; time-space network, interval uncertainty + budget, recoverable robustness.
24. maritime inventory routing OR/TS branch-price-and-cut (standard) — count 24. HITS: Engineer/Furman/Nemhauser/Savelsbergh/Song OR 2012 pubsonline 10.1287/opre.1110.0997; TS "A New Formulation Based on Customer Delivery Patterns for a Maritime Inventory Routing Problem" pubsonline 10.1287/trsc.2013.0503 (authors not in snippet; Rakke/Andersson/Christiansen/Desaulniers from memory — flagged). Snippet mentions a TS LNG branch-and-price IRP (Gronhaug et al.?) — wanted_not_seen.
25. TR-B 2025 fleet deployment + slot allocation DRO (standard) — count 25. Confirms Zhang/Wang/Xin 2025 TR-B 197, "Liner fleet deployment and slot allocation problem: a distributionally robust optimization model with joint chance constraints", doi 10.1016/j.trb.2025.103236 (ideas transb v197y2025ics0191261525000852). Also ideas transb v74y2015icp79-87 appeared next to PolyU "Robust ship fleet deployment with shipping revenue management" (pairing not explicit -> wanted_not_seen).
26. Wang Meng TR-B 2012 schedule design title (standard) — count 26. Confirms "Liner ship route schedule design with sea contingency time and port time uncertainty", TR-B 46(5):615-633; MINLP stochastic programme, ship + expected bunker cost, transit-time service level. "Robust schedule design for liner shipping services" is TR-E (out).
27. "10.1287/trsc.2022/2023/2024" liner/container/vessel (standard) — count 27. No 2022-2024 TS DOIs surfaced; HIT: TS "Joint Planning of Fleet Deployment, Speed Optimization, and Cargo Allocation for Liner Shipping" pubsonline 10.1287/trsc.2015.0625 (authors not in snippet; Xia/Li/Ma/Xu/Lee from memory — flagged). arXiv 2023 simultaneous speed/deployment/scheduling (not a venue).
28. "10.1016/j.trb.2022/2023/2024" liner/container/feeder (standard) — count 28. QUOTA REACHED. Gave Jin/Meng/Wang DOI 10.1016/j.trb.2021.07.002; otherwise TR-E/Transport Policy/EJOR (out).

## Searches used: 28 of 28 (all standard mode; 0 extended). Recency-targeted queries: q16, q21, q22, q25, q27, q28 (6). Pre-2005 classics: q6, q8, q14, q15 (4).

## Corroborated candidates (29) — see JSON for full fields

| # | Paper | Venue/year | DOI or URL evidence | Conf. |
|---|---|---|---|---|
| 1 | Brouer, Alvarez, Plum, Pisinger, Sigurd — A Base Integer Programming Model and Benchmark Suite for Liner-Shipping Network Design | TS 48(2) 2014 | 10.1287/trsc.2013.0471 | high |
| 2 | Agarwal, Ergun — Ship Scheduling and Network Design for Cargo Routing in Liner Shipping | TS 42(2) 2008 | 10.1287/trsc.1070.0205 | high |
| 3 | Koza, Desaulniers, Ropke — Integrated Liner Shipping Network Design and Scheduling | TS 2020 (year from memory) | 10.1287/trsc.2018.0888 | high |
| 4 | Zheng, Gao, Yang, Sun (authors/year from memory) — Network Design and Capacity Exchange for Liner Alliances with Fixed and Variable Container Demands | TS 2015 | 10.1287/trsc.2014.0572 | high (venue) |
| 5 | Zhang, Zheng, Teo — Schedule reliability in liner shipping timetable design: a convex programming approach | TR-B 155 2022 | 10.1016/j.trb.2021.11.010 | high |
| 6 | Wang, Meng — Liner ship route schedule design with sea contingency time and port time uncertainty | TR-B 46(5) 2012 | ideas transb v46y2012i5p615-633 | high |
| 7 | Zhen, Hu, Wang, Laporte, Wu — Fleet deployment and demand fulfillment for container shipping liners | TR-B 120 2019 | 10.1016/j.trb.2018.11.011 | high |
| 8 | Meng, Wang, Andersson, Thun — Containership Routing and Scheduling in Liner Shipping: Overview and Future Research Directions | TS 48(2) 2014 | 10.1287/trsc.2013.0461 | high |
| 9 | Christiansen, Fagerholt, Ronen — Ship Routing and Scheduling: Status and Perspectives | TS 38(1) 2004 | ideas ortrsc v38y2004i1p1-18 | high |
| 10 | Song, Dong — Cargo routing and empty container repositioning in multiple shipping service routes | TR-B 46(10) 2012 | ideas transb v46y2012i10p1556-1575 | high |
| 11 | Cheung, Chen — A Two-Stage Stochastic Network Model and Solution Methods for the Dynamic Empty Container Allocation Problem | TS 32(2) 1998 | 10.1287/trsc.32.2.142 | high |
| 12 | Agarwal, Ergun — Network Design and Allocation Mechanisms for Carrier Alliances in Liner Shipping | OR 2010 | 10.1287/opre.1100.0848 | high |
| 13 | Crainic, Gendreau, Dejax — Dynamic and Stochastic Models for the Allocation of Empty Containers | OR 41(1) 1993 | 10.1287/opre.41.1.102 | high |
| 14 | Wang, Meng, Liu — Containership scheduling with transit-time-sensitive container shipment demand | TR-B 54 2013 | 10.1016/j.trb.2013.04.003 | high |
| 15 | Akyüz, Lee — Service type assignment and container routing with transit time constraints and empty container repositioning for liner shipping service networks | TR-B 88 2016 | 10.1016/j.trb.2016.02.007 | high |
| 16 | Meng, Lee — Liner container assignment model with transit-time-sensitive container shipment demand | TR-B 90 2016 | ideas transb v90y2016icp135-155 | high |
| 17 | Karsten, Ropke, Pisinger — Simultaneous Optimization of Container Ship Sailing Speed and Container Routing with Transit Time Restrictions | TS 52(4) 2018 | 10.1287/trsc.2018.0818 | high |
| 18 | Tierney, Askelsdottir, Jensen, Pisinger — Solving the Liner Shipping Fleet Repositioning Problem with Cargo Flows | TS 49(3) 2015 | ideas ortrsc v49y2015i3p652-674 | high |
| 19 | Jin, Meng, Wang — Feeder vessel routing and transshipment coordination at a congested hub port | TR-B 151 2021 | 10.1016/j.trb.2021.07.002 | high |
| 20 | Rana, Vickson — Routing Container Ships Using Lagrangean Relaxation and Decomposition | TS 25(3) 1991 | 10.1287/trsc.25.3.201 | high |
| 21 | Christiansen — Decomposition of a Combined Inventory and Time Constrained Ship Routing Problem | TS 33(1) 1999 | 10.1287/trsc.33.1.3 | high |
| 22 | Wang, Liu, Meng — Segment-based alteration for container liner shipping network design | TR-B 72 2015 | ideas transb v72y2015icp128-145 | high |
| 23 | Xia, Xu, Baldacci — A Simultaneous Column-and-Row Generation Solution Method for Liner Shipping Network Design | OR 73(4) 2025 | 10.1287/opre.2020.0458 | high |
| 24 | Norstad, Fagerholt, Laporte — Tramp ship routing and scheduling with speed optimization | TR-C 19(5) 2011 | SINTEF/IAOR pages | medium |
| 25 | Zhang, Wang, Xin — Liner fleet deployment and slot allocation problem: a distributionally robust optimization model with joint chance constraints | TR-B 197 2025 | 10.1016/j.trb.2025.103236 | high |
| 26 | Erera, Morales, Savelsbergh — Robust Optimization for Empty Repositioning Problems | OR 57(2) 2009 | 10.1287/opre.1080.0650 | high |
| 27 | Engineer, Furman, Nemhauser, Savelsbergh, Song — A Branch-Price-and-Cut Algorithm for Single-Product Maritime Inventory Routing | OR 2012 | 10.1287/opre.1110.0997 | high |
| 28 | Rakke, Andersson, Christiansen, Desaulniers (authors/year from memory) — A New Formulation Based on Customer Delivery Patterns for a Maritime Inventory Routing Problem | TS 2015 | 10.1287/trsc.2013.0503 | high (venue) |
| 29 | Xia, Li, Ma, Xu, Lee (authors/year from memory) — Joint Planning of Fleet Deployment, Speed Optimization, and Cargo Allocation for Liner Shipping | TS 2015 | 10.1287/trsc.2015.0625 | high (venue) |

## Wanted but not seen (for a later pass)
- Rana & Vickson 1988 TS 22(2):83-95 (ideas ortrsc v22y1988i2p83-95 seen, title not shown) — time-chartered containership routing.
- Wang/Wang/Meng ~2015 "Robust ship fleet deployment with shipping revenue management" — TR-B 74:79-87 likely (ideas transb v74y2015icp79-87 seen next to PolyU page).
- Wang/Meng/Wang/Qu ~2021 "A two-stage stochastic nonlinear integer-programming model for slot allocation of a liner container shipping service" — TR-B? (Chalmers page, venue not shown).
- Gronhaug/Christiansen/Desaulniers/Desrosiers ~2010 LNG inventory routing branch-and-price — TS (mentioned in q24 snippet only).
- Jin et al. "Column generation approach for feeder vessel routing and synchronization at a congested transshipment port" — venue unknown (SMU page).
- "Hub port location and routing for a single hub feeder network..." (HIT page) — venue unknown.
- Meng & Wang 2011 "Intermodal hub-and-spoke network design: incorporating multiple stakeholders and multi-type containers" — TR-B (not surfaced).
- Ng ~2015 "Container vessel fleet deployment for liner shipping with stochastic dependencies in shipping demand" — TR-B? (not surfaced).
- Reinhardt & Pisinger "A branch and cut algorithm for the container shipping network design problem" — FSM (likely out of scope).
- Christiansen/Fagerholt/Nygreen/Ronen 2013 "Ship routing and scheduling in the new millennium" — EJOR (facet brief said TS 2013; likely out of scope).

## Out-of-scope items seen (not recorded): Imai/Shintani/Papadimitriou 2009 TR-E; Meng&Wang 2011 TR-E 47(5); Zheng/Meng/Sun TR-E 75; Mulder&Dekker TR-E; Msakni et al. TR-E; Meng/Wang/Wang 2012 EJOR; Plum/Pisinger/Sigurd EJOR 235; Wang&Meng TRR items; Kjeldsen weekly delivery patterns (MEL); several JMSE/TR-D recovery papers.

## Transfer notes (Topic B) grounded in recorded papers
- Cyclic rotations with weekly frequency and "ships on route = round-trip time / headway" (Agarwal&Ergun 2008; Brouer et al. 2014; Koza et al. 2020) = launch cadence with reusable-vehicle turnaround.
- Per-leg capacity = vessel capacity x frequency, with demand rejection/penalty (Brouer 2014; Zhen 2019; Meng&Lee 2016) = per-window lift capacity at spokes.
- Transshipment at hub ports with connection synchronisation and limited berth slots (Jin/Meng/Wang 2021; Akyuz&Lee 2016) = payload transfer at orbital depot with docking-slot constraints.
- Transit-time / level-of-service limits and speed-time trade-offs (Karsten 2018; Wang/Meng/Liu 2013; Koza 2020) = phasing windows and max time-to-orbit.
- Demand uncertainty via stochastic programming / DRO / robust time-space flows (Wang&Meng 2012; Zhang/Wang/Xin 2025; Erera 2009; Cheung&Chen 1998; Crainic 1993) = uncertain manifest demand and launch slips.
- Fleet repositioning between rotations (Tierney 2015) = re-basing reusable vehicles among spaceports.
