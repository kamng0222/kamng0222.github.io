# Facet B1 — Service Network Design (SND) on time-expanded networks — round 1 notes

Agent: literature-search subagent (facet service-network-design). Date: 2026-10-06.

## IMPORTANT caveat on coverage

Only 5 WebSearch queries executed before the shared per-turn WebSearch budget
(200 calls, shared by all agents in the workflow) was exhausted. Six further
queries were refused by the tool. Everything below is restricted to what those
five result sets corroborated. Nothing was recorded from memory alone; where an
author list or venue is NOT visible in the snippet it is flagged explicitly.
A second round (r2) is needed to reach the 25–45 candidate target; the refused
queries are listed under "Queries NOT executed" as the starting point.

## Queries executed (5)

1. `"service network design" "Transportation Science" Crainic` (standard)
2. `"capacitated multicommodity network design" "Operations Research" INFORMS` (standard)
3. `"dynamic discretization discovery" Boland Hewitt Marshall Savelsbergh Transportation Science` (standard)
4. `"service network design" "asset management" Andersen Crainic Christiansen` (standard)
5. `"10.1016/j.trb" "service network design"` (standard)

## Queries NOT executed (refused: budget exhausted) — run these in r2

6. `"The Continuous-Time Service Network Design Problem" Boland Hewitt Marshall Savelsbergh "Operations Research" 2017`
7. `Pedersen Crainic Madsen "Models and tabu search metaheuristics for service network design with asset-balance requirements" Transportation Science`
8. `Lium Crainic Wallace "A study of demand stochasticity in service network design" Transportation Science 2009`
9. `Jarrah Johnson Neubert "Large-scale, less-than-truckload service network design" Operations Research 2009`
10. `Zhu Crainic Gendreau "Scheduled service network design for freight rail transportation" Operations Research 2014`
11. `Magnanti Wong "Network design and transportation planning: models and algorithms" Transportation Science 1984`

Further r2 suggestions (not yet attempted): Hewitt & Lehuede TRB 2023 "new formulations
scheduled SND"; Hewitt TS 2022 "flexible scheduled SND"; Baubaid Boland Savelsbergh TS 2021/2023;
Greening Dahan Erera TRB 2023 middle-mile consolidation; Scherr Hewitt Neumann Saavedra Mattfeld
TRB 2020 DDD mixed autonomous fleets; Hewitt Crainic Nowak Rei TRB 2019 SND resource acquisition
under uncertainty; Crainic Hewitt Maggioni Rei TS 2021 partial Benders; Rahmaniani et al. OR 2020
Benders dual decomposition; Chouman Crainic Gendron TS 2017 cut-set inequalities; Chouman & Crainic
TS 2015 design-balanced matheuristic; Erera Hewitt Savelsbergh Zhang TS 2013 load plan; Lindsey
Erera Savelsbergh TS 2016; Armacost Barnhart Ware TS 2002 composite variables; Kim Barnhart Ware
Reinhardt TS 1999; Barnhart Jin Vance OR 2000 railroad blocking; Farvolden & Powell TS 1994;
Powell TS 1986; Powell & Sheffi OR 1989; Holmberg & Yuan OR 2000; Holmberg & Hellstrand OR 1998;
Balakrishnan Magnanti Wong OR 1989; Magnanti Mirchandani Vachani OR 1995; Atamturk & Zhang OR 2007
two-stage robust network design; Fragkos Cordeau Jans TRB 2021 network expansion; Crainic Errico
Rei Ricciardi TS 2016 two-tier city logistics under uncertainty; Daganzo OR 1987 break-bulk
terminals; Langevin Mbaraga Campbell TRB 1996 continuous approximation; Ansari et al. TRB 2018
continuous approximation review; Ouyang & Daganzo TS 2006; Carlsson & Jia OR 2013.
Also recency queries with "2023/2024/2025/2026" + "service network design" + each venue, and
"space logistics" "time-expanded network" (Ho, de Weck; Acta Astronautica / JSR) for SECONDARY.

## Candidates corroborated by the executed searches

### In-scope venues

