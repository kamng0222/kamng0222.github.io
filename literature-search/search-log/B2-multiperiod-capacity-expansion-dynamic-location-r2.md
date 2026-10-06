# Facet B2 — Multi-period capacity expansion and dynamic facility/hub location (round 2)

## Status: NO SEARCHES EXECUTED — WebSearch budget exhausted

- Every WebSearch call issued by this agent returned: "Web search was not performed: this turn's web search budget is used up (limit: 200 WebSearch calls per turn, shared by every agent in it)."
- WebSearch is the ONLY tool in this environment that reaches the internet (WebFetch/curl/wget are egress-blocked), so no corroboration of any paper was possible.
- Per the facet rules ("never record a paper from memory alone, and never invent a DOI"), ZERO candidates are recorded. The StructuredOutput for this facet therefore carries an empty candidate list.
- The round-1 file for the overlapping facet (B2-fleet-sizing-capacity-expansion-r1.md) reports the same outcome ("0 of the planned 25-40 searches ran"), so the capacity-expansion / dynamic-location core of Topic B remains UNCORROBORATED after two rounds. This is a real gap the report writer must flag; it is not evidence that the literature is thin.
- Remedy: re-run this facet in a turn with fresh search budget (or raise CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION). The query plan below is ready to execute.

## Queries attempted (all refused by the budget limit; none produced results)

1. Luss 1982 "Operations research and capacity expansion problems: a survey"
2. Fong Srinivasan "multiregion dynamic capacity expansion problem" Operations Research 1981
3. Shulman 1991 "dynamic capacitated plant location problems with discrete expansion sizes" Operations Research
4. Bean Higle Smith 1992 "Capacity expansion under stochastic demands" Operations Research
5. Rajagopalan 1998 "Capacity expansion and equipment replacement: a unified approach" Operations Research
6. Ahmed Sahinidis 2003 "approximation scheme for stochastic integer programs arising in capacity expansion" Operations Research

## Planned query list for a follow-up run (not executed)

Seminal Operations Research (pre-2005):
7. Singh Philpott Wood "Dantzig-Wolfe decomposition" multistage stochastic capacity planning Operations Research 2009
8. "capacity expansion" "Operations Research" 10.1287/opre stochastic demand discrete increments
9. Manne "capacity expansion" probabilistic growth Operations Research (classic)
10. Erlenkotter dynamic capacity expansion Operations Research
11. Freidenfelds capacity expansion Operations Research 1980 1981
12. Davis Dempster Sethi Vermes "optimal capacity expansion under uncertainty" Operations Research 1987
13. Lieberman capacity expansion Operations Research "economies of scale" lead time

Transportation Science (dynamic/modular location, multi-period hub):
14. Jena Cordeau Gendron "Dynamic facility location with generalized modular capacities" Transportation Science 2015 10.1287/trsc
15. Jena Cordeau Gendron "Lagrangian heuristics" dynamic facility location modular capacities Transportation Science 2017
16. Alumur Nickel Saldanha-da-Gama Secerdin "Multi-period hub network design problems with modular capacities" 
17. Contreras Cordeau Laporte "dynamic uncapacitated hub location problem" Transportation Science 2011 10.1287/trsc
18. "multi-period" hub location "Transportation Science" modular capacity 2022 2023 2024
19. "10.1287/trsc" dynamic facility location capacity expansion 2024 2025 2026

Transportation Research Part B (airport capacity expansion, network expansion under uncertainty):
20. Sun Schonfeld "Stochastic capacity expansion models for airport facilities" Transportation Research Part B 2015
21. Ukkusuri Patil "multi-period transportation network design under demand uncertainty" Transportation Research Part B 2009
22. Fragkos Cordeau Jans decomposition "network expansion" Transportation Research Part B 2021
23. "10.1016/j.trb" multi-period network design capacity expansion stochastic 2023 2024 2025
24. Lo Szeto time-dependent network design "Transportation Research Part B" multi-period investment
25. Kim Ouyang "multi-period" airport OR hub capacity expansion stochastic "Transportation Research Part B"

Transportation Research Part C (multi-period rollout of charging/refueling networks):
26. Zhang Kang Kwon "Multi-period planning of EV fast charging stations" Transportation Research Part C 2017
27. "10.1016/j.trc" multi-period charging station network expansion stochastic 2023 2024 2025 2026
28. Li Huang Mason "multi-period optimization" charging station deployment "Transportation Research Part C"
29. "multi-period" hydrogen refueling station rollout "Transportation Research Part C"
30. "multi-stage" vertiport OR eVTOL infrastructure deployment "Transportation Research Part C" 2024 2025 2026

Decomposition / multistage stochastic & robust:
31. "multistage stochastic" capacity expansion "Operations Research" nested Benders SDDP 10.1287/opre
32. Huang Ahmed "value of multistage stochastic programming in capacity planning" Operations Research 2009
33. adjustable robust capacity expansion multi-period "Operations Research" 2022 2023 2024
34. "progressive hedging" multi-period facility location "Transportation Science" OR "Operations Research"
35. "two-stage stochastic" dynamic facility location Benders "Transportation Science" 2021 2022 2023

Space-logistics adjacent (optional secondary, max 8):
36. Ho de Weck Shishko "dynamic network" space logistics multi-period Acta Astronautica
37. Chen Ho "multi-fidelity space logistics" network design Journal of Spacecraft and Rockets
38. Isaji Takubo Ho "multidisciplinary design optimization" space infrastructure deployment JSR / Acta Astronautica

## Candidates

None recorded (no search corroboration possible this round).

## Cross-reference to what the parent already holds (from prior-round notes, NOT re-recorded here)

B2-fleet-sizing-capacity-expansion-r1.md lists as "unsearched/uncorroborated": Luss 1982 (OR 30(5)); Bean, Higle, Smith 1992 (OR 40 S2); Ahmed & Sahinidis 2003 (OR 51(3)); Jena, Cordeau, Gendron 2015 (TS 49(3)); Ukkusuri & Patil 2009 (TR-B 43(6)); Fragkos, Cordeau, Jans 2021 (TR-B 144). It also warns that Ahmed, King, Parija 2003 (J. Global Optim.), Ordonez & Zhao 2007 (Networks), Topaloglu & Powell 2006 (IJOC) and Van Roy & Erlenkotter 1982 (Management Science) are OUT of scope by venue.
B2-network-design-uncertainty-r1.md recorded (medium confidence) Alumur, Nickel, Saldanha-da-Gama 2012 "Hub location under uncertainty" TR-B 46(4), DOI 10.1016/j.trb.2011.11.006, and Contreras, Cordeau, Laporte 2011 Benders for uncapacitated hub location, OR 59(6), DOI 10.1287/opre.1110.0965. These are already in the parent's pipeline and are not duplicated here.
