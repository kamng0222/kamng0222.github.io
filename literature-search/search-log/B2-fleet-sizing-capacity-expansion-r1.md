# Facet B2 — Fleet sizing, asset reuse/turnaround, multi-period capacity expansion (round 1)

Topic B: Spaceport-to-Orbit feeder network design — OR methodology analogs.
Venues in scope: Operations Research (10.1287/opre), Transportation Science (10.1287/trsc), TR-B (10.1016/j.trb), TR-C (10.1016/j.trc).
Agent: literature-search subagent, facet fleet-sizing-capacity-expansion. Date: 2026-10-06.

## STATUS: ZERO searches performed — coverage gap, round 2 required

The shared per-turn WebSearch budget (200 calls, pooled across every agent in this workflow run) was
already exhausted when this facet started. All 8 queries issued by this agent were refused by the tool
("Web search was not performed: this turn's web search budget is used up"). WebFetch, curl, wget and
every other HTTP path are blocked by the egress proxy, and the task rules forbid recording any paper from
memory alone or inventing a DOI. The orchestrator's instruction on budget exhaustion is to continue with
information already gathered, so the ONLY candidates recorded below are items that sibling facet agents in
this same run corroborated with search results (publisher / RePEc / institutional-repository URLs) and that
fall squarely inside this facet (fleet or asset balancing, fleet acquisition, resource-constrained scheduled
service, cyclic vehicle rotations, multi-period/dynamic hub location). They are re-recorded here only to
attach this facet's methodological framing; the merge step should de-duplicate them against B1/B2 notes.
Confidence is capped at "medium" and set to "low" wherever the sibling agent flagged that venue or authors
were not visible in the search result.

**Nothing from the core of this facet (Dejax & Crainic 1987; Beaujon & Turnquist 1991; Godfrey & Powell
2002; Powell / Topaloglu / Simao ADP fleet management; Luss 1982; Ahmed & Sahinidis; dynamic facility
location; fleet sizing for carsharing / eVTOL; empty repositioning) has been corroborated yet.** This is a
budget artefact, not evidence of absence.

## Queries issued by this agent and REFUSED (not performed)

1. Dejax Crainic "empty flows" survey Transportation Science 1987
2. Beaujon Turnquist "fleet sizing and vehicle allocation" Transportation Science 1991
3. Godfrey Powell "adaptive dynamic programming" dynamic fleet management Transportation Science 2002
4. Luss "capacity expansion problems" survey Operations Research 1982
5. Ahmed King Parija multi-stage stochastic integer programming capacity expansion under uncertainty
6. Simao Powell approximate dynamic programming large-scale fleet management Transportation Science 2009
7. Topaloglu Powell dynamic fleet management stochastic "Operations Research" 10.1287/opre
8. Crainic Laporte "planning models for freight transportation" strategic tactical operational

## Round-2 query plan (not yet run; ordered by priority)

### (c) Named authors / classics (pre-2005)
9.  Powell "dynamic vehicle allocation problem" stochastic "Transportation Science" 1986
10. Powell "operational planning model" dynamic vehicle allocation uncertain demands "Transportation Research Part B" 1987
11. Frantzeskakis Powell "successive linear approximation" stochastic dynamic vehicle allocation Transportation Science 1990
12. Cheung Powell "multistage dynamic networks with random arc capacities" dynamic fleet management "Operations Research" 1996
13. Jordan Turnquist "stochastic, dynamic network model" railroad car distribution Transportation Science 1983
14. Turnquist Jordan "fleet sizing under production cycles" Transportation Science 1986
15. Crainic Gendreau Dejax "allocation of empty containers" dynamic stochastic "Operations Research" 1993
16. Holmberg Joborn Lundgren "empty freight car distribution" Transportation Science 1998 ; Joborn Crainic Gendreau Holmberg Lundgren "economies of scale" empty freight car Transportation Science 2004
17. Powell Carvalho "logistics queueing networks" fleet management Transportation Science 1998
18. Powell Shapiro Simao "heterogeneous resource allocation" adaptive dynamic programming Transportation Science 2002
19. Spivey Powell "dynamic assignment problem" Transportation Science 2004
20. Ceder Stern "deficit function" bus scheduling fleet size Transportation Science 1981
21. Bean Higle Smith "capacity expansion under stochastic demands" Operations Research 1992
22. Ahmed Sahinidis "approximation scheme" stochastic integer programs capacity expansion "Operations Research" 2003
23. Magnanti Wong "network design and transportation planning" Transportation Science 1984 (multi-period / capacity expansion sections)