1. **Cycle-Based Neighbourhoods for Fixed-Charge Capacitated Multicommodity Network Design** —
   Ghamlouche, Crainic, Gendreau — Operations Research 51(4), 2003, pp. 655–667 —
   DOI 10.1287/opre.51.4.655.16098 — https://pubsonline.informs.org/doi/references/10.1287/opre.51.4.655.16098
   (also https://ideas.repec.org/a/inm/oropre/v51y2003i4p655-667.html). Publisher page seen → confidence high.
   Snippet: neighbourhood structures for metaheuristics accounting for flow redistribution; moves found by
   shortest-path-like network procedures. (Author names from knowledge of the paper; not in snippet.)

2. **Design of Capacitated Multicommodity Networks with Multiple Facilities** — Agarwal (author NOT in
   snippet; attribution from memory, flag) — Operations Research 50(2), 2002 — DOI 10.1287/opre.50.2.333.423 —
   https://pubsonline.informs.org/doi/references/10.1287/opre.50.2.333.423. Snippet: several facility types with
   different cost/capacity; private telecom networks with Fractional-T1. Confidence medium (author).

3. **Interval-Based Dynamic Discretization Discovery for Solving the Continuous-Time Service Network Design
   Problem** — Marshall, Boland, Savelsbergh, Hewitt — Transportation Science 55(1):29–51, 2021 —
   DOI not seen — https://par.nsf.gov/biblio/10226533 (NSF PAR). Confidence medium.

4. **Dynamic Discretization Discovery for Solving the Time-Dependent Traveling Salesman Problem with Time
   Windows** — Vu, Hewitt, Boland, Savelsbergh — Transportation Science, 2020 (venue/year NOT visible in
   snippet; from knowledge, flag) — https://scholars.luc.edu/en/publications/dynamic-discretization-discovery-for-solving-the-time-dependent-t/
   Confidence medium.

5. **The Continuous-Time Service Network Design Problem** — Boland, Hewitt, Marshall, Savelsbergh —
   Operations Research, 2017 — only indirectly corroborated (DDD snippet from arXiv 2303.01419 refers to the
   algorithm being introduced and "first proven" for the CTSNDP); title/venue not displayed → confidence LOW.
   https://arxiv.org/pdf/2303.01419

6. **Branch and Price for Service Network Design with Asset Management Constraints** — Andersen,
   Christiansen, Crainic, Grønhaug — Transportation Science 45(1):33–49, 2011 — DOI not seen —
   https://ideas.repec.org/a/inm/ortrsc/v45y2011i1p33-49.html (RePEc; snippet mentions "branch-and-price
   algorithms" among the SNDAM publications). Confidence medium.

7. **Service network design with asset management: Formulations and comparative analyses** — Andersen,
   Crainic, Christiansen — Transportation Research Part C 17(2), 2009 (journal venue NOT shown in snippet;
   seen as CIRRELT-2007-55 working paper + "(2009a)" citation; venue from knowledge, flag) —
   https://www.cirrelt.ca/DocumentsTravail/CIRRELT-2007-55.pdf. Confidence medium.

8. **Service network design with resource constraints** — Crainic, Hewitt, Toulouse, Vu — Transportation
   Science 50(4), Nov 2016 — DOI not seen — https://scholars.luc.edu/en/publications/service-network-design-with-resource-constraints/
   Confidence medium (Loyola index page; co-author list beyond Crainic/Hewitt from knowledge).

9. **Stochastic service network design with rerouting** — Bai, Wallace, Li, Chong — Transportation Research
   Part B 60, 2014, pp. 50–65 — DOI not seen — https://ideas.repec.org/a/eee/transb/v60y2014icp50-65.html and
   https://results2021.ref.ac.uk/outputs/e5e69338-c809-45e0-86ea-e23ebd4c68f0?page=1. Confidence medium.

10. **A green intermodal service network design problem with travel time uncertainty** — Demir, Burgholzer,
    Hrušovský, Arıkan, Jammernegg, Van Woensel — Transportation Research Part B 93, 2016, pp. 789–807
    (REF page lists 2015 = online-first; print 2016) — DOI not seen —
    https://results2021.ref.ac.uk/outputs/809f07a3-832e-4ed6-a4f4-72abbd6e2c7a?page=1. Confidence medium.

11. **Multicommodity, multimode freight transportation: A general modeling and algorithmic framework for the
    service network design problem** — Crainic, Rousseau — Transportation Research Part B 20(3), 1986,
    pp. 225–242 — DOI not seen — https://ideas.repec.org/a/eee/transb/v20y1986i3p225-242.html (RePEc URL
    with matching volume/issue/pages surfaced for the Crainic SND query; title not in snippet, flag).
    Confidence medium.

12. **Operations design for high-velocity intra-city package service** — authors NOT shown in snippet —
    Transportation Research Part B 161, 2022, pp. 150–168 — DOI not seen —
    https://ideas.repec.org/a/eee/transb/v161y2022icp150-168.html. Snippet: shuttle activities, rate-based
    models, repeatable cyclic vehicle routes with capacity and timing requirements. Confidence LOW (authors).

### Surfaced but out of scope (not recorded as candidates)

- Andersen, Crainic, Christiansen, "Service network design with management and coordination of multiple
  fleets", EJOR 193(2) 2009 — https://ideas.repec.org/a/eee/ejores/v193y2009i2p377-389.html (EJOR, out).
- Springer book chapter (Network Design with Applications to Transportation and Logistics, 2021, ch. 12)
  https://link.springer.com/10.1007/978-3-030-64018-7_12 (book, out).
- arXiv DDD preprints: "Dynamic discretization discovery under hard node storage constraints" (2303.01419),
  "Sparse DDD via arc-dependent time discretizations" (2305.19176), "DDD for the Multi-Depot Vehicle
  Scheduling Problem with Trip Shifting" (2304.05665) — preprints, venue unknown.
- "Capacitated Network Design with Uncertain Demand" — INFORMS J. Computing 14(3) 2002 (IJOC, out).
- Kang, Chow, Recker, "On activity-based network design problems", TRB 57 (2013) — in-scope venue but
  not SND methodology (activity-based travel), not recorded.
- TR Part E items (transe v174 2023; v126 2019) — out of scope.
- Unidentified: TRB 151 (2021) pp. 22–41 (https://ideas.repec.org/a/eee/transb/v151y2021icp22-41.html) —
  title not shown; check in r2. Also 10.1287/opre.50.2.395.434 — title not shown.

## Gaps

- No 2023–2026 in-scope SND paper corroborated yet (budget). Hewitt & Lehuede TRB 2023, Greening/Dahan/Erera
  TRB 2023, Baubaid et al. TS 2023 are the obvious targets.
- No pre-2005 classics beyond Crainic & Rousseau 1986 and the two OR 2002/2003 papers; Magnanti & Wong 1984,
  Farvolden & Powell 1994, Powell 1986, Keaton 1989/1992, Barnhart et al. 2000 remain to be corroborated.
- Consolidation / continuous-approximation strand (Daganzo, Hall, Campbell, Langevin et al., Ansari et al.)
  not searched.
- No DOIs captured for Elsevier items (snippets showed RePEc/REF pages, not DOI strings).
- No SECONDARY (space-logistics) search was possible.
