# Facet B1 liner-feeder-shipping — round 1 notes

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Facet: liner shipping network design, feeder network design and hub ports, transshipment vs multi-port calling,
fleet deployment and speed optimization, schedule design with transit-time constraints, empty container
repositioning, containership routing/scheduling reviews, tramp/industrial shipping, port-hub location for feeders.
In-scope venues: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).

## STATUS: NO SEARCHES COULD BE EXECUTED IN THIS ROUND

Every WebSearch call issued by this agent was refused with:
"this turn's web search budget is used up (limit: 200 WebSearch calls per turn, shared by every agent in it)".
WebFetch, curl, wget and all other network paths are blocked by the egress proxy, and the budget notice
explicitly forbids working around the limit. Consequently:

- Zero search results were obtained for this facet.
- Zero candidates are recorded (task rule: never record a paper from memory alone; never invent a DOI).
- The structured output for this facet has an EMPTY candidates list. This is a coverage gap, not a finding
  that the literature is empty — the liner-shipping / feeder-network literature in TS, OR, TR-B and TR-C is
  large and directly relevant to spoke-to-hub feeder design with capacitated, time-windowed vehicles.
- Recommended remedy: re-run this facet in a follow-up round (r2) once the per-turn search budget resets, or
  raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION.

Sibling notes in this directory were checked for corroborated liner-shipping items that could be reused:
B1-hub-location-r1.md, B1-service-network-design-r1.md, B2-network-design-uncertainty-r1.md and
B2-time-windows-periodic-launch-r1.md mention only hub-location items (Alumur/Nickel/Saldanha-da-Gama 2012;
a URL-less mention of Meng & Wang 2011 intermodal hub-and-spoke) that belong to other facets. None are
liner-shipping or feeder-network papers, so nothing was borrowed. The verified/ and synthesis/ folders are empty.

## Queries issued (all refused — budget exhausted; none returned results)

1. liner shipping network design "Transportation Science" Brouer Pisinger  (standard) — NOT EXECUTED
2. "Operations Research" INFORMS ship scheduling and network design for cargo routing in liner shipping Agarwal Ergun  (standard) — NOT EXECUTED
3. containership routing and scheduling in liner shipping overview "Transportation Science" Meng Wang Andersson Thun  (standard) — NOT EXECUTED
4. feeder network design hub port container "Transportation Research Part B"  (standard) — NOT EXECUTED
5. liner ship fleet deployment "Transportation Research Part B" Meng Wang  (standard) — NOT EXECUTED
6. hub-and-spoke versus multi-port-calling container liner shipping network design Transportation Research Part E / Part B  (standard) — NOT EXECUTED

## Planned query programme for round 2 (not yet run)

Methodology / problem phrases, each to be paired with the four venue restrictors and the DOI-prefix strings
("10.1287/trsc", "10.1287/opre", "10.1016/j.trb", "10.1016/j.trc"):

- "liner shipping network design" benchmark LINER-LIB; "service network design" liner; "cargo routing" liner
- "feeder network" OR "feeder service" container shipping hub port; "hub-and-spoke" "multi-port calling" liner
- "fleet deployment" liner; "speed optimization" OR "sailing speed" liner; "schedule design" "transit time" liner
- "empty container repositioning"; "container repositioning" stochastic / robust
- "ship routing and scheduling" review; "maritime transportation" review; "tramp shipping" network design
- "transshipment" hub port location; "port selection" feeder; "weekly frequency" "number of ships" liner
- "liner shipping" "column generation"; "liner shipping" "Benders"; "liner shipping" "branch-and-price"
- recency: add 2023 / 2024 / 2025 / 2026 to at least six of the above
- classics (pre-2005): Ronen 1983 / 1993 ship scheduling reviews; Christiansen Fagerholt Ronen 2004 TS review;
  Rana & Vickson 1991 TS routing container ships; Perakis & Jaramillo 1991 fleet deployment; Fagerholt 1999 feeder
