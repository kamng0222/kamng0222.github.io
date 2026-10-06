# Facet A1 — trajectory-airspace (round 1) — STATUS: NO SEARCHES EXECUTED

Date: 2026-10-06
Agent: literature-search subagent, facet "trajectory-airspace" (Topic A: RAM air traffic flow management, OR methodology lineage)

## 1. What happened

Every WebSearch call issued by this agent was refused with:

> "Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn,
> shared by every agent in it)."

The budget is shared across all parallel facet agents in this workflow turn and was already consumed by sibling
agents before this facet's first query ran. The tool explicitly instructs not to work around the limit (no
curl/wget/proxy/archive searches), and the task's precision rule says a paper may be recorded only when a search
result corroborates it and never from memory alone. Consequently:

* **searches actually executed: 0**
* **verified candidates recorded: 0**

Remedy: the per-turn budget resets on a new turn. Re-running this facet in a follow-up turn (or raising
CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION / staggering facet agents across turns) will allow the query plan below to execute.

## 2. Queries attempted this turn (all refused, none performed)

1. Pallottino Feron Bicchi conflict resolution mixed integer programming "Transportation Systems" aircraft  (standard)
2. Vela Solak Clarke conflict resolution aircraft mixed integer program "Transportation Research Part C"  (standard)
3. Cafieri Durand aircraft deconfliction mixed integer nonlinear programming speed regulation  (standard)
4. Rey Rapine Fondacci El Faouzi subliminal speed control conflict minimization "Transportation Research Part C"  (standard)
5. Alonso-Ayuso Escudero Martin-Campo collision avoidance aircraft velocity changes mixed 0-1 nonlinear "Transportation Science"  (standard)
6. Omer mixed integer linear programming aircraft conflict resolution "Transportation Research Part C" space discretization  (standard)

## 3. Remaining planned query set (not yet run) — for the follow-up round

Methodology / problem phrases with venue restrictors:
7.  aircraft conflict resolution mixed integer programming "Transportation Science"
8.  aircraft deconfliction mathematical programming review "Transportation Science" 2022
9.  air conflict resolution uncertainty biobjective mixed integer "Transportation Science" Lehouillier Soumis Desaulniers
10. 4D trajectory optimization air traffic "Transportation Research Part C"
11. trajectory based operations optimization "Transportation Research Part C" 2023
12. speed control air traffic flow management delay absorption "Transportation Research Part C"
13. cruise speed reduction ground delay program "Transportation Research Part C" Delgado Prats
14. linear holding airborne delay no extra fuel "Transportation Research Part C" Xu Prats
15. stochastic optimization transferring delay along flight trajectories fuel "Transportation Science" Jones Lovell Ball
16. dynamic airspace configuration sectorization optimization "Transportation Research Part C"
17. dynamic airspace sectorisation flight-centric operations "Transportation Research Part C" Gerdes Temme Schultz
18. multi-objective dynamic airspace sectorization agent based geometric "Transportation Research Part C" Tang Alam Abbass
19. airspace flow program collaborative en route resource allocation "Transportation Research Part C" Kim Hansen
20. sequential resource allocation en route air traffic management "Transportation Research Part B" Kim Hansen
21. airspace capacity estimation controller workload model "Transportation Research Part C"
22. air traffic complexity metric estimation "Transportation Research Part C"
23. en route congestion flow corridor allocation "Transportation Research Part C" Yousefi
24. free flight free route airspace optimization "Transportation Research Part C"
25. free-route airspace network design optimization "Transportation Research Part B"
26. en route sector capacity constraints trajectory optimization "Operations Research" INFORMS air traffic
27. aircraft rerouting dynamic network flow air traffic "Transportation Science" (overlap check with ATFM facet)

DOI-prefix / site-restricted:
28. "10.1287/trsc" aircraft conflict resolution
29. "10.1287/trsc" speed control air traffic
30. "10.1016/j.trc" conflict detection resolution aircraft optimization
31. "10.1016/j.trc" dynamic airspace configuration
32. "10.1016/j.trb" airspace capacity air traffic
33. "10.1287/opre" air traffic trajectory en route capacity
34. site:pubsonline.informs.org aircraft deconfliction
35. site:sciencedirect.com transportation-research-part-c trajectory-based operations

Recent (2021-2026):
36. aircraft conflict resolution mixed integer 2023 "Transportation Research Part C"
37. trajectory based operations 4D trajectory negotiation 2024 "Transportation Research Part C"
38. dynamic airspace configuration 2025 "Transportation Research Part C"
39. urban air mobility airspace capacity conflict resolution optimization 2024 "Transportation Research Part C"
40. airspace sectorization deep reinforcement learning 2025 "Transportation Research Part C"
41. speed control metering air traffic 2026 "Transportation Research Part C"