### (a)+(b) Methodology and problem phrases, by venue
24. "fleet sizing" "Transportation Science" time-space network empty repositioning
25. "fleet sizing" "Transportation Research Part B" vehicle sharing OR carsharing OR relocation
26. "fleet size" "Operations Research" INFORMS stochastic dynamic vehicle allocation
27. "approximate dynamic programming" fleet management "Transportation Science" 10.1287/trsc
28. Topaloglu Powell "sensitivity analysis" dynamic fleet management approximate dynamic programming "Operations Research" 2007
29. Erera Morales Savelsbergh "robust optimization for empty repositioning" Operations Research 2009
30. Wu Hartman Wilson "fleet sizing with heterogeneous assets" Transportation Science 2005
31. Nair Miller-Hooks "fleet management for vehicle sharing operations" Transportation Science 2011
32. Boyaci Zografos Geroliminis electric carsharing relocation "Transportation Research Part B" 2017 ; Hu Liu "parking capacities and fleet size" one-way carsharing "Transportation Research Part B" 2016
33. Song Dong "empty container repositioning" multiple shipping service routes "Transportation Research Part B"
34. Bouzaiene-Ayari Powell locomotive "approximate dynamic programming" Transportation Science 2016
35. Jena Cordeau Gendron "dynamic facility location" "generalized modular capacities" Transportation Science 2015
36. Contreras Cordeau Laporte "dynamic uncapacitated hub location problem" Transportation Science 2011 (confirm title/authors)
37. Ukkusuri Patil "multi-period transportation network design" demand uncertainty "Transportation Research Part B" 2009
38. Fragkos Cordeau Jans "network expansion" decomposition "Transportation Research Part B" 2021
39. "multi-period" OR "multiperiod" "capacity expansion" network "Operations Research" INFORMS 10.1287/opre
40. "design-balanced" OR "asset-balance" service network design "Transportation Science" Pedersen Crainic Madsen 2009 ; Chouman Crainic 2015 matheuristic
41. "vehicle scheduling" limited fleet "time-space network" "Transportation Research Part B" turnaround OR "cycle time"
42. "rotation planning" OR "aircraft rotation" OR "vehicle rotation" cyclic schedule "Transportation Science"

### Recency (2021-2026) — at least 6
43. fleet sizing eVTOL OR "air taxi" OR "urban air mobility" "Transportation Research Part C" 2023 2024
44. "fleet sizing" OR "fleet size" autonomous mobility-on-demand "Transportation Research Part B" 2022 2023 2024
45. "approximate dynamic programming" OR "reinforcement learning" fleet repositioning "Transportation Science" 2023 2024 2025
46. "10.1016/j.trc" fleet sizing charging turnaround electric aircraft OR drone 2024 2025 2026
47. "10.1287/trsc" fleet management stochastic 2024 2025
48. "multi-period" network design capacity expansion "Transportation Research Part B" 2022 2023 2024 2025
49. "Budget-Driven Multiperiod Hub Location" Operations Research 2025 authors
50. "10.1287/opre" dynamic facility location OR relocation 2023 2024 2025
51. drone delivery fleet sizing "Operations Research" OR "Transportation Science" 2022 2023 2024

### Secondary / adjacent (space logistics; at most 8 candidates)
52. Ho de Weck Hoffman Shishko "space logistics" "time-expanded network" Acta Astronautica 2014
53. Chen Ho "integrated space logistics mission planning and spacecraft design" Journal of Spacecraft and Rockets
54. Jagannatha Ho "generalized multicommodity network flow" Earth-Moon-Mars logistics Journal of Spacecraft and Rockets
55. reusable launch vehicle fleet sizing turnaround "launch cadence" optimization Acta Astronautica OR "Journal of Spacecraft and Rockets" 2023 2024
56. spaceport location OR "launch site selection" optimization network Acta Astronautica

## Candidates recorded in round 1 (all derived from sibling agents' corroborated search results in this run)

