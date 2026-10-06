# Facet A2: UAM / AAM / RAM traffic management and network operations (round 1)

Date: 2026-10-06. Agent: facet uam-aam-ram.

## IMPORTANT LIMITATION
The WebSearch tool is the only route to the internet here. After 12 queries the
shared per-turn WebSearch budget (200 calls across all agents) was exhausted and
every further query was refused. Queries 13-20 below were submitted but NOT
executed. Only papers corroborated by an executed search are recorded as
candidates. Coverage of this facet is therefore partial (about 7 in-scope TR-C
items plus 2 adjacent-venue items against a target of 25-45). A second round is
needed; the unexecuted queries and the leads list at the bottom give the plan.

## Queries executed (12)
1. vertiport scheduling eVTOL "Transportation Research Part C"
2. urban air mobility demand capacity balancing "Transportation Research Part C"
3. "urban air mobility" "Transportation Science" INFORMS
4. UTM strategic deconfliction pre-departure scheduling "10.1016/j.trc"
5. Kleinbekman Mitici Wei eVTOL arrival sequencing vertiport
6. Rimjha Trani regional air mobility demand "Transportation Research Part C"
7. site:sciencedirect.com "urban air mobility" eVTOL scheduling vertiport Transportation Research Part C
8. "Terminal area control rules and eVTOL adaptive scheduling model for multi-vertiport system" Transportation Research Part C
9. "Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility" Delahaye Transportation Research Part C
10. "Automated flight planning of high-density urban air mobility" Transportation Research Part C
11. Willey Salmon "urban air mobility network design" hub location subgraph isomorphism Transportation Research Part C
12. Song Yeo "optimal scheduling strategy and approach control model" multicopter VTOL urban air mobility Transportation Research Part C

## Queries submitted but refused (budget exhausted)
13. "10.1016/j.trc.2021.103385" OR "10.1016/j.trc.2021.103181" OR "10.1016/j.trc.2020.102997" urban air mobility
14. Wang Delahaye Farges Alam "quasi-dynamic air traffic assignment" UAM Transportation Research Part C 2023
15. "On-demand ridesharing based on dynamic scheduling in urban air mobility" Transportation Research Part C 2025
16. "Vertiport capacity planning and operations for urban air mobility commuting"
17. Sunil Ellerbroek Hoekstra "conflict count models" layered airspace Transportation Research Part C
18. Pang Low Duong UAM traffic flow optimization time-space network Transportation Research Part C
19. Cummings Mahmassani urban air mobility congestion simulation Transportation Research Part C
20. Zulqarnain Lee vertiport location air taxi optimization

## Candidates (in-scope venues)

### C1. Shao, Shao, Lu (2021) TR-C 132, art. 103385
- Title: Terminal area control rules and eVTOL adaptive scheduling model for multi-vertiport system in urban air mobility
- Corroboration: query 8 summary (title, authors Quan Shao, Mengxue Shao, Yang Lu, venue TR-C vol 132 art 103385, 2021); also referenced in query 1 and 7 summaries.
- URL seen: https://arxiv.org/pdf/2408.01152 (citing paper) ; venue stated in search summary. DOI not displayed -> "".
- Confidence: medium.