Classic (pre-2005):
42. free flight conflict resolution mixed integer programming 2002 Pallottino
43. air traffic conflict detection resolution 1998 2000 "Transportation Science"
44. airspace sectorization optimization 1990s "Transportation Research Part B"
45. en route air traffic capacity 2000 "Operations Research" INFORMS

## 4. UNVERIFIED LEADS (from the agent's prior knowledge — NOT corroborated by any search; NOT recorded as candidates)

These are search targets for the follow-up round only. Venue/year are the agent's recollection and must be
verified against a publisher or DOI page before any is cited. No DOIs are given because none were seen.

Likely in-scope (TS / TR-C / TR-B / OR):
* Rey, Rapine, Fondacci, El Faouzi — "Subliminal speed control in air traffic management: Optimization and simulation" — believed Transportation Science, ~2016. (MILP on time-expanded conflict graph; small speed adjustments to minimize potential conflicts.)
* Rey, Rapine, Dessouky, Fondacci, El Faouzi — "Minimization of potential air conflicts through speed regulation" — believed TR-C, ~2015.
* Alonso-Ayuso, Escudero, Martín-Campo — "Exact and approximate solving of the aircraft collision resolution problem via turn changes" — believed Transportation Science, ~2016. (Mixed 0-1 nonlinear model, heading changes.)
* Lehouillier, Nasri, Soumis, Desaulniers, Omer — "Solving the air conflict resolution problem under uncertainty using an iterative biobjective mixed integer programming approach" — believed Transportation Science, ~2017.
* Pelegrín, D'Ambrosio — "Aircraft deconfliction via mathematical programming: Review and insights" — believed Transportation Science, ~2022. (Survey of MIP/MINLP CDR formulations.)
* Jones, Lovell, Ball — "Stochastic optimization models for transferring delay along flight trajectories to reduce fuel usage" — believed Transportation Science, ~2018.
* Delgado, Prats, Sridhar — "Cruise speed reduction for ground delay programs: A case study for San Francisco International Airport arrivals" — believed TR-C, ~2013.
* Xu, Dalmau, Prats — "Maximizing airborne delay at no extra fuel cost by means of linear holding" — believed TR-C, ~2017.
* Tang, Alam, Lokan, Abbass — "A multi-objective approach for Dynamic Airspace Sectorization using agent based and geometric models" — believed TR-C, ~2012.
* Gerdes, Temme, Schultz — "Dynamic airspace sectorisation for flight-centric operations" — believed TR-C, ~2018.
* Yousefi, Zadeh — "Dynamic allocation and benefit assessment of NextGen flow corridors" — believed TR-C, ~2013.
* Kim, Hansen — "A framework for the assessment of collaborative en route resource allocation strategies" — believed TR-C, ~2013; and "Some insights into a sequential resource allocation mechanism for en route air traffic management" — believed TR-B, ~2015. (Airspace flow program / CDM.)
* Mukherjee, Hansen — "A dynamic rerouting model for air traffic flow management" — believed TR-B, ~2009 (overlaps ATFM/rerouting facet).
* Bertsimas, Stock Patterson — "The traffic flow management rerouting problem in air traffic control: A dynamic network flow approach" — believed Transportation Science, ~2000 (overlaps ATFM facet).

Named in the facet but believed OUT of scope by venue (useful for lineage narrative only, do not record as candidates):
* Pallottino, Feron, Bicchi (2002) — IEEE Trans. Intelligent Transportation Systems (MILP CDR with speed or heading changes).
* Vela, Solak, Clarke et al. (~2010) — IEEE Trans. ITS (fuel-optimal en route conflict resolution MIP); Vela et al. stochastic CDR — conference.
* Cafieri, Durand (2014) — Journal of Global Optimization (MINLP deconfliction with speed regulation); Cafieri, Omheni (2017) — EJOR.
* Omer (2015) — Computers & Operations Research (space-discretized MILP); Omer, Farges (2013) — IEEE Trans. ITS.
* Alonso-Ayuso, Escudero, Martín-Campo (2011) — IEEE Trans. ITS; (2012) — Computers & OR (velocity changes over time horizon).
* Agustín, Alonso-Ayuso, Escudero, Pizarro (2012) — EJOR (ATFM with rerouting, deterministic/stochastic).
* Dias, Hijazi, Rey (~2022) — EJOR (disjunctive separation conditions for CDR).

## 5. Candidates recorded

None. (Precision rule: no search corroboration was possible this turn.)