- author surnames: Meng, Wang (Shuaian), Zheng (Jianfeng), Christiansen, Fagerholt, Pisinger, Brouer, Agarwal,
  Ergun, Song (Dong-Ping), Dong (Jing-Xin), Notteboom, Gelareh, Nickel, Reinhardt, Karsten, Plum, Alvarez,
  Vaaben, Andersson, Thun, Ronen, Nygreen, Hvattum, Fagerholt, Psaraftis, Kontovas, Ng (ManWo), Bell, Liu,
  Mulder, Dekker, Zhen (Lu), Shen, Du, Qi

## Seed list of search TARGETS from recollection — UNVERIFIED, NOT submitted as candidates

These are titles/authors the round-2 agent should try to corroborate. They are from memory only: years,
exact titles and venues may be imprecise and NO DOIs are given. They are deliberately excluded from the
structured candidates list because no search result corroborated them in this round.

Liner shipping network design (TS / OR):
- Agarwal & Ergun, "Ship scheduling and network design for cargo routing in liner shipping" — TS ~2008
- Brouer, Alvarez, Plum, Pisinger, Sigurd, "A base integer programming model and benchmark suite for liner-shipping
  network design" — TS ~2014 (LINER-LIB)
- Alvarez, "Joint routing and deployment of a fleet of container vessels" — Maritime Econ & Logistics (adjacent)
- Reinhardt & Pisinger, "A branch and cut algorithm for the container shipping network design problem" — Flexible
  Services & Manufacturing (adjacent, check)
- Plum, Pisinger, Sigurd, "A service flow model for the liner shipping network design problem" — EJOR (adjacent)
- Karsten, Brouer, Pisinger, "Competitive liner shipping network design" — C&OR (adjacent, check)
- Karsten, Ropke, Pisinger, "Simultaneous optimization of container ship sailing speed and container routing with
  transit time restrictions" — TS ~2018
- Brouer, Desaulniers, Pisinger, "A matheuristic for the liner shipping network design problem" — TR-E (adjacent)
- Wang & Meng, "Liner shipping network design with deadlines" — C&OR (adjacent, check)
- Zheng, Meng, Sun, "Liner hub-and-spoke shipping network design" — TR-E (adjacent, check)
- Meng & Wang, "Liner shipping service network design with empty container repositioning" — TR-E (adjacent, check)
- Wang, Meng, Bell, "Liner ship route capacity utilization estimation..." (check venue)

Fleet deployment / speed / schedule design (TR-B / TS):
- Meng & Wang, "Liner shipping service network design..." / "Liner ship fleet deployment with week-dependent
  container shipment demand" — EJOR (adjacent)
- Wang & Meng, "Liner ship fleet deployment with container transshipment operations" — TR-E (adjacent, check)
- Wang & Meng, "Robust schedule design for liner shipping services" — TR-E (adjacent, check)
- Wang & Meng, "Sailing speed optimization for container ships in a liner shipping network" — TR-E (adjacent)
- Wang, Meng, Liu, "Containership scheduling with transit-time-sensitive container shipment demand" — TR-B ~2013
- Wang & Meng, "Liner shipping network design with deadlines" / "Schedule design and container routing in liner
  shipping" — check TR-B / TRR
- Ng, "Distribution-free vessel deployment for liner shipping" — EJOR (adjacent); Ng, "Container vessel fleet
  deployment for liner shipping with stochastic dependencies in shipping demand" — TR-B ~2015
- Zhen, Wang, Wang, "Optimization of liner shipping service network..." (check)

Reviews:
- Meng, Wang, Andersson, Thun, "Containership routing and scheduling in liner shipping: overview and future research
  directions" — TS ~2014
- Christiansen, Fagerholt, Ronen, "Ship routing and scheduling: status and perspectives" — TS ~2004
- Christiansen, Fagerholt, Nygreen, Ronen, "Ship routing and scheduling in the new millennium" — EJOR (adjacent)
- Ronen, "Cargo ships routing and scheduling: survey of models and problems" — EJOR 1983 (adjacent)
- Tran & Haasis, "Literature survey of network optimization in container liner shipping" — FSM (adjacent)