| # | Paper | Venue / year | DOI | Where seen (by sibling agent) | Sibling file | Confidence |
|---|-------|--------------|-----|-------------------------------|--------------|------------|
| 1 | Andersen, Christiansen, Crainic, Grønhaug — Branch and Price for Service Network Design with Asset Management Constraints | Transportation Science 45(1):33-49, 2011 | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v45y2011i1p33-49.html | B1-service-network-design-r1.md | medium |
| 2 | Andersen, Crainic, Christiansen — Service network design with asset management: Formulations and comparative analyses | Transportation Research Part C 17(2), 2009 (venue NOT shown in snippet; from sibling's knowledge) | (not seen) | https://www.cirrelt.ca/DocumentsTravail/CIRRELT-2007-55.pdf | B1-service-network-design-r1.md | low |
| 3 | Crainic, Hewitt, Toulouse, Vu — Service network design with resource constraints | Transportation Science 50(4), 2016 | (not seen) | https://scholars.luc.edu/en/publications/service-network-design-with-resource-constraints/ | B1-service-network-design-r1.md | medium |
| 4 | Hewitt, Crainic, Nowak, Rei — Scheduled service network design with resource acquisition and management under uncertainty | Transportation Research Part B 128:324-343, 2019 | 10.1016/j.trb.2019.08.008 | https://ideas.repec.org/a/eee/transb/v128y2019icp324-343.html ; https://scholars.luc.edu/en/publications/scheduled-service-network-design-with-resource-acquisition-and-ma/ | B2-network-design-uncertainty-r1.md | medium |
| 5 | Contreras, Cordeau, Laporte — The Dynamic Uncapacitated Hub Location Problem | Transportation Science 45(1):18-32, 2011 (title/authors flagged "from recollection" by sibling; RePEc index with matching vol/issue/pages) | (not seen) | https://ideas.repec.org/a/inm/ortrsc/v45y2011i1p18-32.html | B1-hub-location-r1.md | low |
| 6 | (authors not captured) — Budget-Driven Multiperiod Hub Location: A Robust Time-Series Approach | Operations Research 73(2):613-631, 2025 | (not seen) | https://ideas.repec.org/a/inm/oropre/v73y2025i2p613-631.html ; https://academicnewsletter.sufe.edu.cn/info/401695 | B2-network-design-uncertainty-r1.md | low (authors not captured; method inferred from title) |
| 7 | (authors not captured) — Operations design for high-velocity intra-city package service | Transportation Research Part B 161:150-168, 2022 | (not seen) | https://ideas.repec.org/a/eee/transb/v161y2022icp150-168.html | B1-service-network-design-r1.md | low (authors not captured; snippet: repeatable cyclic vehicle routes with capacity/timing requirements) |

### Why these belong to this facet
- 1, 2: asset-balance ("design-balanced") constraints force vehicles to follow closed cycles on a cyclic time-space network; cycle-based variables enumerate vehicle rotations and the number of cycles selected IS the fleet size. Branch-and-price over cycles (1) and the arc/path/cycle formulation comparison (2) are the standard toolkit for sizing a small reusable fleet that must return to base.
- 3: resource (vehicle) constraints — each vehicle anchored to a home terminal, bounded fleet per terminal, must complete its cycle within the schedule period — solved by a column-generation / slope-scaling matheuristic.
- 4: fleet acquisition as a first-stage decision in a two-stage stochastic scheduled SND with outsourcing recourse; the direct analog of deciding how many launch vehicles to buy before demand is known.
- 5, 6: multi-period / dynamic hub location — phasing hub openings over a horizon under budget and demand growth; 6 adds robustness to time-series demand.
- 7: rate-based, repeatable cyclic vehicle routes with capacity and timing requirements (shuttle operations) — a template for fixed-cadence feeder shuttles.

## UNVERIFIED leads from model memory — NOT candidates (titles/venues to be confirmed in r2; no DOIs recorded)

These are listed ONLY to seed round-2 queries. None appeared in any search result in this run and none is
recorded in the structured output.

- Dejax, Crainic (1987) review of empty flows and fleet management models in freight transportation — TS 21(4).
- Beaujon, Turnquist (1991) a model for fleet sizing and vehicle allocation — TS 25(1).
- Godfrey, Powell (2002) adaptive dynamic programming for dynamic fleet management, parts I and II — TS 36(1).
- Powell (1986) stochastic model of the dynamic vehicle allocation problem — TS 20(2); Powell (1987) operational planning model for dynamic vehicle allocation with uncertain demands — TR-B 21(3).
- Frantzeskakis, Powell (1990) successive linear approximation for stochastic dynamic vehicle allocation — TS 24(1).
- Cheung, Powell (1996) multistage dynamic networks with random arc capacities / dynamic fleet management — OR 44(6).
- Jordan, Turnquist (1983) stochastic dynamic network model for railroad car distribution — TS 17(2); Turnquist, Jordan (1986) fleet sizing under production cycles and uncertain travel times — TS 20(4).
- Crainic, Gendreau, Dejax (1993) dynamic and stochastic models for allocation of empty containers — OR 41(1).
- Holmberg, Joborn, Lundgren (1998) improved empty freight car distribution — TS 32(2); Joborn et al. (2004) economies of scale in empty freight car distribution — TS 38(2).
- Powell, Carvalho (1998) logistics queueing networks for large-scale fleet management — TS 32(2).
- Powell, Shapiro, Simao (2002) ADP for heterogeneous resource allocation — TS 36(2); Spivey, Powell (2004) the dynamic assignment problem — TS 38(4).
- Topaloglu, Powell (2007) sensitivity analysis of a dynamic fleet management model using ADP — OR 55(2).
- Simao, Day, George, Gifford, Nienow, Powell (2009) ADP for large-scale fleet management: a case application — TS 43(2).
- Bouzaiene-Ayari, Cheng, Das, Fiorillo, Powell (2016) locomotive optimization, IP vs ADP — TS 50(2).
- Erera, Morales, Savelsbergh (2009) robust optimization for empty repositioning problems — OR 57(2).
- Wu, Hartman, Wilson (2005) fleet sizing with heterogeneous assets — TS 39(1).
- Nair, Miller-Hooks (2011) fleet management for vehicle sharing operations — TS 45(4).
- Boyaci, Zografos, Geroliminis (2017) vehicle and personnel relocations in electric carsharing — TR-B 95; Hu, Liu (2016) parking capacities and fleet size for one-way carsharing — TR-B 93.
- Song, Dong (2012) cargo routing and empty container repositioning in multiple shipping service routes — TR-B 46(10).
- Ceder, Stern (1981) deficit-function bus scheduling with deadheading for fleet-size reduction — TS 15(4).
- Luss (1982) OR and capacity expansion problems: a survey — OR 30(5); Bean, Higle, Smith (1992) capacity expansion under stochastic demands — OR 40(S2); Ahmed, Sahinidis (2003) approximation scheme for stochastic integer programs in capacity expansion — OR 51(3).
- Jena, Cordeau, Gendron (2015) dynamic facility location with generalized modular capacities — TS 49(3).
- Ukkusuri, Patil (2009) multi-period transportation network design under demand uncertainty — TR-B 43(6); Fragkos, Cordeau, Jans (2021) decomposition for large-scale network expansion — TR-B 144.
- Pedersen, Crainic, Madsen (2009) tabu search for SND with asset-balance requirements — TS 43(2); Chouman, Crainic (2015) design-balanced matheuristic — TS 49(1).
- NOTE: several items named in the facet brief are OUT of scope by venue and should not be recorded even if found: Ahmed, King, Parija (2003) is in J. Global Optimization; Crainic & Laporte (1997) "Planning models for freight transportation" is in EJOR; Ordonez & Zhao (2007) robust capacity expansion is in Networks; Topaloglu & Powell (2006) time-staged multicommodity ADP is in IJOC; Van Roy & Erlenkotter (1982) dynamic facility location is in Management Science.
- Secondary (adjacent venues): Ho, de Weck, Hoffman, Shishko (2014) space logistics via time-expanded networks — Acta Astronautica; Chen, Ho (2018) integrated space logistics planning and spacecraft design — JSR; Jagannatha, Bui, Ho (2019) generalized multicommodity network flow for Earth-Moon-Mars logistics — JSR; Chen, Gardner, Grogan, Ho (2021) flexibility management for space logistics via decision rules — JSR.

## Gaps
- Entire facet core (fleet sizing, empty repositioning, ADP fleet management, capacity-expansion theory, dynamic facility location, eVTOL/drone fleet sizing, space-logistics secondary venues) is uncorroborated: 0 of the planned 25-40 searches ran.
- No DOI captured for any Elsevier item except Hewitt et al. 2019 (from sibling notes).
- No 2021-2026 fleet-sizing paper corroborated; the only recent items (6, 7) have uncaptured author lists.
- No pre-2005 classic corroborated for this facet.