### C2. Song, Yeo (2021) TR-C 128, art. 103181
- Title: Development of optimal scheduling strategy and approach control model of multicopter VTOL aircrafts for urban air mobility (UAM) operation
- Corroboration: query 12 (KAIST pages https://dspace.kaist.ac.kr/handle/10203/286733 , https://smartcity.kaist.ac.kr/2021/07/an-article-development-of-optimal.html ); query 7 summary gives vol 128, 103181 (2021).
- Method (from snippets): three approach-control/scheduling strategies (BQA branch queuing approach, SBA sequence-based approach, SBAM sequence-based with moving circles) compared by simulation on punctuality and loss-of-separation risk; BQA found most efficient with no LOS risk.
- DOI not displayed -> "". Confidence: medium.

### C3. Tang, Zhang, Mohmoodian, Charkhgard (2021) TR-C 131
- Title: Automated flight planning of high-density urban air mobility
- Corroboration: query 10 summary (authors Hualong Tang, Yu Zhang, Vahid Mohmoodian, Hadi Charkhgard; TR-C vol 131, Oct 2021); supporting pages: USF dissertation https://digitalcommons.usf.edu/etd/10410 , Berkeley tech-transfer slides, USPTO patent.
- Method (from snippets): semi-structured airspace with layered topology and direct routes between entry/exit points; conflict-free 4D trajectory generation for medium-to-high-density UAM.
- DOI not displayed -> "". Confidence: medium.

### C4. Willey, Salmon (2021) TR-C 125, art. 102997
- Title: A method for urban air mobility network design using hub location and subgraph isomorphism
- Corroboration: query 11 summary (Landon C. Willey, John L. Salmon; TR-C vol 125, art 102997, April 2021); cited on INFORMS references page https://pubsonline.informs.org/doi/references/10.1287/msom.2022.1148
- DOI not displayed -> "". Confidence: medium.

### C5. Wang, Delahaye, Farges, Alam (2022) "Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility operations"
- Corroboration: query 9 summary described the model (macroscopic traffic assignment on multilayer network, Linear Dynamical System complexity metric, two-step method based on Dafermos' algorithm, two-layer case study). HAL pages https://hal-enac.archives-ouvertes.fr/hal-03701655 and https://hal.archives-ouvertes.fr/hal-03082598 (the latter is the earlier JAIS paper "Air Traffic Assignment for Intensive Urban Air Mobility Operations").
- Venue: believed TR-C 2022 but NOT shown in snippet -> confidence LOW; verify before use.

### C6. Wang, Delahaye, Farges, Alam (2023) "A quasi-dynamic air traffic assignment model for mitigating air traffic complexity and congestion for high-density UAM operations"
- Corroboration: query 9 summary described QATA (allocate flows among routes over planning horizon, network dynamics, LDS complexity + congestion objective, centralized strategic planning).
- Venue: believed TR-C 2023 but NOT shown -> confidence LOW; verify (query 14 was refused).

### C7. (authors not captured) (2025) "On-demand ridesharing based on dynamic scheduling in urban air mobility"
- Corroboration: query 7: Beihang University research portal https://research.buaa.edu.cn/en/publications/on-demand-ridesharing-based-on-dynamic-scheduling-in-urban-air-mo/ ; search summary states TR-C, June 2025.
- Authors not visible in snippet. Confidence: medium on venue, authors missing.

## Candidates (adjacent venues, tagged adjacent-venue)

### S1. Kleinbekman, Mitici, Wei (2020) Journal of Aerospace Information Systems
- Title: Rolling-horizon electric vertical takeoff and landing arrival scheduling for on-demand urban air mobility
- Corroboration: query 5 and 8: https://research.tudelft.nl/en/publications/rolling-horizon-electric-vertical-takeoff-and-landing-arrival-sch ; TU Delft repository file; DASC 2018 precursor https://www.aere.iastate.edu/~pwei/proceedings/dasc18_imke.pdf
- Method (snippet): MILP assigning required times of arrival to arriving eVTOLs competing for terminal airspace and pads, battery-energy and performance constraints, rolling horizon, minimise total arrival delay.

### S2. Wang (Kai), Jacquillat, Vaze (2022) Manufacturing & Service Operations Management
- Title: Vertiport Planning for Urban Aerial Mobility: An Adaptive Discretization Approach
- Corroboration: query 11: https://pubsonline.informs.org/doi/references/10.1287/msom.2022.1148 (DOI visible in URL).
- Confidence high.

## Leads seen but NOT recorded (venue unverified or out of scope)
- "Vertiport capacity planning and operations for urban air mobility commuting" (TRID https://trid.trb.org/View/2737035) - venue unknown.
- "On-demand urban air mobility scheduling with operational considerations" JAIS DOI 10.2514/1.i011460 (citedrive) - authors not captured; JAIS.
- Rimjha, Hotle, Trani, Hinze (2021) UAM commuter demand / feasibility Northern California, Transportation Research Part A 148: 506-524 (ideas.repec.org) - TR-A out of scope; demand not traffic management.
- Kleinbekman, Mitici, Wei (2018) eVTOL arrival sequencing and scheduling for on-demand UAM, DASC 2018 - conference.
- arXiv 2008.05535 "Analysis of Fleet Management and Network Design for On-Demand Urban Air Mobility Operations" - journal venue unknown.
- arXiv 2305.10556 "Integrated Conflict Management for UAM with Strategic Demand Capacity Balancing and Learning-based Tactical Deconfliction" - journal venue unknown.
- arXiv 2408.01152 "Vertiport Terminal Scheduling and Throughput Analysis for Multiple Surface Directions" (MILP) - preprint.
- arXiv 2401.04851 graph-learning fleet scheduling; arXiv 2403.18166 auction-based vertiport reservation - preprints.
- TUM "Hierarchical Vertiport Network for an UAM System: Munich" - venue unknown.
- NASA NTRS DCB reports (Lee DASC 2022; 20240007944; 20240011341; 20250009400) - technical reports / conferences.
- EconPapers RePEc:eee:transa:v:192:y:2025 - TR-A 2025, title not shown.
- INFORMS Open Forum: "Operations Management for Urban Air Mobility" session, INFORMS 2023 Phoenix - no paper.
- Mahmassani group UAM "system fundamental diagram" microscopic simulation work (its.ucdavis.edu seminar page) - venue unknown; candidate for query 19.

## Plan for round 2 (not executed)
- Verify venues/DOIs for C1-C7 with DOI-string queries.
- Author sweeps still pending: Bosson/Lauderdale, Guo, Hansen, Kohlman/Patterson, Sun/Wandelt, Rajendran, Zulqarnain, Shihab, Vascik/Hansman, Pradeep, Straubinger/Rothfeld, Alonso-Mora, Zhao, Mendonca.
- Venue sweeps pending: TR-B + UAM; Transportation Science + air taxi/eVTOL; Operations Research + urban air mobility; "10.1016/j.trc" + "advanced air mobility" 2024/2025/2026; "regional air mobility" electric aircraft charging TR-C; UTM/U-space drone traffic TR-C; Sunil/Ellerbroek/Hoekstra airspace structure TR-C 2018; Pang/Low/Duong TR-C; Cummings/Mahmassani TR-C.
- Pre-2005 classics pending: free-flight airspace capacity (TS/OR), small aircraft transportation system / thin-haul, helicopter or air-taxi scheduling in Transportation Science.