Empty container repositioning:
- Song & Dong, "Cargo routing and empty container repositioning in multiple shipping service routes" — TR-B ~2012
- Song & Dong, "Long-haul liner service route design with ship deployment and empty container repositioning" —
  TR-B ~2013
- Crainic, Gendreau, Dejax, "Dynamic and stochastic models for the allocation of empty containers" — OR 1993
- Cheung & Chen, "A two-stage stochastic network model and solution methods for the dynamic empty container
  allocation problem" — TS 1998
- Erera, Morales, Savelsbergh, "Robust optimization for empty repositioning problems" — OR ~2009
- Shintani, Imai, Nishimura, Papadimitriou, "The container shipping network design problem with empty container
  repositioning" — TR-E (adjacent)

Hub ports / feeder / transshipment (TR-B / TR-E):
- Gelareh, Nickel, Pisinger, "Liner shipping hub network design in a competitive environment" — TR-E (adjacent)
- Gelareh & Pisinger, "Fleet deployment, network design and hub location of liner shipping companies" — TR-E (adjacent)
- Imai, Shintani, Papadimitriou, "Multi-port vs hub-and-spoke port calls by containerships" — TR-E (adjacent)
- Meng & Wang, "Intermodal hub-and-spoke network design: incorporating multiple stakeholders and multi-type
  containers" — TR-B ~2011 (also cited by hub-location facet)
- Hsu & Hsieh, "Routing, ship size, and sailing frequency decision-making for a maritime hub-and-spoke container
  network" — Math & Comp Modelling (adjacent)
- Fagerholt, "Optimal fleet design in a ship routing problem" — ITOR (adjacent)
- Polat, Günther, Kulak, "The feeder network design problem: application to container services in the Black Sea
  region" — Maritime Econ & Logistics (adjacent)
- Santini, Plum, Ropke, "A branch-and-price approach to the feeder network design problem" — EJOR (adjacent)
- Msakni, Fagerholt, Meisel, Lindstad, "Analyzing different designs of liner shipping feeder networks: a case study"
  — TR-E (adjacent, check)

Tramp / industrial / inventory routing (TS / OR / TR-B):
- Christiansen, "Decomposition of a combined inventory and time constrained ship routing problem" — TS 1999
- Fagerholt & Christiansen, "A combined ship scheduling and allocation problem" — JORS (adjacent)
- Brønmo, Christiansen, Fagerholt, Nygreen, "A multi-start local search heuristic for ship scheduling — a
  computational study" — C&OR (adjacent)
- Hemmati, Hvattum, Fagerholt, Norstad, "Benchmark suite for industrial and tramp ship routing and scheduling
  problems" — INFOR (adjacent)
- Norstad, Fagerholt, Laporte, "Tramp ship routing and scheduling with speed optimization" — TR-C ~2011
- Andersson, Christiansen, Fagerholt, "The maritime pickup and delivery problem with time windows and split loads" —
  INFOR (adjacent)
- Halvorsen-Weare & Fagerholt, "Routing and scheduling in a liquefied natural gas shipping problem with inventory and
  berth constraints" — Annals of OR (adjacent)

Transfer notes for the spaceport-to-orbit feeder problem (for the writer; based on the facet brief, not on
verified sources): liner-shipping network design is the closest commercial analogue of a periodic, capacitated,
hub-and-spoke feeder system — weekly frequency maps to launch cadence, vessel capacity to payload mass/volume,
transit-time constraints to orbital-phasing windows, fleet deployment with round-trip time to reusable-vehicle
turnaround, and hub ports to orbital depots. Empty-container repositioning is the analogue of returning reusable
stages/capsules or empty payload adapters. None of these transfer statements is sourced in this round.
