# Facet B1 — retry-not-found (round 2): re-search of 22 specific papers an earlier pass could not corroborate

Overall topic: Topic B — Spaceport-to-Orbit feeder network design, OR methodology analogs.
Venues in scope: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc),
TR Part B (10.1016/j.trb, 0191-2615), TR Part C (10.1016/j.trc, 0968-090X).
Agent: literature-search subagent, facet retry-not-found (r2). Date: 2026-10-06.

## STATUS: NO SEARCH COULD BE EXECUTED — 4 PASS-THROUGH CANDIDATES, 18 TARGETS SKIPPED

The per-turn WebSearch budget (200 calls, shared by every agent in this workflow turn) was already
exhausted when this agent issued its first batch of six queries; all six were refused with
"Web search was not performed: this turn's web search budget is used up". WebSearch is the only
route to the internet in this environment (WebFetch, curl, wget and pip are blocked by the egress
proxy) and the budget notice forbids working around the limit, so no further query was attempted.

Fallback performed (no internet needed): every notes file under research_notes/ and every
verified/*.ndjson record left by sibling agents in this run was grepped for each of the 22 target
papers (author surnames and title fragments). For each target the question asked was: did ANY
executed search in this run return a publisher page, DOI link or reputable index page showing the
title and venue? Only four targets pass that test. The remaining eighteen appear in sibling notes
solely as planned/refused queries or as "from recollection" verification queues, which under the
facet rules ("never record a paper from memory alone; never invent a DOI; a wrong venue or an
invented paper is worse than a missing one") is not corroboration. They are therefore SKIPPED, as
the facet brief instructs ("otherwise skip them").

Note on one misleading sibling line: B1-air-cargo-express-airline-network-r1.md says the hub-location
facet "corroborated ... O'Kelly & Bryan TR-B 1998, Yaman/Kara/Tansel TR-B 2007". Inspection of
B1-hub-location-r1.md shows both titles appear only in its "Verification queue for round 2 ...
NOT recorded here" section (the queries for them were refused). They are NOT corroborated.

Remedy: the user can send a follow-up message (new turn, fresh budget) or raise
CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION; the round-3 query plan below is ready to run as-is.

## Queries issued this round — ALL REFUSED (budget exhausted; none executed)

1. Contreras Cordeau Laporte "Benders decomposition for large-scale uncapacitated hub location" Operations Research  (standard) — REFUSED
2. Agarwal Ergun "Ship scheduling and network design for cargo routing in liner shipping" Transportation Science  (standard) — REFUSED
3. Brouer Alvarez Plum Pisinger Sigurd "base integer programming model and benchmark suite for liner-shipping network design"  (standard) — REFUSED
4. Koza Desaulniers Ropke "Integrated liner shipping network design and scheduling" Transportation Science  (standard) — REFUSED
5. Meng Wang Andersson Thun "Containership routing and scheduling in liner shipping: overview and future research directions"  (standard) — REFUSED
6. Armacost Barnhart Ware "Composite variable formulations for express shipment service network design" Operations Research  (standard) — REFUSED

## Target-by-target disposition (22 targets)

| # | Target (as given in facet brief) | Seen in any executed search this run? | Disposition |
|---|----------------------------------|----------------------------------------|-------------|
| 1 | Contreras, Cordeau, Laporte — Benders Decomposition for Large-Scale Uncapacitated Hub Location (OR 2011) | YES — B2-network-design-uncertainty-r1 query 7 returned researchportal.bath.ac.uk page + CIRRELT-2010-26 PDF; DOI 10.1287/opre.1110.0965 recorded by that agent | RECORDED (pass-through, medium) |
| 2 | Agarwal, Ergun — Ship Scheduling and Network Design for Cargo Routing in Liner Shipping (TS 2008) | NO — only planned/refused queries (B1-liner-feeder r1, r2) | SKIPPED |
| 3 | Brouer, Alvarez, Plum, Pisinger, Sigurd — A Base Integer Programming Model and Benchmark Suite for Liner-Shipping Network Design (TS 2014) | NO — planned/refused only | SKIPPED |
| 4 | Koza, Desaulniers, Ropke — Integrated Liner Shipping Network Design and Scheduling (TS 2020) | NO — planned/refused only | SKIPPED |
| 5 | Meng, Wang, Andersson, Thun — Containership Routing and Scheduling in Liner Shipping: Overview and Future Research Directions (TS 2014) | NO — planned/refused only | SKIPPED |
| 6 | Armacost, Barnhart, Ware — Composite Variable Formulations for Express Shipment Service Network Design (OR 2002) | NO — planned/refused only (facet brief says OR; sibling memory says TS 36(1); venue itself unresolved) | SKIPPED |
| 7 | Barnhart, Schneur — Air Network Design for Express Shipment Service (OR 1996) | NO — planned/refused only | SKIPPED |
| 8 | Kim, Barnhart, Ware, Reinhardt — Multimodal Express Package Delivery: A Service Network Design Application (TS 1999) | NO — planned/refused only | SKIPPED |
| 9 | Derigs, Friederichs, Schafer — A New Approach for Air Cargo Network Planning (TS 2009) | NO — planned/refused only | SKIPPED |
| 10 | Lin, Chen — The hierarchical network design problem for time-definite express common carriers (TR-B 2004) | NO — appears only in hub-location r1 "verification queue (NOT recorded)" | SKIPPED |
| 11 | Correia, Nickel, Saldanha-da-Gama — Single-assignment hub location problems with multiple capacity levels (TR-B 2010) | NO — verification queue only | SKIPPED |
| 12 | Yaman, Kara, Tansel — The latest arrival hub location problem for cargo delivery systems with stopovers (TR-B 2007) | NO — query refused in hub-location r1; verification queue only | SKIPPED |
| 13 | O'Kelly, Bryan — Hub location with flow economies of scale (TR-B 1998) | NO — query refused in hub-location r1; verification queue only | SKIPPED |
| 14 | Zhu, Crainic, Gendreau — Scheduled Service Network Design for Freight Rail Transportation (OR 2014) | YES — B2-time-windows-periodic-launch-r1 query 27 returned https://pubsonline.informs.org/doi/suppl/10.1287/opre.2013.1254 (OR 62(2):383-400) | RECORDED (pass-through, high) |
| 15 | Pedersen, Crainic, Madsen — Models and Tabu Search Metaheuristics for Service Network Design with Asset-Balance Requirements (TS 2009) | NO — queries refused in B1-SND r1 (q7) and B2-fleet-sizing r1 (q40); mention in "why these belong" section is from memory | SKIPPED |
| 16 | Lium, Crainic, Wallace — A Study of Demand Stochasticity in Service Network Design (TS 2009) | YES — B2-network-design-uncertainty-r1 query 2 returned eprints.lancs.ac.uk/id/eprint/45407, iaorifors.com/paper/64598, CIRRELT-2007-22 PDF; TS 43(2):144-157; DOI not seen | RECORDED (pass-through, medium) |
| 17 | Hewitt, Crainic, Nowak, Rei — Scheduled service network design with resource acquisition and management under uncertainty (TR-B 2019) | YES — B2-network-design-uncertainty-r1 query 9 returned ideas.repec.org/a/eee/transb/v128y2019icp324-343.html + scholars.luc.edu page; DOI 10.1016/j.trb.2019.08.008 recorded by that agent | RECORDED (pass-through, medium) |
| 18 | Perboli, Tadei, Vigo — The Two-Echelon Capacitated Vehicle Routing Problem: Models and Math-Based Heuristics (TS 2011) | NO — refused in multi-echelon r1 and two-echelon r2 | SKIPPED |
| 19 | Baldacci, Mingozzi, Roberti, Wolfler Calvo — An Exact Algorithm for the Two-Echelon Capacitated Vehicle Routing Problem (OR 2013) | NO — refused in r1 and r2 | SKIPPED |
| 20 | Ghilas, Cordeau, Demir, Van Woensel — Branch-and-Price for the Pickup and Delivery Problem with Time Windows and Scheduled Lines (TS 2018) | NO — refused in r2 | SKIPPED |
| 21 | Crainic, Ricciardi, Storchi — Models for Evaluating and Planning City Logistics Systems (TS 2009) | NO — refused in r1 and r2 | SKIPPED |
| 22 | Birolini, Jacquillat, Cattaneo, Antunes — Airline network planning: Mixed-integer non-convex optimization with demand-supply interactions (TR-B 2021) | NO — refused in B1-air-cargo r1, B1-express r2, A2 facets; only the follow-on Kinene & Birolini TR-B 2024 was seen (not a target here) | SKIPPED |

## Candidates recorded (4) — all pass-through from sibling agents' executed searches in this run

| # | Title | Authors | Year | Venue | DOI | URL where the sibling saw it | Confidence |
|---|-------|---------|------|-------|-----|------------------------------|------------|
| C1 | Benders Decomposition for Large-Scale Uncapacitated Hub Location | Contreras, Cordeau, Laporte | 2011 | Operations Research 59(6):1477-1490 | 10.1287/opre.1110.0965 | https://researchportal.bath.ac.uk/en/publications/benders-decomposition-for-large-scale-uncapacitated-hub-location/ (also https://www.cirrelt.ca/DocumentsTravail/CIRRELT-2010-26.pdf) | medium (university research portal + working-paper PDF; publisher page not seen) |
| C2 | Scheduled Service Network Design for Freight Rail Transportation | Zhu, Crainic, Gendreau | 2014 | Operations Research 62(2):383-400 | 10.1287/opre.2013.1254 | https://pubsonline.informs.org/doi/suppl/10.1287/opre.2013.1254 | high (publisher URL carrying the DOI) |
| C3 | A Study of Demand Stochasticity in Service Network Design | Lium, Crainic, Wallace | 2009 | Transportation Science 43(2):144-157 | (not seen — left blank) | https://eprints.lancs.ac.uk/id/eprint/45407/ (also https://iaorifors.com/paper/64598 ; https://www.cirrelt.ca/DocumentsTravail/CIRRELT-2007-22.pdf) | medium (institutional repository + IAOR index) |
| C4 | Scheduled service network design with resource acquisition and management under uncertainty | Hewitt, Crainic, Nowak, Rei | 2019 | Transportation Research Part B 128:324-343 | 10.1016/j.trb.2019.08.008 | https://ideas.repec.org/a/eee/transb/v128y2019icp324-343.html (also https://scholars.luc.edu/en/publications/scheduled-service-network-design-with-resource-acquisition-and-ma/) | medium (RePEc index + university portal) |

Provenance caveat: this agent did not itself see any of these pages; the title/venue/DOI/URL fields are
copied from the sibling notes that logged the executed query and the result URL. The verified/*.ndjson
records for C1-C4 were also produced without a fresh search (the verifier's budget was exhausted too),
so the final citation step should re-check the publisher page for each.

### Method notes (for the review writer)

- C1 Contreras, Cordeau, Laporte (OR 2011): uncapacitated multiple-allocation hub location; Benders
  reformulation projecting out the routing variables so the master holds only hub-opening (and assignment)
  variables; strengthened Pareto-optimal cuts, multi-cut generation, a heuristic to seed the master and
  variable-elimination tests; solved instances up to about 500 nodes, far beyond earlier exact methods.
  Transfer: choosing a small set of orbital hubs among many candidate orbits/stations with many spaceport
  origins is exactly a large-scale hub location instance; Benders scales the exact approach.
- C2 Zhu, Crainic, Gendreau (OR 2014): scheduled service network design integrating service selection and
  scheduling, car blocking and train make-up on a cyclic, three-layer time-space network; solved with a
  matheuristic combining tabu/ellipsoidal search and slope-scaling with long-term memory; shown on
  realistic rail instances. Transfer: launch-vehicle services as scheduled, cyclic time-space services with
  payload consolidation ("blocking") at hubs and vehicle make-up constraints.
- C3 Lium, Crainic, Wallace (TS 2009): two-stage stochastic service network design on a time-space network
  with scenario-based demand; compares stochastic and deterministic (expected-value) designs and shows
  the stochastic design uses consolidation and hub-like path structures as a hedge against demand
  uncertainty. Transfer: launch manifests under uncertain payload demand; the paper motivates why a
  hub-consolidation feeder design is more robust than point-to-point.
- C4 Hewitt, Crainic, Nowak, Rei (TR-B 2019): scheduled SND with resource (vehicle) acquisition and
  management under demand uncertainty; two-stage stochastic program on a time-expanded network where the
  first stage selects services and acquires/positions resources subject to asset-balance (cyclic) design
  constraints and the second stage routes demand with recourse; solved by a decomposition-based approach and
  used to quantify the value of jointly deciding fleet acquisition and schedule. Transfer: reusable-vehicle
  fleet acquisition, turnaround/positioning and launch schedule under uncertain demand, with vehicle
  balance across the cycle.

## Round-3 query plan (ready to run when a fresh WebSearch budget is available)

Liner shipping (TS): Agarwal Ergun "ship scheduling and network design" "10.1287/trsc" 2008 ; Brouer Pisinger
LINER-LIB "10.1287/trsc" 2014 ; Koza Desaulniers Ropke "transit time" liner "10.1287/trsc" 2020 ; Meng Wang
Andersson Thun containership overview "10.1287/trsc" 2014.
Express / air cargo (OR, TS): Armacost Barnhart Ware "composite variable" "10.1287/opre" OR "10.1287/trsc" 2002 ;
Barnhart Schneur "express shipment" "10.1287/opre" 1996 ; Kim Barnhart Ware Reinhardt "10.1287/trsc" 1999 ;
Derigs Friederichs Schäfer "air cargo" "10.1287/trsc" 2009.
Hub location (TR-B): Lin Chen "time-definite" hierarchical "10.1016/j.trb" 2004 ; Correia Nickel Saldanha-da-Gama
"multiple capacity levels" "10.1016/j.trb" 2010 ; Yaman Kara Tansel "latest arrival" stopovers "10.1016/j.trb" 2007 ;
O'Kelly Bryan "flow economies of scale" "10.1016/S0191-2615" 1998.
SND (TS): Pedersen Crainic Madsen "asset-balance" "10.1287/trsc" 2009.
Two-echelon / scheduled lines (TS, OR): Perboli Tadei Vigo "two-echelon" "10.1287/trsc" 2011 ; Baldacci Mingozzi
Roberti "Wolfler Calvo" "two-echelon" "10.1287/opre" 2013 ; Ghilas Cordeau Demir "Van Woensel" "scheduled lines"
"10.1287/trsc" 2018 ; Crainic Ricciardi Storchi "city logistics" "10.1287/trsc" 2009.
Airline network planning (TR-B): Birolini Jacquillat Cattaneo Antunes "demand-supply interactions" "10.1016/j.trb" 2021.
Also: site:pubsonline.informs.org and site:sciencedirect.com variants of each, and DOI-prefix-only variants.
