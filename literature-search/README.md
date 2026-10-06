# Methodology literature search: Regional Air Mobility air-traffic-flow management and Spaceport-to-Orbit feeder network design

**Venues:** INFORMS *Operations Research*, INFORMS *Transportation Science*, *Transportation Research Part B: Methodological*, *Transportation Research Part C: Emerging Technologies*
**Compiled:** 2026-10-06 · **Verified in-scope papers:** 453 (Operations Research 76, Transportation Science 238, TR-B 101, TR-C 38) · **Relevance:** RAM flow problem 138, spaceport feeder design 237, both 78

Companion files: [`bibliography.csv`](bibliography.csv) (one row per paper with annotations), [`bibliography.bib`](bibliography.bib) (BibTeX), [`data/papers.json`](data/papers.json) (full records), [`data/leads_unconfirmed.json`](data/leads_unconfirmed.json) (83 leads that could not be confirmed), [`search-log/`](search-log/) (every query run by every search agent).

## Contents

1. [Executive summary](#1-executive-summary)
2. [Scope, assumptions and method](#2-scope-assumptions-and-method)
3. [Part I: methodology for the RAM air-traffic-flow problem](#3-part-i-methodology-for-the-ram-air-traffic-flow-problem)
4. [Part II: methodology analogs for Spaceport-to-Orbit feeder network design](#4-part-ii-methodology-analogs-for-spaceport-to-orbit-feeder-network-design)
5. [Part III: cross-cutting toolbox and transfer map](#5-part-iii-cross-cutting-toolbox-and-transfer-map)
6. [Part IV: gaps and a research agenda](#6-part-iv-gaps-and-a-research-agenda)
7. [Annotated bibliography by methodology family](#7-annotated-bibliography-by-methodology-family)
8. [Appendix A: counts by venue, period and family](#appendix-a-counts-by-venue-period-and-family)
9. [Appendix B: search protocol, verification and limitations](#appendix-b-search-protocol-verification-and-limitations)
10. [Appendix C: unconfirmed leads and out-of-venue sightings](#appendix-c-unconfirmed-leads-and-out-of-venue-sightings)

---

## 1. Executive summary

**What this is.** A methodology-oriented literature map, restricted to INFORMS *Operations Research*, INFORMS *Transportation Science*, *Transportation Research Part B* and *Transportation Research Part C*, for two modelling problems: an air-traffic-flow problem for Regional Air Mobility (RAM), and the design of a feeder network that carries payload or passengers from many ground spaceports to a few orbital hubs. Every paper listed had its venue proven by a DOI or publisher URL seen in a live search result; nothing was added from memory.

**Main findings.**

- **The RAM flow problem has a mature, directly reusable core.** The time-indexed 0-1 formulation with cumulative "has departed by t" variables [[bertsimas1998](#bertsimas1998)] and its rerouting and network-flow extensions [[bertsimas2000](#bertsimas2000); [bertsimas2011](#bertsimas2011)] remain the reference model. Its descendants add uncertainty through scenario trees and stochastic integer programs [[ball2003](#ball2003); [mukherjee2007](#mukherjee2007); [liu2008](#liu2008); [wang2020](#wang2020)], and fairness among operators [[barnhart2012](#barnhart2012); [bertsimas2016](#bertsimas2016); [jacquillat2018](#jacquillat2018)]. A RAM model mainly needs new capacity resources: vertiport pads, chargers and aircraft state of charge.
- **Urban and regional air mobility is almost entirely a Transportation Research Part C literature, and recent.** Vertiport terminal scheduling, traffic assignment in layered urban airspace, chance-constrained UAM flow optimisation, and integrated electric regional fleet scheduling appeared in 2021 to 2026 [[shao2021](#shao2021); [song2021](#song2021); [wang2022](#wang2022); [justin2022](#justin2022); [trc-chance2024](#trc-chance2024); [trc-spacetime2022](#trc-spacetime2022)]. Transportation Science and Operations Research contribute the exact-method backbone, such as branch-and-price for drone service planning in urban airspace [[levin2023](#levin2023)].
- **The spaceport feeder problem has almost no direct literature in these venues.** A dedicated sweep found only six space-related Operations Research papers, from 1966 to 1978, on space-operations supply support, orbital transfers and Space Shuttle scheduling [[freeman1966](#freeman1966); [waespy1970](#waespy1970); [fisher1978](#fisher1978)]. Modern space-logistics optimisation is published in aerospace journals, outside the requested scope.
- **The spaceport problem is therefore best assembled from analogs.** Hub location with capacities, economies of scale, uncertainty and service-time limits [[campbell2012](#campbell2012); [contreras2011](#contreras2011); [alumur2012](#alumur2012); [yaman2007](#yaman2007)] supplies the strategic layer. Scheduled service network design with asset balancing on time-expanded networks [[pedersen2009](#pedersen2009); [andersen2011](#andersen2011); [crainic2016a](#crainic2016a)] and dynamic discretization discovery [[boland2017](#boland2017); [marshall2021](#marshall2021)] supplies the tactical layer. Liner-shipping feeder design [[brouer2014](#brouer2014); [agarwal2008](#agarwal2008); [jin2021](#jin2021)] and express air-network design [[barnhart1996](#barnhart1996); [armacost2002](#armacost2002)] are the closest structural cousins.
- **Both problems share one toolbox.** That toolbox is time-expanded networks, Benders and Lagrangian decomposition, column generation, and two-stage stochastic or robust models. Section 5 maps each tool to its canonical papers and to where it applies in each problem.

**Coverage.** 453 verified papers: 138 relevant mainly to the RAM problem, 237 mainly to the spaceport problem, 78 to both. Transportation Science dominates (about half). Transportation Research Part C is concentrated in the UAM and airspace families. Section 6 lists the gaps, and Appendix C lists 83 leads that could not be confirmed.


## 2. Scope, assumptions and method

### What was asked

A large literature search, restricted to INFORMS *Operations Research* (OR), INFORMS *Transportation Science* (TS), *Transportation Research Part B* (TR-B) and *Transportation Research Part C* (TR-C), for work related to the **methodology** behind two problems: a Regional Air Mobility (RAM) air-traffic-flow problem and a Spaceport-to-Orbit feeder network design problem. The search is methodology-oriented: a paper qualifies when its model or solution approach is one a modeller of either problem would reuse, whether or not the application is aviation or space.

### Assumptions made

* **RAM** is read as *Regional Air Mobility*: scheduled or on-demand flights with small electric or hybrid aircraft between many regional airports. The flow problem assigns departure times, routes, speeds and ground or airborne holds subject to airport, airspace-sector and charging or turnaround capacity, possibly under weather or demand uncertainty and with fairness across operators. The methodology that was searched for is the air traffic flow management (ATFM) lineage: time-indexed integer programs, stochastic and robust extensions, decomposition methods, equity and slot allocation, trajectory-based operations, runway and vertiport scheduling, dynamic network flows, and the urban or advanced air mobility literature. If RAM was meant differently, the ATFM coverage still applies because the search was organised by method rather than by application label.
* **Spaceport-to-Orbit feeder network design** is read as a hub-and-spoke design problem in which many spaceports (spokes) feed payload or passengers to a few orbital hubs through launch vehicles with limited, time-windowed capacity (launch windows, orbital phasing), reusable vehicles with turnaround times, hub capacity and uncertain demand. Because almost no paper in the four venues treats space transport directly, Part II is built from the methodological analogs: hub location, service network design, liner and feeder shipping, air cargo and express networks, multi-echelon and synchronised routing, network design under uncertainty, periodic and time-window scheduling, transit feeder design, fleet sizing and capacity expansion, and emerging-technology network design. A dedicated sweep for in-venue space, launch, satellite and orbital papers was run and its (sparse) results are reported.
* The methodology described in any earlier conversation was not available to this session, so the review covers the standard OR methodology families for both problems rather than one specific formulation.

### How the search was run

1. **Facet decomposition.** Each topic was split into ten methodology facets (listed in Appendix B). Each facet was searched by a dedicated agent using many distinct web-search queries that combined method phrases, problem phrases, author surnames, venue restrictors and DOI-prefix strings (`10.1287/opre`, `10.1287/trsc`, `10.1016/j.trb`, `10.1016/j.trc`). Every query is logged in `search-log/`.
2. **Mechanical venue verification.** Only the web-search tool could reach the internet from the session; publisher sites and bibliographic APIs were blocked. The venue of every paper was therefore established mechanically from evidence in real search results: a publisher URL or DOI whose prefix identifies the journal (`10.1287/opre` = OR, `10.1287/trsc` = TS, `10.1016/j.trb` or `S0191-2615` = TR-B, `10.1016/j.trc` or `S0968-090X` = TR-C), or an IDEAS/RePEc series page for the journal. A paper a search agent recorded from memory, or whose DOI never appeared in a real search result, was *not* counted; it was queued as a lead and re-searched. Leads that still lacked publisher evidence are listed in Appendix C rather than in the bibliography.
3. **Deduplication** by DOI, then by normalised title, across all agents and rounds.
4. **Gap rounds.** After the first facet pass, the families that came back thin (urban and regional air mobility, recent ATFM in TR-B and TR-C, transit feeders, emerging-technology networks, fleet sizing, and in-venue space papers) were searched again with different query strategies. A planned coverage critic and a full lead-resolution round were cut short by a usage limit; the partial results that completed were merged.
5. **Summaries.** Each entry's summary and transfer note come from the search agent that found it, written from the abstract text visible in search results. A separate per-paper abstract pass was not completed, so a small number of entries have no summary.
6. **Narrative synthesis** was written against the verified index only; a build step rejects any citation key that is not in the index, so every bracketed citation in Parts I to IV resolves to a verified entry in Section 7.

### How to read the entries

Each entry in Section 7 gives the citation key used in the text, authors (surnames as captured), year, venue, a DOI or publisher link, a summary, and a transfer note saying how the method applies to the RAM problem, the spaceport problem, or both. The CSV and BibTeX files carry the same fields.


## 3. Part I: methodology for the RAM air-traffic-flow problem

The RAM flow problem decides, for every flight of a fleet of small electric or hybrid aircraft, when it departs, which route it takes, how long it holds on the ground or in the air, and possibly its speed. These decisions must respect per-period capacities at regional airports and vertiports, in airspace sectors or corridors, and at charging and turnaround resources. The literature below is organised from the core formulation outward.

### 3.1 The core: time-indexed integer programs for ground holding and flow management

The lineage starts with single-airport ground holding. Andreatta and Romanin-Jacur studied a star network congested at one arrival airport [[andreatta1987](#andreatta1987)]. Richetta and Odoni solved the static stochastic problem as a linear program [[richetta1993](#richetta1993)] and later gave optimal dynamic algorithms and a fast heuristic [[richetta1995](#richetta1995)]. Terrab and Odoni framed strategic flow management [[terrab1993](#terrab1993)]. The multi-airport version, in which an aircraft's delay propagates to its next leg, was formulated as a 0-1 program [[vranas1994a](#vranas1994a)] and then made dynamic so that holds are revised as forecasts improve [[vranas1994](#vranas1994)]. Exact algorithms for it were benchmarked computationally [[andreatta1998](#andreatta1998)], and connections between flights were modelled explicitly [[navazio1998](#navazio1998)]. Hoffman and Ball compared formulations with banking constraints [[hoffman2000](#hoffman2000)].

The reference formulation is Bertsimas and Stock Patterson's model with en-route sector capacities [[bertsimas1998](#bertsimas1998)]. Its binary variables state whether flight f has reached resource j by period t. Capacity constraints become differences of consecutive variables, and the LP relaxation is strong because many constraints are facet-defining. Rerouting was added by recasting the problem as a dynamic multicommodity flow on a time-expanded airspace network, solved by Lagrangian generation and randomised rounding [[bertsimas2000](#bertsimas2000)]. The 2011 model encodes route choice through sector-adjacency constraints and solves instances the size of the US airspace in minutes [[bertsimas2011](#bertsimas2011)]. Lulli and Odoni adapted the model to the European setting, where en-route capacity binds and equity side effects appear [[lulli2007](#lulli2007)]. A dynamic rerouting model followed in TR-B [[mukherjee2009](#mukherjee2009)].

Recent work in this family adds operator preferences and new control regimes. Examples include central-authority flow management [[hamdan2022](#hamdan2022)], data-driven trajectory preferences [[degiovanni2024](#degiovanni2024)], passenger-centric ground delay programs [[jacquillat2022](#jacquillat2022)], and the effect of scheduling limits at a congested hub [[pyrgiotis2016](#pyrgiotis2016)]. Dynamic airspace sectorisation for flight-centric operations [[gerdes2018](#gerdes2018)] shows how to treat sector boundaries as decisions.

**Transfer to RAM.** The cumulative "by-time" variables extend directly. Each regional airport, vertiport pad group, corridor segment and charger bank becomes a resource with per-period capacity. Aircraft-continuation constraints [[vranas1994a](#vranas1994a)] become turnaround-and-charging constraints, which need one additional ingredient: a state-of-charge index on the time-expanded node, or a minimum-ground-time arc that depends on the energy used on the previous leg.

### 3.2 Uncertainty: stochastic, chance-constrained and robust flow management

Capacity uncertainty is the main reason holds are revised. Ball and co-authors showed that the stochastic ground-holding program has a dual network structure, so its LP relaxation is integral [[ball2003](#ball2003)]. Mukherjee and Hansen made the single-airport problem dynamic with a scenario tree [[mukherjee2007](#mukherjee2007)]. Liu, Hansen and Mukherjee brought scenario-based flow management to practice [[liu2008](#liu2008)]. Clarke and co-authors estimated stochastic airspace capacity from weather [[clarke2013](#clarke2013)]. Liu and Hansen added predictability to the cost function [[liu2016](#liu2016)]. Chen and co-authors used chance constraints [[chen2017](#chen2017)]. Wang and Jacquillat built a stochastic integer program that integrates scheduling and operations [[wang2020](#wang2020)]. Estes and Ball studied equity and formulation strength in stochastic integer models [[estes2020](#estes2020)]. Khassiba and co-authors used a two-stage program with chance constraints for extended arrival management [[khassiba2020](#khassiba2020)]. Capacity planning for air traffic control under demand and staffing uncertainty is treated in [[starita2020](#starita2020)] and across borders in [[starita2023](#starita2023)]. Airport-level control of runway configurations and service rates under uncertainty is solved by dynamic programming [[jacquillat2017](#jacquillat2017)]. Stochastic runway scheduling [[solak2018](#solak2018)] and airport congestion pricing under uncertainty [[czerny2010](#czerny2010)] complete the family.

**Transfer to RAM.** Weather affects small, low-altitude aircraft more than airliners, and charger outages add a second source of capacity uncertainty. A two-stage model in which first-stage departure slots are fixed and second-stage holds and diversions adapt per scenario [[mukherjee2007](#mukherjee2007); [liu2008](#liu2008)] is the natural template. The integrality result in [[ball2003](#ball2003)] suggests looking for network structure before using a general MIP solver.

### 3.3 Equity, collaborative decision making and slot allocation

A RAM system with several operators needs allocation rules that operators accept. The collaborative decision making literature formalised ration-by-schedule, compression and slot trading [[vossen2006](#vossen2006); [kotnyek2006](#kotnyek2006)]. Bard and Mohan reallocated arrival slots during a ground delay program [[bard2008](#bard2008)]. Manley and Sherry analysed the performance and equity of ground delay programs [[manley2010](#manley2010)]. Ration-by-distance [[ball2010](#ball2010)] gives priority to flights that can still use late capacity information. Equity at the network level is treated as a constraint or a second objective in [[barnhart2012](#barnhart2012)], with fairness and collaboration studied jointly in [[bertsimas2016](#bertsimas2016)]. Bertsimas, Farias and Trichakis quantified the efficiency lost to fairness in general allocation problems [[bertsimas2011a](#bertsimas2011a)]. Kuhn [[kuhn2013](#kuhn2013)] and Glover and Ball [[glover2013](#glover2013)] analysed the equity-efficiency trade-off in ground delay planning. Sherali and co-authors built airspace-planning models with equity and slot-exchange mechanisms [[sherali2002](#sherali2002); [sherali2003](#sherali2003); [sherali2006](#sherali2006); [sherali2011](#sherali2011)].

Strategic slot allocation is a related layer. It covers slot allocation under IATA rules [[ribeiro2018](#ribeiro2018); [ribeiro2019](#ribeiro2019)], allocation under uncertain capacity [[corolli2014](#corolli2014)], inter-airline equity in scheduling interventions [[jacquillat2018](#jacquillat2018)], fairness-aware slot mechanisms [[fairbrother2020](#fairbrother2020)], network-wide slot adjustments with connectivity [[keskin2023](#keskin2023)], and passenger-centric allocation [[birolini2023](#birolini2023)]. Collaborative demand-capacity balancing that minimises airspace users' costs [[xu2020](#xu2020); [xu2020a](#xu2020a)], stakeholder priorities in 4D trajectory optimisation [[dalsasso2018](#dalsasso2018)], and user-driven prioritisation of hotspots [[gasparin2025](#gasparin2025)] bring operator preferences into the flow model. Economics papers in TR-B compare pricing and slot policies [[verhoef2010](#verhoef2010); [basso2010](#basso2010)].

**Transfer to RAM.** RAM vertiports will be slot-controlled from the start. The constraint-based equity formulations [[barnhart2012](#barnhart2012); [bertsimas2016](#bertsimas2016)] attach directly to the time-indexed model of Section 3.1. The price-of-fairness bounds [[bertsimas2011a](#bertsimas2011a)] tell a regulator how much throughput an equity rule costs.

### 3.4 Large-scale solution methods

Most RAM instances will be smaller than national airline networks but will be solved more often. The relevant methods are LP-based branch-and-bound with strong formulations [[bertsimas1998](#bertsimas1998); [andreatta1998](#andreatta1998)], Lagrangian and dual decomposition by sector [[sun2011](#sun2011)], column generation [[lubbecke2005](#lubbecke2005)], and Benders variants [[rahmaniani2020](#rahmaniani2020); [crainic2021](#crainic2021)]. Starita and co-authors quantified the value of flexible flight-to-route assignment in pre-tactical planning [[starita2022](#starita2022)]. Integrated airline recovery papers solve flow-like problems with column-and-row generation [[maher2016](#maher2016)].

### 3.5 Trajectories, airspace structure and conflict resolution

Corridor-based RAM operations need capacity and conflict models for airspace. Early TS papers predicted conflict counts and durations at route intersections [[siddiqee1973](#siddiqee1973); [siddiqee1974](#siddiqee1974)], and an en-route sector capacity model followed [[janic1991](#janic1991)]. Optimisation of aircraft deconfliction is reviewed in [[pelegrin2022](#pelegrin2022)], with exact turn-change formulations [[alonsoayuso2016](#alonsoayuso2016)] and a bi-objective approach under uncertainty [[lehouillier2017](#lehouillier2017)]. Speed control to absorb delay without fuel penalty appears as subliminal speed control [[rey2016](#rey2016); [trc-simulation2011](#trc-simulation2011)] and as linear holding [[xu2017](#xu2017)]. Airspace design is studied through dynamic sectorisation [[tang2012](#tang2012)], conflict counts in layered airspace [[trc-three2018](#trc-three2018)], strategic deconfliction by simulated annealing [[trc-simulated2019](#trc-simulated2019)], and main-flow systems that replace free routes [[trc-free2020](#trc-free2020)]. Robust terminal routes in convective weather [[pfeil2012](#pfeil2012)] and sequential en-route allocation mechanisms [[kim2015](#kim2015)] complete the set.

### 3.6 Airports, runways and terminal areas

Vertiports are small airports, so runway and terminal scheduling methods transfer almost unchanged. These include static aircraft landing scheduling [[beasley2000](#beasley2000)], constrained position shifting [[balakrishnan2010](#balakrishnan2010)], pruning rules for exact runway sequencing [[demaere2018](#demaere2018)], runway configuration selection [[bertsimas2011b](#bertsimas2011b)], and unified optimisation of flows through airports [[bertsimas2016a](#bertsimas2016a)]. Queueing models describe airport capacity and delay [[venkatakrishnan1993](#venkatakrishnan1993); [simaiakis2016](#simaiakis2016); [nikoleris2012](#nikoleris2012); [peterson1995](#peterson1995)]. Jacquillat and Odoni integrated scheduling with operations [[jacquillat2015](#jacquillat2015)]. Terminal airspace scheduling is solved as an optimisation problem in [[ng2024](#ng2024)].

### 3.7 Urban, advanced and regional air mobility

This is the newest family and sits mostly in TR-C. At the vertiport level, [[shao2021](#shao2021)] proposes terminal-area control rules and adaptive eVTOL scheduling across several vertiports, and [[song2021](#song2021)] develops approach control for multicopter VTOL operations. In urban airspace, complexity-minimising traffic assignment on layered networks is treated in [[wang2022](#wang2022); [wang2022a](#wang2022a); [wang2023](#wang2023)], and high-density automated flight planning in [[tang2021](#tang2021)]. UAV parcel-delivery traffic management is studied in [[trc-traffic2022](#trc-traffic2022)], and branch-and-price drone service planning in urban airspace in [[levin2023](#levin2023)]. Under uncertainty, recent work covers chance-constrained UAM flow optimisation with disruption recovery [[trc-chance2024](#trc-chance2024)], conflict-probability-based strategic deconfliction for UAS traffic management [[trc-conflict2025](#trc-conflict2025)], real-time simulation and management of large UAM systems [[trc-real2025](#trc-real2025)], and a comparison of pre-planned routes with dynamic 4D trajectories [[trc-pre2026](#trc-pre2026)]. For regional electric aviation, [[justin2022](#justin2022)] integrates fleet assignment and scheduling, and [[trc-spacetime2022](#trc-spacetime2022)] gives a space-time-energy flow formulation for designing and operating a regional air mobility network. Earlier on-demand aviation papers in TS model per-seat on-demand service as an integer multicommodity flow [[espinoza2008](#espinoza2008); [espinoza2008a](#espinoza2008a)] and schedule time-shared jets [[keskinocak1998](#keskinocak1998)].

Planning-side work includes air taxi demand across 40 US cities [[haan2021](#haan2021)], a UAM review comparing it with autonomous and electric ground modes [[garrow2021](#garrow2021)], UAM network design through hub location [[willey2021](#willey2021)], battery charging and swapping infrastructure for electric short-haul aircraft [[trc-optimizing2023](#trc-optimizing2023)], integrated air-rail scheduling [[trb-integrated2025](#trb-integrated2025)], and on-demand UAM ridesharing [[trc-demand2025](#trc-demand2025)]. Frequency competition [[teodorovic1989](#teodorovic1989); [vaze2012](#vaze2012)] and air-rail competition [[adler2010](#adler2010)] inform how RAM services will compete.

**Transfer to RAM.** The space-time-energy network of [[trc-spacetime2022](#trc-spacetime2022)] is the closest existing formulation to a RAM flow model with charging. Combining it with the cumulative variables of [[bertsimas1998](#bertsimas1998)] and the scenario structure of [[liu2008](#liu2008)] gives a defensible base model.

### 3.8 Airline scheduling, recovery and dynamic flows

Two adjacent families provide reusable components. Airline planning and recovery uses time-space networks for fleet assignment and routing [[barnhart2002](#barnhart2002); [lohatepanont2004](#lohatepanont2004); [rexing2000](#rexing2000)], robust routing against delay propagation [[lan2006](#lan2006); [dunbar2012](#dunbar2012); [yan2018](#yan2018)], and integrated recovery [[petersen2012](#petersen2012); [maher2016](#maher2016); [marla2017](#marla2017); [cadarso2023](#cadarso2023)]. Cruise-speed control during recovery [[akturk2014](#akturk2014); [arikan2017](#arikan2017); [delgado2013](#delgado2013); [delgado2014](#delgado2014)] is directly relevant to energy-limited aircraft. Barnhart, Belobaba and Odoni survey the field [[barnhart2003](#barnhart2003)].

Dynamic network flow theory supplies the time-expansion machinery. Maximal dynamic flows date to Ford and Fulkerson [[ford1958](#ford1958)]. System-optimal dynamic traffic assignment has formulations from Merchant and Nemhauser [[merchant1978](#merchant1978)] through cell-based models [[ziliaskopoulos2000](#ziliaskopoulos2000); [zheng2011](#zheng2011); [nie2011](#nie2011)]. Continuous-time network design via dynamic discretization discovery [[boland2017](#boland2017); [marshall2021](#marshall2021); [vu2020](#vu2020)] avoids building the full time-expanded network, which matters when RAM periods are short. NextGen flow corridors were allocated dynamically in [[yousefi2013](#yousefi2013)].


## 4. Part II: methodology analogs for Spaceport-to-Orbit feeder network design

The spaceport feeder problem has a strategic layer and a tactical layer. The strategic layer chooses which spaceports and orbital hubs to open, which spoke-to-hub and hub-to-hub links to serve, and with what vehicle capacity. The tactical layer schedules launches inside launch windows, rotates reusable vehicles through turnaround, and consolidates payload at hubs. The four venues contain almost no work on space transport itself, so this part first reports what exists and then assembles the methodology from analogs.

### 4.1 What the four venues contain on space transport

A dedicated sweep of all four journals for spaceports, launch scheduling, satellites, orbital logistics and space tourism found six papers, all in *Operations Research* between 1966 and 1978. They cover a supply-support model for space operations [[freeman1966](#freeman1966)], a method to compare solar-system exploration policies [[chamberlain1970](#chamberlain1970)], the logistics of lunar astronomy research [[freeman1970](#freeman1970)], linear programming for orbital-transfer trajectories [[waespy1970](#waespy1970)], queueing analysis of satellite networks [[elbardai1970](#elbardai1970)], and an algorithm for Space Shuttle scheduling [[fisher1978](#fisher1978)]. Nothing was found in *Transportation Science*, TR-B or TR-C. Modern space-logistics network models, such as the generalised multicommodity network flow and time-expanded campaign models, are published in aerospace journals and are outside the requested venues. Appendix C lists the ones the search encountered.

The practical consequence is that a spaceport feeder paper aimed at these venues would be the first of its kind there. It would need to position itself against the analog families below.

### 4.2 Hub location: the strategic backbone

Spaceports feeding a few orbital hubs form a hub-and-spoke network, so hub location is the natural strategic model. The field began with O'Kelly's quadratic formulation [[okelly1986](#okelly1986)], followed by Aykin's work on locating hubs [[aykin1988](#aykin1988)] and Campbell's p-hub median and related formulations [[campbell1996](#campbell1996)], with a continuous-demand version in TR-B [[campbell1993](#campbell1993)]. Campbell and O'Kelly reviewed twenty-five years of the field [[campbell2012](#campbell2012)], and a reference benchmark now exists [[wandelt2022](#wandelt2022)].

Several extensions map directly onto spaceport features:

- **Hub capacity and modular capacity levels**, matching limited docking or propellant capacity at an orbital depot [[correia2010](#correia2010); [contreras2012](#contreras2012)].
- **Economies of scale on inter-hub links**, matching the cost advantage of large transfer vehicles between orbital hubs [[okelly1998](#okelly1998); [decamargo2009](#decamargo2009); [rostami2022](#rostami2022)].
- **Service-time limits.** Latest-arrival hub location [[yaman2007](#yaman2007)], release-time scheduling with hub location for next-day delivery [[yaman2012](#yaman2012)], and stratified p-hub centre and covering models [[ghaffarinasab2022](#ghaffarinasab2022)] correspond to payload delivery deadlines.
- **Incomplete and hierarchical hub networks**, where not every hub pair is linked [[alumur2009](#alumur2009); [yaman2009](#yaman2009)], and hub line location [[martinsdesa2015](#martinsdesa2015)].
- **Uncertainty and reliability.** This includes stochastic and robust hub location [[alumur2012](#alumur2012); [zetina2017](#zetina2017); [merakli2016](#merakli2016); [taherkhani2021](#taherkhani2021)], distributionally robust hub location [[wang2020a](#wang2020a)], reliable hub-and-spoke design under hub failure [[an2015](#an2015)], and stochastic p-hub median heuristics [[peiro2019](#peiro2019)].
- **Exact methods at scale.** Benders decomposition for large uncapacitated hub location [[contreras2011](#contreras2011)] and for profit-maximising capacitated variants [[taherkhani2020](#taherkhani2020)] scales to large instances. Supermodular set-function views give fast heuristics [[contreras2014](#contreras2014)].
- **Multi-period and dynamic hub location**, matching phased deployment of spaceports [[contreras2011a](#contreras2011a); [or-budget2025](#or-budget2025)].

Freight-network cousins add useful modelling devices. These include direct versus terminal routing with concave costs [[hall1987](#hall1987)], the break-bulk role of terminals [[daganzo1987](#daganzo1987)], intermodal hub location and design with several vehicle types [[racunica2005](#racunica2005); [meng2011](#meng2011); [serper2016](#serper2016)], hub location combined with route dimensioning [[yildiz2021](#yildiz2021)], and Benders for hub-and-shuttle transit [[maheo2019](#maheo2019)].

### 4.3 Service network design on time-expanded networks

Launch windows, vehicle turnaround and consolidation are tactical features. Service network design on time-expanded networks handles all three. Magnanti and Wong set out network design models for transportation planning [[magnanti1984](#magnanti1984)], and Crainic and co-authors gave a general multicommodity, multimode freight framework [[crainic1986](#crainic1986)]. Classic solution methods include dual ascent [[balakrishnan1989](#balakrishnan1989)], Lagrangian heuristics inside branch-and-bound [[holmberg1998](#holmberg1998); [holmberg2000](#holmberg2000)], subgradient methods [[farvolden1994](#farvolden1994)], and cycle-based neighbourhoods [[ghamlouche2003](#ghamlouche2003)].

The features most relevant to reusable launch vehicles are the following:

- **Asset balance.** Every vehicle that leaves a node must eventually return, as with design-balanced service network design [[pedersen2009](#pedersen2009); [chouman2015](#chouman2015)] and branch-and-price with asset management [[andersen2011](#andersen2011)].
- **Resource constraints on fleets** [[crainic2016a](#crainic2016a)] and **resource acquisition under uncertainty** [[hewitt2019a](#hewitt2019a)].
- **Demand uncertainty** in two-stage service network design [[lium2009](#lium2009)] and robust variants [[ts-robust2020](#ts-robust2020)]. Stochastic design with rerouting is treated in [[bai2014](#bai2014)].
- **Continuous time.** Dynamic discretization discovery solves the continuous-time problem without a full time-expanded network [[boland2017](#boland2017); [hewitt2019](#hewitt2019); [scherr2020](#scherr2020); [marshall2021](#marshall2021)]. This matters when launch windows are short and irregular. New formulations [[hewitt2023](#hewitt2023)], flexible schedules [[hewitt2022](#hewitt2022)], holding costs [[shu2024](#shu2024)] and dynamic variants with cost-function approximation [[ts-cost2025](#ts-cost2025)] extend it.

Large-scale less-than-truckload and parcel networks show how far these models scale [[jarrah2009](#jarrah2009); [erera2013](#erera2013); [lindsey2016](#lindsey2016); [baubaid2021](#baubaid2021); [baubaid2023](#baubaid2023); [greening2023](#greening2023); [malik2026](#malik2026)].

### 4.4 Liner and feeder shipping: the closest structural analog

Container shipping has the same architecture as a spaceport network. Mother vessels on trunk loops call at transshipment hubs, feeder vessels shuttle between hubs and small ports, ships are reusable assets on cyclic rotations, and port calls are slotted. The liner-shipping network design benchmark and base model [[brouer2014](#brouer2014)] and the review of containership routing and scheduling [[meng2014](#meng2014)] are the entry points. Agarwal and Ergun combined ship scheduling with network design for cargo routing [[agarwal2008](#agarwal2008)] and designed networks for carrier alliances [[agarwal2010](#agarwal2010)]. Koza and co-authors integrated network design with scheduling [[koza2020](#koza2020)], and Xia and co-authors solved network design by simultaneous column-and-row generation [[xia2025](#xia2025)].

The features that transfer most directly to spaceports are:

- **Feeder routing at a congested hub**, with transshipment coordination [[jin2021](#jin2021)].
- **Fleet deployment and speed optimisation**, which correspond to launch cadence and vehicle allocation [[xia2015](#xia2015); [zhen2019](#zhen2019); [karsten2018](#karsten2018)].
- **Transit-time-sensitive demand** [[wang2013](#wang2013); [meng2016](#meng2016); [akyuz2016](#akyuz2016)].
- **Schedule reliability** under port-time uncertainty [[wang2012](#wang2012); [zhang2022](#zhang2022)].
- **Empty repositioning** of reusable assets [[song2012](#song2012); [erera2009](#erera2009); [tierney2015](#tierney2015)].
- **Distributionally robust fleet deployment with slot allocation** [[zhang2025](#zhang2025)].

Christiansen and co-authors provide the broader ship routing and scheduling survey [[christiansen2004](#christiansen2004)].

### 4.5 Air cargo, express and airline network design

Express parcel networks have overnight time windows, a few sort hubs and expensive aircraft. They are the second closest analog. Barnhart and Schneur designed air networks for express shipment service [[barnhart1996](#barnhart1996)]. Composite-variable formulations made the problem tractable [[armacost2002](#armacost2002)], and multimodal express delivery was treated as service network design [[kim1999](#kim1999)]. Time-definite freight delivery networks and their hierarchical variants are in [[lin2001](#lin2001); [lin2004](#lin2004)]. Air cargo network planning [[derigs2009](#derigs2009)] and consolidation of air cargo shipments [[leung2009](#leung2009)] cover the cargo side.

Airline hub-and-spoke design covers when hubbing pays. Relevant work includes scheduling and routing in hub-and-spoke systems [[dobson1993](#dobson1993)], networking policies [[jaillet1995](#jaillet1995)], network design [[lederer1998](#lederer1998)], competition-driven hub choice [[hansen1990](#hansen1990); [adler2005](#adler2005)], and flight scheduling at hub airports [[trietsch1993](#trietsch1993)]. Integrated schedule design and fleet assignment [[lohatepanont2004](#lohatepanont2004); [pita2013](#pita2013); [cacchiani2017](#cacchiani2017); [birolini2021a](#birolini2021a)] shows how to co-optimise network and vehicle assignment. Electric aircraft on subsidised networks [[kinene2024](#kinene2024)] are a near-term analog for capacity-limited vehicles with operational range limits.

### 4.6 Multi-echelon design, location-routing and synchronisation

Ground spaceport to orbital hub to final orbit is a two-echelon system. The two-echelon capacitated vehicle routing problem has math-based heuristics [[perboli2011](#perboli2011)], branch-and-cut [[jepsen2013](#jepsen2013)], exact algorithms [[baldacci2013](#baldacci2013)] and recent branch-cut-and-price methods [[marques2022](#marques2022); [mhamedi2022](#mhamedi2022)]. Chance-constrained variants handle stochastic demand [[sluijk2023](#sluijk2023)]. Location-routing gives the joint facility and route design [[laporte1988](#laporte1988); [prins2007](#prins2007); [baldacci2011](#baldacci2011); [schiffer2018](#schiffer2018)]. City-logistics two-tier planning under demand uncertainty is the closest tactical analog [[crainic2009](#crainic2009); [crainic2016](#crainic2016)].

Synchronisation is the key feature for orbital rendezvous. Drexl surveys vehicle routing with synchronisation constraints [[drexl2012](#drexl2012)]. Pickup and delivery with transfers [[masson2013](#masson2013)] and with scheduled lines [[ghilas2016](#ghilas2016); [ghilas2018](#ghilas2018)] model payload handed between vehicles at a hub at a scheduled time. Joint location-inventory models [[shen2003](#shen2003); [atamturk2012](#atamturk2012)] cover propellant or spare-part depots at hubs.

### 4.7 Network design under uncertainty and disruption

Launch failures, weather scrubs and demand uncertainty call for robust and reliable design. Snyder and Daskin introduced reliability models for facility location [[snyder2005](#snyder2005)]. Cui, Ouyang and Shen designed reliable facility locations under disruption risk [[cui2010](#cui2010)], and Peng and co-authors applied reliability to logistics networks [[peng2011](#peng2011)]. Two-stage robust network flow and design under demand uncertainty is due to Atamtürk and Zhang [[atamturk2007](#atamturk2007)]. Reliable location-routing under probabilistic facility disruption [[xie2016](#xie2016)] and the stochastic multiperiod location-transportation problem [[klibi2010](#klibi2010)] extend these ideas to routing.

### 4.8 Launch windows as periodic and time-window scheduling

Launch windows recur with orbital geometry, so periodic scheduling is the right abstraction. The periodic event scheduling problem and cyclic timetabling supply the tools: constraint generation [[odijk1996](#odijk1996)], variable trip times [[kroon2003](#kroon2003)], flexible connections [[kroon2014](#kroon2014)], cycle-time optimisation [[sparing2017](#sparing2017)], adjustable robust periodic timetabling [[polinder2019](#polinder2019)], and the first optimised railway timetable in practice [[liebchen2008](#liebchen2008)]. Timetable synchronisation for transfers [[wong2008](#wong2008)] corresponds to rendezvous timing.

Berth allocation is a slot-assignment problem on a shared resource with time windows. It maps onto pad and docking-port assignment through the dynamic and continuous berth allocation models [[imai2001](#imai2001); [imai2003](#imai2003); [imai2005](#imai2005)], tabu search [[cordeau2005](#cordeau2005)], integrated berth and crane planning [[meisel2013](#meisel2013)], and distributionally robust berth allocation [[agra2022](#agra2022)]. Gate reassignment [[zhang2017](#zhang2017)] is the airport analog.

### 4.9 Transit feeder design and continuum approximation

Before detailed optimisation, continuum approximation gives closed-form insight on how many hubs to open and how dense the feeder layer should be. Relevant work includes the structure of competitive transit networks [[daganzo2010](#daganzo2010)], radial-city designs [[badia2014](#badia2014)], spatially heterogeneous demand [[ouyang2014](#ouyang2014)], coordinated rail and bus feeders [[wirasinghe1977](#wirasinghe1977)], parallel transit lines [[hurdle1973](#hurdle1973)], and paired-line hybrid transit [[chen2017a](#chen2017a)]. Discrete feeder design and timed transfers [[chang1991a](#chang1991a); [kim2014](#kim2014); [fonseca2018](#fonseca2018)], with the Ibarra-Rojas review of bus system planning [[ibarrarojas2015](#ibarrarojas2015)], cover the operational side. Data-driven transit network design at scale [[bertsimas2021](#bertsimas2021)] shows a modern exact approach.

### 4.10 Emerging-technology network design

Range-limited, recharge-dependent vehicles are a common thread between drones and launch vehicles. Truck-and-drone routing [[agatz2018](#agatz2018); [roberti2021](#roberti2021); [dayarian2020](#dayarian2020); [ts-coordinated2021](#ts-coordinated2021)], drone routing with energy functions [[cheng2020](#cheng2020)], range-limited drone deliveries with speed optimisation [[dukkanci2021](#dukkanci2021)], and alternative-fuel or charging station location [[arslan2018](#arslan2018); [ts-charging2021](#ts-charging2021); [mahmutogullari2024](#mahmutogullari2024)] contain reusable modelling ideas for propellant-constrained vehicles and refuelling depots.

### 4.11 Fleet sizing, reuse and capacity expansion

Reusable launch vehicles turn the fleet into a repositioned asset. Fleet sizing under production cycles and uncertain travel times [[turnquist1986](#turnquist1986)], fleet sizing and vehicle allocation [[beaujon1991](#beaujon1991)], and heterogeneous-asset fleet sizing [[wu2005](#wu2005)] cover the size question. Empty-flow management is reviewed in [[dejax1987](#dejax1987)] and modelled stochastically in [[crainic1993](#crainic1993); [cheung1998](#cheung1998)]. Adaptive dynamic programming for fleet management [[godfrey2002](#godfrey2002); [godfrey2002a](#godfrey2002a); [topaloglu2007](#topaloglu2007); [simao2009](#simao2009)] covers the operational side. Locomotive routing and scheduling [[ahuja2005](#ahuja2005); [vaidyanathan2008](#vaidyanathan2008)] shows asset rotation with maintenance cycles. Integrated periodic timetabling with vehicle circulation [[vanlieshout2021](#vanlieshout2021)] corresponds to launch cadence with vehicle turnaround.

Capacity expansion covers phased build-out. The Luss survey [[luss1982](#luss1982)], multiregion dynamic expansion [[fong1981](#fong1981)], expansion under stochastic demand [[bean1992](#bean1992)], approximation schemes [[ahmed2003](#ahmed2003)], multistage stochastic capacity planning with Dantzig-Wolfe decomposition [[singh2009](#singh2009)], the value of multistage models [[huang2009](#huang2009)], dynamic facility location with modular capacities [[jena2015](#jena2015)], and airport capacity expansion under uncertainty [[sun2015](#sun2015); [gong2023](#gong2023)] supply the methods. Real-option network models [[chow2011](#chow2011)] value staged investment under uncertain demand.


## 5. Part III: cross-cutting toolbox and transfer map

The two problems share most of their methodology. The table maps each tool to canonical papers in the verified set and to where it enters each problem.

| Tool | Canonical papers | In the RAM flow problem | In spaceport feeder design |
|---|---|---|---|
| Time-indexed 0-1 variables with cumulative "by-time" form | [[bertsimas1998](#bertsimas1998); [bertsimas2011](#bertsimas2011)] | Departure times, holds and capacity at airports, vertiports, corridors and chargers | Launch slot assignment inside windows |
| Time-expanded multicommodity network | [[bertsimas2000](#bertsimas2000); [ford1958](#ford1958); [pedersen2009](#pedersen2009)] | Rerouting and airborne holding | Vehicle rotation, consolidation, asset balance |
| Dynamic discretization discovery | [[boland2017](#boland2017); [marshall2021](#marshall2021); [hewitt2019](#hewitt2019)] | Short periods without a huge network | Irregular launch windows in continuous time |
| Space-time-energy networks | [[trc-spacetime2022](#trc-spacetime2022); [justin2022](#justin2022)] | Charging and state of charge | Propellant state and refuelling at depots |
| Lagrangian and dual decomposition | [[bertsimas2000](#bertsimas2000); [sun2011](#sun2011); [holmberg2000](#holmberg2000)] | Decompose by sector or by flight | Decompose by commodity or hub |
| Benders decomposition | [[contreras2011](#contreras2011); [rahmaniani2020](#rahmaniani2020); [crainic2021](#crainic2021)] | Strategic slots versus operational holds | Hub opening versus routing |
| Column generation and branch-and-price | [[lubbecke2005](#lubbecke2005); [levin2023](#levin2023); [andersen2011](#andersen2011)] | Route or trajectory columns per flight | Vehicle rotation columns |
| Two-stage and multistage stochastic programs | [[mukherjee2007](#mukherjee2007); [liu2008](#liu2008); [lium2009](#lium2009); [singh2009](#singh2009)] | Weather and charger outages | Demand, launch scrubs, phased build-out |
| Chance constraints | [[chen2017](#chen2017); [khassiba2020](#khassiba2020); [trc-chance2024](#trc-chance2024); [sluijk2023](#sluijk2023)] | Probabilistic capacity | Probabilistic launch success |
| Robust and distributionally robust optimisation | [[atamturk2007](#atamturk2007); [wang2020a](#wang2020a); [zhang2025](#zhang2025)] | Capacity ranges | Demand ranges |
| Equity constraints and price of fairness | [[barnhart2012](#barnhart2012); [bertsimas2016](#bertsimas2016); [bertsimas2011a](#bertsimas2011a)] | Fairness among operators | Fairness among spaceports or customers |
| Periodic event scheduling | [[kroon2003](#kroon2003); [liebchen2008](#liebchen2008); [polinder2019](#polinder2019)] | Recurring schedule banks at vertiports | Recurring launch windows |
| Continuum approximation | [[daganzo2010](#daganzo2010); [ouyang2014](#ouyang2014); [ouyang2006](#ouyang2006)] | Fleet and vertiport sizing | Number of hubs and feeder density |
| Approximate dynamic programming | [[godfrey2002](#godfrey2002); [simao2009](#simao2009); [jacquillat2017](#jacquillat2017)] | Real-time control | Fleet repositioning under uncertainty |

**A combined architecture.** A defensible model for each problem stacks three layers that the literature has solved separately:

1. **Strategic network.** Hub location with capacity levels and uncertainty [[contreras2012](#contreras2012); [alumur2012](#alumur2012)] chooses spaceports and orbital hubs. For RAM, it chooses vertiports and regional airports [[willey2021](#willey2021)].
2. **Tactical schedule.** Scheduled service network design with asset balance [[pedersen2009](#pedersen2009); [andersen2011](#andersen2011)] on a time-expanded network sets launch or flight frequencies, solved with dynamic discretization discovery [[boland2017](#boland2017)].
3. **Operational flow.** A time-indexed flow model [[bertsimas1998](#bertsimas1998)] with scenario recourse [[liu2008](#liu2008)] assigns slots and holds on the day.

Benders decomposition [[contreras2011](#contreras2011); [crainic2021](#crainic2021)] links layers 1 and 2. Rolling-horizon re-optimisation [[vranas1994](#vranas1994)] links layers 2 and 3.


## 6. Part IV: gaps and a research agenda

### 6.1 Gaps in the literature

- **No space transport network design in the four venues since 1978.** The only in-venue work is [[fisher1978](#fisher1978)] and the 1966 to 1970 Operations Research papers. A spaceport feeder model built on hub location and service network design would be new in these journals.
- **Energy is rarely a network resource in flow management.** The classic flow models [[bertsimas1998](#bertsimas1998); [bertsimas2011](#bertsimas2011)] have no state of charge. Only a few TR-C papers add energy [[trc-spacetime2022](#trc-spacetime2022); [justin2022](#justin2022); [trc-optimizing2023](#trc-optimizing2023)]. A RAM flow model with charger capacity, state-of-charge-dependent turnaround and stochastic capacity combines pieces that have not been combined.
- **UAM traffic management has few exact methods.** Most TR-C UAM papers use simulation or heuristics. Exact decomposition, as in [[levin2023](#levin2023)], is the exception.
- **Equity among small operators is unexplored for RAM.** The equity literature [[barnhart2012](#barnhart2012); [bertsimas2016](#bertsimas2016); [jacquillat2018](#jacquillat2018)] targets airlines. RAM introduces many small operators and public-service routes, as in the subsidised electric network of [[kinene2024](#kinene2024)].
- **Launch windows as periodic constraints inside network design.** Periodic event scheduling [[kroon2003](#kroon2003); [polinder2019](#polinder2019)] and service network design [[pedersen2009](#pedersen2009)] have not been combined with hub location in these venues.
- **Uncertainty in launch success.** Reliable hub design [[an2015](#an2015); [snyder2005](#snyder2005)] models facility failure, not stochastic loss of a vehicle and its payload on an arc. That is an open modelling question.

### 6.2 Suggested research agenda

1. **RAM flow model.** Extend [[bertsimas1998](#bertsimas1998)] with charger and pad resources and a state-of-charge dimension as in [[trc-spacetime2022](#trc-spacetime2022)]. Add two-stage capacity scenarios as in [[liu2008](#liu2008)] and an equity constraint as in [[barnhart2012](#barnhart2012)]. Solve with Benders or column generation [[rahmaniani2020](#rahmaniani2020); [levin2023](#levin2023)].
2. **Spaceport feeder design.** Formulate a capacitated, multi-period hub location [[contreras2012](#contreras2012); [contreras2011a](#contreras2011a)] with design-balanced service network design for reusable vehicles [[pedersen2009](#pedersen2009); [andersen2011](#andersen2011)]. Represent launch windows as periodic event constraints [[kroon2003](#kroon2003)]. Handle demand and launch uncertainty with a two-stage or distributionally robust model [[alumur2012](#alumur2012); [wang2020a](#wang2020a)].
3. **Benchmarking.** Reuse the instance-generation conventions of hub location [[wandelt2022](#wandelt2022)] and liner shipping [[brouer2014](#brouer2014)] so the new models can be compared with established ones.

### 6.3 Limitations of this search

- **Abstracts were not retrieved per paper.** Summaries come from search-result text captured by the search agents. Roughly 14 entries have no summary.
- **Some author lists are incomplete.** Where a search result did not show authors, the entry says "authors not captured" and its key is built from the venue and title. Complete these from the DOI before citing.
- **Coverage is broad, not exhaustive.** Each facet had one search pass of about 28 queries. A second resolver pass and a coverage critic were interrupted by a usage limit. The 83 unconfirmed leads in Appendix C are the most likely missing papers.
- **Venue proof is mechanical.** It relies on DOI prefixes and publisher URLs. A paper whose search result showed neither was excluded even if it is real.


## 7. Annotated bibliography by methodology family

Entries are generated from the verified records. Each shows the model class, solution method, a summary, and how the methodology transfers to the RAM flow problem (→ RAM) and to spaceport feeder design (→ Spaceport). Author fields hold surnames as captured from search results; complete them from the DOI before citing.

### Deterministic ATFM IP (14 papers)

<a id="andreatta1987"></a>**[andreatta1987]** Andreatta, Romanin-Jacur (1987). *Aircraft Flow Management under Congestion*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v21y1987i4p249-253.html)  
Earliest stochastic ground-holding model: an idealized star-shaped airway network with congestion only at the central arrival airport and probabilistic landing capacity; chooses ground delays for inbound flights to minimize total expected delay cost and gives a polynomial-time (dynamic-programming style) exact algorithm for this single-period problem.  
*→ RAM flow problem:* The star network with one congested node is exactly a RAM regional hub or vertiport fed by many small fields; its polynomial structure suggests fast exact subroutines for per-hub hold assignment inside a larger RAM flow model.  

<a id="vranas1994"></a>**[vranas1994]** Vranas, Bertsimas, Odoni (1994). *Dynamic Ground-Holding Policies for a Network of Airports*. Transp. Sci. [10.1287/trsc.28.4.275](https://doi.org/10.1287/trsc.28.4.275)  
First dynamic treatment of the multi-airport ground-holding problem: compact pure 0-1 integer programs on a discretized time horizon for a network of airports with connected flights, re-solved as time advances and weather forecasts improve; one formulation lets the arrival/departure capacity mix be updated via runway use.  
*→ RAM flow problem:* Provides the rolling-horizon re-solve template a RAM operations centre needs when weather or charger availability updates arrive during the day.  

<a id="vranas1994a"></a>**[vranas1994a]** Vranas, Bertsimas, Odoni (1994). *The Multi-Airport Ground-Holding Problem in Air Traffic Control*. Oper. Res. [10.1287/opre.42.2.249](https://doi.org/10.1287/opre.42.2.249)  
First network (multi-airport) ground-holding formulation: several 0-1 integer programs assign ground holds to flights over discrete time periods subject to per-period arrival/departure capacities at each airport, with flights coupled through aircraft continuation (down-the-road delay propagation). Solved by LP relaxation plus a rounding heuristic; instances with 6 airports and 3,000 flights solved in reasonable time.  
*→ RAM flow problem:* Aircraft-connectivity constraints are exactly what links successive RAM legs of a small electric fleet through turnaround and charging; this is the first network-level GHP that models them.  

<a id="richetta1995"></a>**[richetta1995]** Richetta, Odoni (1995). *Optimal Algorithms and a Remarkably Efficient Heuristic for the Ground-Holding Problem in Air Traffic Control*. Oper. Res. [10.1287/opre.43.5.758](https://doi.org/10.1287/opre.43.5.758)  
Compares optimal static and dynamic stochastic-LP solutions to the single-airport ground-holding problem with a very fast heuristic that uses probabilistic landing-capacity forecasts and accounts for the dynamic nature of decisions; on Boston Logan data the heuristic beats the static optimum and deterministic approaches and is within 5% of the dynamic optimum at a fraction of the computing time.  
*→ RAM flow problem:* Shows when a cheap slot-assignment heuristic suffices at a single capacity-constrained regional airport, useful as the inner solver in a decomposed RAM network model.  

<a id="bertsimas1998"></a>**[bertsimas1998]** Bertsimas, Stock Patterson (1998). *The Air Traffic Flow Management Problem with Enroute Capacities*. Oper. Res. [10.1287/opre.46.3.406](https://doi.org/10.1287/opre.46.3.406)  
The canonical BSP model: a time-indexed 0-1 IP with cumulative variables (flight f has reached sector j by time t) that enforces airport arrival/departure and en-route sector capacities per period, with ground holding, airborne holding and speed control chosen jointly. Shows the formulation is strong (several inequalities are facet-defining, LP bound at least as tight as earlier models), extends to rerouting and hub-and-spoke banks, and solves instances with thousands of flights.  
*→ RAM flow problem:* The by-time variable discretization is the standard way to encode departure-time assignment and holds on a time-expanded network; for RAM it extends directly to vertiport/regional-airport, airspace and charging-slot capacities per period.  

<a id="bertsimas2000"></a>**[bertsimas2000]** Bertsimas, Stock Patterson (2000). *The Traffic Flow Management Rerouting Problem in Air Traffic Control: A Dynamic Network Flow Approach*. Transp. Sci. [10.1287/trsc.34.3.239.12300](https://doi.org/10.1287/trsc.34.3.239.12300)  
Formulates ATFM with ground holding, airborne holding and rerouting as an integer dynamic multicommodity network flow problem with side constraints on a time-expanded airspace network (airports and sectors as nodes, time-indexed arcs, per-period airport and sector capacities). Solved by a Lagrangian relaxation scheme (Lagrangian generation) that aggregates flights into commodity flows, solves the relaxed network problem, and disaggregates back to integral flight routes and schedules via randomized rounding; near-optimal solutions reported on national-scale instances.  
*→ both problems:* The RAM flow problem is exactly a dynamic multicommodity flow on a time-expanded regional network with airport/airspace capacities, and the aggregate-then-disaggregate Lagrangian scheme suits many small-aircraft flights; the same machinery gives the operational flow sub-problem of a spaceport feeder network.  

<a id="lulli2007"></a>**[lulli2007]** Lulli, Odoni (2007). *The European Air Traffic Flow Management Problem*. Transp. Sci. [10.1287/trsc.1070.0214](https://doi.org/10.1287/trsc.1070.0214)  
Integer program on a time-expanded network with binding en-route sector capacities (European setting) that assigns ground and airborne holds; shows that minimising total delay can produce inequitable, non-FCFS allocations and introduces equity-related objective terms to study the efficiency-equity trade-off.  
*→ RAM flow problem:* RAM corridors between small airports resemble the en-route-constrained European case more than the airport-constrained US case, so the model's treatment of airborne holding and the equity side effects transfer directly.  

<a id="mukherjee2009"></a>**[mukherjee2009]** Mukherjee, Hansen (2009). *A dynamic rerouting model for air traffic flow management*. Transp. Res. B. [10.1016/j.trb.2008.05.011](https://doi.org/10.1016/j.trb.2008.05.011)  
Stochastic integer programming model for traffic inbound to one airport when both the airport and its approach routes/arrival fixes are subject to adverse weather; jointly decides ground holding and dynamic rerouting among arrival routes over a capacity scenario tree; dynamic rerouting cuts delay cost 10-15% versus static rerouting and about 50% versus pure ground holding.  
*→ RAM flow problem:* Gives the dynamic (multi-stage) version of the time-expanded flow model, directly applicable to RAM flows whose airspace or weather capacity is revealed over the day.  

<a id="bertsimas2011"></a>**[bertsimas2011]** Bertsimas, Lulli, Odoni (2011). *An Integer Optimization Approach to Large-Scale Air Traffic Flow Management*. Oper. Res. [10.1287/opre.1100.0899](https://doi.org/10.1287/opre.1100.0899)  
Integer optimization model jointly deciding ground holding, airborne holding, rerouting and speed control for every flight, using cumulative time-indexed variables on a sector graph with route choice encoded via sector-adjacency (local routing) constraints. Facet-defining inequalities are identified and the LP relaxation is shown to be integral in most cases; instances with about 6,500 flights and 145 sectors (US-NAS scale) are solved in minutes.  
*→ RAM flow problem:* Shows that a single time-indexed flow formulation can absorb routing and speed decisions for very many flights, which is the scale regime of a RAM network with many small electric aircraft.  

<a id="pyrgiotis2016"></a>**[pyrgiotis2016]** Pyrgiotis, Odoni (2016). *On the Impact of Scheduling Limits: A Case Study at Newark Liberty International Airport*. Transp. Sci. [10.1287/trsc.2014.0564](https://doi.org/10.1287/trsc.2014.0564)  
Evaluates airport scheduling limits (slot caps) by combining an IP that smooths/displaces the schedule to meet a cap with a stochastic queuing delay model, quantifying the delay response to alternative caps at Newark.  
*→ RAM flow problem:* The schedule-displacement IP is the strategic demand-management counterpart for RAM airports whose hourly caps are set by pads, chargers or noise rules.  

<a id="gerdes2018"></a>**[gerdes2018]** Gerdes, Temme, Schultz (2018). *Dynamic airspace sectorisation for flight-centric operations*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x18310520)  
Dynamic sectorisation that shifts from 'flow follows structure' to 'structure follows flow': sectors are built around actual traffic flows (flight-centric operations) to balance controller workload under operational, economic and ecological constraints.  
*→ RAM flow problem:* Flow-driven capacity partitioning is relevant to defining time-varying airspace capacity constraints for RAM networks.  

<a id="hamdan2022"></a>**[hamdan2022]** Hamdan, Cheaitou, Jouini, Andersson Granberg, Jemai, Alsyouf, Bettayeb, Josefsson (2022). *Central Authority-Controlled Air Traffic Flow Management: An Optimization Approach*. Transp. Sci. [10.1287/trsc.2021.1087](https://doi.org/10.1287/trsc.2021.1087)  
Integer programming ATFM model with path rerouting and diversion options plus pre-existing en-route flights, comparing a central-authority regime (controls all ground/air delay, reroute, cancellation decisions) with decentralised ATFM-authority/airline decisions; includes inter-flight and inter-airline fairness measures; exact solution for small/medium instances and a modified fix-and-relax heuristic for large ones. Reported delay reductions up to 8% and cancellations up to 23%; fairness costs 0.2-3.0%.  
*→ RAM flow problem:* A recent centralized flow-control model that a single RAM network operator could adopt directly for departure-time, route and hold assignment.  

<a id="jacquillat2022"></a>**[jacquillat2022]** Jacquillat (2022). *Predictive and Prescriptive Analytics Toward Passenger-Centric Ground Delay Programs*. Transp. Sci. [10.1287/trsc.2021.1081](https://doi.org/10.1287/trsc.2021.1081)  
Large-scale integer optimisation for GDPs that balances flight and passenger delays (including misconnections), combined with statistical learning models that predict passenger itineraries; shows passenger delays fall substantially for small flight-delay cost increases via delay allocation and deliberate delay introduction, and that results are robust to itinerary misprediction.  
*→ RAM flow problem:* RAM itineraries will often be multi-leg feeder trips; predicting itineraries and allocating holds to protect connections is directly transferable.  

<a id="degiovanni2024"></a>**[degiovanni2024]** De Giovanni, Lancia, Lulli (2024). *Data-Driven Optimization for Air Traffic Flow Management with Trajectory Preferences*. Transp. Sci. [10.1287/trsc.2022.0309](https://doi.org/10.1287/trsc.2022.0309)  
Trajectory-based ATFM in which airspace users' trajectory preferences are learned from historical traffic by clustering and classification, then a binary integer program assigns each flight a feasible 4D trajectory and possible ground delay subject to sector and airport capacities; Eurocontrol instances with more than 32,000 flights solve in practical times.  
*→ RAM flow problem:* Shows how to learn operator preferences from data and still solve a network-scale IP, relevant for on-demand RAM where operator utilities are heterogeneous.  

### Stochastic/robust ATFM (13 papers)

<a id="ball2003"></a>**[ball2003]** Ball, Hoffman, Odoni, Rifkin (title/authors matched to IDEAS OR 51(1):167-171 record) (2003). *A Stochastic Integer Program with Dual Network Structure and Its Application to the Ground-Holding Problem*. Oper. Res. [10.1287/opre.51.1.167.12795](https://doi.org/10.1287/opre.51.1.167.12795)  
Static stochastic ground-holding model with aggregate per-period demand and a scenario set for airport arrival capacity; proves the constraint matrix is dual network (totally unimodular) so the stochastic IP can be solved as an LP / network flow; output is a planned arrival-rate profile that plugs into CDM ground delay program procedures (slot allocation).  
*→ both problems:* A reusable structural result: RAM slot planning at a weather-limited regional airport can be formulated to inherit this integrality and solve as an LP inside a larger decomposition.  

<a id="mukherjee2007"></a>**[mukherjee2007]** Mukherjee, Hansen (2007). *A Dynamic Stochastic Model for the Single Airport Ground Holding Problem*. Transp. Sci. [10.1287/trsc.1070.0210](https://doi.org/10.1287/trsc.1070.0210)  
Multistage dynamic stochastic integer program for the single-airport GHP in which airport capacity evolves along a scenario tree and ground delays assigned to individual flights can be revised at each decision stage as weather forecasts update; LP relaxation observed to yield integer solutions; includes intra-airline substitution/cancellation to fit CDM; gains largest under stringent ground-holding policy, early GDP cancellation and low bad/good-weather capacity ratios; optimal policy releases long-haul flights on time and uses short-haul flights to absorb delay.  
*→ RAM flow problem:* RAM flights are short-haul and highly revisable, exactly the flights this model uses as the flexible recourse; the scenario-tree multistage structure transfers to RAM departure-time revision under evolving airport/vertiport capacity.  

<a id="liu2008"></a>**[liu2008]** Liu, Hansen, Mukherjee (2008). *Scenario-based air traffic flow management: From theory to practice*. Transp. Res. B. [10.1016/j.trb.2008.01.002](https://doi.org/10.1016/j.trb.2008.01.002)  
Methodology for building the capacity scenarios and scenario trees that static and dynamic stochastic ground-holding models require: clusters empirical airport capacity profiles into a small number of nominal scenarios and identifies branch points where profiles diverge; finds most US airports have few nominal profiles that combine naturally into trees; demonstrates use in stochastic GHP models.  
*→ both problems:* Provides the recipe for turning historical capacity data into tractable scenario trees, needed for RAM airports with sparse history and for spaceport launch-window availability profiles alike.  

<a id="czerny2010"></a>**[czerny2010]** Czerny (2010). *Airport congestion management under uncertainty*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v44y2010i3p371-380.html)  
Analytical comparison of congestion pricing and slot (quantity) instruments for airport congestion management under uncertainty.  
*→ both problems:* Price-versus-quantity analysis under demand/capacity uncertainty informs how to ration RAM airport capacity or launch windows when demand is uncertain.  

<a id="clarke2013"></a>**[clarke2013]** Clarke, Solak, Ren, Vela (2013). *Determining Stochastic Airspace Capacity for Air Traffic Flow Management*. Transp. Sci. [10.1287/trsc.1120.0440](https://doi.org/10.1287/trsc.1120.0440)  
Fast simulation-based method for the stochastic capacity of an airspace region: ensemble weather forecasts are combined with an air-traffic-control routing algorithm in an integrated weather-traffic model to produce time-varying probabilistic capacity maps for use as inputs to stochastic ATFM models, addressing capacity left unused by deterministic decisions.  
*→ both problems:* Provides the airspace-side counterpart to airport capacity scenarios, needed for RAM low-altitude corridors and for the airspace closures a spaceport launch imposes on surrounding traffic.  

<a id="liu2016"></a>**[liu2016]** Liu, Hansen (2016). *Incorporating Predictability Into Cost Optimization for Ground Delay Programs*. Transp. Sci. [10.1287/trsc.2015.0594](https://doi.org/10.1287/trsc.2015.0594)  
Introduces predictability (dispersion of realized delay) into GDP cost optimization under capacity uncertainty and develops two stochastic GDP models, a static no-revision model and a dynamic model allowing one GDP revision, to trade expected delay cost against unpredictability.  
*→ RAM flow problem:* RAM passengers and charging logistics value predictable departure times; this gives a way to price unpredictability inside a stochastic hold model.  

<a id="chen2017"></a>**[chen2017]** Chen, Chen, Sun (2017). *Air traffic flow management under uncertainty using chance-constrained optimization*. Transp. Res. B. [10.1016/j.trb.2017.05.014](https://doi.org/10.1016/j.trb.2017.05.014)  
Chance-constrained formulation of the ATFM problem (ground/airborne holding on a time-expanded flight network) in which sector/airport capacity constraints must hold with prescribed probability under weather-driven capacity uncertainty; reformulated to a tractable deterministic (mixed-integer) equivalent and tested on US airspace instances. TR-B 102:124-141.  
*→ both problems:* Chance-constrained capacity handling transfers to RAM airport/charging slots and to launch-window capacity under weather uncertainty in spaceport feeder networks.  

<a id="jacquillat2017"></a>**[jacquillat2017]** Jacquillat, Odoni, Webster (2017). *Dynamic Control of Runway Configurations and of Arrival and Departure Service Rates at JFK Airport Under Stochastic Queue Conditions*. Transp. Sci. [10.1287/trsc.2015.0644](https://doi.org/10.1287/trsc.2015.0644)  
Dynamic programming model that jointly and dynamically selects runway configuration and the arrival/departure service-rate split to minimize congestion cost under stochastic queue dynamics and stochastic weather/wind; state includes schedules, queue lengths and weather; exact DP solves in reasonable time at JFK and a one-step look-ahead approximation gives near-optimal policies much faster.  
*→ RAM flow problem:* Endogenous capacity control via DP is relevant to RAM airports/vertiports where the manager can reconfigure pads, runways or charging stalls in response to queues and weather.  

<a id="solak2018"></a>**[solak2018]** Solak et al. (co-authors not captured) (2018). *Stochastic Runway Scheduling*. Transp. Sci. [10.1287/trsc.2017.0784](https://doi.org/10.1287/trsc.2017.0784)  
Stochastic runway sequencing and scheduling with uncertain aircraft ready times formulated as a two-stage stochastic integer program and solved with sample-based decomposition/branching techniques, extending the authors' stochastic branch-and-bound work to a rigorous stochastic programming treatment.  
*→ both problems:* Stochastic sequence-then-time structure transfers to RAM departure/arrival slotting with uncertain turnaround and charging completion times, and to launch-slot scheduling under weather/readiness uncertainty.  

<a id="wang2020"></a>**[wang2020]** Wang, Jacquillat (2020). *A Stochastic Integer Programming Approach to Air Traffic Scheduling and Operations*. Oper. Res. [10.1287/opre.2020.1985](https://doi.org/10.1287/opre.2020.1985)  
Integrated model of strategic scheduling interventions and tactical ground-holding across an airport network under operating uncertainty, formulated as a two-stage stochastic program with integer recourse; an original decomposition algorithm with provable solution-quality guarantees uses new dual integer cuts derived from reduced costs of the second-stage LP dual.  
*→ both problems:* Joint strategic scheduling + tactical holding under uncertainty is the template for RAM timetable design and for feeder launch schedule design with recourse.  

<a id="starita2020"></a>**[starita2020]** Starita, Strauss, Fei, Jovanović, Ivanov, Pavlović, Fichert (2020). *Air Traffic Control Capacity Planning Under Demand and Capacity Provision Uncertainty*. Transp. Sci. [10.1287/trsc.2019.0962](https://doi.org/10.1287/trsc.2019.0962)  
Stochastic optimization of future ATC capacity provision (controller sector-hours and sector opening schemes) against uncertain traffic and uncertain delivered capacity; a scalable decomposition approach exploits problem structure to handle a large number of traffic scenarios; several decision policies are tested on real European data.  
*→ both problems:* Capacity-provision planning under demand uncertainty is the strategic question for sizing RAM airspace services and for spaceport/range capacity ahead of uncertain launch demand.  

<a id="khassiba2020"></a>**[khassiba2020]** Khassiba, Bastin, Cafieri, Gendron, Mongeau (2020). *Two-Stage Stochastic Mixed-Integer Programming with Chance Constraints for Extended Aircraft Arrival Management*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v54y2020i4p897-919.html)  
Extended arrival management as a two-stage stochastic MIP with chance constraints: first stage fixes the sequence and target times over the initial approach fix to minimize landing-sequence length; actual times deviate randomly, and the second stage sets landing times minimizing time-deviation costs while separation constraints hold with high probability; solved via scenario-based approximation.  
*→ RAM flow problem:* Combines sequencing, target-time setting and probabilistic separation, the structure needed for metering RAM arrivals into a regional airport with uncertain flight times.  

<a id="starita2023"></a>**[starita2023]** Starita, Strauss, Fei, Jovanović, Ivanov, Pavlović, Fichert (2023). *Cross-Border Capacity Planning in Air Traffic Management Under Uncertainty*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v57y2023i4p999-1018.html)  
Extends the 2020 stochastic ATC capacity-planning model to coordinated cross-border capacity provision among several air navigation service providers under traffic and capacity uncertainty, using scenario-based stochastic optimization with decomposition to compare coordinated and uncoordinated policies.  
*→ both problems:* Multi-jurisdiction capacity coordination under uncertainty parallels RAM networks spanning several regional airport owners and spaceport-range coordination with adjacent airspace.  

### Equity/CDM/slot allocation (28 papers)

<a id="sherali2002"></a>**[sherali2002]** Sherali, Smith, Trani (2002). *An Airspace Planning Model for Selecting Flight-plans Under Workload, Safety, and Equity Considerations*. Transp. Sci. [10.1287/trsc.36.4.378.546](https://doi.org/10.1287/trsc.36.4.378.546)  
0-1 integer program selecting one flight plan per flight from alternatives to minimise fuel/delay cost subject to sector workload, conflict/safety and inter-airline equity constraints (bounds on each airline's relative cost deviation); motivated by special-use-airspace closures for space launches; solved by branch-and-bound with valid inequalities.  
*→ both problems:* The one-plan-per-flight assignment IP with strengthening transfers to RAM corridor/time selection, and the model explicitly handles airspace closures around spaceport launches, linking topics A and B.  

<a id="sherali2003"></a>**[sherali2003]** Sherali, Staats, Trani (2003). *An Airspace Planning and Collaborative Decision-Making Model: Part I—Probabilistic Conflicts, Workload, and Equity Considerations*. Transp. Sci. [10.1287/trsc.37.4.434.23272](https://doi.org/10.1287/trsc.37.4.434.23272)  
Extends the airspace planning model into a collaborative decision-making framework: a mixed-integer program selects flight plans from airline-submitted alternatives subject to probabilistic conflict (safety) constraints, sector workload limits and inter-airline equity measures.  
*→ both problems:* Supplies the probabilistic-conflict and equity constraint structure for a collaborative RAM flow model where several small operators submit preferred trajectories.  

<a id="sherali2006"></a>**[sherali2006]** Sherali, Staats, Trani (2006). *An Airspace-Planning and Collaborative Decision-Making Model: Part II—Cost Model, Data Considerations, and Computations*. Transp. Sci. [10.1287/trsc.1050.0141](https://doi.org/10.1287/trsc.1050.0141)  
Develops the fuel/delay cost model and data treatment for the APCDM 0-1 integer program and reports computational results on realistic instances with equity (cost-sharing) considerations.  
*→ both problems:* Shows how to make the flight-plan selection IP solve at realistic scale, the computational side a RAM implementation would need.  

<a id="kotnyek2006"></a>**[kotnyek2006]** Kotnyek, Richetta (2006). *Equitable Models for the Stochastic Ground-Holding Problem Under Collaborative Decision Making*. Transp. Sci. [10.1287/trsc.1050.0129](https://doi.org/10.1287/trsc.1050.0129)  
Static stochastic integer programs for the single-airport ground-holding problem under capacity scenarios, modified so that slot assignments respect CDM equity (airline-ordered flight sets / RBS-consistent allocations); analyses the polyhedral structure and the cost of imposing equity.  
*→ RAM flow problem:* RAM will involve several operators sharing scarce regional-airport and charging capacity; equity-constrained stochastic rationing is the template for a fair RAM demand-capacity balancing service.  

<a id="vossen2006"></a>**[vossen2006]** Vossen, Ball (2006). *Slot Trading Opportunities in Collaborative Ground Delay Programs*. Transp. Sci. [10.1287/trsc.1050.0121](https://doi.org/10.1287/trsc.1050.0121)  
Models CDM slot exchange after a ration-by-schedule (RBS) initial allocation of arrival slots at one airport: inter-airline slot trades (a generalisation of the compression algorithm) are formulated as assignment / network-flow integer programs over a flight-to-slot bipartite structure with airline-declared substitutions, including a mediated-bartering variant; shows delay-cost gains over compression.  
*→ RAM flow problem:* Gives the single-resource slot-assignment and mediated-exchange machinery a RAM scheduler needs to let scheduled and on-demand operators swap departure, arrival or charger slots at a capacity-constrained regional airport after a proportional initial allocation.  

<a id="bard2008"></a>**[bard2008]** Bard, Mohan (2008). *Reallocating arrival slots during a ground delay program*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v42y2008i2p113-134.html)  
Airline-side arrival-slot reallocation problem in response to a GDP, minimising flight delay and passenger missed-connection costs; formulated as a dynamic program solved by branch and bound within a rolling-horizon framework; practical instances solved within five minutes.  
*→ RAM flow problem:* Operator-side substitution/reallocation model that complements the mediator-side CDM models for RAM operators holding multiple slots.  

<a id="manley2010"></a>**[manley2010]** Manley, Sherry (2010). *Analysis of performance and equity in ground delay programs*. Transp. Res. C. [10.1016/j.trc.2010.03.009](https://doi.org/10.1016/j.trc.2010.03.009)  
Analysis of GDP performance and equity metrics (flight- and passenger-based) across GDP rationing/exemption configurations.  
*→ RAM flow problem:* Supplies equity metrics for evaluating RAM flow-management outcomes across operators and passengers.  

<a id="verhoef2010"></a>**[verhoef2010]** Verhoef (2010). *Congestion pricing, slot sales and slot trading in aviation*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v44y2010i3p381-391.html)  
Analytical duopoly model of airlines at a congested airport addressing uninternalized congestion and market power. Derives first-best (airline-differentiated) charges, shows undifferentiated charges are a weighted average and less efficient, and shows tradable slots reach first-best only when congestion dominates the market-power distortion.  
*→ both problems:* Economic foundations for slot/charging mechanisms that allocate scarce airport capacity among regional operators.  

<a id="ball2010"></a>**[ball2010]** Ball, Hoffman, Mukherjee (2010). *Ground Delay Program Planning Under Uncertainty Based on the Ration-by-Distance Principle*. Transp. Sci. [10.1287/trsc.1090.0289](https://doi.org/10.1287/trsc.1090.0289)  
GDP planning under airport-capacity uncertainty using ration-by-distance (RBD): ground delay is assigned preferentially to short-haul flights that can still exploit late capacity information, with explicit equity guarantees expressed as bounded deviation from the RBS allocation; stochastic analysis shows RBD approaches the minimum expected delay while keeping airline equity.  
*→ RAM flow problem:* Shows how distance (flight time) to the constrained resource should drive who is held under cancellation uncertainty; RAM has very heterogeneous short stage lengths, making the RBD logic directly applicable.  

<a id="basso2010"></a>**[basso2010]** Basso, Zhang (2010). *Pricing vs. slot policies when airport profits matter*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v44y2010i3p381-391.html)  
*→ both problems:* Benchmark for price versus quantity instruments when scarce take-off/landing or launch-window capacity is allocated by a profit-seeking infrastructure owner.  

<a id="sherali2011"></a>**[sherali2011]** Sherali et al. (co-authors not captured) (2011). *Integrating Slot Exchange, Safety, Capacity, and Equity Mechanisms Within an Airspace Flow Program*. Transp. Sci. [10.1287/trsc.1100.0356](https://doi.org/10.1287/trsc.1100.0356)  
*→ RAM flow problem:* Combines rerouting under airspace constraints with slot trading and equity, the situation RAM faces during weather or launch-related airspace closures.  

<a id="bertsimas2011a"></a>**[bertsimas2011a]** Bertsimas, Farias, Trichakis (2011). *The Price of Fairness*. Oper. Res. [10.1287/opre.1100.0865](https://doi.org/10.1287/opre.1100.0865)  
Introduces the price of fairness, the relative efficiency loss of a fair allocation, and derives bounds for proportional fairness and max-min fairness in resource allocation problems.  
*→ both problems:* Gives the theoretical bound on efficiency lost when slots or launch capacity are allocated fairly among operators.  

<a id="barnhart2012"></a>**[barnhart2012]** Barnhart, Bertsimas, Caramanis, Fearing (2012). *Equitable and Efficient Coordination in Traffic Flow Management*. Transp. Sci. [10.1287/trsc.1110.0393](https://doi.org/10.1287/trsc.1110.0393)  
Augments the Bertsimas-Stock Patterson 0-1 IP on a time-expanded network with sector and airport capacities with a network fairness metric that generalises RBS (time-order deviation, reversals and overtaking), penalised in the objective; national-scale instances show large equity gains for small efficiency loss.  
*→ RAM flow problem:* The reversal/overtaking fairness constraints can be added verbatim to a time-expanded RAM flow IP in which several operators compete for corridor and airport capacity.  

<a id="kuhn2013"></a>**[kuhn2013]** Kuhn (2013). *Ground delay program planning: Delay, equity, and computational complexity*. Transp. Res. C. [10.1016/j.trc.2013.07.008](https://doi.org/10.1016/j.trc.2013.07.008)  
Analyses GDP planning as a slot-assignment problem with delay and equity (RBS-based) objectives, gives computational-complexity results and integer-programming / heuristic approaches.  
*→ RAM flow problem:* Clarifies which equity-constrained slot-assignment variants are tractable before embedding them in a RAM flow model.  

<a id="glover2013"></a>**[glover2013]** Glover, Ball (2013). *Stochastic optimization models for ground delay program planning with equity-efficiency tradeoffs*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/abs/pii/S0968090X11001653)  
Two-stage stochastic integer programs for GDP planning (program scope and rates) over capacity scenarios, with a multiobjective treatment of total expected delay versus an equity measure based on deviation from RBS.  
*→ RAM flow problem:* The two-stage stochastic multi-objective structure is a direct template for RAM demand-capacity balancing where operators with different stage lengths must be treated fairly.  

<a id="corolli2014"></a>**[corolli2014]** Corolli, Lulli, Ntaimo (2014). *The time slot allocation problem under uncertain capacity*. Transp. Res. C. [10.1016/j.trc.2014.05.004](https://doi.org/10.1016/j.trc.2014.05.004)  
Two two-stage stochastic programming models for strategic allocation of airport time slots across a network of airports with uncertain capacity; first stage allocates slots respecting airline requests and operational constraints, second stage captures operational delays under capacity scenarios; exposes the tradeoff between schedule displacement from requests and expected operational delay.  
*→ both problems:* Directly transferable to seasonal slot coordination at capacity-constrained regional airports under weather uncertainty, and analogous to allocating launch windows at a spaceport whose usable capacity is uncertain.  

<a id="bertsimas2016"></a>**[bertsimas2016]** Bertsimas, Gupta (2016). *Fairness and Collaboration in Network Air Traffic Flow Management: An Optimization Approach*. Transp. Sci. [10.1287/trsc.2014.0567](https://doi.org/10.1287/trsc.2014.0567)  
Two-stage approach: a network ATFM integer program on a time-expanded network with fairness controls (reversals/overtaking), followed by an airline-collaboration stage in which each airline re-optimises flight-to-slot substitutions within its own allocation via network-flow / IP models; large US instances show a tractable efficiency-fairness-collaboration trade-off.  
*→ RAM flow problem:* Demonstrates that the cumulative-variable network model keeps scaling when fairness side constraints are added, which a multi-operator RAM network would need.  

<a id="ribeiro2018"></a>**[ribeiro2018]** Ribeiro, Jacquillat, Antunes, Odoni, Pita (2018). *An optimization approach for airport slot allocation under IATA guidelines*. Transp. Res. B. [10.1016/j.trb.2018.04.005](https://doi.org/10.1016/j.trb.2018.04.005)  
Priority-based Slot Allocation Model: a lexicographic multi-objective integer program implementing IATA priority classes (historic, change-to-historic, new entrants), schedule-displacement objectives and series-of-slots regularity constraints under rolling-window capacity limits, solved sequentially and applied to Portuguese airports.  
*→ both problems:* The lexicographic priority structure is the natural way to encode operator classes (scheduled vs on-demand, incumbent vs new entrant) in RAM slot coordination and in launch-window allocation.  

<a id="dalsasso2018"></a>**[dalsasso2018]** Dal Sasso, Djeumou Fomeni, Lulli, Zografos (2018). *Incorporating Stakeholders' priorities and preferences in 4D trajectory optimization*. Transp. Res. B. [10.1016/j.trb.2018.09.009](https://doi.org/10.1016/j.trb.2018.09.009)  
Integer programming model that selects one 4D trajectory per flight from airspace-user-submitted alternatives (route/level/time options) subject to sector and airport capacity on a time-discretised network, while incorporating stakeholders' priorities and preferences through a multi-criteria objective; TR-B 117(Part A):594-609.  
*→ RAM flow problem:* Trajectory-option selection with operator priorities is the trajectory-based-operations form of the RAM flow problem (choice among a few corridor/altitude/time options per flight).  

<a id="jacquillat2018"></a>**[jacquillat2018]** Jacquillat, Vaze (2018). *Interairline Equity in Airport Scheduling Interventions*. Transp. Sci. [10.1287/trsc.2017.0817](https://doi.org/10.1287/trsc.2017.0817)  
Integrated Capacity Utilization and Scheduling Model with Equity Considerations: schedule-displacement optimisation coupled with a stochastic queuing model of capacity utilisation, with explicit inter-airline equity objectives; on JFK scenarios the model prioritises airlines equally with little or no efficiency loss.  
*→ RAM flow problem:* Shows how to add operator-equity objectives to strategic schedule-coordination models that would cap demand at congested RAM airports or vertiports.  

<a id="ribeiro2019"></a>**[ribeiro2019]** Ribeiro, Jacquillat, Antunes (2019). *A Large-Scale Neighborhood Search Approach to Airport Slot Allocation*. Transp. Sci. [10.1287/trsc.2019.0922](https://doi.org/10.1287/trsc.2019.0922)  
Large-scale neighbourhood search for slot allocation at large coordinated airports: a constructive heuristic builds a feasible schedule and an improvement heuristic iteratively re-optimises subsets of slot requests with the IP model; at Lisbon it finds optimal or near-optimal solutions in hours where commercial solvers do not terminate after days.  
*→ RAM flow problem:* Decomposition-by-request-subset heuristics apply to any large slot-assignment IP, including seasonal RAM schedule coordination.  

<a id="fairbrother2020"></a>**[fairbrother2020]** Fairbrother et al. (co-authors not captured) (2020). *A Slot-Scheduling Mechanism at Congested Airports that Incorporates Efficiency, Fairness, and Airline Preferences*. Transp. Sci. [10.1287/trsc.2019.0926](https://doi.org/10.1287/trsc.2019.0926)  
Two-stage slot-scheduling mechanism: stage 1 constructs a reference schedule that is fair to airlines (efficiency and fairness objectives); stage 2 lets each airline specify how its total displacement should be distributed among its requests, and the mechanism adjusts the schedule to satisfy as many preferences as possible; IP models throughout.  
*→ RAM flow problem:* A preference-elicitation layer on top of a fair reference allocation is directly reusable for allocating slots among competing RAM operators.  

<a id="xu2020"></a>**[xu2020]** Xu, Dalmau, Melgosa, Montlaur, Prats (2020). *A framework for collaborative air traffic flow management minimizing costs for airspace users: Enabling trajectory options and flexible pre-tactical delay management*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v134y2020icp229-255.html)  
Collaborative ATFM framework in which airspace users submit trajectory options (alternative routes/levels, linear holding, in-flight delay recovery) and a network-level optimisation assigns options and pre-tactical delays to resolve demand-capacity hotspots at minimum user cost; integer programming on sector-capacity hotspots; TR-B 134:229-255.  
*→ RAM flow problem:* Cost-based option selection with flexible delay absorption (ground vs. airborne vs. speed) is directly applicable to RAM flow management where electric aircraft have asymmetric costs of ground vs. in-flight delay.  

<a id="estes2020"></a>**[estes2020]** Estes, Ball (2020). *Equity and Strength in Stochastic Integer Programming Models for the Dynamic Single Airport Ground-Holding Problem*. Transp. Sci. [10.1287/trsc.2020.0975](https://doi.org/10.1287/trsc.2020.0975)  
Dynamic (multistage) stochastic integer programming formulations of the single-airport ground-holding problem; studies the equity properties of their solutions relative to RBS-type allocations and the strength (LP relaxation / integrality) of alternative formulations.  
*→ RAM flow problem:* Recent evidence on which equity-constrained slot formulations stay tight, relevant when fairness across RAM operators is embedded in a decomposed network model.  

<a id="xu2020a"></a>**[xu2020a]** Xu, Prats, Delahaye (2020). *Synchronised demand-capacity balancing in collaborative air traffic flow management*. Transp. Res. C. [10.1016/j.trc.2020.02.007](https://doi.org/10.1016/j.trc.2020.02.007)  
Mixed-integer model that jointly assigns each flight a delay and a choice among alternative trajectories and, for each airspace block and time period, a sector opening scheme (or dynamic sectorisation); per-period sector capacities couple the two. Solved as an integrated MIP with pre-generated trajectory and sectorisation options; shows large delay reductions versus sequential practice.  
*→ RAM flow problem:* Makes the capacity profile itself a decision (time-varying airspace configuration), the airspace analogue of time-varying link capacity in DTA; for RAM, low-altitude corridor structure can likewise be reconfigured over the day alongside flow regulation.  

<a id="keskin2023"></a>**[keskin2023]** Keskin, Zografos (2023). *Optimal network-wide adjustments of initial airport slot allocations with connectivity and fairness objectives*. Transp. Res. B. [10.1016/j.trb.2023.102801](https://doi.org/10.1016/j.trb.2023.102801)  
Network-level model that adjusts single-airport initial slot allocations so that aircraft rotations remain connectable across airports, optimising connectivity together with fairness among airlines in a multi-objective integer program.  
*→ RAM flow problem:* Network-wide slot coordination with fairness is directly the strategic layer of a multi-airport RAM schedule where aircraft rotations couple slots at different airports.  

<a id="birolini2023"></a>**[birolini2023]** Birolini, Jacquillat, Schmedeman, Ribeiro (2023). *Passenger-Centric Slot Allocation at Schedule-Coordinated Airports*. Transp. Sci. [10.1287/trsc.2022.1165](https://doi.org/10.1287/trsc.2022.1165)  
*→ RAM flow problem:* Passenger-weighted slot allocation is relevant when RAM demand is on-demand and passenger itineraries drive priorities.  

<a id="gasparin2025"></a>**[gasparin2025]** Gasparin et al. (co-authors not captured) (2025). *A User-Driven Prioritisation Process implementation and optimisation for ATFM hotspot resolution*. Transp. Res. C. [10.1016/j.trc.2024.104894](https://doi.org/10.1016/j.trc.2024.104894)  
Studies UDPP solutions letting airlines prioritise their own flights within ATFM regulations; shows that with an accurate delay cost model the prioritisation can be fully automated via an integer programming model, and uses it for cost-benefit estimates of UDPP against the current ATFM regulation process.  
*→ RAM flow problem:* Operator-side re-prioritisation within assigned slots is reusable for RAM operators managing their own fleet rotations under flow constraints.  

### Decomposition & large-scale methods (6 papers)

<a id="andreatta1998"></a>**[andreatta1998]** Andreatta, Brunetta (1998). *Multiairport Ground Holding Problem: A Computational Evaluation of Exact Algorithms*. Oper. Res. [10.1287/opre.46.1.57](https://doi.org/10.1287/opre.46.1.57)  
Computational comparison of exact algorithms for the multiairport ground holding problem (own algorithms vs Vranas-Bertsimas-Odoni and Bertsimas-Stock formulations) when arrival capacity is limited at congested airports.  
*→ RAM flow problem:* Benchmarks formulation strength and exact-method scalability for networked holding problems.  

<a id="lubbecke2005"></a>**[lubbecke2005]** Lübbecke, Desrosiers (2005). *Selected Topics in Column Generation*. Oper. Res. [10.1287/opre.1050.0234](https://doi.org/10.1287/opre.1050.0234)  
Survey of column generation / Dantzig-Wolfe decomposition theory and practice: pricing, dual stabilization, branch-and-price, acceleration strategies; standard methodological reference.  
*→ both problems:* Methodological backbone for path/trajectory-based ATFM and for service-network-design formulations of feeder networks.  

<a id="sun2011"></a>**[sun2011]** Sun et al. (co-authors not captured) (2011). *A dual decomposition method for sector capacity constrained traffic flow optimization*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v45y2011i6p880-902.html)  
Aggregate (Eulerian) multicommodity network model of NAS traffic; minimizing total travel time under sector capacity constraints is posed as a large IP/LP. Dual decomposition on the capacity constraints splits the problem into independent per-commodity subproblems solvable in parallel, making NAS-scale LPs tractable.  
*→ both problems:* Aggregate-flow dual decomposition is a scalable alternative to flight-level IPs for RAM corridor flows and for capacity-coupled time-expanded feeder networks.  

<a id="rahmaniani2020"></a>**[rahmaniani2020]** Rahmaniani, Ahmed, Crainic, Gendreau, Rei (2020). *The Benders Dual Decomposition Method*. Oper. Res. [10.1287/opre.2019.1892](https://doi.org/10.1287/opre.2019.1892)  
Combines Benders decomposition with Lagrangian dual decomposition for two-stage stochastic integer programs with integer recourse, producing stronger optimality cuts than classical Benders; tested on stochastic network design and facility location instances.  
*→ both problems:* Integer recourse (discrete launch assignments per scenario) is where classical Benders for hub design weakens; this method is the remedy for stochastic spaceport-to-hub models.  

<a id="crainic2021"></a>**[crainic2021]** Crainic, Hewitt, Maggioni, Rei (2021). *Partial Benders Decomposition: General Methodology and Application to Stochastic Network Design*. Transp. Sci. [10.1287/trsc.2020.1022](https://doi.org/10.1287/trsc.2020.1022)  
Strengthens Benders decomposition for two-stage stochastic programs by retaining explicit scenario-subproblem information (retained or artificial scenarios) in the master problem; applied to two-stage stochastic multicommodity network design with stochastic demands and arc capacities, improving efficiency, solution quality and stability. Published online December 2020, print volume 55(2) 2021.  
*→ both problems:* Exact decomposition for scenario-based launch network design with both uncertain demand and uncertain launch-window capacity; the same machinery scales stochastic flow-management models.  

<a id="starita2022"></a>**[starita2022]** Starita, Strauss, Fei, Jovanović, Ivanov, Pavlović, Fichert (2022). *The value of flexible flight-to-route assignments in pre-tactical air traffic management*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v160y2022icp76-96.html)  
*→ RAM flow problem:* Deferring route commitment is a natural strategy for RAM operations with uncertain weather and charging availability.  

### Trajectory-based ops & airspace (16 papers)

<a id="siddiqee1973"></a>**[siddiqee1973]** Siddiqee (1973). *A Mathematical Model for Predicting the Number of Potential Conflict Situations at Intersecting Air Routes*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v7y1973i2p158-167.html)  
Probabilistic model of the expected number of potential conflicts at the intersection of air routes as a function of flows, speeds and crossing angle. TS 7(2):158-167.  
*→ RAM flow problem:* Earliest analytical conflict-rate model; basis for complexity/capacity estimates of route crossings in regional route networks.  

<a id="siddiqee1974"></a>**[siddiqee1974]** Siddiqee (1974). *A Mathematical Model for Predicting the Duration of Potential Conflict Situations at Intersecting Air Routes*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v8y1974i1p58-64.html)  
Companion probabilistic model giving the expected duration of potential conflicts at intersecting air routes. TS 8(1):58-64.  
*→ RAM flow problem:* Conflict-duration estimates feed controller-workload and capacity models for crossing regional routes.  

<a id="janic1991"></a>**[janic1991]** Janić, Tošić (1991). *En Route Sector Capacity Model*. Transp. Sci. [10.1287/trsc.25.4.299](https://doi.org/10.1287/trsc.25.4.299)  
Analytical model of en-route sector capacity from the geometry of routes and the concept of expected capacity under saturation (controller continuously busy), relating traffic mix, route configuration and separation to sector throughput. TS 25(4):299-307.  
*→ RAM flow problem:* Classic analytical basis for the sector-capacity parameters used as constraints in flow models; adaptable to regional sectors.  

<a id="trc-simulation2011"></a>**[trc-simulation2011]** (authors not captured) (2011). *A simulation based study of subliminal control for air traffic management*. Transp. Res. C. [10.1016/j.trc.2010.03.002](https://doi.org/10.1016/j.trc.2010.03.002)  
Simulation study of subliminal (small speed-change) control in en-route ATM, precursor to the Rey et al. optimization models. year inferred from DOI (2010 online).  
*→ RAM flow problem:* Evidence base for how much delay/conflict reduction small speed adjustments can deliver before resorting to holds.  

<a id="tang2012"></a>**[tang2012]** Tang et al. (co-authors not captured) (2012). *A multi-objective approach for Dynamic Airspace Sectorization using agent based and geometric models*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x11001185)  
Multi-objective genetic algorithm sectorises airspace balancing controller workload, maximizing average sector flight time and maximizing distance between sector boundaries and flow crossing points, using an agent-based traffic model and geometric (region-growing) sector construction.  
*→ RAM flow problem:* Multi-objective sector design offers a way to define capacity regions for RAM-scale airspace with heterogeneous traffic.  

<a id="pfeil2012"></a>**[pfeil2012]** Pfeil, Balakrishnan (2012). *Identification of Robust Terminal-Area Routes in Convective Weather*. Transp. Sci. [10.1287/trsc.1110.0372](https://doi.org/10.1287/trsc.1110.0372)  
Translates convective-weather forecasts into probabilistic route-blockage forecasts via machine learning (classifying whether a route will be open), then optimizes terminal-area operations by dynamically relocating arrival/departure routes to maximize expected capacity. TS 46(1):56-73.  
*→ RAM flow problem:* Data-driven route-availability forecasting feeds stochastic capacity parameters for RAM terminal-area and low-altitude routes.  

<a id="kim2015"></a>**[kim2015]** Kim, Hansen (2015). *Some insights into a sequential resource allocation mechanism for en route air traffic management*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v79y2015icp1-15.html)  
Game-theoretic model of sequential capacity allocation in a congestible system: analyses the First-Submitted-First-Assigned (FSFA) process of an en-route flow program such as CTOP, deriving airline submission incentives and allocation outcomes. TR-B 79:1-15.  
*→ RAM flow problem:* Incentive analysis for sequential slot/route allocation applies to many small RAM operators competing for constrained airspace or vertiport capacity.  

<a id="alonsoayuso2016"></a>**[alonsoayuso2016]** Alonso-Ayuso, Escudero, Martín-Campo (2016). *Exact and Approximate Solving of the Aircraft Collision Resolution Problem via Turn Changes*. Transp. Sci. [10.1287/trsc.2014.0557](https://doi.org/10.1287/trsc.2014.0557)  
Mixed 0-1 nonlinear model for conflict detection and resolution using heading (turn) changes under the geometric separation condition; solved exactly with a global MINLP solver and approximately with a sequential/heuristic scheme. TS 50(1):263-274.  
*→ RAM flow problem:* Heading-change deconfliction model transferable to en-route separation assurance in free-route regional airspace with many small aircraft.  

<a id="rey2016"></a>**[rey2016]** Rey, Rapine, Fondacci, El Faouzi (2016). *Subliminal Speed Control in Air Traffic Management: Optimization and Simulation*. Transp. Sci. [10.1287/trsc.2015.0602](https://doi.org/10.1287/trsc.2015.0602)  
Deterministic conflict-resolution models restricted to minor (subliminal) speed adjustments, formulated as nonlinear optimization problems minimizing controller-workload indicators over a potential-conflict set; validated by simulation under perturbations, showing a large share of potential conflicts can be removed with a narrow speed-modulation range and little delay. TS 50(1):240-262.  
*→ RAM flow problem:* Speed-modulation-only deconfliction is the natural tactical complement to departure-time/ground-hold assignment in a RAM flow model.  

<a id="trc-flight2017"></a>**[trc-flight2017]** (authors not captured) (2017). *Flight and passenger delay assignment optimization strategies*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x17301420)  
Optimization strategies for assigning ATFM delay to flights considering flight-centric versus passenger-centric objectives. From title/URL only.  
*→ RAM flow problem:* Passenger-centric delay allocation objectives matter for RAM where small aircraft make per-passenger impacts visible.  

<a id="xu2017"></a>**[xu2017]** Xu, Dalmau, Prats (2017). *Maximizing airborne delay at no extra fuel cost by means of linear holding*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x17301419)  
Linear-holding (speed reduction at no extra fuel) strategy extended from cruise to climb and descent using aircraft-performance data; evaluates keeping vs. changing the requested cruise flight level to maximize holding time, with airborne delay roughly 2-3x earlier estimates for short/mid-haul flights. TR-C 81:137-152.  
*→ RAM flow problem:* Quantifies the airborne-delay capacity usable as a decision variable in RAM demand-capacity balancing for short-haul flights.  

<a id="lehouillier2017"></a>**[lehouillier2017]** Lehouillier, Nasri, Omer, Soumis, Desaulniers (2017). *Solving the Air Conflict Resolution Problem Under Uncertainty Using an Iterative Biobjective Mixed Integer Programming Approach*. Transp. Sci. [10.1287/trsc.2016.0714](https://doi.org/10.1287/trsc.2016.0714)  
Tactical conflict resolution under wind, speed-prediction and maneuver-execution uncertainty. A geometric derivation gives the minimum inter-aircraft distance and conflict probability, which are embedded in a deterministic maximum-clique-of-minimum-weight model on a graph whose vertices are candidate maneuvers; an iterative biobjective MIP trades maneuver cost against conflict probability. TS 51(4):1242-1258.  
*→ RAM flow problem:* Maneuver-graph MIP with probabilistic separation is directly reusable for strategic/tactical deconfliction of dense small-aircraft RAM traffic where trajectory prediction is noisy.  

<a id="trc-three2018"></a>**[trc-three2018]** (authors not captured) (2018). *Three-dimensional conflict count models for unstructured and layered airspace designs*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x1830771x)  
Analytical models of instantaneous conflict counts as a function of traffic demand and airspace design parameters (separation requirements, heading range per flight level) for unstructured and layered en-route airspace, including climbing/descending traffic; validated by fast-time simulation, which showed climbing/descending traffic causes most conflicts in narrow-heading-range layered designs.  
*→ RAM flow problem:* Gives an analytic airspace-capacity function (conflicts vs. density and structure) that can serve as the sector/airspace capacity constraint in a UAM or RAM demand-capacity balancing model.  

<a id="trc-simulated2019"></a>**[trc-simulated2019]** (authors not captured) (2019). *A Simulated Annealing Approach to 3D Strategic Aircraft Deconfliction based on En-Route Speed Changes under Wind and Temperature Uncertainties*. Transp. Res. C. [10.1016/j.trc.2019.03.024](https://doi.org/10.1016/j.trc.2019.03.024)  
Strategic (pre-departure) 3D deconfliction of 4D trajectories using en-route speed changes, with wind and temperature uncertainty handled via ensemble forecasts; solved by simulated annealing. TR-C 103:194-210. DOI quoted in a citing paper's reference list.  
*→ RAM flow problem:* Metaheuristic strategic deconfliction under weather uncertainty scales to network-wide RAM trajectory planning.  

<a id="trc-free2020"></a>**[trc-free2020]** (authors not captured) (2020). *From free-route air traffic to an adapted dynamic main-flow system*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x19304218)  
Derives a dynamic main-flow (corridor-like) structure from free-route traffic to organise en-route flows adaptively. From title/URL only; year inferred from PII.  
*→ RAM flow problem:* Bridges free-route operations and structured flows, relevant to deciding whether RAM airspace should be structured or free-route.  

<a id="pelegrin2022"></a>**[pelegrin2022]** Pelegrín, D'Ambrosio (2022). *Aircraft Deconfliction via Mathematical Programming: Review and Insights*. Transp. Sci. [10.1287/trsc.2021.1056](https://doi.org/10.1287/trsc.2021.1056)  
Survey of OR models for tactical conflict detection and resolution: unifies the different mathematical representations of pairwise separation conditions (MILP, MINLP, disjunctive, continuous-time) and revisits the models to compare their computational performance. TS 56(1):118-140.  
*→ RAM flow problem:* Reference taxonomy of separation-constraint formulations for any trajectory-level RAM flow model that must guarantee conflict-free 4D trajectories.  

### Airport/runway/terminal scheduling (15 papers)

<a id="venkatakrishnan1993"></a>**[venkatakrishnan1993]** Venkatakrishnan, Barnett, Odoni (1993). *Landings at Logan Airport: Describing and Increasing Airport Capacity*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v27y1993i3p211-227.html)  
Empirical and optimization analysis of landing sequences at Boston Logan: statistical characterisation of interarrival separations and an optimisation of landing order/timing to increase runway throughput.  

<a id="richetta1993"></a>**[richetta1993]** Richetta, Odoni (1993). *Solving Optimally the Static Ground-Holding Policy Problem in Air Traffic Control*. Transp. Sci. [10.1287/trsc.27.3.228](https://doi.org/10.1287/trsc.27.3.228)  
Static single-airport ground-holding problem with capacity uncertainty represented by a small set of probabilistic capacity-profile scenarios over discrete time periods; aircraft aggregated into classes by scheduled arrival period; formulated as a stochastic linear program with recourse (airborne holding) whose LP solution is integer, solvable on a PC for the largest US airports; compared with deterministic and no-hold strategies across weather scenarios.  
*→ RAM flow problem:* Provides the canonical two-stage recourse template (ground hold now, airborne hold later) and the aggregate-by-period demand representation that a RAM airport-capacity model under weather uncertainty can adopt directly.  

<a id="terrab1993"></a>**[terrab1993]** Terrab, Odoni (1993). *Strategic Flow Management for Air Traffic Control*. Oper. Res. [10.1287/opre.41.1.138](https://doi.org/10.1287/opre.41.1.138)  
Single-airport ground-holding problem for flights from many origins arriving at one congested airport: the deterministic case is solved as a minimum-cost network flow (assignment of flights to arrival time slots with time-varying capacity, with a simple greedy algorithm under certain cost assumptions); heuristics and dynamic programming are given for the stochastic-capacity case.  
*→ RAM flow problem:* Shows the min-cost-flow structure of single-destination hold assignment and why exact DP over capacity states explodes, motivating scenario-based or ADP approaches for RAM networks.  

<a id="peterson1995"></a>**[peterson1995]** Peterson, Bertsimas, Odoni (1995). *Decomposition Algorithms for Analyzing Transient Phenomena in Multiclass Queueing Networks, with an Application to Air Transportation*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v43y1995i6p995-1011.html)  
Decomposition approach for transient, time-varying multiclass queueing networks, applied to delays propagating across a network of airports with time-dependent demand and capacity.  

<a id="navazio1998"></a>**[navazio1998]** Navazio, Romanin-Jacur (1998). *The Multiple Connections Multi-Airport Ground Holding Problem: Models and Algorithms*. Transp. Sci. [10.1287/trsc.32.3.268](https://doi.org/10.1287/trsc.32.3.268)  
Multi-airport ground-holding problem with multiple connections between flights (same aircraft continuing legs), formulated as an integer program over discrete time periods with airport capacity constraints and connection coupling; exact and heuristic algorithms.  
*→ RAM flow problem:* Multiple-connection structure maps to RAM aircraft rotations with several dependent legs per day and to passenger transfers at regional hubs.  

<a id="hoffman2000"></a>**[hoffman2000]** Hoffman, Ball (2000). *A Comparison of Formulations for the Single-Airport Ground-Holding Problem with Banking Constraints*. Oper. Res. [10.1287/opre.48.4.578.12417](https://doi.org/10.1287/opre.48.4.578.12417)  
Builds five 0-1 IP formulations of the single-airport ground-holding problem with hub banking constraints (groups of flights must land within fixed windows), compares them analytically and computationally, proves the banking constraints induce facets for two formulations, and exploits a variable transformation and tailored branching.  
*→ RAM flow problem:* Guides the choice of slot-assignment formulation when RAM schedules at a hub-like regional airport must keep groups of connecting flights (or aircraft rotations) together.  

<a id="beasley2000"></a>**[beasley2000]** Beasley, Krishnamoorthy, Sharaiha, Abramson (2000). *Scheduling Aircraft Landings—The Static Case*. Transp. Sci. [10.1287/trsc.34.2.180.12302](https://doi.org/10.1287/trsc.34.2.180.12302)  
Mixed-integer 0-1 formulation of the aircraft landing problem: each aircraft gets a landing time within a time window subject to sequence-dependent minimum separations; single-runway model extended to multiple runways with runway-assignment binaries. Solved by LP-based tree search with strengthened relaxations plus a heuristic; instances up to 50 aircraft and 4 runways (OR-Library benchmarks).  
*→ both problems:* The time-window plus pairwise-separation structure is the canonical building block for runway/vertiport slot assignment in a RAM flow model and maps directly onto launch-window sequencing with pad turnaround separations at a spaceport.  

<a id="balakrishnan2010"></a>**[balakrishnan2010]** Balakrishnan, Chandran (2010). *Algorithms for Scheduling Runway Operations Under Constrained Position Shifting*. Oper. Res. [10.1287/opre.1100.0869](https://doi.org/10.1287/opre.1100.0869)  
Runway sequencing with Constrained Position Shifting (each aircraft may move at most k positions from its FCFS order), precedence, time-window and sequence-dependent separation constraints. Scalable dynamic programming over a network whose nodes are feasible (position, k-window subsequence) states; polynomial in number of aircraft for fixed k; real-time capable prototype.  
*→ both problems:* CPS gives a tractable, equity-aware way to re-sequence small-aircraft arrivals at a regional airport or vertiport inside a larger flow model, and the same DP applies to ordering launches on a shared pad with bounded deviation from a published manifest order.  

<a id="bertsimas2011b"></a>**[bertsimas2011b]** Bertsimas, Frankovich, Odoni (2011). *Optimal Selection of Airport Runway Configurations*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v59y2011i6p1407-1419.html)  
Integer programming model over discrete time periods that selects the runway configuration and the arrival/departure rate point on each configuration's capacity envelope to minimise delay/configuration-change costs.  

<a id="nikoleris2012"></a>**[nikoleris2012]** Nikoleris, Hansen (2012). *Queueing Models for Trajectory-Based Aircraft Operations*. Transp. Sci. [10.1287/trsc.1120.0411](https://doi.org/10.1287/trsc.1120.0411)  
Single-server queue where aircraft hold scheduled times of arrival met with normally distributed error; expected queueing delay estimated by the Clark approximation, with exact results for metering at constant excess headway. Quantifies the trade-off between stochastic delay from imperfect adherence and deterministic delay from larger metered headways.  
*→ RAM flow problem:* Gives closed-form delay-versus-buffer trade-offs for 4D-trajectory RAM operations where small aircraft are metered into regional airport fixes.  

<a id="jacquillat2015"></a>**[jacquillat2015]** Jacquillat, Odoni (2015). *An Integrated Scheduling and Operations Approach to Airport Congestion Mitigation*. Oper. Res. [10.1287/opre.2015.1428](https://doi.org/10.1287/opre.2015.1428)  
Integrates a strategic scheduling-intervention IP (displacing flights subject to airline schedule preferences and connections) with a stochastic dynamic queuing model of runway operations and a dynamic program controlling runway configurations and service rates; an iterative algorithm alternates between the two and shows large delay reductions for small displacement at JFK.  
*→ RAM flow problem:* Template for coupling a strategic RAM network flow IP with a tactical stochastic model of regional-airport/vertiport throughput via alternating decomposition.  

<a id="simaiakis2016"></a>**[simaiakis2016]** Simaiakis, Balakrishnan (2016). *A Queuing Model of the Airport Departure Process*. Transp. Sci. [10.1287/trsc.2015.0603](https://doi.org/10.1287/trsc.2015.0603)  
Analytical model of the departure process: estimation of unimpeded taxi-out time distributions and a transient D(t)/Ek(t)/1 queueing model of the departure runway server; validated at Newark (EWR) and used for departure metering/pushback rate control.  
*→ RAM flow problem:* Provides the departure-server queue and metering logic for small-airport RAM operations where gate/charging-stand holds substitute for taxi queues.  

<a id="bertsimas2016a"></a>**[bertsimas2016a]** Bertsimas, Frankovich (2016). *Unified Optimization of Traffic Flows Through Airports*. Transp. Sci. [10.1287/trsc.2015.0590](https://doi.org/10.1287/trsc.2015.0590)  
Integer program over a time-discretised airport network (taxiways, runways, arrival/departure fixes, gates) that jointly assigns runway configurations, sequencing and flow rates to minimise delay; large instances solved with commercial MIP after strengthening.  

<a id="demaere2018"></a>**[demaere2018]** De Maere, Atkin, Burke (2018). *Pruning Rules for Optimal Runway Sequencing*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v52y2018i4p898-916.html)  
Exact runway sequencing (take-offs and landings) with sequence-dependent separations and complex objectives; exploits problem structure through dominance and pruning rules within a dynamic-programming / tree search to solve realistic instances to optimality.  
*→ RAM flow problem:* Pruning/dominance techniques transfer to exact sequencing of mixed eVTOL and conventional arrivals at RAM airports.  

<a id="ng2024"></a>**[ng2024]** Ng, Ribeiro, Jorge (2024). *An optimization approach for the terminal airspace scheduling problem*. Transp. Res. C. [10.1016/j.trc.2024.104856](https://doi.org/10.1016/j.trc.2024.104856)  
Joint runway sequencing and TMA control (speed, holding, vectoring, point-merge) formulated with a linear programming core embedded in a metaheuristic search; validated on Singapore Changi, reporting about 27 percent delay reduction versus baseline sequences.  
*→ RAM flow problem:* Shows how speed control and holding in terminal airspace can be co-optimised with runway slots, which is the tactical layer of a RAM flow model.  

### UAM/AAM traffic management (18 papers)

<a id="keskinocak1998"></a>**[keskinocak1998]** Keskinocak, Tayur (1998). *Scheduling of Time-Shared Jet Aircraft*. Transp. Sci. [10.1287/trsc.32.3.277](https://doi.org/10.1287/trsc.32.3.277)  
Fractional-ownership jet scheduling: aircraft dispersed over locations, customer requests (origin, departure time, destination) must be served at minimum cost under maintenance and pre-scheduled trips. Shows the problem is NP-complete, gives a polynomial network-flow algorithm and a pseudo-polynomial DP for two special cases, a 0-1 integer program solved by CPLEX for small/medium instances and a fast heuristic for large ones. TS 32(3) 277-294.  
*→ RAM flow problem:* Classic pre-2005 root of on-demand small-aircraft fleet dispatch; its network-flow special cases and IP model are the template for assigning RAM aircraft to requests subject to turnaround (maintenance/charging) constraints.  

<a id="espinoza2008"></a>**[espinoza2008]** Espinoza, Garcia, Goycoolea, Nemhauser, Savelsbergh (2008). *Per-Seat, On-Demand Air Transportation Part I: Problem Description and an Integer Multicommodity Flow Model*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v42y2008i3p263-278.html)  
Defines the dial-a-flight problem (on-demand per-seat air transportation with small jets between many airports) and formulates it as an integer multicommodity network flow model with side constraints on a time-expanded network of airports; each aircraft is a commodity, passenger requests with time windows ride on arcs. Part I of a two-part study; TS 42(3) 263-278.  
*→ RAM flow problem:* Direct ancestor of RAM on-demand operations: the time-space multicommodity flow with airport and aircraft constraints is the same skeleton a RAM flow model would use to assign departures, routes and holds for small aircraft across many regional airports.  

<a id="espinoza2008a"></a>**[espinoza2008a]** Espinoza, Garcia, Goycoolea, Nemhauser, Savelsbergh (2008). *Per-Seat, On-Demand Air Transportation Part II: Parallel Local Search*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v42y2008i3p279-291.html)  
Companion paper solving the large-scale dial-a-flight integer multicommodity flow model of Part I by a parallel local search that repeatedly re-optimises small subsets of aircraft/requests with an IP solver; shown to handle realistic instance sizes for a per-seat on-demand air carrier. TS 42(3) 279-291.  
*→ RAM flow problem:* Supplies the large-scale solution strategy (IP-based neighbourhood re-optimisation) that a RAM network-wide departure/route/hold assignment would need once the time-expanded model exceeds exact-solver reach.  

<a id="tang2021"></a>**[tang2021]** Tang et al. (co-authors not captured) (2021). *Automated flight planning of high-density urban air mobility*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x21003302)  
Proposes a semi-structured UAM airspace with a layered altitude topology and direct routes between entry and exit points, and an optimisation-based automated flight-planning procedure that generates conflict-free 4D trajectories (route/layer, departure time and speed adjustments) for medium- to high-density operations; evaluated in a metropolitan case study (TR-C vol. 131, 2021).  
*→ RAM flow problem:* Strategic pre-departure 4D trajectory assignment in structured low-altitude airspace is trajectory-based ATFM for UAM; the layered route structure is a candidate airspace model for RAM corridors.  

<a id="song2021"></a>**[song2021]** Song, Yeo (2021). *Development of optimal scheduling strategy and approach control model of multicopter VTOL aircrafts for urban air mobility (UAM) operation*. Transp. Res. C. [10.1016/j.trc.2021.103181](https://doi.org/10.1016/j.trc.2021.103181)  
Proposes three approach-control and arrival-scheduling strategies for multicopter VTOL aircraft at a vertiport: BQA (branch queuing approach, aircraft constrained to fixed paths), SBA (sequence-based approach with free movement) and SBAM (SBA with moving separation circles); strategies are compared by simulation on punctuality and loss-of-separation risk, with BQA found most efficient with zero LOS risk (TR-C vol. 128, art. 103181).  
*→ RAM flow problem:* Vertiport-side arrival sequencing under pad capacity is the terminal module of a RAM flow model; the queuing/sequence rules define the capacity profile the network-level model must respect.  

<a id="shao2021"></a>**[shao2021]** Shao, Shao, Lu (2021). *Terminal area control rules and eVTOL adaptive scheduling model for multi-vertiport system in urban air Mobility*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x21003843)  
Defines terminal-area airspace structure and control rules (approach/departure fixes, holding) for a system of several vertiports and formulates an adaptive scheduling model that assigns landing and take-off slots to eVTOLs across the vertiports subject to separation and pad capacity, minimising delay; performance is evaluated by simulation of the multi-vertiport system (TR-C vol. 132, art. 103385).  
*→ RAM flow problem:* Multi-vertiport slot scheduling with pad and separation capacity is the terminal-side building block of a RAM flow model where regional airports replace vertiports.  

<a id="trc-spacetime2022"></a>**[trc-spacetime2022]** (authors not captured) (2022). *A space–time-energy flow-based integer programming model to design and operate a regional shared automated electric vehicle (SAEV) system and corresponding charging network*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x22004107)  
Integer program on a space-time-energy expanded network that jointly designs charging infrastructure and operates a regional shared automated electric vehicle fleet (vehicle flows with state-of-charge layers, charging arcs, demand service).  
*→ both problems:* The space-time-energy expanded network is exactly the representation needed for electric RAM flow management (and for time-expanded feeder service design with vehicle balancing).  

<a id="wang2022"></a>**[wang2022]** Wang, Delahaye, Farges, Alam (2022). *Complexity optimal air traffic assignment in multi-layer transport network for Urban Air Mobility operations*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x22002054)  
Macroscopic traffic assignment of UAM flows on a multi-layer corridor network that minimises congestion and an intrinsic air-traffic complexity metric based on a linear dynamical system; solved by a two-step method based on Dafermos' algorithm; two-layer case study shows congestion mitigation and low-complexity flow patterns. TR-C 142 (2022), venue from a citing paper's reference list.  
*→ RAM flow problem:* Network-level flow assignment with a complexity-based capacity proxy is strategic ATFM for UAM corridors; transfers to RAM route-network demand-capacity balancing.  

<a id="wang2022a"></a>**[wang2022a]** Wang, Delahaye, Farges, Alam (2022). *Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility operations*. Transp. Res. C. [link](https://hal-enac.archives-ouvertes.fr/hal-03701655)  
Macroscopic static traffic assignment on a multilayer UAM route network: flows are allocated to routes to minimise a congestion factor plus intrinsic air-traffic complexity measured with a linear dynamical system (LDS) metric, solved by a two-step method based on Dafermos' algorithm; a two-layer network case study shows congestion mitigation and low-complexity flow organisation.  
*→ RAM flow problem:* The aggregate flow-assignment view is the UAM/RAM counterpart of Eulerian ATFM and DTA models and gives a strategic flow layer above flight-level time-expanded models.  

<a id="justin2022"></a>**[justin2022]** Justin, Payan, Mavris (authors per facet brief; not displayed in result) (2022). *Integrated fleet assignment and scheduling for environmentally friendly electrified regional air mobility*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x22000158)  
Integrated fleet assignment and schedule optimisation for electrified regional air mobility (small electric aircraft, short routes between regional airports) with battery/charging constraints and environmental objectives; built on a US-wide RAM demand model and a fleet routing/schedule optimisation environment. TR-C 138, art. 103567 (from Georgia Tech faculty page and result text).  
*→ RAM flow problem:* The closest in-scope paper to the RAM problem statement itself: schedule and fleet assignment for small electric aircraft between many regional airports with charging/turnaround capacity.  

<a id="trc-traffic2022"></a>**[trc-traffic2022]** (authors not captured) (2022). *Traffic management and resource allocation for UAV-based parcel delivery in low-altitude urban space*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x22002339)  
Framework for UAV traffic management in low-altitude urban airspace: clustering-based UAV path planning, UTM conflict detection and resolution, and mechanism design (auction-type) for allocating scarce airspace resources among UAV operators (TR-C Oct 2022).  
*→ RAM flow problem:* Treats low-altitude drone traffic as a capacity-allocation problem, an analogue of UAM/RAM demand-capacity balancing in constrained urban airspace.  

<a id="wang2023"></a>**[wang2023]** Wang, Delahaye, Farges, Alam (2023). *A quasi-dynamic air traffic assignment model for mitigating air traffic complexity and congestion for high-density UAM operations*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x23002681)  
Quasi-dynamic traffic assignment (QATA) that splits the planning horizon into time slices, assigns UAM route flows per slice and propagates loading across slices (semi-dynamic loading without per-vehicle FIFO or spillback), minimising congestion plus LDS-based complexity inside a centralised strategic planning scheme; iterative assignment solved slice by slice. Corroborated only by a search summary describing the model; no page or venue string was seen.  
*→ RAM flow problem:* Adds the time dimension to aggregate UAM flow assignment, bridging dynamic traffic assignment machinery and time-expanded RAM flow scheduling.  

<a id="levin2023"></a>**[levin2023]** Levin, Rey (2023). *Branch-and-Price for Drone Delivery Service Planning in Urban Airspace*. Transp. Sci. [10.1287/trsc.2022.1175](https://doi.org/10.1287/trsc.2022.1175)  
Plans drone delivery flights within an urban UTM network modelled as airspace above the road network with multiple flight levels; drones are routed conflict-free (time-space separation) through the network and the problem is solved by branch-and-price with customised heuristics to obtain near-optimal integer solutions on realistic instances. TS 57(4) 843-865.  
*→ RAM flow problem:* Treats low-altitude drone traffic management as a capacitated time-space routing problem solved by column generation, directly transferable to RAM/UAM strategic deconfliction and pre-departure scheduling.  

<a id="trc-chance2024"></a>**[trc-chance2024]** (authors not captured) (2024). *Chance-constrained UAM traffic flow optimization with fast disruption recovery under uncertain waypoint occupancy time*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x24000688)  
Trajectory-based UAM traffic flow management: chance-constrained optimisation that assigns conflict-free 4D trajectories/waypoint occupancy times under stochastic occupancy durations, with a fast re-optimisation procedure for disruption recovery.  
*→ RAM flow problem:* Stochastic ATFM with recourse for UAM; waypoint occupancy windows are the UAM counterpart of sector/airport capacity slots.  

<a id="trc-conflict2025"></a>**[trc-conflict2025]** (authors not captured) (2025). *Conflict probability based strategic conflict resolution for UAS traffic management considering Reasonable-Time-To-Act principle*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x25002803)  
Strategic (pre-departure) conflict resolution for UTM: two-step detection (coarse screening then conflict-probability estimation over operational volumes) followed by resolution respecting a reasonable-time-to-act principle; operational-volume abstraction reduces computation.  
*→ RAM flow problem:* Strategic deconfliction is the UTM form of pre-departure ATFM; probabilistic capacity/occupancy treatment is relevant to RAM flow models.  

<a id="trc-demand2025"></a>**[trc-demand2025]** (authors not captured) (2025). *On-demand ridesharing based on dynamic scheduling in urban air mobility*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x25001159)  
Integrated dynamic scheduling model for multimodal UAM ridesharing (ground legs to/from vertiports plus eVTOL legs) solved in four stages: travel service plan generation, available-resource search (improved pulse algorithm), dynamic cooperative multi-task assignment and vehicle rebalancing (hybrid adaptive large neighbourhood search). NYC experiments report about 25 percent higher service rate and 52 percent lower detour time than conventional ridesharing. TR-C, June 2025.  
*→ RAM flow problem:* Recent on-demand UAM operations model whose dynamic vehicle schedules are the demand stream a tactical RAM/UAM flow manager must deconflict.  

<a id="trc-real2025"></a>**[trc-real2025]** (authors not captured) (2025). *Real-time traffic simulation and management for large-scale urban air mobility: Integrating route guidance and collision avoidance*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x25004814)  
Large-scale real-time UAM traffic simulation and management combining network-level route guidance (congestion-aware routing) with tactical collision avoidance; evaluates throughput and delay at city scale (arXiv 2412.01235 preprint).  
*→ RAM flow problem:* Hierarchical strategic routing + tactical separation evaluated by simulation is the standard way UAM flow management is validated; relevant to RAM test-beds.  

<a id="trc-pre2026"></a>**[trc-pre2026]** (authors not captured) (2026). *Pre-planned air routes or dynamic 4D trajectories? A comparative study of UTM ConOps*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x26003797)  
Comparative study of UTM concepts of operation: fixed pre-planned air-route (corridor) networks versus free dynamic 4D trajectories, assessed on capacity, delay and safety via simulation/optimisation.  
*→ RAM flow problem:* Structured corridors vs free-routing is the UAM version of the fixed-route vs trajectory-based-operations question central to ATFM modelling.  

### AAM demand & network planning (8 papers)

<a id="teodorovic1989"></a>**[teodorovic1989]** Teodorović, Krčmar-Nožić (1989). *Multicriteria Model to Determine Flight Frequencies on an Airline Network under Competitive Conditions*. Transp. Sci. [10.1287/trsc.23.1.14](https://doi.org/10.1287/trsc.23.1.14)  
Nonlinear integer multicriteria model choosing route frequencies on an airline network under competition, maximizing profit and passengers carried while minimizing total passenger schedule delay; solved by Monte Carlo random generation of solutions and selection of the best (TS 23(1):14-25).  
*→ RAM flow problem:* Early frequency-design model on a route network with competition and schedule-delay objectives; the frequency decisions it makes are the demand input to a RAM flow problem.  

<a id="adler2010"></a>**[adler2010]** Adler et al. (co-authors not captured) (2010). *High-speed rail and air transport competition: Game engineering as tool for cost-benefit analysis*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v44y2010i7p812-833.html)  
Game-engineering methodology for infrastructure cost-benefit analysis: high-speed rail, hub-and-spoke legacy airlines and regional low-cost carriers maximize best-response functions over prices, frequencies and vehicle sizes given infrastructure, costs and environmental charges; applied to EU-27 Trans-European network corridors.  
*→ RAM flow problem:* Framework for assessing regional air services competing with high-speed rail on frequency and aircraft size, central to RAM market viability.  

<a id="vaze2012"></a>**[vaze2012]** Vaze, Barnhart (2012). *Modeling Airline Frequency Competition for Airport Congestion Mitigation*. Transp. Sci. [10.1287/trsc.1120.0412](https://doi.org/10.1287/trsc.1120.0412)  
Game-theoretic model of airline frequency competition under airport slot constraints; Nash equilibrium found by successive optimizations, each solved by dynamic programming. Validated against observed frequencies; used to evaluate slot-allocation schemes, showing small slot reductions cut flight/passenger delays and raise airline profits (TS 46(4):512-535).  
*→ RAM flow problem:* Links strategic frequency choice to airport capacity and delay, the interface between RAM network planning and demand-capacity balancing at capacity-limited regional airports and vertiports.  

<a id="willey2021"></a>**[willey2021]** Willey, Salmon (2021). *A method for urban air mobility network design using hub location and subgraph isomorphism*. Transp. Res. C. [10.1016/j.trc.2021.102997](https://doi.org/10.1016/j.trc.2021.102997)  
Formulates UAM network design as a hub location problem whose candidate hub-and-spoke topologies are enumerated via subgraph isomorphism against a candidate-site graph, selecting a small set of vertiport hubs and spoke assignments to serve regional demand. Reported in TR-C vol. 125, art. 102997 (April 2021).  
*→ both problems:* Hub location over a candidate-site graph with a small hub set serving many spokes is the direct structural analog of choosing a few orbital hubs fed by many ground spaceports;  

<a id="haan2021"></a>**[haan2021]** Haan, Garrow, Marzuoli, Roy, Bierlaire (2021). *Are commuter air taxis coming to your city? A case study for 40 cities in the United States*. Transp. Res. C. [10.1016/j.trc.2021.103392](https://doi.org/10.1016/j.trc.2021.103392)  
Demand-side feasibility study of commuter air-taxi service across 40 US cities using commute data and time-savings/cost thresholds (TR-C 132, 2021).  
*→ RAM flow problem:* Provides the demand inputs and vertiport-pair structure for UAM/RAM flow models.  

<a id="garrow2021"></a>**[garrow2021]** Garrow, German, Leonard (2021). *Urban air mobility: A comprehensive review and comparative analysis with autonomous and electric ground transportation for informing future research*. Transp. Res. C. [10.1016/j.trc.2021.103377](https://doi.org/10.1016/j.trc.2021.103377)  
Review paper (TR-C 132): surveys UAM demand, vehicle, infrastructure (vertiport), airspace/UTM and operations research streams and contrasts them with autonomous/electric ground transport; identifies open modelling questions (fleet/vertiport operations, scheduling, demand-capacity).  
*→ RAM flow problem:* Anchor review that situates UAM traffic-management and network-operations research; useful to frame the RAM ATFM extension and locate further TR-C work.  

<a id="trc-optimizing2023"></a>**[trc-optimizing2023]** (authors not captured) (2023). *Optimizing the battery charging and swapping infrastructure for electric short-haul aircraft—The case of electric flight in Norway*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x23003029)  
Electric short-haul aircraft fleet scheduling with charging and battery-swapping as a MILP, embedded as a subroutine in an infrastructure-sizing problem solved by simulated annealing; Norway case shows charger/spare-battery mix lets fleets fly about three times fleet size in round trips, charging early and swapping in busy afternoons.  
*→ RAM flow problem:* Charging/turnaround capacity at regional airports is an explicit RAM flow constraint; this gives the scheduling model and sizing logic.  

<a id="trb-integrated2025"></a>**[trb-integrated2025]** (authors not captured) (2025). *Integrated air-rail scheduling: A branch-and-price approach for adaptive passenger-centric planning*. Transp. Res. B. [link](https://www.sciencedirect.com/science/article/pii/s0191261525002127)  
Integrated scheduling of air and rail services with passenger-centric (itinerary) objectives, solved by branch-and-price; adaptive planning across modes (from title and PII only; TR-B 2025).  
*→ RAM flow problem:* Recent TR-B treatment of air services scheduled jointly with a competing/complementary ground mode, relevant to RAM networks feeding or competing with high-speed rail.  

### Airline scheduling & recovery (45 papers)

<a id="talluri1996"></a>**[talluri1996]** Talluri (1996). *Swapping Applications in a Daily Airline Fleet Assignment*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v30y1996i3p237-248.html)  
Swap-based moves on a daily fleet assignment time-space network to restore maintenance/crew feasibility or improve cost with polynomial swap detection. IDEAS URL (TS 30(3) 237-248) seen; title from memory, not displayed in result.  
*→ RAM flow problem:* Swap operators on the time-space network are the basic recovery moves for a RAM flow re-plan.  

<a id="rushmeier1997"></a>**[rushmeier1997]** Rushmeier, Kontogiorgis (1997). *Advances in the Optimization of Airline Fleet Assignment*. Transp. Sci. [10.1287/trsc.31.2.159](https://doi.org/10.1287/trsc.31.2.159)  
Large-scale fleet assignment as a multicommodity flow on a per-fleet time-space (connection) network with flight-cover, flow-balance and fleet-count constraints; model enhancements (node consolidation, maintenance/crew-driven restrictions) plus LP/branch-and-bound strategies solve a USAir-scale daily problem.  
*→ both problems:* The time-space network with ground arcs and aircraft-count constraints is the canonical template for assigning a RAM fleet to legs across many regional airports.  

<a id="luo1997"></a>**[luo1997]** Luo, Yu (1997). *On the Airline Schedule Perturbation Problem Caused by the Ground Delay Program*. Transp. Sci. [10.1287/trsc.31.4.298](https://doi.org/10.1287/trsc.31.4.298)  
*→ RAM flow problem:* Operator response to flow-management holds, relevant for RAM fleets with tight turnaround and charging chains.  

<a id="gopalan1998"></a>**[gopalan1998]** Gopalan, Talluri (1998). *The Aircraft Maintenance Routing Problem*. Oper. Res. [10.1287/opre.46.2.260](https://doi.org/10.1287/opre.46.2.260)  
Routing aircraft so that each visits a maintenance station every three days and satisfies balance-check requirements; static and dynamic models with fast polynomial-time algorithms based on Euler tours / graph structure of the line-of-flight network.  
*→ both problems:* Rotation cycles with periodic maintenance visits are the structure of reusable vehicle rotations between spaceports and refurbishment sites.  

<a id="talluri1998"></a>**[talluri1998]** Talluri (1998). *The Four-Day Aircraft Maintenance Routing Problem*. Transp. Sci. [10.1287/trsc.32.1.43](https://doi.org/10.1287/trsc.32.1.43)  
Extends maintenance routing to a four-day visit requirement; shows NP-completeness and gives heuristics/exact approaches for constructing rotations on the daily line-of-flight graph; TS 32(1):43-53.  
*→ Spaceport feeder design:* Complexity boundary for periodic asset-cycle constraints informs how reusable-vehicle turnaround rules should be modelled.  

<a id="rexing2000"></a>**[rexing2000]** Rexing, Barnhart, Kniker, Jarrah, Krishnamurthy (2000). *Airline Fleet Assignment with Time Windows*. Transp. Sci. [10.1287/trsc.34.1.1.12277](https://doi.org/10.1287/trsc.34.1.1.12277)  
Generalised FAM that assigns fleet types and simultaneously chooses departure times: each flight gets a time window discretised into flight copies on the time-space network; a direct solution approach and an iterative memory-saving approach solve real large-scale instances with lower cost and tighter schedules.  
*→ both problems:* Discrete departure-time copies within windows is exactly how launch-window choice (B) or RAM departure-time assignment (A) can be embedded in a fleet/vehicle assignment model.  

<a id="cordeau2001"></a>**[cordeau2001]** Cordeau, Stojković, Soumis, Desrosiers (2001). *Benders Decomposition for Simultaneous Aircraft Routing and Crew Scheduling*. Transp. Sci. [10.1287/trsc.35.4.375.10432](https://doi.org/10.1287/trsc.35.4.375.10432)  
Integrated aircraft routing and crew pairing with linking (short-connection) constraints; Benders decomposition iterating between a routing master and a crew-pairing subproblem, each solved by column generation; cost reductions versus sequential planning.  
*→ both problems:* Benders between two column-generation problems is a reusable pattern for coupling vehicle rotations with a second resource (crews, pads, recovery ships).  

<a id="barnhart2002"></a>**[barnhart2002]** Barnhart, Kniker, Lohatepanont (2002). *Itinerary-Based Airline Fleet Assignment*. Transp. Sci. [10.1287/trsc.36.2.199.566](https://doi.org/10.1287/trsc.36.2.199.566)  
Extends leg-based FAM to itinerary-level passenger demand with spill and recapture (IFAM): a MIP coupling time-space fleet flows with passenger itinerary flows, solved by combined row and column generation; shows revenue gains over leg-based FAM on major US airline data.  
*→ both problems:* Couples capacity assignment on the time-space network to O-D passenger flows, the structure needed to size RAM aircraft to multi-leg regional itineraries.  

<a id="barnhart2003"></a>**[barnhart2003]** Barnhart, Belobaba, Odoni (2003). *Applications of Operations Research in the Air Transport Industry*. Transp. Sci. [10.1287/trsc.37.4.368.23276](https://doi.org/10.1287/trsc.37.4.368.23276)  
Survey of OR in air transport: schedule planning (schedule design, fleet assignment, routing, crew), revenue management, and aviation infrastructure planning and operations (airport/airspace capacity, ATFM); historical perspective and state of the art.  
*→ both problems:* Anchor review connecting airline-side time-space scheduling with airport/airspace capacity management for both topics.  

<a id="cohn2003"></a>**[cohn2003]** Cohn, Barnhart (2003). *Improving Crew Scheduling by Incorporating Key Maintenance Routing Decisions*. Oper. Res. [10.1287/opre.51.3.387.14759](https://doi.org/10.1287/opre.51.3.387.14759)  
Extended crew pairing model that embeds only the maintenance routing decisions that matter for crews (short connections), using composite 'routing solution' variables to keep the integrated problem tractable; OR 51(3):387-396 per search summary.  
*→ both problems:* Composite-variable integration of a vehicle-routing layer into a resource-covering layer is reusable for coupling RAM aircraft rotations with pilot/charger resources.  

<a id="rosenberger2003"></a>**[rosenberger2003]** Rosenberger, Johnson, Nemhauser (2003). *Rerouting Aircraft for Airline Recovery*. Transp. Sci. [10.1287/trsc.37.4.408.23271](https://doi.org/10.1287/trsc.37.4.408.23271)  
Aircraft recovery as a set-packing model over candidate aircraft routes with cancellations and delays; an aircraft-selection heuristic restricts rerouting to a small subset so the MIP stays tractable; evaluated with SimAir, showing large savings over simple strategies.  
*→ RAM flow problem:* Restricting re-optimisation to a chosen subset of vehicles is a scalable pattern for rolling-horizon RAM recovery.  

<a id="rosenberger2004"></a>**[rosenberger2004]** Rosenberger, Johnson, Nemhauser (2004). *A Robust Fleet-Assignment Model with Hub Isolation and Short Cycles*. Transp. Sci. [10.1287/trsc.1030.0038](https://doi.org/10.1287/trsc.1030.0038)  
Modifies FAM to generate rotations with many short cycles and low hub connectivity so cancellations and swaps remain local; evaluated with the SimAir simulation; better recovery at small planning-cost increase.  
*→ RAM flow problem:* Short-cycle rotations contain delay propagation across a many-airport regional network.  

<a id="lohatepanont2004"></a>**[lohatepanont2004]** Lohatepanont, Barnhart (2004). *Airline Schedule Planning: Integrated Models and Algorithms for Schedule Design and Fleet Assignment*. Transp. Sci. [10.1287/trsc.1030.0026](https://doi.org/10.1287/trsc.1030.0026)  
Integrated schedule design and fleet assignment: mixed-integer model that selects which optional flight legs to operate and assigns fleet types while capturing demand recapture/spill across itineraries (itinerary-based fleet assignment with demand corrections). Solved with column/row generation on a time-space network per fleet; demonstrated on a major US airline's schedule (TS 38(1):19-32).  
*→ both problems:* The time-space fleet network with leg selection and aircraft-size choice is the template for deciding which regional legs an electric fleet flies and with what capacity before flow management.  

<a id="sherali2005"></a>**[sherali2005]** Sherali, Bish, Zhu (2005). *Polyhedral Analysis and Algorithms for a Demand-Driven Refleeting Model for Aircraft Assignment*. Transp. Sci. [10.1287/trsc.1040.0090](https://doi.org/10.1287/trsc.1040.0090)  
MIP for demand-driven refleeting: dynamically reassigning aircraft capacities within a fleet family close to departure as demand forecasts improve, maximising revenue; polyhedral study yields tightened reformulations and valid inequalities; tested on United Airlines instances.  
*→ both problems:* Late capacity re-assignment as forecasts sharpen transfers to RAM aircraft-size swaps (A) and reallocation of launch-vehicle capacity among spokes (B).  

<a id="lan2006"></a>**[lan2006]** Lan, Clarke, Barnhart (2006). *Planning for Robust Airline Operations: Optimizing Aircraft Routings and Flight Departure Times to Minimize Passenger Disruptions*. Transp. Sci. [10.1287/trsc.1050.0134](https://doi.org/10.1287/trsc.1050.0134)  
Two models: robust aircraft routing minimising expected propagated delay with a string-based stochastic MIP solved by branch-and-price, and flight retiming within small time windows to minimise misconnecting passengers; real data show large reductions in propagated delay and disruptions.  
*→ RAM flow problem:* Retiming within windows and slack placement along rotations are the levers a RAM flow model needs to protect tight turnaround/charging buffers.  

<a id="sandhu2007"></a>**[sandhu2007]** Sandhu, Klabjan (2007). *Integrated Airline Fleeting and Crew-Pairing Decisions*. Oper. Res. [10.1287/opre.1070.0395](https://doi.org/10.1287/opre.1070.0395)  
Integrates fleet assignment with crew pairing (bypassing routing through plane-count constraints); two solution methods, Lagrangian relaxation with column generation and Benders decomposition; results on a major airline.  
*→ RAM flow problem:* Plane-count constraints as a proxy for routing feasibility is a lightweight way to keep RAM vehicle-balance constraints in an integrated model.  

<a id="jacobs2008"></a>**[jacobs2008]** Jacobs, Smith, Johnson (2008). *Incorporating Network Flow Effects into the Airline Fleet Assignment Process*. Transp. Sci. [10.1287/trsc.1080.0242](https://doi.org/10.1287/trsc.1080.0242)  
*→ both problems:* Decomposition that couples a capacity-assignment MIP with a flow/revenue subproblem suits vehicle-to-window assignment with payload flow valuation.  

<a id="barnhart2009"></a>**[barnhart2009]** Barnhart, Farahat, Lohatepanont (2009). *Airline Fleet Assignment with Enhanced Revenue Modeling*. Oper. Res. [10.1287/opre.1070.0503](https://doi.org/10.1287/opre.1070.0503)  
Fleet assignment with a subnetwork-based revenue model that approximates itinerary-level spill and recapture more accurately than leg-based models while keeping tractability; DOI quoted in a search summary (Articles in Advance 2008, print 2009).  
*→ both problems:* Intermediate-granularity demand modelling between leg and full itinerary is useful when payload demand is defined by origin-destination-orbit groups.  

<a id="jiang2009"></a>**[jiang2009]** Jiang, Barnhart (2009). *Dynamic Airline Scheduling*. Transp. Sci. [10.1287/trsc.1090.0269](https://doi.org/10.1287/trsc.1090.0269)  
Re-times flights and re-fleets during the booking period as demand information updates, preserving connectivity and aircraft balance on a time-space network with flight copies; MIP shows profit gains over a static schedule.  
*→ both problems:* Rolling re-timing/re-fleeting as information arrives is the planning-side analogue of a dynamic RAM flow re-plan (A) and of re-slotting launches as manifests firm up (B).  

<a id="dumas2009"></a>**[dumas2009]** Dumas, Aithnard, Soumis (2009). *Improving the objective function of the fleet assignment problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v43y2009i4p466-475.html)  
Iteratively improves the fleet assignment objective by alternating between generating fleet assignments and analysing them with a modified passenger flow model, correcting leg-based revenue estimates that ignore multileg itinerary interdependence; TR-B 43(4):466-475.  
*→ Spaceport feeder design:* Iterative assignment-evaluation loop is a practical way to couple a vehicle-window assignment MIP with a payload flow simulator.  

<a id="gao2009"></a>**[gao2009]** Gao, Johnson, Smith (2009). *Integrated Airline Fleet and Crew Robust Planning*. Transp. Sci. [10.1287/trsc.1080.0257](https://doi.org/10.1287/trsc.1080.0257)  
Integrates fleet assignment and crew planning with station-purity/crew-base restrictions to limit crew connections and improve robustness; decomposition-based solution. From title/venue seen; details from known paper.  
*→ both problems:* Purity constraints limiting vehicle types per station translate to limiting vehicle classes per spaceport for ground-support simplicity.  

<a id="petersen2012"></a>**[petersen2012]** Petersen, Sölveling, Clarke, Johnson, Shebalov (2012). *An Optimization Approach to Airline Integrated Recovery*. Transp. Sci. [10.1287/trsc.1120.0414](https://doi.org/10.1287/trsc.1120.0414)  
Fully integrated recovery of schedule, aircraft, crew and passengers via Benders decomposition with a schedule-recovery master and aircraft/crew/passenger subproblems using column generation; single-day horizon on a US hub-and-spoke carrier; first computational results for the fully integrated problem.  
*→ RAM flow problem:* Decomposition architecture for re-planning a flow schedule with coupled resources after disruption.  

<a id="dunbar2012"></a>**[dunbar2012]** Dunbar, Froyland, Wu (2012). *Robust Airline Schedule Planning: Minimizing Propagated Delay in an Integrated Routing and Crewing Framework*. Transp. Sci. [10.1287/trsc.1110.0395](https://doi.org/10.1287/trsc.1110.0395)  
Computes propagated delay jointly along aircraft routes and crew pairings; iterative algorithm alternating routing and crew column generation with updated propagated-delay costs; real network data show lower propagated delay than sequential planning.  
*→ RAM flow problem:* Delay-propagation accounting across coupled resources is needed when RAM aircraft and pilots share tight regional rotations.  

<a id="haouari2013"></a>**[haouari2013]** Haouari, Shao, Sherali (2013). *A Lifted Compact Formulation for the Daily Aircraft Maintenance Routing Problem*. Transp. Sci. [10.1287/trsc.1120.0433](https://doi.org/10.1287/trsc.1120.0433)  
Compact polynomial-size MIP for daily maintenance routing strengthened by lifting / RLT-based valid inequalities, solving large instances to optimality without column generation; TS 47(4):508-525.  
*→ Spaceport feeder design:* Compact lifted formulations are an alternative to string-based branch-and-price for vehicle rotation cycles.  

<a id="liang2013"></a>**[liang2013]** Liang, Chaovalitwongse (2013). *A Network-Based Model for the Integrated Weekly Aircraft Maintenance Routing and Fleet Assignment Problem*. Transp. Sci. [10.1287/trsc.1120.0434](https://doi.org/10.1287/trsc.1120.0434)  
Weekly rotation-tour network representation yielding a compact MILP (WRTNM) whose size grows linearly with the weekly schedule and has a very tight LP relaxation; integrated with fleet assignment; optimal solutions for 5,700 flights and 330 aircraft within five minutes; TS 47(4):493-507.  
*→ both problems:* Shows how periodic service constraints (charging, inspection) can be enforced with flow constraints rather than route enumeration in a RAM time-space model.  

<a id="sherali2013"></a>**[sherali2013]** Sherali, Bae, Haouari (2013). *An Integrated Approach for Airline Flight Selection and Timing, Fleet Assignment, and Aircraft Routing*. Transp. Sci. [10.1287/trsc.2013.0460](https://doi.org/10.1287/trsc.2013.0460)  
Integrated MIP covering selection and re-timing of optional flights, fleet assignment and aircraft (maintenance) routing with itinerary-based demand; solved with Benders decomposition and lifting; matches TS 47(4):455-476 IDEAS entry.  
*→ Spaceport feeder design:* Fully integrated choose-time-assign-route model is the most complete analog for launch window selection plus vehicle assignment plus rotation.  

<a id="delgado2013"></a>**[delgado2013]** Delgado, Prats, Sridhar (2013). *Cruise speed reduction for ground delay programs: A case study for San Francisco International Airport arrivals*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x13001642)  
Aircraft-performance trajectory model that computes the 'equivalent cruise speed' (slower speed with the same fuel burn as nominal cruise) so that GDP-assigned delay is absorbed airborne and remains recoverable if the GDP is cancelled early; recoverable delay is quantified against flight length, aircraft type and cancellation time on SFO arrivals. DOI not seen; already in the A1 verified pipeline.  
*→ RAM flow problem:* Supplies the speed-versus-energy feasibility envelope a RAM flow model needs to price airborne delay absorption for small electric aircraft (battery-equivalent speed in place of fuel-equivalent speed).  

<a id="pita2013"></a>**[pita2013]** Pita, Barnhart, Antunes (2013). *Integrated Flight Scheduling and Fleet Assignment Under Airport Congestion*. Transp. Sci. [10.1287/trsc.1120.0442](https://doi.org/10.1287/trsc.1120.0442)  
Integrated flight scheduling and fleet assignment MIP that maximizes expected airline profit while internalizing aircraft and passenger delay costs at congested, slot-constrained airports; delays are modeled as functions of scheduled demand versus capacity and embedded in the schedule-design network (TS 47(4):477-492).  
*→ both problems:* Endogenous congestion/delay costs at capacity-limited nodes connect airline schedule design to ATFM demand-capacity balancing (A) and to hub-capacity-aware launch scheduling (B).  

<a id="akturk2014"></a>**[akturk2014]** Akturk, Atamtürk, Gürel (2014). *Aircraft Rescheduling with Cruise Speed Control*. Oper. Res. [10.1287/opre.2014.1279](https://doi.org/10.1287/opre.2014.1279)  
Recovery MIP choosing cruise speeds (nonlinear fuel and emission costs) together with aircraft swaps and delays to absorb disruptions; conic quadratic mixed-integer reformulation; first model with speed as an explicit recovery decision under environmental costs.  
*→ RAM flow problem:* Conic reformulation of speed-energy tradeoffs is the modelling route for battery-energy-vs-block-time decisions in RAM recovery.  

<a id="delgado2014"></a>**[delgado2014]** Delgado, Prats (2014). *Operating cost based cruise speed reduction for ground delay programs: Effect of scope length*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x1400285x)  
Extends the cruise-speed-reduction GDP strategy with a cost-index (airline operating-cost) speed criterion and a parametric analysis of GDP scope length, i.e. which flights are included and hence how long they are airborne, trading controller commitment under uncertainty against airline cost. DOI not seen; already in the A1 verified pipeline.  
*→ RAM flow problem:* Shows how the geographic scope of a flow-control programme interacts with speed control; for RAM the analogue is deciding which regional feeder legs are long enough to absorb delay airborne rather than on the ground or at a charger.  

<a id="froyland2014"></a>**[froyland2014]** Froyland, Maher, Wu (2014). *The Recoverable Robust Tail Assignment Problem*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v48y2014i3p351-372.html)  
Recoverable-robust tail assignment as a two-stage stochastic program (planning plus recovery scenarios with cancellation, delay and swap options and passenger rerouting cost); Benders decomposition with column generation in master and subproblems; lower recovery costs shown.  
*→ both problems:* Tail assignment with explicit recovery recourse maps to assigning reusable launch vehicles with recourse for scrubs (B) and RAM tail assignment under charging/weather disruptions (A).  

<a id="zhang2016"></a>**[zhang2016]** Zhang, Lau, Yu (2016). *A math-heuristic algorithm for the integrated air service recovery*. Transp. Res. B. [10.1016/j.trb.2015.11.016](https://doi.org/10.1016/j.trb.2015.11.016)  
Integrated aircraft, crew and passenger recovery solved by a math-heuristic that iterates between MIP stages on time-band/flight-copy networks. DOI quoted in search summary (no page URL seen); details  
*→ RAM flow problem:* Staged matheuristic is a practical route to fast RAM recovery when a monolithic model is too large.  

<a id="evans2016"></a>**[evans2016]** Evans, Vaze, Barnhart (2016). *Airline-Driven Performance-Based Air Traffic Management: Game Theoretic Models and Multicriteria Evaluation*. Transp. Sci. [10.1287/trsc.2014.0543](https://doi.org/10.1287/trsc.2014.0543)  
Proposes mechanisms (averaging, voting, ranking variants) to collect airline inputs and aggregate them into implementable ATM initiatives, with a game-theoretic analysis of strategic gaming by airlines and a multicriteria evaluation of outcomes.  
*→ RAM flow problem:* Preference-aggregation mechanisms for setting flow-management objectives across heterogeneous RAM operators, with gaming analysis.  

<a id="maher2016"></a>**[maher2016]** Maher (2016). *Solving the Integrated Airline Recovery Problem Using Column-and-Row Generation*. Transp. Sci. [10.1287/trsc.2014.0552](https://doi.org/10.1287/trsc.2014.0552)  
Integrated schedule, crew and aircraft recovery in one model solved by column-and-row generation (linking rows added dynamically), reducing problem size and improving runtime and solution quality over standard column generation.  
*→ RAM flow problem:* Column-and-row generation is a reusable large-scale method for RAM recovery models with dynamically generated coupling constraints.  

<a id="arikan2017"></a>**[arikan2017]** Arıkan, Deshpande, Sohoni (2017). *Flight Network-Based Approach for Integrated Airline Recovery with Cruise Speed Control*. Transp. Sci. [10.1287/trsc.2016.0716](https://doi.org/10.1287/trsc.2016.0716)  
New flight-network representation of integrated recovery for aircraft, crew and passengers with delays, rerouting, cancellations and cruise-speed decisions; conic quadratic MIP solved in reasonable time for practical instances.  
*→ RAM flow problem:* Flow-of-entities network with speed decisions is a compact alternative to flight-copy networks for RAM recovery.  

<a id="marla2017"></a>**[marla2017]** Marla, Vaaben, Barnhart (2017). *Integrated Disruption Management and Flight Planning to Trade Off Delays and Fuel Burn*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v51y2017i1p88-111.html)  
Integrates flight planning (cruise speed choice) with schedule recovery (holds, swaps, cancellations) on a time-space recovery network with multiple flight copies per leg encoding speed/time options; MIP minimising fuel plus passenger-delay cost; 66-83% fewer passenger disruptions for about 0.15% extra fuel.  
*→ RAM flow problem:* Speed as a recourse encoded via flight copies gives the RAM flow model an energy-vs-time lever directly comparable with ATFM speed control.  

<a id="yan2018"></a>**[yan2018]** Yan, Kung (2018). *Robust Aircraft Routing*. Transp. Sci. [10.1287/trsc.2015.0657](https://doi.org/10.1287/trsc.2015.0657)  
Robust optimisation of aircraft routing minimising worst-case total propagated delay over a budgeted uncertainty set that captures correlated leg delays (weather, ATM initiatives); reformulation and decomposition algorithm; real airline data.  
*→ RAM flow problem:* Correlated-delay uncertainty sets link ATFM-induced delays to airline routing robustness, directly transferable to RAM rotations under weather.  

<a id="jones2018"></a>**[jones2018]** Jones, Lovell, Ball (2018). *Stochastic Optimization Models for Transferring Delay Along Flight Trajectories to Reduce Fuel Usage*. Transp. Sci. [10.1287/trsc.2016.0689](https://doi.org/10.1287/trsc.2016.0689)  
Two-stage stochastic integer program over ground-delay-program cancellation-time scenarios in which part of each flight's assigned ground delay is converted into en-route cruise-speed reduction, so that if the GDP ends early the flight can accelerate and recover delay at no extra fuel burn relative to the ground-hold baseline. Expected fuel use is traded against expected delay on realistic GDP instances.  
*→ RAM flow problem:* Treats airborne speed reduction as a continuous recourse that shifts delay between ground and air; a RAM flow model can use the same lever when charging or airport capacity recovers earlier than forecast, with an energy-time rather than fuel-time trade-off.  

<a id="wei2020"></a>**[wei2020]** Wei, Vaze, Jacquillat (2020). *Airline Timetable Development and Fleet Assignment Incorporating Passenger Choice*. Transp. Sci. [10.1287/trsc.2019.0924](https://doi.org/10.1287/trsc.2019.0924)  
Integrated timetable development and fleet assignment with a passenger choice (discrete choice) demand model; nonlinear integer program solved by an iterative decomposition / linearization scheme with convergence results; demonstrated on an airline network.  
*→ Spaceport feeder design:* Choice-based demand responding to schedule times is the analog of shippers choosing among launch windows/hubs based on timing.  

<a id="lee2020"></a>**[lee2020]** Lee, Marla, Jacquillat (2020). *Dynamic Disruption Management in Airline Networks Under Airport Operating Uncertainty*. Transp. Sci. [10.1287/trsc.2020.0983](https://doi.org/10.1287/trsc.2020.0983)  
Stochastic reactive-and-proactive disruption management combining a stochastic queuing model of hub airport congestion, a flight-planning tool and an IP for airline recovery; anticipating probabilistic future delays cuts expected recovery cost 1-2%, largely via deliberate departure holds.  
*→ RAM flow problem:* Explicitly links airport-capacity uncertainty (the ATFM input) to airline-side holds, the natural coupling for a RAM flow model.  

<a id="birolini2021"></a>**[birolini2021]** Birolini et al. (co-authors not captured) (2021). *Integrated Flight Scheduling and Fleet Assignment with Improved Supply-Demand Interactions*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v149y2021icp162-180.html)  
Integrated flight scheduling and fleet assignment with an improved representation of supply-demand interactions (itinerary attractiveness depending on schedule); title seen on a ranking page and an IDEAS TR-B 149:162-180 entry in the same result set.  
*→ both problems:* Recent integrated schedule/fleet design with endogenous demand, a direct basis for RAM network scheduling with demand feedback.  

<a id="wei2022"></a>**[wei2022]** Wei, Vaze, Jacquillat (2022). *Choice-Based Airline Schedule Design and Fleet Assignment: A Decomposition Approach*. Transp. Sci. [10.1287/trsc.2022.1141](https://doi.org/10.1287/trsc.2022.1141)  
Integrated schedule design (selecting from optional flights) and fleet assignment with a passenger choice model over fare products; decomposition partitions the flight network into subnetworks solved and recombined; TS 56(6):1410-1431.  
*→ both problems:* Recent template for embedding demand response in time-expanded schedule/fleet design, relevant to RAM demand modelling and feeder service design.  

<a id="bayram2023"></a>**[bayram2023]** Bayram, Yıldız, Farham (2023). *Hub Network Design Problem with Capacity, Congestion, and Stochastic Demand Considerations*. Transp. Sci. [10.1287/trsc.2022.0112](https://doi.org/10.1287/trsc.2022.0112)  
Generalises hub location with capacity acquisition, convex congestion costs at hubs, stochastic demand and dynamic O-D routing; path-based mixed-integer SOCP formulation, with SOCP duality giving an exact Benders decomposition plus column generation; shows congestion, uncertainty and complete vs incomplete hub graphs change designs materially (TS 57(5):1276-1295).  
*→ Spaceport feeder design:* Capacitated, congestion-aware hub design under demand uncertainty is the closest hub-location analogue to orbital hubs with limited launch capacity.  

<a id="cadarso2023"></a>**[cadarso2023]** Cadarso, Vaze (2023). *Passenger-Centric Integrated Airline Schedule and Aircraft Recovery*. Transp. Sci. [10.1287/trsc.2022.1174](https://doi.org/10.1287/trsc.2022.1174)  
Integrated schedule and aircraft recovery with explicit passenger itinerary reaccommodation on a flight-copy time-space network; MIP with decomposition for large instances. From title/venue seen; details from known paper.  
*→ RAM flow problem:* Recent passenger-centred recovery template for RAM where passenger re-accommodation across small aircraft dominates cost.  

<a id="hizir2026"></a>**[hizir2026]** Hizir, Barnhart, Vaze (2026). *Large-Scale Airline Crew Recovery Using Mixed-Integer Optimization and Supervised Machine Learning*. Transp. Sci. [10.1287/trsc.2025.0105](https://doi.org/10.1287/trsc.2025.0105)  
Large-scale crew recovery via MIP with supervised machine learning to predict and prune candidate variables;  
*→ RAM flow problem:* ML-pruned MIP is a recent large-scale solution device applicable to RAM resource recovery.  

### Dynamic network flows (39 papers)

<a id="ford1958"></a>**[ford1958]** Ford, Fulkerson (1958). *Constructing Maximal Dynamic Flows from Static Flows*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v6y1958i3p419-433.html)  
Origin of flows over time: a maximal dynamic (s-t) flow over a horizon is obtained from a static min-cost flow by temporal repetition, avoiding the time-expanded network. Title taken from result summary (IDEAS record for OR 6(3) 419-433 seen).  
*→ both problems:* Foundational result that time-expanded networks can sometimes be bypassed; temporally repeated flows mirror periodic launch windows and repeating RAM schedules.  

<a id="wilkinson1971"></a>**[wilkinson1971]** Wilkinson (1971). *An Algorithm for Universal Maximal Dynamic Flows in a Network*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v19y1971i7p1602-1612.html)  
Earliest-arrival (universal maximal) dynamic flow algorithm: a flow over time that is maximal at every intermediate time.  
*→ both problems:* Earliest-arrival flows underpin evacuation and SO-DTA equivalences later used for capacity-constrained flow scheduling.  

<a id="ts-temporal1972"></a>**[ts-temporal1972]** (authors not captured) (1972). *Temporal Expansion of a Transportation Network—I*. Transp. Sci. [10.1287/trsc.6.3.306](https://doi.org/10.1287/trsc.6.3.306)  
Model for the optimal timing of investments in transportation network capacity over a finite planning horizon (temporal expansion);  
*→ Spaceport feeder design:* Multi-period capacity expansion of a network is the planning layer for adding spaceport/hub capacity as demand grows.  

<a id="ts-temporal1972a"></a>**[ts-temporal1972a]** (authors not captured) (1972). *Temporal Expansion of a Transportation Network—II*. Transp. Sci. [10.1287/trsc.6.4.395](https://doi.org/10.1287/trsc.6.4.395)  
Early model of scheduling link/capacity additions to a transportation network over time as demand grows (temporal network expansion). From title only.  
*→ Spaceport feeder design:* Capacity-timing with usage feedback relates to phasing hub/spaceport capacity against uncertain feeder demand.  

<a id="bellmore1973"></a>**[bellmore1973]** Bellmore, Vemuganti (1973). *On Multi-Commodity Maximal Dynamic Flows*. Oper. Res. [10.1287/opre.21.1.10](https://doi.org/10.1287/opre.21.1.10)  
Extends Ford-Fulkerson maximal dynamic flows to several commodities; examines when temporally repeated static flows remain optimal in the multicommodity case;  
*→ both problems:* Multicommodity flows over time are the aggregate form of ATFM rerouting models (Bertsimas and Stock Patterson 2000) and of multi-payload feeder flows.  

<a id="merchant1978"></a>**[merchant1978]** Merchant, Nemhauser (1978). *A Model and an Algorithm for the Dynamic Traffic Assignment Problems*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v12y1978i3p183-199.html)  
Discrete-time, single-destination, system-optimal DTA: node demands routed through links whose per-period outflow is an exit function of occupancy; nonconvex NLP whose piecewise-linear version has staircase structure and is solved to global optimum by a one-pass simplex.  
*→ RAM flow problem:* The original time-discretised system-optimal flow model; its holding/exit-function structure is the ancestor of time-indexed ATFM capacity constraints.  

<a id="merchant1978a"></a>**[merchant1978a]** Merchant, Nemhauser (1978). *Optimality Conditions for a Dynamic Traffic Assignment Model*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v12y1978i3p200-207.html)  
Necessary optimality conditions for the Merchant-Nemhauser model: equalisation of marginal costs over used paths, generalising static assignment conditions.  
*→ RAM flow problem:* Marginal-cost interpretation of time-varying flows informs pricing/equity analysis of ATFM delay allocation.  

<a id="carey1986"></a>**[carey1986]** Carey (1986). *A Constraint Qualification for a Dynamic Traffic Assignment Model*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v20y1986i1p55-58.html)  
Resolves whether the Merchant-Nemhauser DTA model satisfies a constraint qualification, validating the earlier optimality analysis.  
*→ RAM flow problem:* Technical underpinning of the SO-DTA lineage that ATFM time-expanded models inherit.  

<a id="carey1987"></a>**[carey1987]** Carey (1987). *Optimal Time-Varying Flows on Congested Networks*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v35y1987i1p58-69.html)  
Convex programming reformulation of least-cost time-varying flows on congested networks with flow-dependent arc traversal times (relaxing Merchant-Nemhauser exit-function equalities to inequalities), making the SO-DTA convex and solvable by standard methods.  
*→ RAM flow problem:* Convexification by relaxing flow-propagation equalities is the same device behind LP relaxations of time-indexed ATFM models.  

<a id="friesz1989"></a>**[friesz1989]** Friesz, Luque, Tobin, Wie (1989). *Dynamic Network Traffic Assignment Considered as a Continuous Time Optimal Control Problem*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v37y1989i6p893-901.html)  
*→ RAM flow problem:* Continuous-time counterpart to discrete time-expanded models; frames the continuous-versus-discrete-time question for RAM flow models.  

<a id="carey1992"></a>**[carey1992]** Carey (1992). *Nonconvexity of the dynamic traffic assignment problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v26y1992i2p127-133.html)  
Shows that the FIFO requirement yields a nonconvex constraint set in dynamic assignment, especially with multiple destinations/commodities, identifying a central difficulty for multicommodity flows over time.  
*→ RAM flow problem:* Explains why flight-level (per-commodity) integer formulations are preferred over aggregate FIFO-consistent flows in ATFM and RAM.  

<a id="boyce1993"></a>**[boyce1993]** Boyce, Ran, LeBlanc (1993). *A New Class of Instantaneous Dynamic User-Optimal Traffic Assignment Models*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v41y1993i1p192-202.html)  
Defines instantaneous dynamic user-optimal assignment and formulates two models via optimal control theory for congested networks.  
*→ RAM flow problem:* Part of the OR DTA lineage whose time-discretised versions share machinery with time-expanded ATFM.  

<a id="friesz1993"></a>**[friesz1993]** Friesz, Bernstein, Smith, Tobin, Wie (1993). *A Variational Inequality Formulation of the Dynamic Network User Equilibrium Problem*. Oper. Res. [10.1287/opre.41.1.179](https://doi.org/10.1287/opre.41.1.179)  
First VI formulation of dynamic user equilibrium with simultaneous route and departure-time choice that preserves FIFO; continuous-time infinite-dimensional VI.  
*→ RAM flow problem:* Departure-time choice under congestion is the user-side counterpart of centrally assigned ground delays in ATFM/RAM.  

<a id="daganzo1994"></a>**[daganzo1994]** Daganzo (1994). *The cell transmission model: A dynamic representation of highway traffic consistent with the hydrodynamic theory*. Transp. Res. B. [link](https://www.sciencedirect.com/science/article/pii/0191-2615(94)90002-7)  
Discretises a link into cells and time into steps; cell-to-cell flows follow sending/receiving (min) rules consistent with LWR hydrodynamics, generating shockwaves automatically. Basis for cell-based linear SO-DTA.  
*→ RAM flow problem:* The cell/time discretisation is the ground-traffic template for Eulerian/cell-based air traffic flow models and for capacity-propagating airspace flow models.  

<a id="wie1995"></a>**[wie1995]** Wie, Tobin, Friesz, Bernstein (1995). *A Discrete Time, Nested Cost Operator Approach to the Dynamic Network User Equilibrium Problem*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v29y1995i1p79-92.html)  
Discrete-time dynamic user equilibrium with a nested path-cost operator and heuristic solution on a time-discretised network;  
*→ RAM flow problem:* Discrete-time DUE computation on time-expanded path sets parallels time-indexed route/slot assignment.  

<a id="daganzo1995"></a>**[daganzo1995]** Daganzo (1995). *The Cell Transmission Model, Part II: Network Traffic*. Transp. Res. B. [10.1016/0191-2615(94)00022-r](https://doi.org/10.1016/0191-2615(94)00022-r)  
Extends the cell transmission model to networks: predicts multi-commodity flow evolution with a macroscopic representation consistent with kinematic wave theory; models three-legged junctions and gives a numerical procedure given a time-varying OD table and known turning proportions.  
*→ RAM flow problem:* Network CTM is embedded in the LP SO-DTA models that mirror time-expanded airspace flow formulations.  

<a id="brannlund1998"></a>**[brannlund1998]** Brännlund, Lindberg, Nõu, Nilsson (1998). *Railway timetabling using Lagrangian relaxation*. Transp. Sci. [link](https://drops.dagstuhl.de/entities/document/10.4230/OASIcs.ATMOS.2017.11)  
Time-discretised track-occupancy model where capacity constraints are dualised by Lagrangian relaxation so each train becomes a shortest path in a time-expanded network; TS 32(4) 358-369 per citing-paper reference list. Co-authors from recollection.  
*→ both problems:* Capacity-constrained flow scheduling over time by dualising per-period resource constraints is directly reusable for airport/sector capacities and launch-pad/hub slots.  

<a id="wu1998"></a>**[wu1998]** Wu, Chen, Florian (1998). *The continuous dynamic network loading problem: A mathematical formulation and solution method*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v32y1998i3p173-187.html)  
Formulates continuous dynamic network loading (temporal arc volumes, arc and path travel times given time-dependent path flows) as a system of functional equations, shows FIFO under a reasonable assumption, and develops a polynomial approximation yielding a finite-dimensional system solved as a (possibly nonsmooth) optimization problem.  
*→ RAM flow problem:* Continuous-time network loading theory for propagating time-dependent flows through a congested network.  

<a id="florian1999"></a>**[florian1999]** Florian et al. (co-authors not captured) (1999). *Advances in the Continuous Dynamic Network Loading Problem*. Transp. Sci. [10.1287/trsc.33.4.341](https://doi.org/10.1287/trsc.33.4.341)  
*→ RAM flow problem:* Continuation of the continuous DNL theory line.  

<a id="ziliaskopoulos2000"></a>**[ziliaskopoulos2000]** Ziliaskopoulos et al. (co-authors not captured) (2000). *A Linear Programming Model for the Single Destination System Optimum Dynamic Traffic Assignment Problem*. Transp. Sci. [10.1287/trsc.34.1.37.12281](https://doi.org/10.1287/trsc.34.1.37.12281)  
Embeds a relaxed cell transmission model in an LP over a cell-time grid to solve single-destination SO-DTA; relaxation of the min operator yields linear constraints (and the holding-back artefact).  
*→ RAM flow problem:* Canonical LP-over-time-expanded-grid formulation; the airspace analogue is an Eulerian cell-based ATFM LP.  

<a id="carey2000"></a>**[carey2000]** Carey, Subrahmanian (2000). *An approach to modelling time-varying flows on congested networks*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v34y2000i8p625-644.html)  
Time-expanded network model of time-varying congested flows with flow-dependent link travel times handled by discretised time intervals; title inferred from the IDEAS record (TR-B 34(8) 625-644) seen in results.  
*→ RAM flow problem:* Direct precedent for discretised time-expanded flow models with capacity and travel-time coupling.  

<a id="szeto2004"></a>**[szeto2004]** Szeto, Lo (2004). *A cell-based simultaneous route and departure time choice model with elastic demand*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v38y2004i7p593-612.html)  
Variational inequality formulation of simultaneous route and departure-time choice with elastic demand following the ideal DUO principle, encapsulating a network cell transmission model; correctly resolves DUO under queue spillback and junction blockage and shows OD FIFO holds only under certain cost conditions.  
*→ RAM flow problem:* Cell-based dynamic equilibrium with departure-time choice is a methodological reference for time-slot/route choice in air traffic flow models.  

<a id="heydecker2005"></a>**[heydecker2005]** Heydecker, Addison (2005). *Analysis of Dynamic Traffic Equilibrium with Departure Time Choice*. Transp. Sci. [10.1287/trsc.1030.0075](https://doi.org/10.1287/trsc.1030.0075)  
Analytical dynamic equilibrium with departure-time choice under deterministic queueing; authors and year from recollection (only title and DOI shown in result).  
*→ RAM flow problem:* Departure-time equilibrium at a capacity bottleneck is the behavioural counterpart to assigned departure slots at a capacity-limited vertiport/airport.  

<a id="ts-convergence2005"></a>**[ts-convergence2005]** (authors not captured) (2005). *Convergence of a Discretised Travel-Time Model*. Transp. Sci. [10.1287/trsc.1030.0083](https://doi.org/10.1287/trsc.1030.0083)  
*→ RAM flow problem:* Companion theory to discretised link travel-time models in time-expanded flow formulations.  

<a id="zheng2011"></a>**[zheng2011]** Zheng, Chiu (2011). *A Network Flow Algorithm for the Cell-Based Single-Destination System Optimal Dynamic Traffic Assignment Problem*. Transp. Sci. [10.1287/trsc.1100.0343](https://doi.org/10.1287/trsc.1100.0343)  
Shows the CTM-based single-destination SO-DTA LP is equivalent to an earliest arrival flow problem and solves it with a network-flow algorithm that avoids the vehicle-holding artefacts of simplex/interior-point solutions.  
*→ RAM flow problem:* Bridges flows-over-time theory (earliest arrival) and cell-based SO-DTA, the two pillars of this facet.  

<a id="nie2011"></a>**[nie2011]** Nie (2011). *A cell-based Merchant-Nemhauser model for the system optimum dynamic traffic assignment problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v45y2011i2p329-342.html)  
Proposes a cell-based variant of the Merchant-Nemhauser model for SO-DTA; once linearized and augmented with cross-cell interaction constraints it becomes an LP embedding a relaxed cell transmission model. Shows CTM dynamics derive from M-N with a suitable exit-flow function; uniform treatment of cells/intersections; an algorithm addresses the flow holding-back problem.  
*→ RAM flow problem:* System-optimal dynamic flow LP with CTM dynamics is the ground-traffic analogue of network ATFM flow models.  

<a id="long2011"></a>**[long2011]** Long, Gao, Szeto (2011). *Discretised link travel time models based on cumulative flows: Formulations and properties*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v45y2011i1p232-254.html)  
Piecewise-linearizes cumulative inflow/outflow curves using step-function (SF) and linear-interpolation (LI) approximations to derive discretised link travel time models that ensure FIFO and continuity of travel times in flows; a modified LI model restores causality and strong FIFO.  
*→ RAM flow problem:* Cumulative-flow (by-time) variables are exactly the encoding of Bertsimas-Stock Patterson ATFM models; this paper studies their discretisation properties.  

<a id="doan2012"></a>**[doan2012]** Doan, Ukkusuri (2012). *On the holding-back problem in the cell transmission based dynamic traffic assignment models*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v46y2012i9p1218-1238.html)  
Analyses the artificial holding-back of vehicles in relaxed-CTM SO-DTA LPs (vehicles held despite downstream capacity) and proposes formulations/conditions to eliminate it.  
*→ RAM flow problem:* Holding-back is the artefact a time-indexed ATFM LP relaxation can exhibit when flow may be delayed for free; relevant to RAM flow LPs with holding arcs.  

<a id="yousefi2013"></a>**[yousefi2013]** Yousefi, Zadeh (2013). *Dynamic allocation and benefit assessment of NextGen flow corridors*. Transp. Res. C. [link](https://www.sciencedirect.com/science/article/pii/s0968090x12000666)  
Flow-based modelling identifies candidate airspace for high-density flow corridors (long narrow trajectory-based tubes), builds a corridor network mimicking user-preferred trajectories, dynamically allocates corridors and assesses benefits in complexity reduction and capacity. TR-C 33:297-310.  
*→ RAM flow problem:* Corridor networks are a direct analogue for structured RAM/UAM routes between regional airports; the allocation model informs route-capacity constraints.  

<a id="zheng2015"></a>**[zheng2015]** Zheng, Chiu, Mirchandani (2015). *On the System Optimum Dynamic Traffic Assignment and Earliest Arrival Flow Problems*. Transp. Sci. [10.1287/trsc.2013.0485](https://doi.org/10.1287/trsc.2013.0485)  
Investigates CTM-based single-destination SO-DTA and shows backward propagation of congestion does not affect the optimal arrival flow pattern, linking SO-DTA to earliest arrival flows; authors from recollection.  
*→ RAM flow problem:* Supports using earliest-arrival flow algorithms for capacity-constrained arrival scheduling over time.  

<a id="boland2017"></a>**[boland2017]** Boland, Hewitt, Marshall, Savelsbergh (2017). *The Continuous-Time Service Network Design Problem*. Oper. Res. [10.1287/opre.2017.1624](https://doi.org/10.1287/opre.2017.1624)  
Introduces dynamic discretization discovery (DDD): a fixed-charge capacitated multicommodity flow IP is solved on a partially time-expanded network whose arcs under-estimate travel times (valid lower bound), the relaxed solution is repaired into a continuous-time-feasible plan (upper bound), and time points are added only where the relaxation is time-inconsistent; proven to converge to an exact continuous-time optimum without a fine uniform grid.  
*→ both problems:* Both the RAM departure-time/holding problem and spaceport feeder schedule design are hurt by fine time grids; DDD keeps exact continuous-time timing while using only the time points that matter.  

<a id="long2018"></a>**[long2018]** Long, Wang, Szeto (2018). *Link-Based System Optimum Dynamic Traffic Assignment Problems in General Networks*. Oper. Res. [10.1287/opre.2018.1775](https://doi.org/10.1287/opre.2018.1775)  
*→ RAM flow problem:* Recent OR treatment of multi-OD system-optimal flows over time, the aggregate form of network-wide ATFM.  

<a id="hewitt2019"></a>**[hewitt2019]** Hewitt (2019). *Enhanced Dynamic Discretization Discovery for the Continuous Time Load Plan Design Problem*. Transp. Sci. [10.1287/trsc.2019.0890](https://doi.org/10.1287/trsc.2019.0890)  
Strengthens DDD for the continuous-time load plan design (consolidation network) problem with improved relaxations, refinement rules and primal heuristics on partially time-expanded networks;  
*→ both problems:* Shows how DDD is tuned for consolidation networks, the analogue of consolidating regional payloads onto scheduled launch vehicles or feeder flights.  

<a id="vu2020"></a>**[vu2020]** Vu, Hewitt, Boland, Savelsbergh (2020). *Dynamic Discretization Discovery for Solving the Time-Dependent Traveling Salesman Problem with Time Windows*. Transp. Sci. [10.1287/trsc.2019.0911](https://doi.org/10.1287/trsc.2019.0911)  
Exact DDD algorithm for the TSP with hard time windows and time-dependent (FIFO) travel times: an IP relaxation on a partially time-expanded network with travel-time-under-estimating arcs gives lower bounds, infeasible tours are repaired for upper bounds, and time points are added where the relaxation is inaccurate, exploiting piecewise-linear travel-time structure.  
*→ both problems:* RAM routes have congestion-dependent (time-dependent) transit times and slot time windows at regional airports; this shows DDD handles both exactly.  

<a id="scherr2020"></a>**[scherr2020]** Scherr, Hewitt, Neumann-Saavedra, Mattfeld (2020). *Dynamic discretization discovery for the service network design problem with mixed autonomous fleets*. Transp. Res. B. [10.1016/j.trb.2020.09.009](https://doi.org/10.1016/j.trb.2020.09.009)  
Scheduled SND for city parcel logistics where level-4 autonomous vehicles must be platooned by manned vehicles outside feasible zones (vehicle synchronization); DDD on partially time-expanded networks with relaxation-based enhancements and heuristic restrictions outperforms a commercial solver.  
*→ both problems:* Fleet-mix plus scheduled-service design on a time-expanded network is the template for electric/hybrid RAM fleets and for reusable launch-vehicle fleets with turnaround constraints.  

<a id="marshall2021"></a>**[marshall2021]** Marshall, Boland, Savelsbergh, Hewitt (2021). *Interval-Based Dynamic Discretization Discovery for Solving the Continuous-Time Service Network Design Problem*. Transp. Sci. [10.1287/trsc.2020.0994](https://doi.org/10.1287/trsc.2020.0994)  
Continuous-time SND solved on a partially time-expanded network by interval-based dynamic discretization discovery: each iteration solves a small IP on a coarse time-expanded network that yields a lower bound, checks whether the solution is implementable in continuous time, and refines node time intervals only where needed, converging to a provably optimal continuous-time plan. Computations show models smaller than 1% of a full time-expanded network suffice.  
*→ both problems:* Interval-based discretization is the natural fit for RAM flow holds and spaceport launch windows, where feasibility is defined over time intervals rather than instants.  

<a id="hewitt2023"></a>**[hewitt2023]** Hewitt, Lehuede (2023). *New formulations for the Scheduled Service Network Design Problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v172y2023icp117-133.html)  
Formulates the SSNDP with enumerated consolidations of shipments routed on the physical network instead of a time-expanded network; stronger LP relaxation, less symmetry and much faster solution with an off-the-shelf solver.  
*→ both problems:* Formulation choices for time-expanded SND carry directly to scheduled feeder (launch) networks and scheduled RAM services.  

<a id="ts-cost2025"></a>**[ts-cost2025]** (authors not captured) (2025). *Cost Function Approximation for the Dynamic Scheduled Service Network Design Problem*. Transp. Sci. [10.1287/trsc.2025.0428](https://doi.org/10.1287/trsc.2025.0428)  
Dynamic (rolling, uncertain-demand) scheduled service network design on a time-expanded network solved via cost-function-approximation policies; from title only. Year inferred from manuscript number.  
*→ both problems:* Recent (2025) treatment of dynamic scheduled network design under uncertainty, relevant to rolling RAM schedule updates and to launch-manifest planning with uncertain payload demand.  

<a id="ts-cross2025"></a>**[ts-cross2025]** (authors not captured) (2025). *Cross-Dock Trailer Scheduling with Workforce Constraints: A Dynamic Discretization Discovery Approach*. Transp. Sci. [10.1287/trsc.2023.0406](https://doi.org/10.1287/trsc.2023.0406)  
Trailer scheduling at cross-dock doors with workforce constraints formulated on a time-expanded network and solved with DDD; outperforms full time-expanded MIP on instances with 180 trailers and ~100 doors.  
*→ both problems:* Capacity-constrained scheduling of arrivals/departures at a hub with limited handling resources is the structure of vertiport/spaceport turnaround capacity.  

### Hub location (39 papers)

<a id="okelly1986"></a>**[okelly1986]** O'Kelly (1986). *The Location of Interacting Hub Facilities*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v20y1986i2p92-106.html)  
Seminal paper (TS 20(2):92-106) introducing the hub location problem: planar one- and two-hub models in which all origin-destination interactions are routed via hubs with a discounted inter-hub link, minimizing total weighted distance; solved with iterative continuous-location heuristics and illustrated on US air passenger interactions. Index page corroborates venue/pages; title and author from the search summary's reference to the 1986 Transportation Science seminal paper.  
*→ Spaceport feeder design:* Origin of the spoke-hub-hub-spoke cost structure; the continuous version is useful for first-cut reasoning about where a small number of transfer nodes (orbital hubs) should sit relative to a dispersed demand field of spaceports.  

<a id="hall1987"></a>**[hall1987]** Hall (1987). *Direct versus terminal freight routing on a network with concave costs*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v21y1987i4p287-298.html)  
Procedure for deciding whether a shipment should be routed through an intermediate terminal or directly to its destination on a network with concave (economies-of-scale) costs (TR-B 21(4):287-298).  
*→ Spaceport feeder design:* The spoke-level decision of hub routing versus direct launch under concave launch-cost curves.  

<a id="daganzo1987"></a>**[daganzo1987]** Daganzo (1987). *The Break-Bulk Role of Terminals in Many-to-Many Logistic Networks*. Oper. Res. [10.1287/opre.35.4.543](https://doi.org/10.1287/opre.35.4.543)  
Continuum-approximation analysis of terminals as break-bulk/swapping points in many-to-many networks; quantifies benefits and disadvantages of routing vehicles through a terminal lying in their general direction of travel (OR 35(4):543-555). Venue from secondary page.  
*→ Spaceport feeder design:* Analytical trade-off for consolidating many origins through a hub versus direct service, the essential economics of orbital hubs.  

<a id="aykin1988"></a>**[aykin1988]** Aykin (1988). *On the Location of Hub Facilities*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v22y1988i2p155-157.html)  
Short technical note (TS 22(2):155-157) on O'Kelly's interacting hub facilities model, discussing the allocation of demand points to hubs and the solution of the continuous hub location problem. Title corroborated by TRID; venue/pages by IDEAS (https://ideas.repec.org/a/inm/ortrsc/v22y1988i2p155-157.html).  
*→ Spaceport feeder design:* Early clarification of allocation logic in hub systems; mainly of historical value for framing the spoke-to-hub assignment subproblem in a spaceport feeder network.  

<a id="campbell1990"></a>**[campbell1990]** Campbell (1990). *Freight consolidation and routing with transportation economies of scale*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v24y1990i5p345-361.html)  
Analyses three routing schemes via consolidation terminals in an idealised many-to-many network where consolidation exploits transportation economies of scale; continuous approximation of costs versus number/location of terminals (TR-B 24(5):345-361).  
*→ Spaceport feeder design:* Analytical sizing of how many hubs a many-to-many feeder system should have given scale economies.  

<a id="klincewicz1990"></a>**[klincewicz1990]** Klincewicz et al. (co-authors not captured) (1990). *Solving a Freight Transport Problem Using Facility Location Techniques*. Oper. Res. [10.1287/opre.38.1.99](https://doi.org/10.1287/opre.38.1.99)  
Freight routing through consolidation terminals with concave (economies-of-scale) link costs reformulated as an uncapacitated facility location problem and solved with facility-location heuristics/dual ascent (OR 38(1):99-109). From title and listing only.  
*→ Spaceport feeder design:* Shows the hub/consolidation routing problem can be cast as facility location, a modelling trick reusable for feeder networks.  

<a id="campbell1993"></a>**[campbell1993]** Campbell (1993). *Continuous and discrete demand hub location problems*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v27y1993i6p473-482.html)  
Analytical (continuous approximation) hub location models with rectilinear distances comparing transport cost of hub networks for continuously distributed versus discrete demand; derives expressions relating number of hubs, discount and cost, and compares with discrete formulations.  
*→ Spaceport feeder design:* Gives closed-form style sizing of how many hubs a dispersed demand field warrants as a function of the inter-hub discount, useful for order-of-magnitude design of orbital hub count before detailed optimization.  

<a id="campbell1996"></a>**[campbell1996]** Campbell (1996). *Hub Location and the p-Hub Median Problem*. Oper. Res. [10.1287/opre.44.6.923](https://doi.org/10.1287/opre.44.6.923)  
Integer (linear) programming formulations of the uncapacitated multiple- and single-allocation p-hub median problems with inter-hub discount factor, including variants with flow thresholds and fixed hub costs; discusses LP-relaxation quality and proposes heuristics (e.g., allocation rules derived from the multiple-allocation solution) for the single-allocation case.  
*→ Spaceport feeder design:* Baseline static model for choosing p orbital hubs and assigning each spaceport to one hub (single allocation) or several (multiple allocation) with discounted hub-to-hub transfer; the fixed-cost and threshold variants map to hub set-up and minimum-flow-per-launch conditions.  

<a id="okelly1998"></a>**[okelly1998]** O'Kelly, Bryan (1998). *Hub location with flow economies of scale*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v32y1998i8p605-616.html)  
Argues that fixed inter-hub discount factors miscalculate cost and misplace hubs; introduces the FLOWLOC model with flow-dependent (piecewise-linear concave) inter-hub costs so that scale economies depend on realised bundled flow (TR-B 32(8):605-616).  
*→ Spaceport feeder design:* Core reference for making inter-hub transfer cost depend on consolidated flow volume.  

<a id="ts-designing2004"></a>**[ts-designing2004]** (authors not captured) (2004). *Designing Distribution Networks: Formulations and Solution Heuristic*. Transp. Sci. [10.1287/trsc.1030.0064](https://doi.org/10.1287/trsc.1030.0064)  
Distribution network design formulations with transshipment/consolidation facilities and a solution heuristic; returned for a hub-and-spoke network design query. Title only; year inferred from the trsc.1030 DOI series.  

<a id="racunica2005"></a>**[racunica2005]** Racunica, Wynter (2005). *Optimal location of intermodal freight hubs*. Transp. Res. B. [10.1016/j.trb.2004.07.001](https://doi.org/10.1016/j.trb.2004.07.001)  
Hub location model to raise rail share in intermodal freight via hub-and-spoke networks, generalizing hub location with non-linear concave cost functions on segments; solved via a linearization plus two variable-reduction heuristics exploiting polyhedral results; Alpine freight case study.  
*→ Spaceport feeder design:* Concave-cost hub consolidation is the core economics of spaceport feeder consolidation.  

<a id="yaman2007"></a>**[yaman2007]** Yaman, Kara, Tansel (2007). *The latest arrival hub location problem for cargo delivery systems with stopovers*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v41y2007i8p906-919.html)  
Minimax hub location minimising the arrival time of the last item, including transient (unloading/loading/sorting) times from non-simultaneous arrivals at hubs and allowing stopovers on spoke routes; generic MIP strengthened with valid inequalities and lifting; US and Turkey data (TR-B 41(8):906-919).  
*→ Spaceport feeder design:* Latest-arrival objectives with synchronisation waiting at hubs match orbital rendezvous timing and multi-stop feeder legs.  

<a id="decamargo2009"></a>**[decamargo2009]** de Camargo, de Miranda, Luna (2009). *Benders Decomposition for Hub Location Problems with Economies of Scale*. Transp. Sci. [10.1287/trsc.1080.0233](https://doi.org/10.1287/trsc.1080.0233)  
Multiple-allocation hub-and-spoke network with flow-dependent (piecewise) economies of scale on inter-hub arcs; a tighter MIP formulation and a specialised Benders decomposition solve large instances in reasonable time (TS 43(1):86-97).  
*→ Spaceport feeder design:* Flow-dependent discounts on hub-to-hub legs correspond to consolidated inter-orbit transfers; Benders is the standard exact route for large spoke sets.  

<a id="alumur2009"></a>**[alumur2009]** Alumur, Kara, Karasan (2009). *The design of single allocation incomplete hub networks*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v43y2009i10p936-951.html)  
Uniform modelling of single-allocation hub problems when the inter-hub network need not be complete: incomplete p-hub median, hub location with fixed costs, hub covering and p-hub center variants with efficient formulations; CAB and Turkish instances (TR-B 43(10):936-951).  
*→ Spaceport feeder design:* Only a subset of inter-hub (inter-orbit) links can be afforded; incomplete hub network design captures this.  

<a id="yaman2009"></a>**[yaman2009]** Yaman (2009). *The hierarchical hub median problem with single assignment*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v43y2009i6p643-658.html)  
Three-level hub network: complete network among central hubs, star networks from hubs to central hubs and from demand centres to hubs; MIP models deciding locations of a given number of hubs and central hubs and the connections to minimise routing cost; CAB and Turkey data (TR-B 43(6):643-658). Venue from repository page and summary.  
*→ Spaceport feeder design:* Multi-level hub hierarchy is a natural template for regional collection points feeding a small set of launch sites.  

<a id="correia2010"></a>**[correia2010]** Correia, Nickel, Saldanha-da-Gama (2010). *Single-assignment hub location problems with multiple capacity levels*. Transp. Res. B. [10.1016/j.trb.2009.12.016](https://doi.org/10.1016/j.trb.2009.12.016)  
Extends the capacitated single-allocation hub location problem by making hub size a decision chosen from a discrete set of capacity levels. Several MIP formulations are compared via LP-relaxation bounds, strengthened with valid inequalities, and preprocessing tests reduce model size.  
*→ Spaceport feeder design:* Hub sizing with discrete capacity options maps directly to choosing spaceport/consolidation-node capacities in a feeder network.  

<a id="contreras2011"></a>**[contreras2011]** Contreras, Cordeau, Laporte (2011). *Benders Decomposition for Large-Scale Uncapacitated Hub Location*. Oper. Res. [10.1287/opre.1110.0965](https://doi.org/10.1287/opre.1110.0965)  
Uncapacitated multiple-allocation hub location with fixed hub set-up costs on a complete hub network, formulated as a path-based MIP and decomposed by Benders: the subproblem separates by origin-destination pair, Pareto-optimal cuts, a multi-cut scheme, elimination tests and a warm-start heuristic are added. Solved instances with up to 500 nodes to optimality, far beyond prior exact methods.  
*→ Spaceport feeder design:* Choosing a small set of orbital hubs among many candidate orbits or stations to serve many spaceport origins is a large-scale hub location instance; this Benders scheme is the exact-method backbone for that choice (  

<a id="meng2011"></a>**[meng2011]** Meng, Wang (2011). *Intermodal hub-and-spoke network design: Incorporating multiple stakeholders and multi-type containers*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v45y2011i4p724-742.html)  
Mathematical program with equilibrium constraints for intermodal hub-and-spoke design: network designer at the upper level, parametric variational inequality capturing user-equilibrium route choice of intermodal operators and multi-type containers at the lower level; heuristic solution (TR-B 45(4):724-742).  
*→ Spaceport feeder design:* Multi-stakeholder hub design (infrastructure owner vs launch operators choosing routes) with heterogeneous payload types.  

<a id="contreras2012"></a>**[contreras2012]** Contreras, Cordeau, Laporte (2012). *Exact Solution of Large-Scale Hub Location Problems with Multiple Capacity Levels*. Transp. Sci. [10.1287/trsc.1110.0398](https://doi.org/10.1287/trsc.1110.0398)  
Capacitated hub location where each hub is installed at one of several discrete capacity levels; exact algorithm based on Lagrangean relaxation bounds and branch-and-bound/reduction tests, solving large instances (TS 46(4):439-459). From title/index only.  
*→ Spaceport feeder design:* Discrete capacity levels map to sizing orbital hubs (docking ports, propellant/payload storage modules).  

<a id="alumur2012"></a>**[alumur2012]** Alumur, Nickel, Saldanha-da-Gama (2012). *Hub location under uncertainty*. Transp. Res. B. [10.1016/j.trb.2011.11.006](https://doi.org/10.1016/j.trb.2011.11.006)  
Introduces uncertainty in hub set-up costs and in demand into single- and multiple-allocation hub location; scenario-based two-stage stochastic MIPs (location first, allocation/routing by scenario) and a robust (minimax) variant; computational study shows that designs from expected-value deterministic models can differ substantially from stochastic solutions. IAOR corroborates title; volume 46(4):529-543 from recollection.  
*→ Spaceport feeder design:* Template for orbital hub siting when hub set-up cost (construction/launch cost to orbit) and spaceport demand are both uncertain; establishes the value of scenario-based over expected-value design.  

<a id="yaman2012"></a>**[yaman2012]** Yaman, Karasan, Kara (2012). *Release Time Scheduling and Hub Location for Next-Day Delivery*. Oper. Res. [link](https://repository.bilkent.edu.tr/items/9b937618-6feb-4695-b3a3-286e49d2d14a/full)  
Selects p hubs, single-allocates demand centres and decides truck release (departure) times so that the cargo guaranteed to arrive next day at every destination meets a threshold while routing cost is minimised; MIP models with valid inequalities and computational study on Turkish data. Venue stated on secondary pages only.  
*→ Spaceport feeder design:* Joint hub choice and departure-time scheduling under a delivery deadline is a direct analog of launch-window timing into orbital hubs.  

<a id="campbell2012"></a>**[campbell2012]** Campbell, O'Kelly (2012). *Twenty-Five Years of Hub Location Research*. Transp. Sci. [10.1287/trsc.1120.0410](https://doi.org/10.1287/trsc.1120.0410)  
Retrospective survey (TS 46(2):153-169) tracing hub location from O'Kelly's 1986-87 interacting-hub models through p-hub median/center/covering, single vs. multiple allocation, hub arc location and flow-dependent (economies-of-scale) discounts, and linking hub location to classical location analysis and network design. Identifies modelling gaps (constant inter-hub discount, ignoring capacity/congestion, time) and research directions.  
*→ Spaceport feeder design:* Provides the taxonomy of hub models (median/center/covering, allocation rules, arc vs node hubs, discount structure) from which a spaceport-spoke / orbital-hub design can be classified, and warns that constant inter-hub discounts misrepresent vehicle cost structures such as launch economics.  

<a id="contreras2014"></a>**[contreras2014]** Contreras, Fernández (2014). *Hub Location as the Minimization of a Supermodular Set Function*. Oper. Res. [10.1287/opre.2014.1263](https://doi.org/10.1287/opre.2014.1263)  
Shows that a general class of hub location problems (uncapacitated hub location, p-hub median, hub arc location, etc.) is the minimisation of a supermodular set function over hub sets; derives compact formulations and supermodular inequalities enabling branch-and-cut (OR 62(3):557-570).  
*→ Spaceport feeder design:* Unifying structure that yields strong cuts for any hub-set selection, including orbital-hub choice.  

<a id="martinsdesa2015"></a>**[martinsdesa2015]** Martins de Sá, Contreras, Cordeau, de Camargo, de Miranda (2015). *The Hub Line Location Problem*. Transp. Sci. [10.1287/trsc.2014.0576](https://doi.org/10.1287/trsc.2014.0576)  
Locates hubs connected by a path (line) rather than a complete inter-hub graph, minimising weighted travel time including access/exit times; exact Benders decomposition of a strong path-based formulation with multicuts, a fast subproblem algorithm, stronger optimality cuts and Benders branch-and-cut (TS 49(3):500-518). Result page lists the first three authors; remaining two from the paper's author list.  
*→ Spaceport feeder design:* Incomplete inter-hub topologies (a chain of orbital nodes, e.g. LEO depot to higher-energy hub) rather than full interconnection.  

<a id="an2015"></a>**[an2015]** An, Zhang, Zeng (2015). *The reliable hub-and-spoke design problem: Models and algorithms*. Transp. Res. B. [10.1016/j.trb.2015.02.006](https://doi.org/10.1016/j.trb.2015.02.006)  
Hub-and-spoke design in which hubs may be disrupted: each O-D pair is given a primary hub route and backup hubs/routes used upon failure; nonlinear integer programs are linearized and solved by Lagrangian relaxation with branch-and-bound, showing reliable designs cost little extra in normal operation.  
*→ Spaceport feeder design:* Provides the backup-hub and re-routing logic needed when an orbital hub is unavailable (outage, phasing window missed), a key robustness feature for a spaceport feeder network.  

<a id="merakli2016"></a>**[merakli2016]** Meraklı, Yaman (2016). *Robust intermodal hub location under polyhedral demand uncertainty*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v86y2016icp66-85.html)  
Robust uncapacitated multiple-allocation p-hub median under polyhedral demand uncertainty (hose model with node-flow upper limits, hybrid model adding pairwise bounds); minmax linear MIP formulations and two Benders-decomposition exact algorithms for large instances (TR-B 86:66-85).  
*→ Spaceport feeder design:* Hose-type uncertainty (known per-spaceport totals, unknown O-D split) is realistic for payload demand forecasts.  

<a id="serper2016"></a>**[serper2016]** Serper, Alumur (2016). *The design of capacitated intermodal hub networks with different vehicle types*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v86y2016icp51-65.html)  
Determines hub locations and capacities, which transport modes each hub serves, allocation of non-hub nodes and the number of vehicles of each type on hub-network arcs; MIP with a variable-neighbourhood-search heuristic for large instances (TR-B 86:51-65).  
*→ Spaceport feeder design:* Explicit vehicle-count decisions per arc are the launch-vehicle fleet sizing embedded in feeder hub design.  

<a id="zetina2017"></a>**[zetina2017]** Zetina, Contreras, Cordeau, Nikbakhsh (2017). *Robust uncapacitated hub location*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v106y2017icp393-410.html)  
Robust counterparts of uncapacitated multiple-allocation hub location under interval demand uncertainty, interval transportation-cost uncertainty, and both, using Bertsimas-Sim budgeted uncertainty; compact MIP reformulations solved by a Benders-based branch-and-cut, with the price of robustness quantified on CAB/AP instances.  
*→ Spaceport feeder design:* Budgeted robustness lets a feeder-network designer protect the orbital-hub choice against bounded deviations in payload demand and launch cost without full scenario trees.  

<a id="meier2018"></a>**[meier2018]** Meier, Clausen (2018). *Solving Single Allocation Hub Location Problems on Euclidean Data*. Transp. Sci. [10.1287/trsc.2017.0751](https://doi.org/10.1287/trsc.2017.0751)  
Single-allocation hub location on Euclidean instances using a compact formulation that exploits the geometric distance structure, solved by branch-and-cut; solves standard AP instances up to 200 nodes to optimality that earlier exact methods could not.  
*→ Spaceport feeder design:* Scalable exact solution of single-allocation designs when feeder costs follow a metric (e.g., distance- or delta-v-like structure), useful for networks with many candidate spaceports.  

<a id="maheo2019"></a>**[maheo2019]** Mahéo, Kilby, Van Hentenryck (2019). *Benders Decomposition for the Design of a Hub and Shuttle Public Transit System*. Transp. Sci. [link](https://arxiv.org/pdf/1601.00367)  
Design of a hub-and-shuttle transit system (bus hubs with feeder shuttles) via Benders decomposition. Search summary gives vol 53(1):77-88, 2019, which matches Transportation Science, but names the venue inconsistently; publisher page not seen.  
*→ Spaceport feeder design:* Hub plus feeder-shuttle structure is the transit analog of spaceport spokes feeding orbital hubs.  

<a id="peiro2019"></a>**[peiro2019]** Peiró, Corberán, Martí, Saldanha-da-Gama (2019). *Heuristic Solutions for a Class of Stochastic Uncapacitated p-Hub Median Problems*. Transp. Sci. [10.1287/trsc.2018.0871](https://doi.org/10.1287/trsc.2018.0871)  
r-allocation p-hub median extended with fixed allocation costs, non-stop (direct) services between terminals and stochastic traffic and transport costs with finite support; heuristic (GRASP/path-relinking style) producing high-quality feasible solutions (TS 53(4):1126-1149).  
*→ Spaceport feeder design:* Combines allocation flexibility, direct shipments and demand uncertainty, all features of a spaceport feeder design with uncertain payload demand.  

<a id="taherkhani2020"></a>**[taherkhani2020]** Taherkhani, Alumur, Hosseini (2020). *Benders Decomposition for the Profit Maximizing Capacitated Hub Location Problem with Multiple Demand Classes*. Transp. Sci. [10.1287/trsc.2020.1003](https://doi.org/10.1287/trsc.2020.1003)  
Profit-maximising capacitated hub location with several demand classes having different revenues/service requirements, allowing demand to be left unserved; exact Benders decomposition with enhancements for large instances.  
*→ Spaceport feeder design:* Payload classes (crew, priority cargo, bulk) with different willingness-to-pay and the option to drop unprofitable spaceports.  

<a id="wang2020a"></a>**[wang2020a]** Wang, Chen, Liu (2020). *Distributionally Robust Hub Location*. Transp. Sci. [10.1287/trsc.2019.0948](https://doi.org/10.1287/trsc.2019.0948)  
Hub location under demand ambiguity described by a moment-based ambiguity set; the distributionally robust model is reformulated via duality into a tractable mixed-integer program and solved with a decomposition / cutting-plane scheme, showing DRO designs hedge mis-specified demand at modest cost.  
*→ Spaceport feeder design:* Launch demand forecasts for new orbital services are poorly characterised distributions, so a moment-based DRO hub model is a direct fit for depot location under deep demand uncertainty.  

<a id="yildiz2021"></a>**[yildiz2021]** Yıldız, Yaman, Karaşan (2021). *Hub Location, Routing, and Route Dimensioning: Strategic and Tactical Intermodal Transportation Hub Network Design*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v55y2021i6p1351-1369.html)  
Integrated strategic/tactical model that locates hubs, allocates demand nodes, routes commodities over an intermodal hub network and dimensions routes (number and type of vehicles per hub arc) subject to service-time limits; mixed-integer formulation with an exact decomposition-based solution approach, tested on intermodal instances. Index page corroborates TS 55(6):1351-1369 and the search summary cites 'strategic and tactical intermodal transportation hub network design' in TS; author list from recollection.  
*→ Spaceport feeder design:* Closest hub-location analog to the spaceport problem: it jointly chooses hubs, vehicle types and the number of vehicles on each feeder/inter-hub leg under delivery-time limits, i.e., launch-vehicle class and launch count per route.  

<a id="taherkhani2021"></a>**[taherkhani2021]** Taherkhani, Alumur, Hosseini (2021). *Robust Stochastic Models for Profit-Maximizing Hub Location Problems*. Transp. Sci. [10.1287/trsc.2021.1064](https://doi.org/10.1287/trsc.2021.1064)  
Profit-maximizing capacitated hub location with uncertain demand and revenues, modelled as two-stage stochastic programs and robust-stochastic variants that hedge over scenario distributions; solved with Benders decomposition combined with sample average approximation, comparing risk-neutral and risk-averse hub designs.  
*→ Spaceport feeder design:* Capacitated orbital hubs serving uncertain payload demand with class-dependent revenues can be sized and located with the same Benders-SAA machinery, letting the model drop unprofitable spaceports.  

<a id="rostami2022"></a>**[rostami2022]** Rostami, Chitsaz, Arslan, Laporte, Lodi (2022). *Single Allocation Hub Location with Heterogeneous Economies of Scale*. Oper. Res. [10.1287/opre.2021.2185](https://doi.org/10.1287/opre.2021.2185)  
Single-allocation hub location where inter-hub discount factors depend on the flow (heterogeneous, piecewise economies of scale); mixed-integer nonlinear formulation with linearisation/convexification and an exact decomposition algorithm.  
*→ Spaceport feeder design:* Vehicle-size-dependent cost per kg on consolidated inter-orbit legs is a heterogeneous economies-of-scale structure.  

<a id="ghaffarinasab2022"></a>**[ghaffarinasab2022]** Ghaffarinasab, Kara, Campbell (2022). *The stratified p-hub center and p-hub maximal covering problems*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v157y2022icp120-148.html)  
Multiple-allocation p-hub center and p-hub maximal covering where each O-D pair's traffic is split into strata with distinct service-level (time) requirements; MILP models and efficient Benders decomposition algorithms for large instances (TR-B 157:120-148).  
*→ Spaceport feeder design:* Service-level strata per O-D pair correspond to payload classes with different delivery-time guarantees via orbital hubs.  

<a id="wandelt2022"></a>**[wandelt2022]** Wandelt, Dai, Zhang, Sun (2022). *Toward a Reference Experimental Benchmark for Solving Hub Location Problems*. Transp. Sci. [10.1287/trsc.2021.1094](https://doi.org/10.1287/trsc.2021.1094)  
Systematic computational benchmark of exact and heuristic methods across standard hub location variants and instance sets, proposing a reference experimental protocol.  
*→ Spaceport feeder design:* Guides choice of solution method and instance scale for a feeder-network hub model.  

<a id="ts-demand2025"></a>**[ts-demand2025]** (authors not captured) (2025). *Demand-Driven Hub Network Design Under Uncertainty for Less-Than-Truckload Carriers*. Transp. Sci. [10.1287/trsc.2025.0180](https://doi.org/10.1287/trsc.2025.0180)  
*→ Spaceport feeder design:* Most recent in-scope treatment of consolidation hub network design under demand uncertainty, the closest commercial analogue to spaceport-to-hub payload consolidation; details need a second search round.  

### Service network design (20 papers)

<a id="magnanti1984"></a>**[magnanti1984]** Magnanti, Wong (1984). *Network Design and Transportation Planning: Models and Algorithms*. Transp. Sci. [10.1287/trsc.18.1.1](https://doi.org/10.1287/trsc.18.1.1)  
Survey/unifying framework for discrete-choice network design as integer programs over fixed-charge multicommodity flow networks; reviews Benders, Lagrangian and dual-ascent algorithms and computational experience; foundation of the fixed-charge capacitated multicommodity network design lineage.  
*→ both problems:* Root model class for choosing which spaceport-hub launch services to open (fixed charge) and routing payload flows over them.  

<a id="powell1986"></a>**[powell1986]** Powell (1986). *A Local Improvement Heuristic for the Design of Less-than-Truckload Motor Carrier Networks*. Transp. Sci. [10.1287/trsc.20.4.246](https://doi.org/10.1287/trsc.20.4.246)  
Early service network design for LTL consolidation networks: local-improvement (add/drop of direct services) heuristic over a load-planning network with consolidation at break-bulk terminals.  
*→ Spaceport feeder design:* Classic hub-and-spoke consolidation design heuristic transferable to spoke-to-hub feeder service selection.  

<a id="crainic1986"></a>**[crainic1986]** Crainic, Rousseau (1986). *Multicommodity, multimode freight transportation: A general modeling and algorithmic framework for the service network design problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v20y1986i3p225-242.html)  
Seminal frequency-based SND: nonlinear mixed-integer model choosing service frequencies and commodity itineraries (paths) with congestion/delay costs at terminals; heuristic decomposition alternating itinerary column generation with descent on service frequencies. RePEc URL (TRB 20(3), 225-242) surfaced for the Crainic SND query.  
*→ Spaceport feeder design:* The frequency-and-itinerary view (how often to serve each spaceport-hub corridor, which payload paths to use, congestion at hubs) is the tactical layer of feeder design before detailed time-expanded scheduling.  

<a id="balakrishnan1989"></a>**[balakrishnan1989]** Balakrishnan, Magnanti, Wong (1989). *A Dual-Ascent Procedure for Large-Scale Uncapacitated Network Design*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v37y1989i5p716-740.html)  
Dual-ascent (Lagrangian/dual) algorithm producing near-optimal bounds for large uncapacitated fixed-charge network design.  
*→ Spaceport feeder design:* Classic bounding technique for fixed-charge network design.  

<a id="farvolden1994"></a>**[farvolden1994]** Farvolden, Powell (1994). *Subgradient Methods for the Service Network Design Problem*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v28y1994i3p256-272.html)  
Service network design over a time-space network for LTL carriers; subgradient-based (dual) methods combined with add/drop of services, using primal-dual information from the multicommodity flow subproblem.  
*→ Spaceport feeder design:* Early scheduled-SND formulation on a time-space network with vehicle balance, directly analogous to scheduling launch services.  

<a id="holmberg1998"></a>**[holmberg1998]** Holmberg, Hellstrand (1998). *Solving the uncapacitated network design problem by a Lagrangean heuristic and branch-and-bound*. Oper. Res. [10.1287/opre.46.2.247](https://doi.org/10.1287/opre.46.2.247)  
Exact branch-and-bound for uncapacitated fixed-charge network design using Lagrangian heuristic bounds. DOI in result text only.  
*→ Spaceport feeder design:* Exact baseline for fixed-charge network design.  

<a id="holmberg2000"></a>**[holmberg2000]** Holmberg, Yuan (2000). *A Lagrangian Heuristic Based Branch-and-Bound Approach for the Capacitated Network Design Problem*. Oper. Res. [10.1287/opre.48.3.461.12439](https://doi.org/10.1287/opre.48.3.461.12439)  
Exact branch-and-bound for fixed-charge capacitated multicommodity network design with Lagrangian relaxation bounds and a Lagrangian heuristic for primal solutions.  
*→ Spaceport feeder design:* Exact method for the capacitated fixed-charge core of a feeder network design.  

<a id="ts-dynamic2000"></a>**[ts-dynamic2000]** (authors not captured) (2000). *Dynamic Routing for Priority Shipments in LTL Service Networks*. Transp. Sci. [10.1287/trsc.34.1.86.12279](https://doi.org/10.1287/trsc.34.1.86.12279)  
Dynamic routing of priority shipments through an LTL service network given the load plan. From title only.  
*→ Spaceport feeder design:* Operational routing of time-critical payload over a fixed feeder service network.  

<a id="agarwal2002"></a>**[agarwal2002]** Agarwal (2002). *Design of Capacitated Multicommodity Networks with Multiple Facilities*. Oper. Res. [10.1287/opre.50.2.333.423](https://doi.org/10.1287/opre.50.2.333.423)  
Capacitated multicommodity network loading in which several facility types with different costs and capacities can be installed on each edge (motivated by private telecom networks using Fractional-T1 services); integer-programming formulation solved with strengthened (partition/cut-set type) inequalities and branch-and-bound.  
*→ Spaceport feeder design:* Choosing among launch-vehicle classes with different payload capacities and costs on each spaceport-to-orbit corridor is a multi-facility capacitated network loading problem; the cutting-plane approach transfers directly.  

<a id="ghamlouche2003"></a>**[ghamlouche2003]** Ghamlouche, Crainic, Gendreau (2003). *Cycle-Based Neighbourhoods for Fixed-Charge Capacitated Multicommodity Network Design*. Oper. Res. [10.1287/opre.51.4.655.16098](https://doi.org/10.1287/opre.51.4.655.16098)  
Arc-based MIP for the fixed-charge capacitated multicommodity network design (CMND) problem: open arcs at fixed cost and route commodity flows at linear cost subject to arc capacity. Proposes cycle-based neighbourhoods for tabu search in which a move redirects flow around a cycle (opening/closing arcs) and candidate cycles are identified by shortest-path-like network procedures; outperforms earlier arc/path-based tabu heuristics on benchmark CMND instances.  
*→ Spaceport feeder design:* Selecting which spaceport-to-hub launch services to open at fixed cost while routing payload flows under per-launch capacity is a CMND; cycle-based moves give a scalable heuristic for large feeder instances where exact MIP fails.  

<a id="ouyang2006"></a>**[ouyang2006]** Ouyang, Daganzo (2006). *Discretization and Validation of the Continuum Approximation Scheme for Terminal System Design*. Transp. Sci. [10.1287/trsc.1040.0110](https://doi.org/10.1287/trsc.1040.0110)  
Algorithm that translates continuum-approximation (CA) location recipes into discrete terminal designs and validates CA accuracy for terminal systems. DOI stated in result text, publisher URL not seen.  
*→ Spaceport feeder design:* Bridges analytical hub-count/frequency estimates and a discrete spaceport-hub design.  

<a id="pedersen2009"></a>**[pedersen2009]** Pedersen, Crainic, Madsen (2009). *Models and Tabu Search Metaheuristics for Service Network Design with Asset-Balance Requirements*. Transp. Sci. [10.1287/trsc.1080.0234](https://doi.org/10.1287/trsc.1080.0234)  
Design-balanced capacitated multicommodity network design (DBCMND) with constraints balancing assets at terminals on a time-space network; arc- and cycle-based formulations; tabu search on the arc formulation tested on standard instances.  
*→ Spaceport feeder design:* Design-balance constraints model reusable launch vehicles returning to spaceports between missions.  

<a id="chouman2015"></a>**[chouman2015]** Chouman, Crainic (2015). *Cutting-Plane Matheuristic for Service Network Design with Design-Balanced Requirements*. Transp. Sci. [10.1287/trsc.2013.0493](https://doi.org/10.1287/trsc.2013.0493)  
Design-balanced capacitated multicommodity network design solved by a cutting-plane procedure (tight lower bounds, learning which variables are promising) feeding a variable-fixing MIP phase.  
*→ Spaceport feeder design:* Exact-bound-guided heuristic for balanced-asset feeder designs.  

<a id="winkenbach2016"></a>**[winkenbach2016]** Winkenbach, Kleindorfer, Spinler (2016). *Enabling Urban Logistics Services at La Poste through Multi-Echelon Location-Routing*. Transp. Sci. [10.1287/trsc.2015.0624](https://doi.org/10.1287/trsc.2015.0624)  
Multi-echelon location-routing model with continuous-approximation routing cost estimates for urban logistics facility design.  
*→ Spaceport feeder design:* Multi-echelon facility design with approximated routing cost; by-catch for the location-routing facet.  

<a id="chouman2017"></a>**[chouman2017]** Chouman, Crainic, Gendron (2017). *Commodity Representations and Cut-Set-Based Inequalities for Multicommodity Capacitated Fixed-Charge Network Design*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v51y2017i2p650-667.html)  
Cutting-plane algorithm for MCFND using strong, cover, minimum cardinality, flow cover and flow pack inequalities expressed on network cut sets; compares aggregated vs disaggregated commodity representations.  
*→ Spaceport feeder design:* Strengthened formulations for the capacitated fixed-charge core of the feeder design.  

<a id="gendron2017"></a>**[gendron2017]** Gendron, Gouveia (2017). *Reformulations by Discretization for Piecewise Linear Integer Multicommodity Network Flow Problems*. Transp. Sci. [10.1287/trsc.2015.0634](https://doi.org/10.1287/trsc.2015.0634)  
Discretization-based reformulations (unit-capacity/staircase cost) for multicommodity network flow with piecewise linear integer costs, generalizing fixed-charge network design; stronger relaxations.  
*→ Spaceport feeder design:* Models stepwise launch cost as a function of number of vehicles dispatched on a lane.  

<a id="ts-robust2020"></a>**[ts-robust2020]** (authors not captured) (2020). *Robust Service Network Design Under Demand Uncertainty*. Transp. Sci. [10.1287/trsc.2019.0935](https://doi.org/10.1287/trsc.2019.0935)  
Robust optimization formulation of SND with uncertain demand. From title only.  
*→ Spaceport feeder design:* Robust alternative to scenario-based feeder design when demand distributions are unknown.  

<a id="hewitt2022"></a>**[hewitt2022]** Hewitt (2022). *The Flexible Scheduled Service Network Design Problem*. Transp. Sci. [10.1287/trsc.2021.1114](https://doi.org/10.1287/trsc.2021.1114)  
Scheduled SND where shipment availability/due times may be shifted at a cost to enable consolidation; integer program on a time-expanded network with a solution approach outperforming a commercial solver on US LTL instances.  
*→ Spaceport feeder design:* Shifting payload readiness dates to match launch windows is exactly service-time flexibility.  

<a id="shu2024"></a>**[shu2024]** Shu, Xu, Baldacci (2024). *Incorporating Holding Costs in Continuous-Time Service Network Design: New Model, Relaxation, and Exact Algorithm*. Transp. Sci. [10.1287/trsc.2022.0104](https://doi.org/10.1287/trsc.2022.0104)  
Extends the continuous-time SND problem with in-transit holding costs; new model, relaxation and exact algorithm (DDD-type).  
*→ Spaceport feeder design:* Holding payload at hubs awaiting a launch window incurs storage cost, as modelled here.  

<a id="malik2026"></a>**[malik2026]** Malik, Chakraborty, Jayaswal (2026). *E-Commerce Middle-Mile Network Design with Delivery Speed Choices and Service Level Constraints*. Transp. Sci. [10.1287/trsc.2024.0930](https://doi.org/10.1287/trsc.2024.0930)  
Middle-mile consolidation network design with multiple delivery-speed products and service-level constraints. From title only.  
*→ Spaceport feeder design:* Multiple service classes with deadline constraints over a consolidation network.  

### Liner/feeder shipping (26 papers)

<a id="rana1991"></a>**[rana1991]** Rana, Vickson (1991). *Routing Container Ships Using Lagrangean Relaxation and Decomposition*. Transp. Sci. [10.1287/trsc.25.3.201](https://doi.org/10.1287/trsc.25.3.201)  
Profit-maximising mixed-integer non-linear model choosing each ship's port-call sequence, number of trips in the horizon and cargo carried between ports; solved by Lagrangean relaxation and decomposition. TS 25(3):201-214.  
*→ Spaceport feeder design:* Classic decomposition of per-vehicle route/trip-count decisions coupled through cargo, a template for per-vehicle launch sequences coupled by payload demand.  

<a id="christiansen1999"></a>**[christiansen1999]** Christiansen (1999). *Decomposition of a Combined Inventory and Time Constrained Ship Routing Problem*. Transp. Sci. [10.1287/trsc.33.1.3](https://doi.org/10.1287/trsc.33.1.3)  
Industrial shipping of a single product (ammonia) between production and consumption harbours with inventory limits and time windows; Dantzig-Wolfe decomposition into ship-routing and inventory subproblems, solved by branch-and-bound. TS 33(1):3-16.  
*→ Spaceport feeder design:* Inventory-coupled vehicle routing with time windows transfers to depot-stock-driven resupply launches to orbital hubs.  

<a id="christiansen2004"></a>**[christiansen2004]** Christiansen, Fagerholt, Ronen (2004). *Ship Routing and Scheduling: Status and Perspectives*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v38y2004i1p1-18.html)  
Survey of ship routing and scheduling research of the preceding decade, organised by strategic fleet planning, tactical/operational planning and mode of operation (industrial, tramp, liner); TS 38(1):1-18.  
*→ Spaceport feeder design:* Classic review that distinguishes liner (fixed-schedule feeder-like) from tramp/industrial operation, useful for positioning scheduled versus on-demand launch services.  

<a id="agarwal2008"></a>**[agarwal2008]** Agarwal, Ergun (2008). *Ship Scheduling and Network Design for Cargo Routing in Liner Shipping*. Transp. Sci. [10.1287/trsc.1070.0205](https://doi.org/10.1287/trsc.1070.0205)  
Integrated MILP that simultaneously designs cyclic ship routes with a weekly frequency constraint and routes cargo as multicommodity flow, allowing transshipment between service routes, on a time-space (weekly) network. Solved by a greedy heuristic, a column-generation algorithm and a two-phase Benders decomposition; instances up to 20 ports and 100 ships show high capacity utilisation and many transshipments.  
*→ Spaceport feeder design:* Direct analogue of jointly choosing periodic launch services and payload routing through orbital hubs; the weekly-frequency constraint corresponds to a fixed launch cadence and the decomposition separates service design from payload flow.  

<a id="erera2009"></a>**[erera2009]** Erera, Morales, Savelsbergh (2009). *Robust Optimization for Empty Repositioning Problems*. Oper. Res. [10.1287/opre.1080.0650](https://doi.org/10.1287/opre.1080.0650)  
Robust dynamic empty repositioning on time-space networks with interval forecasts of supplies/demands and a budget on total scaled deviation; defines recoverable robust plans and gives necessary and sufficient conditions for three recovery-action types. OR 57(2):468-483.  
*→ Spaceport feeder design:* Recoverable-robust asset balancing on a time-expanded network for reusable launch assets under forecast uncertainty.  

<a id="agarwal2010"></a>**[agarwal2010]** Agarwal, Ergun (2010). *Network Design and Allocation Mechanisms for Carrier Alliances in Liner Shipping*. Oper. Res. [10.1287/opre.1100.0848](https://doi.org/10.1287/opre.1100.0848)  
*→ Spaceport feeder design:* Relevant when several launch operators share hub capacity: joint network design with incentive-compatible capacity allocation.  

<a id="engineer2012"></a>**[engineer2012]** Engineer, Furman, Nemhauser, Savelsbergh, Song (2012). *A Branch-Price-and-Cut Algorithm for Single-Product Maritime Inventory Routing*. Oper. Res. [10.1287/opre.1110.0997](https://doi.org/10.1287/opre.1110.0997)  
Maritime inventory routing with varying storage capacities and production/consumption rates; branch-price-and-cut with exact dynamic-programming pricing, structure-preserving branching and VRP-inspired capacity cuts; solves practically sized oil-industry instances to optimality.  
*→ Spaceport feeder design:* Exact method for inventory-driven vehicle routing between supply and consumption nodes, analogous to resupply launches sized by orbital-depot inventory.  

<a id="song2012"></a>**[song2012]** Song, Dong (2012). *Cargo routing and empty container repositioning in multiple shipping service routes*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v46y2012i10p1556-1575.html)  
Operational joint laden-cargo routing and empty container repositioning over a network of several service routes, deployed vessels and voyages; minimises lifting, backlog, transshipment demurrage, inventory and empty-transport costs; TR-B 46(10):1556-1575.  
*→ Spaceport feeder design:* Repositioning of empty assets across periodic services is the analogue of returning reusable capsules/adapters and balancing vehicle inventory across spaceports.  

<a id="wang2012"></a>**[wang2012]** Wang, Meng (2012). *Liner ship route schedule design with sea contingency time and port time uncertainty*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v46y2012i5p615-633.html)  
Tactical schedule design that fixes arrival times at each port call and the speed function on each leg under random sea and port times. Mixed-integer non-linear stochastic programme minimising ship cost plus expected bunker cost subject to a transit-time service level; TR-B 46(5):615-633.  
*→ Spaceport feeder design:* Template for setting launch-slot times and vehicle speed/energy profiles under uncertain ground-processing and transfer times with a time-to-orbit service level.  

<a id="wang2013"></a>**[wang2013]** Wang, Meng, Liu (2013). *Containership scheduling with transit-time-sensitive container shipment demand*. Transp. Res. B. [10.1016/j.trb.2013.04.003](https://doi.org/10.1016/j.trb.2013.04.003)  
TR-B 54:68-83.  
*→ Spaceport feeder design:* Captures demand elasticity to delivery time, relevant where payload customers value shorter time-to-orbit.  

<a id="brouer2014"></a>**[brouer2014]** Brouer, Alvarez, Plum, Pisinger, Sigurd (2014). *A Base Integer Programming Model and Benchmark Suite for Liner-Shipping Network Design*. Transp. Sci. [10.1287/trsc.2013.0471](https://doi.org/10.1287/trsc.2013.0471)  
Service-based integer programme for liner-shipping network design: non-simple cyclic rotations with weekly frequency, vessel-class capacity per leg, multicommodity cargo routing with transshipment, revenue minus operating cost. Proves strong NP-hardness and releases the LINER-LIB benchmark (Maersk data); first best-known solutions via tabu search with heuristic column generation.  
*→ Spaceport feeder design:* Canonical periodic hub-and-spoke feeder design with capacitated cyclic services: rotations map to launch cadence, vessel capacity to lift capacity, transshipment to orbital-hub transfer; LINER-LIB offers a benchmark template for a spaceport feeder instance set.  

<a id="meng2014"></a>**[meng2014]** Meng, Wang, Andersson, Thun (2014). *Containership Routing and Scheduling in Liner Shipping: Overview and Future Research Directions*. Transp. Sci. [10.1287/trsc.2013.0461](https://doi.org/10.1287/trsc.2013.0461)  
Review of 30 years of OR for containership routing and scheduling at strategic (fleet size and mix, alliances, network design), tactical (frequency, fleet deployment, speed, schedule design) and operational (booking, container routing, rescheduling) levels; identifies gaps between research and practice.  
*→ Spaceport feeder design:* Provides the planning-level taxonomy (strategic/tactical/operational) to structure a spaceport-to-orbit feeder review and names the modelling conventions for frequency, capacity and transit time.  

<a id="rakke2015"></a>**[rakke2015]** Rakke, Andersson, Christiansen, Desaulniers (2015). *A New Formulation Based on Customer Delivery Patterns for a Maritime Inventory Routing Problem*. Transp. Sci. [10.1287/trsc.2013.0503](https://doi.org/10.1287/trsc.2013.0503)  
Reformulates a maritime inventory routing problem using customer delivery patterns (feasible visit/quantity sequences) to tighten the model and enable branch-and-price (title and venue corroborated; authors and year from memory, confirm).  
*→ Spaceport feeder design:* Pattern-based formulation of periodic delivery sequences is reusable for discrete launch-window delivery patterns to a hub.  

<a id="xia2015"></a>**[xia2015]** Xia, Li, Ma, Xu, Lee (2015). *Joint Planning of Fleet Deployment, Speed Optimization, and Cargo Allocation for Liner Shipping*. Transp. Sci. [10.1287/trsc.2015.0625](https://doi.org/10.1287/trsc.2015.0625)  
Integrates fleet deployment, sailing-speed optimisation and cargo allocation with container transshipment over a liner network; mixed-integer non-linear model with linearisation/decomposition (title and venue corroborated; authors and year from memory, confirm).  
*→ Spaceport feeder design:* Joint vehicle assignment, energy/speed profile and payload allocation on a hub network with transfers.  

<a id="zheng2015a"></a>**[zheng2015a]** Zheng, Gao, Yang, Sun (2015). *Network Design and Capacity Exchange for Liner Alliances with Fixed and Variable Container Demands*. Transp. Sci. [10.1287/trsc.2014.0572](https://doi.org/10.1287/trsc.2014.0572)  
Liner alliance network design in which carriers design services and exchange slot capacity, with both fixed and price-dependent (variable) container demand (title and venue corroborated; authors and year from memory, confirm).  
*→ Spaceport feeder design:* Relevant to multi-operator spaceport feeders: shared lift capacity exchanged among launch providers under fixed and elastic payload demand.  

<a id="wang2015"></a>**[wang2015]** Wang, Liu, Meng (2015). *Segment-based alteration for container liner shipping network design*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v72y2015icp128-145.html)  
Improves an existing liner network by altering route segments (insert/remove/replace port calls) with laden and empty container flow re-evaluation; TR-B 72:128-145.  
*→ Spaceport feeder design:* Incremental redesign of an existing periodic feeder network, suited to evolving spaceport networks.  

<a id="tierney2015"></a>**[tierney2015]** Tierney, Askelsdottir, Jensen, Pisinger (2015). *Solving the Liner Shipping Fleet Repositioning Problem with Cargo Flows*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v49y2015i3p652-674.html)  
Moves vessels between liner services without disrupting cargo flows; novel graph-based mathematical model plus simulated annealing evaluated on Maersk data (profit raised from 18.1 to 31.8 M USD in minutes). TS 49(3):652-674.  
*→ Spaceport feeder design:* Re-basing reusable launch vehicles between spoke routes while preserving committed payload flows.  

<a id="meng2016"></a>**[meng2016]** Meng, Lee (2016). *Liner container assignment model with transit-time-sensitive container shipment demand*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v90y2016icp135-155.html)  
TR-B 90:135-155.  
*→ Spaceport feeder design:* Profit-maximising acceptance and routing of time-sensitive payload demand through a hub network.  

<a id="akyuz2016"></a>**[akyuz2016]** Akyuz, Lee (2016). *Service type assignment and container routing with transit time constraints and empty container repositioning for liner shipping service networks*. Transp. Res. B. [10.1016/j.trb.2016.02.007](https://doi.org/10.1016/j.trb.2016.02.007)  
Decision tool assigning vessel service types (fleet deployment) to routes and routing laden and empty containers with transit-time constraints; TR-B 88:46-71.  
*→ Spaceport feeder design:* Joint vehicle-type assignment and payload routing with maximum transit times mirrors choosing launch-vehicle class per spoke subject to phasing deadlines.  

<a id="karsten2018"></a>**[karsten2018]** Karsten, Ropke, Pisinger (2018). *Simultaneous Optimization of Container Ship Sailing Speed and Container Routing with Transit Time Restrictions*. Transp. Sci. [10.1287/trsc.2018.0818](https://doi.org/10.1287/trsc.2018.0818)  
Determines sailing speeds and fleet needed for a global liner network while routing containers with tight per-container transit-time limits; exact algorithm combining Benders decomposition and column generation exploiting separability. TS 52(4):769-787.  
*→ Spaceport feeder design:* Speed/energy versus fleet-size trade-off under hard delivery deadlines parallels trajectory energy versus vehicle count under orbital phasing windows.  

<a id="zhen2019"></a>**[zhen2019]** Zhen, Hu, Wang, Laporte, Wu (2019). *Fleet deployment and demand fulfillment for container shipping liners*. Transp. Res. B. [10.1016/j.trb.2018.11.011](https://doi.org/10.1016/j.trb.2018.11.011)  
Joint fleet deployment (which ship type and how many per route) and demand-fulfilment/cargo-acceptance decisions on a liner network; MIP with decomposition-based solution.  
*→ Spaceport feeder design:* Assigning reusable launch vehicles of different classes to periodic spoke routes while deciding which payload demand to accept.  

<a id="koza2020"></a>**[koza2020]** Koza, Desaulniers, Ropke (2020). *Integrated Liner Shipping Network Design and Scheduling*. Transp. Sci. [10.1287/trsc.2018.0888](https://doi.org/10.1287/trsc.2018.0888)  
Column-generation-based matheuristic on LINER-LIB instances.  
*→ Spaceport feeder design:* Shows how to couple service design with timetable so that hub connections are synchronised under maximum transit times, the maritime counterpart of orbital-phasing windows and time-to-orbit limits.  

<a id="jin2021"></a>**[jin2021]** Jin, Meng, Wang (2021). *Feeder vessel routing and transshipment coordination at a congested hub port*. Transp. Res. B. [10.1016/j.trb.2021.07.002](https://doi.org/10.1016/j.trb.2021.07.002)  
Feeder liner company designs vessel routes and schedules when only limited berthing time slots exist at a congested hub, coordinating transshipment connections with long-haul services; arc-based MILP and set-partitioning model; branch-and-price solves up to 30 ports exactly, column-generation heuristic for larger cases. TR-B 151:1-21.  
*→ Spaceport feeder design:* Closest maritime analogue of spokes feeding a capacity-limited hub with discrete docking/launch slots and connection synchronisation to trunk services.  

<a id="zhang2022"></a>**[zhang2022]** Zhang, Zheng, Teo (2022). *Schedule reliability in liner shipping timetable design: a convex programming approach*. Transp. Res. B. [10.1016/j.trb.2021.11.010](https://doi.org/10.1016/j.trb.2021.11.010)  
Timetable design for a liner service under uncertain port and sailing times, choosing buffer times and speeds to maximise schedule reliability; reformulated as a convex programme.  
*→ Spaceport feeder design:* Buffer allocation for a periodic service with uncertain dwell/transit times transfers to launch-window and turnaround buffers for reusable vehicles.  

<a id="xia2025"></a>**[xia2025]** Xia, Xu, Baldacci (2025). *A Simultaneous Column-and-Row Generation Solution Method for Liner Shipping Network Design*. Oper. Res. [10.1287/opre.2020.0458](https://doi.org/10.1287/opre.2020.0458)  
Set-partitioning-like formulation of liner network design with transshipment costs, exponentially many variables and constraints; simultaneous column-and-row generation with speed-ups embedded in branch-and-price yields an exact method; joint fleet deployment, cargo routing and rotation design. OR 73(4):1825-1848.  
*→ Spaceport feeder design:* State-of-the-art exact approach for periodic hub-and-spoke service design with transfer costs; directly reusable for spaceport feeder rotation design.  

<a id="zhang2025"></a>**[zhang2025]** Zhang, Wang, Xin (2025). *Liner fleet deployment and slot allocation problem: a distributionally robust optimization model with joint chance constraints*. Transp. Res. B. [10.1016/j.trb.2025.103236](https://doi.org/10.1016/j.trb.2025.103236)  
Joint fleet deployment and slot allocation under uncertain container demand without a known distribution; two-stage data-driven distributionally robust chance-constrained model reformulated as second-order cone programme, solved by a customised outer-approximation algorithm. TR-B 197.  
*→ Spaceport feeder design:* Modern treatment of uncertain demand for capacity-slot allocation on periodic services, directly applicable to allocating launch-manifest slots under demand ambiguity.  

### Air cargo/express network design (29 papers)

<a id="daskin1989"></a>**[daskin1989]** Daskin, Panayotopoulos (1989). *A Lagrangian Relaxation Approach to Assigning Aircraft to Routes in Hub and Spoke Networks*. Transp. Sci. [10.1287/trsc.23.2.91](https://doi.org/10.1287/trsc.23.2.91)  
Integer program assigning aircraft to routes in a hub-and-spoke network to maximize profit; Lagrangian relaxation with subgradient optimization yields bounds and heuristic solutions. Authors recalled from TS 23(2):91-99 listing.  
*→ Spaceport feeder design:* Early Lagrangian decomposition for vehicle-to-route assignment in hub-and-spoke networks, an analogue of launch-vehicle assignment to spaceport-hub routes.  

<a id="hansen1990"></a>**[hansen1990]** Hansen (1990). *Airline competition in a hub-dominated environment: An application of noncooperative game theory*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v24y1990i1p27-43.html)  
N-player noncooperative game of hub carriers (connecting plus local direct service) and direct carriers choosing frequencies to maximize profit; market shares follow from a frequency-based share model. Equilibria computed and applied to the US system (TR-B 24(1):27-43).  
*→ both problems:* Foundational TR-B model of competitive frequency and hub choice; frames how RAM entrants would compete with incumbent hub networks and ground modes.  

<a id="hong1992"></a>**[hong1992]** Hong, Harker (1992). *Air traffic network equilibrium: Toward frequency, price and slot priority analysis*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v26y1992i4p307-323.html)  
Network equilibrium model of airline frequency and price choices with airport slot (capacity) priority, formulated as a variational inequality / game to analyse hub-and-spoke network outcomes; TR-B 26(4):307-323.  
*→ both problems:* Links airline network economics to scarce node capacity (slots), bridging hub network design (B) and capacity allocation (A).  

<a id="dobson1993"></a>**[dobson1993]** Dobson, Lederer (1993). *Airline Scheduling and Routing in a Hub-and-Spoke System*. Transp. Sci. [10.1287/trsc.27.3.281](https://doi.org/10.1287/trsc.27.3.281)  
Competitive model of airlines choosing flight schedules (departure times and routes through a hub) and route prices in a hub-and-spoke system; passengers choose by price and schedule inconvenience. Equilibrium schedules and prices are computed and compared with a social optimum:281-297).  
*→ both problems:* Shows how timetable and routing decisions through a hub interact with demand quality; analog for scheduling launch windows into an orbital hub when service time drives demand.  

<a id="trietsch1993"></a>**[trietsch1993]** Trietsch (1993). *Scheduling flights at hub airports*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v27y1993i2p133-150.html)  
Generalized newsboy models choose scheduled ground (connection) time at a hub to minimize expected costs and misconnection penalties, with a pure-waiting model (no misconnections) and a no-waiting model (aircraft do not wait for late feeders); TR-B 27(2):133-150.  
*→ both problems:* Optimal buffer between feeder arrivals and hub departures under delay uncertainty transfers to orbital-hub transfer windows (B) and to RAM connection/turnaround buffers (A).  

<a id="jaillet1995"></a>**[jaillet1995]** Jaillet, Song, Yu (1995). *Networking Policies for Hub-and-Spoke Systems with Application to the Air Transportation System*. Transp. Sci. [10.1287/trsc.29.3.201](https://doi.org/10.1287/trsc.29.3.201)  
Framework for designing hub-and-spoke networks under alternative networking policies: nonstrict hubbing (direct shipments allowed when cheaper) versus strict/restrictive hubbing (all flows of a node through one hub); exact and heuristic procedures (Lagrangian-based) tested on 1989 US air passenger flows among the top 40 cities.  
*→ both problems:* Directly models the choice between routing via hubs and direct spoke-to-destination service, the key design question for whether every spaceport must feed an orbital hub or may launch direct.  

<a id="barnhart1996"></a>**[barnhart1996]** Barnhart, Schneur (1996). *Air Network Design for Express Shipment Service*. Oper. Res. [10.1287/opre.44.6.852](https://doi.org/10.1287/opre.44.6.852)  
Express shipment service design: pickup-and-delivery within fixed time intervals through hubs; aircraft routes generated on a time-space network by column generation. Finds near-optimal air service designs for a fixed fleet or simultaneously determines service design, fleet size and fleet composition; millions of dollars in annual savings reported.  
*→ Spaceport feeder design:* Spokes feeding hubs inside hard time windows with vehicle routes and fleet size/mix chosen jointly is the direct template for spaceport-to-orbital-hub feeder design with launch windows.  

<a id="lederer1998"></a>**[lederer1998]** Lederer, Nambimadom (1998). *Airline Network Design*. Oper. Res. [10.1287/opre.46.6.785](https://doi.org/10.1287/opre.46.6.785)  
Analytical model of a profit-maximizing airline's joint choice of network structure (direct, hub-and-spoke, tour, subtour routings) and schedule (frequency and built-in schedule slack for on-time arrival). Compares network types via cost and passenger schedule-delay functions; characterizes when hub-and-spoke dominates direct service as a function of demand density and distance.  
*→ both problems:* Gives the economic logic for choosing point-to-point versus hub routing for thin regional markets, the structural decision a RAM operator makes before any flow model assigns departures and holds.  

<a id="barnhart1998"></a>**[barnhart1998]** Barnhart, Boland, Clarke, Johnson, Nemhauser, Shenoi (1998). *Flight String Models for Aircraft Fleeting and Routing*. Transp. Sci. [10.1287/trsc.32.3.208](https://doi.org/10.1287/trsc.32.3.208)  
Solves fleet assignment and maintenance routing simultaneously using 'strings' (leg sequences between maintenance opportunities) as variables in a string-based multicommodity flow model over a time-space network; branch-and-price with column generation; tested on US airline data. DOI not displayed.  
*→ both problems:* String variables (vehicle itineraries between mandatory service stops) map to electric-aircraft routings between charging/inspection stops (A) and reusable-launch-vehicle rotations between refurbishments (B).  

<a id="kim1999"></a>**[kim1999]** Kim, Barnhart, Ware, Reinhardt (1999). *Multimodal Express Package Delivery: A Service Network Design Application*. Transp. Sci. [10.1287/trsc.33.4.391](https://doi.org/10.1287/trsc.33.4.391)  
Large-scale service network design for express package delivery: cost-minimizing package movement from origins to destinations given tight service windows, limited hub sort capacity and finite ground vehicles and aircraft. Multimodal (air + ground) time-space network with aircraft routes as columns; decomposition and column/row generation to solve a UPS-scale instance.  
*→ Spaceport feeder design:* Explicit hub sort-capacity and service-window constraints map to orbital-hub transfer capacity and launch/phasing windows; multimodal legs map to ground-feeder plus launch segments.  

<a id="lin2001"></a>**[lin2001]** Lin (2001). *The freight routing problem of time-definite freight delivery common carriers*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v35y2001i6p525-547.html)  
Freight routing for time-definite (deadline) delivery carriers over a hub-and-spoke network with time-constrained paths; integer programming with implicit enumeration / shortest-path subproblems (TR-B 35(6):525-547). Title from recollection matched to the IDEAS index entry; index only.  
*→ Spaceport feeder design:* Routing payloads through hubs under hard delivery-time commitments equals orbital-insertion deadline constraints.  

<a id="armacost2002"></a>**[armacost2002]** Armacost, Barnhart, Ware (2002). *Composite Variable Formulations for Express Shipment Service Network Design*. Transp. Sci. [10.1287/trsc.36.1.1.571](https://doi.org/10.1287/trsc.36.1.1.571)  
Reformulates express shipment SND with composite variables that bundle aircraft routes with the package flows they carry, removing the weak flow-capacity coupling and yielding much stronger LP relaxations; solved by column generation / branch-and-price. Applied to UPS Next Day Air with potential savings in the hundreds of millions of dollars. Note: venue is Transportation Science 36(1), not Operations Research as the facet brief stated.  
*→ Spaceport feeder design:* Composite 'route plus covered demand' variables translate to launch-mission variables bundling spaceport, window, vehicle and manifest, giving tractable exact formulations.  

<a id="lin2004"></a>**[lin2004]** Lin, Chen (2004). *The hierarchical network design problem for time-definite express common carriers*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v38y2004i3p271-283.html)  
Hierarchical hub-and-spoke design for time-definite express carriers: centers assigned to primary hubs via secondary routes, hubs connected by primary routes with larger vehicles; integer model with implicit enumeration / heuristic to choose hubs and routes meeting time guarantees; TR-B 38(3):271-283.  
*→ Spaceport feeder design:* Two-echelon design with small vehicles on spokes and large vehicles between hubs under time guarantees maps to ground feeders plus heavy launchers between hubs.  

<a id="adler2005"></a>**[adler2005]** Adler (2005). *Hub-Spoke Network Choice Under Competition with an Application to Western Europe*. Transp. Sci. [10.1287/trsc.1030.0081](https://doi.org/10.1287/trsc.1030.0081)  
Two-stage Nash best-response game: airlines first choose hub-and-spoke network configurations, then compete on fares and frequencies; passenger choice via a logit-type demand. Searches for equilibria over candidate hub networks in Western Europe, identifying profitable hubs and monopolistic vs duopolistic equilibria.  
*→ both problems:* Shows how to embed hub/airport selection inside a competitive equilibrium, applicable to choosing which regional airports anchor a RAM network against competing operators.  

<a id="dumas2008"></a>**[dumas2008]** Dumas et al. (co-authors not captured) (2008). *Passenger Flow Model for Airline Networks*. Transp. Sci. [10.1287/trsc.1070.0206](https://doi.org/10.1287/trsc.1070.0206)  
Stochastic passenger flow model estimating itinerary-level spill and recapture across an airline network for use in fleet assignment evaluation; title and venue seen, authorship not shown in result.  
*→ Spaceport feeder design:* Flow-evaluation module for scoring candidate capacity assignments under uncertain demand.  

<a id="leung2009"></a>**[leung2009]** Leung, Van Hui, Wang, Chen (2009). *A 0-1 LP Model for the Integration and Consolidation of Air Cargo Shipments*. Oper. Res. [10.1287/opre.1080.0583](https://doi.org/10.1287/opre.1080.0583)  
Freight-forwarder assignment of sequential shipment activities (pickup, trucking, warehousing, air transport) to processing units, with cost savings from integrating consecutive activities and consolidating similar activities of different jobs; formulated as a linear 0-1 program solved by heuristics plus branch-and-bound.  
*→ Spaceport feeder design:* Consolidation of shipments across units with integration economies transfers to payload manifesting/rideshare consolidation across launch vehicles.  

<a id="derigs2009"></a>**[derigs2009]** Derigs, Friederichs, Schaefer (2009). *A New Approach for Air Cargo Network Planning*. Transp. Sci. [10.1287/trsc.1090.0282](https://doi.org/10.1287/trsc.1090.0282)  
Two integrated models for freighter network planning combining flight selection, aircraft rotation planning and cargo routing to maximize network profit; both solved by column generation with shortest-path pricing subproblems; developed for a decision support system of a cargo airline.  
*→ Spaceport feeder design:* Joint selection of flights, vehicle rotations and cargo paths is the integrated launch-selection, vehicle-rotation and payload-routing problem of a feeder network.  

<a id="jarrah2009"></a>**[jarrah2009]** Jarrah, Johnson, Neubert (2009). *Large-Scale, Less-than-Truckload Service Network Design*. Oper. Res. [10.1287/opre.1080.0587](https://doi.org/10.1287/opre.1080.0587)  
Novel formulation for LTL service network design capturing the load-plan requirement that all freight at a terminal loads to the same next terminal; fragments a 1.3M-variable model into separate IPs solved in about two hours with USD 20-25M annual savings; OR 57(3):609-625.  
*→ Spaceport feeder design:* Single-next-hop (in-tree) consolidation rules and decomposition of very large SND models transfer to payload routing rules at hubs.  

<a id="erera2013"></a>**[erera2013]** Erera, Hewitt, Savelsbergh, Zhang (2013). *Improved Load Plan Design Through Integer Programming Based Local Search*. Transp. Sci. [10.1287/trsc.1120.0441](https://doi.org/10.1287/trsc.1120.0441)  
LTL load plan design on a time-expanded network with in-tree constraints solved by integer-programming-based local search (IP neighborhoods over terminal subsets), producing better plans than carriers' incumbent methods; TS 47(3):412-427.  
*→ Spaceport feeder design:* IP-based neighborhood search is a scalable matheuristic for large time-expanded feeder network designs.  

<a id="lindsey2016"></a>**[lindsey2016]** Lindsey et al. (co-authors not captured) (2016). *Improved Integer Programming-Based Neighborhood Search for Less-Than-Truckload Load Plan Design*. Transp. Sci. [10.1287/trsc.2016.0700](https://doi.org/10.1287/trsc.2016.0700)  
Neighborhood search heuristics for LTL load plan design that determine the terminal path for freight between origin and destination; improved IP neighborhoods and evaluation over the 2013 approach. Title and venue seen; authorship not in result.  
*→ Spaceport feeder design:* Further scaling of matheuristics for consolidation network design.  

<a id="cadarso2017"></a>**[cadarso2017]** Cadarso, Vaze, Barnhart, Marin (2017). *Integrated airline scheduling: Considering competition effects and the entry of the high speed rail*. Transp. Sci. [link](https://pubsonline.informs.org/doi/fpi/10.1287/trsc.2022.1141)  
Integrated schedule design and fleet assignment with frequency-based competitive market share and HSR entry; mixed-integer model solved with decomposition; venue stated in a search summary only.  
*→ Spaceport feeder design:* Frequency-dependent demand capture is relevant when launch cadence drives payload share between competing launch providers or hubs.  

<a id="fedtke2017"></a>**[fedtke2017]** Fedtke, Boysen (2017). *Layout Planning of Sortation Conveyors in Parcel Distribution Centers*. Transp. Sci. [10.1287/trsc.2014.0540](https://doi.org/10.1287/trsc.2014.0540)  
Design alternatives for closed-loop tilt-tray sortation conveyors in parcel hubs; a novel destination-to-dock-door assignment problem is formalized and solved, and simulation quantifies hub throughput against investment cost; TS 51(1):3-18.  
*→ Spaceport feeder design:* Hub throughput as a design variable (sort capacity vs investment) is the orbital-hub berthing/transfer capacity sizing question.  

<a id="cacchiani2017"></a>**[cacchiani2017]** Cacchiani, Salazar-Gonzalez (2017). *Optimal Solutions to a Real-World Integrated Airline Scheduling Problem*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v51y2017i1p250-268.html)  
Integrated fleet assignment, aircraft routing (with maintenance) and crew pairing for a regional carrier solved exactly via a column-generation / branch-and-price approach; TS 51(1):250-268.  
*→ both problems:* Exact integrated planning for a regional carrier is directly relevant to RAM operators (A) and demonstrates exact methods for small-fleet asset cycles (B).  

<a id="birolini2021a"></a>**[birolini2021a]** Birolini, Jacquillat, Cattaneo, Antunes (2021). *Airline Network Planning: Mixed-Integer Non-convex Optimization with Demand-Supply Interactions*. Transp. Res. B. [10.1016/j.trb.2021.09.003](https://doi.org/10.1016/j.trb.2021.09.003)  
ANPSD model: mixed-integer non-convex optimization that jointly selects routes, flight frequencies and fleet composition while endogenizing passenger demand response to the supplied network (demand-supply interactions through a market-share/choice function). Solved with a tailored decomposition/approximation scheme; applied to a real airline network (TR-B 154:100-124).  
*→ both problems:* State-of-the-art template for RAM network planning where frequencies and aircraft size on many thin regional routes must respond to induced demand; its outputs are the schedule a RAM ATFM model manages.  

<a id="baubaid2021"></a>**[baubaid2021]** Baubaid, Boland, Savelsbergh (2021). *The Value of Limited Flexibility in Service Network Designs*. Transp. Sci. [10.1287/trsc.2020.1009](https://doi.org/10.1287/trsc.2020.1009)  
p-alt model generalizing load plans by allowing up to p next-terminal options per terminal-destination pair under demand uncertainty; shows two options yield about 10% cost savings over deterministic single-path plans; TS 55(1):52-74.  
*→ Spaceport feeder design:* Limited routing flexibility (primary plus alternate hub) hedges uncertain payload volumes without full re-optimization.  

<a id="greening2023"></a>**[greening2023]** Greening, Dahan, Erera (2023). *Lead-Time-Constrained Middle-Mile Consolidation Network Design with Fixed Origins and Destinations*. Transp. Res. B. [link](https://www.sciencedirect.com/science/article/pii/s0191261523001078)  
Middle-mile consolidation network design for e-commerce minimizing cost while meeting shipment lead-time constraints on a time-expanded network; computational experiments show tight lead times increase consolidation and dispatch frequency; TR-B 174 (2023).  
*→ Spaceport feeder design:* Lead-time constrained consolidation with fixed O-D pairs is the payload consolidation problem with orbital delivery deadlines.  

<a id="baubaid2023"></a>**[baubaid2023]** Baubaid, Boland, Savelsbergh (2023). *The Dynamic Freight Routing Problem for Less-Than-Truckload Carriers*. Transp. Sci. [10.1287/trsc.2022.1190](https://doi.org/10.1287/trsc.2022.1190)  
Dynamic routing of shipments to primary or alternate arcs of a load plan as demand is revealed, solved by an offline-online approximate dynamic programming approach.  
*→ Spaceport feeder design:* Operational re-routing of payload across hubs as actual demand and launch slips materialise.  

<a id="kinene2024"></a>**[kinene2024]** Kinene, Birolini (full author list unconfirmed) (2024). *Optimization of subsidized air transport networks using electric aircraft*. Transp. Res. B. [link](https://www.sciencedirect.com/science/article/pii/s0191261524001899)  
Bi-objective MILP choosing routes, frequencies and a mixed electric/conventional fleet for publicly subsidised regional air networks on a time-space-energy network that tracks battery energy along aircraft rotations under a subsidy budget, preceded by a demand-disaggregation step.  
*→ both problems:* Choosing which spoke-to-hub legs to serve at what frequency with a range-limited, turnaround-constrained vehicle class under a budget is structurally the spaceport-to-orbit feeder question, and its route/frequency output is the schedule input a RAM flow model consumes; it is the only corroborated item in the Birolini/Jacquillat/Antunes airline-network-planning lineage named in this facet.  

<a id="erera2025"></a>**[erera2025]** Erera et al. (co-authors not captured) (2025). *Outbound Load Planning in Parcel Delivery Service Networks Using Machine Learning and Optimization*. Transp. Sci. [10.1287/trsc.2024.0672](https://doi.org/10.1287/trsc.2024.0672)  
Outbound load planning for a parcel carrier's hub combining machine-learning volume prediction with optimization of trailer/load assignments; TS 59:1057-1075 per author publication list.  
*→ Spaceport feeder design:* Hub-level load building under predicted volumes is the manifest-building step at an orbital or ground consolidation hub.  

### Multi-echelon & synchronization (30 papers)

<a id="blumenfeld1985"></a>**[blumenfeld1985]** Blumenfeld, Burns, Diltz, Daganzo (1985). *Analyzing trade-offs between transportation, inventory and production costs on freight networks*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v19y1985i5p361-380.html)  
Analytic (EOQ-type) models trading off shipment size, inventory and transport cost on direct, consolidation-terminal and mixed networks; shows when consolidation via a terminal pays.  
*→ Spaceport feeder design:* Shipment-size/frequency versus hub inventory trade-off governs how often spokes feed hubs relative to launch cadence.  

<a id="laporte1988"></a>**[laporte1988]** Laporte, Nobert, Taillefer (1988). *Solving a Family of Multi-Depot Vehicle Routing and Location-Routing Problems*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v22y1988i3p161-172.html)  
Asymmetric multi-depot VRPs and LRPs with capacity or maximum-cost restrictions transformed via graph extension into constrained assignment problems and solved exactly by branch-and-bound.  
*→ Spaceport feeder design:* Classic exact LRP: simultaneous choice of depots (hubs) and routes (feeder legs) under capacity.  

<a id="bookbinder1992"></a>**[bookbinder1992]** Bookbinder, Désilets (1992). *Transfer Optimization in a Transit Network*. Transp. Sci. [link](https://libraryarchives.metro.net/DPGTL/conferences/1993_Optimal_Headways.pdf)  
Optimisation of schedule offsets to minimise transfer disutility at network transfer points under stochastic arrivals; seen via a citing review.  
*→ Spaceport feeder design:* Timed-transfer coordination at hubs maps to synchronising feeder arrivals with launch departures (by-catch, timetable facet).  

<a id="anily1993"></a>**[anily1993]** Anily, Federgruen (1993). *Two-Echelon Distribution Systems with Vehicle Routing Costs and Central Inventories*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v41y1993i1p37-47.html)  
Integrated inventory-routing in a two-echelon system (central warehouse with inventory, retailers served by vehicle routes); long-run average cost analysis with asymptotically optimal region-partitioning policies.  
*→ Spaceport feeder design:* Classic coupling of hub inventory (payload staging) with periodic feeder routing cost; relevant to hub buffer sizing versus launch frequency.  

<a id="shen2003"></a>**[shen2003]** Shen, Coullard, Daskin (2003). *A Joint Location-Inventory Model*. Transp. Sci. [10.1287/trsc.37.1.40.12823](https://doi.org/10.1287/trsc.37.1.40.12823)  
Single supplier, multiple retailers with variable demand; some retailers become distribution centres to pool risk; nonlinear location model reformulated as set covering with column generation pricing via a low-order algorithm.  
*→ Spaceport feeder design:* Hub selection with safety-stock (payload staging) and risk-pooling benefits transfers to choosing which spaceports act as consolidation hubs under uncertain demand.  

<a id="shu2005"></a>**[shu2005]** Shu, Teo, Shen (2005). *Stochastic Transportation-Inventory Network Design Problem*. Oper. Res. [10.1287/opre.1040.0140](https://doi.org/10.1287/opre.1040.0140)  
One supplier, many retailers with uncertain demand; chooses retailers to serve as DCs with risk pooling; set-covering column generation whose pricing is solved efficiently via a sorting-based algorithm.  
*→ Spaceport feeder design:* Hub designation with pooled safety stock; efficient pricing for nonlinear hub cost.  

<a id="berger2007"></a>**[berger2007]** Berger, Coullard, Daskin (2007). *Location-Routing Problems with Distance Constraints*. Transp. Sci. [10.1287/trsc.1060.0156](https://doi.org/10.1287/trsc.1060.0156)  
Set-partitioning-based LRP where routes are limited by maximum distance; branch-and-price with route pricing (authors from recollection; title and DOI seen).  
*→ Spaceport feeder design:* Range-limited feeder legs (vehicle energy/delta-v limits) in a hub-location-routing model.  

<a id="prins2007"></a>**[prins2007]** Prins, Prodhon, Ruiz, Soriano, Wolfler Calvo (2007). *Solving the Capacitated Location-Routing Problem by a Cooperative Lagrangean Relaxation-Granular Tabu Search Heuristic*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v41y2007i4p470-483.html)  
Capacitated LRP solved by alternating a Lagrangean relaxation for the location phase with granular tabu search for routing, exchanging information cooperatively.  
*→ Spaceport feeder design:* Location/routing decomposition heuristic reusable for spaceport-hub selection with feeder routing.  

<a id="ozsen2009"></a>**[ozsen2009]** Ozsen, Daskin, Coullard (2009). *Facility Location Modeling and Inventory Management with Multisourcing*. Transp. Sci. [link]((seen in result text of query 22 only; result quoted a variant title 'Location-Inventory Planning with Risk Pooling and Multi-Sourcing', TS 43(4):455-472))  
Capacitated location-inventory model allowing retailers to be sourced from multiple DCs; Lagrangean relaxation.  
*→ Spaceport feeder design:* Spokes allowed to feed several hubs with capacity-limited hubs.  

<a id="crainic2009"></a>**[crainic2009]** Crainic, Ricciardi, Storchi (2009). *Models for Evaluating and Planning City Logistics Systems*. Transp. Sci. [link](https://iris.uniroma1.it/handle/11573/86328)  
Two-tier city logistics: freight moves from external distribution centres to satellites by urban vehicles and then to customers by dedicated vehicles; integrated short-term scheduling of operations and resources with synchronization at satellites, formulated as time-dependent service network design (venue/pages seen on university page).  
*→ Spaceport feeder design:* Two-tier system with synchronised vehicle meetings at satellites is the closest structural analog of spoke-to-hub-to-orbit consolidation.  

<a id="klibi2010"></a>**[klibi2010]** Klibi, Lasalle, Martel, Ichoua (2010). *The Stochastic Multiperiod Location Transportation Problem*. Transp. Sci. [10.1287/trsc.1090.0307](https://doi.org/10.1287/trsc.1090.0307)  
Multiperiod depot location with stochastic demands and transportation (routing) costs; scenario-based stochastic program solved with sample average approximation and heuristics (authors from recollection; title and DOI seen).  
*→ Spaceport feeder design:* Multi-period hub opening under uncertain demand with routing costs is a network-design-under-uncertainty analog (by-catch).  

<a id="baldacci2011"></a>**[baldacci2011]** Baldacci, Mingozzi, Wolfler Calvo (2011). *An Exact Method for the Capacitated Location-Routing Problem*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v59y2011i5p1284-1296.html)  
Set-partitioning-like formulation of the CLRP with lower bounds from dynamic programming and dual ascent; exact algorithm closing many benchmark instances.  
*→ Spaceport feeder design:* Exact CLRP bounding technology for joint hub-opening and capacitated feeder-route design.  

<a id="perboli2011"></a>**[perboli2011]** Perboli, Tadei, Vigo (2011). *The Two-Echelon Capacitated Vehicle Routing Problem: Models and Math-Based Heuristics*. Transp. Sci. [10.1287/trsc.1110.0368](https://doi.org/10.1287/trsc.1110.0368)  
Defines the 2E-CVRP in which all freight must pass through intermediate satellites; gives a flow-based MIP, valid inequalities and two math-heuristics derived from the model; instances up to 50 customers and 4 satellites solved.  
*→ Spaceport feeder design:* Foundational two-echelon model: spaceports act as satellites that consolidate payload for capacitated trunk (launch) vehicles, with echelon-coupling flow constraints.  

<a id="atamturk2012"></a>**[atamturk2012]** Atamtürk, Berenguer, Shen (2012). *A Conic Integer Programming Approach to Stochastic Joint Location-Inventory Problems*. Oper. Res. [link](https://atamturk.ieor.berkeley.edu/pubs/_published/or60-2012.pdf)  
Reformulates stochastic joint location-inventory models (safety stock, risk pooling) as conic quadratic mixed-integer programs with strengthening cuts, solved by off-the-shelf solvers (venue inferred from author-page filename;).  
*→ Spaceport feeder design:* Exact conic MIP route for nonlinear hub-location-with-buffer models.  

<a id="drexl2012"></a>**[drexl2012]** Drexl (2012). *Synchronization in Vehicle Routing—A Survey of VRPs with Multiple Synchronization Constraints*. Transp. Sci. [10.1287/trsc.1110.0400](https://doi.org/10.1287/trsc.1110.0400)  
DOI left empty because the only DOI in the verified records was filled from recollection, not seen.  
*→ Spaceport feeder design:* Launch-vehicle/orbital-hub rendezvous timing (operation and movement synchronization), payload transfer between vehicles at hubs (load synchronization) and shared docking or launch-pad slots (resource synchronization) map directly onto the survey's taxonomy, and its warning about interdependence informs heuristic design for the feeder network.  

<a id="jepsen2013"></a>**[jepsen2013]** Jepsen, Spoorendonk, Ropke (2013). *A Branch-and-Cut Algorithm for the Symmetric Two-Echelon Capacitated Vehicle Routing Problem*. Transp. Sci. [10.1287/trsc.1110.0399](https://doi.org/10.1287/trsc.1110.0399)  
Edge-flow formulation of the symmetric 2E-CVRP with new valid inequalities and a branch-and-cut algorithm; solves benchmark instances to optimality (venue/pages seen on RePEc; DOI from result text).  
*→ Spaceport feeder design:* Exact cutting-plane machinery for two-level consolidation networks where spoke demand is aggregated at satellites before trunk transport.  

<a id="masson2013"></a>**[masson2013]** Masson, Lehuédé, Péton (2013). *An Adaptive Large Neighborhood Search for the Pickup and Delivery Problem with Transfers*. Transp. Sci. [10.1287/trsc.1120.0432](https://doi.org/10.1287/trsc.1120.0432)  
PDP with transfers at specified transfer points; new insertion heuristics that insert a request through a transfer point embedded in ALNS; gains up to 9% on generated and disabled-persons transport instances.  
*→ Spaceport feeder design:* Request transfer between vehicles at transfer points with timing feasibility is the operational core of payload hand-over at hubs.  

<a id="baldacci2013"></a>**[baldacci2013]** Baldacci, Mingozzi, Roberti, Wolfler Calvo (2013). *An Exact Algorithm for the Two-Echelon Capacitated Vehicle Routing Problem*. Oper. Res. [10.1287/opre.1120.1153](https://doi.org/10.1287/opre.1120.1153)  
Decomposes the 2E-CVRP into a limited set of multi-depot CVRPs with side constraints; set-partitioning based bounding (dual ascent, column-and-cut generation) and an exact algorithm solving instances with up to 100 customers.  
*→ Spaceport feeder design:* Shows how a two-level feeder/trunk design decomposes into satellite-assignment plus multi-depot routing subproblems, a template for spoke-to-hub assignment with trunk capacity.  

<a id="cherkesly2015"></a>**[cherkesly2015]** Cherkesly, Desaulniers, Laporte (2015). *Branch-Price-and-Cut Algorithms for the Pickup and Delivery Problem with Time Windows and Last-in-First-Out Loading*. Transp. Sci. [link]((seen in result text of query 24 only))  
PDPTW with LIFO loading constraints; three branch-price-and-cut algorithms differing in how LIFO is handled in pricing.  
*→ Spaceport feeder design:* Loading-order constraints inside capacitated vehicles map to payload stacking constraints in launch vehicles (by-catch).  

<a id="ghilas2016"></a>**[ghilas2016]** Ghilas, Demir, Van Woensel (2016). *A scenario-based planning for the pickup and delivery problem with time windows, scheduled lines and stochastic demands*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v91y2016icp34-51.html)  
Two-stage stochastic PDPTW with scheduled lines; scenario-based sample average approximation with ALNS; shows value of integrating scheduled public-transport lines under demand uncertainty.  
*→ Spaceport feeder design:* Uncertain feeder demand against fixed scheduled-line (launch) capacity solved by scenario-based planning.  

<a id="crainic2016"></a>**[crainic2016]** Crainic, Errico, Rei, Ricciardi (2016). *Modeling Demand Uncertainty in Two-Tier City Logistics Tactical Planning*. Transp. Sci. [10.1287/trsc.2015.0606](https://doi.org/10.1287/trsc.2015.0606)  
Tactical plan of a two-tier city logistics system under uncertain forecast demand as a two-stage stochastic program over the time-dependent service network; analysis of flexibility in managing resources and consolidation benefits.  
*→ Spaceport feeder design:* Two-tier consolidation design under demand uncertainty with recourse is directly analogous to planning hub launches against uncertain payload demand.  

<a id="xie2016"></a>**[xie2016]** Xie, Ouyang, Wong (2016). *Reliable Location-Routing Design Under Probabilistic Facility Disruptions*. Transp. Sci. [10.1287/trsc.2015.0630](https://doi.org/10.1287/trsc.2015.0630)  
*→ Spaceport feeder design:* Orbital hubs/depots that may be unavailable (phasing windows, outages) with spoke spaceports re-assigned to surviving hubs is the same reliable location-routing structure.  

<a id="gianessi2016"></a>**[gianessi2016]** Gianessi, Alfandari, Létocart, Wolfler Calvo (2016). *The Multicommodity-Ring Location Routing Problem*. Transp. Sci. [10.1287/trsc.2015.0600](https://doi.org/10.1287/trsc.2015.0600)  
Locates urban distribution centres on a ring served by a circular trunk line and routes multicommodity flows from/to customers; MIP with valid inequalities and branch-and-cut (authors from recollection; title and DOI seen).  
*→ Spaceport feeder design:* Ring-trunk plus feeder routing is structurally similar to an orbital ring of hubs fed from ground spokes.  

<a id="bodnar2017"></a>**[bodnar2017]** Bodnar, de Koster, Azadeh (2017). *Scheduling Trucks in a Cross-Dock with Mixed Service Mode Dock Doors*. Transp. Sci. [link](https://repub.eur.nl/pub/98963)  
Inbound/outbound truck scheduling with time windows at a multi-door cross-dock where doors can serve both modes; mathematical model and ALNS for real-size instances (TS 51(1):112-131 from repository page).  
*→ Spaceport feeder design:* Hub cross-dock scheduling of inbound feeders and outbound trunks with shared doors transfers to launch-pad / docking-slot assignment at orbital hubs.  

<a id="schiffer2018"></a>**[schiffer2018]** Schiffer, Walther (2018). *An Adaptive Large Neighborhood Search for the Location-Routing Problem with Intra-Route Facilities*. Transp. Sci. [10.1287/trsc.2017.0746](https://doi.org/10.1287/trsc.2017.0746)  
LRP in which intermediate facilities (e.g., charging/replenishment) are located and visited within routes; ALNS with facility-insertion operators (DOI from result text; university record).  
*→ both problems:* Locating intermediate refuel/recharge facilities within routes applies to electric regional aircraft (A) and to staging facilities for reusable launch vehicles (B).  

<a id="ghilas2018"></a>**[ghilas2018]** Ghilas, Cordeau, Demir, Van Woensel (2018). *Branch-and-Price for the Pickup and Delivery Problem with Time Windows and Scheduled Lines*. Transp. Sci. [10.1287/trsc.2017.0798](https://doi.org/10.1287/trsc.2017.0798)  
PDPTW-SL: requests may be routed partly on fixed-timetable, capacitated scheduled lines with transfers at stations; exact branch-and-price with pricing over vehicle routes coordinated with timetable departures.  
*→ Spaceport feeder design:* Feeders delivering to fixed-timetable capacitated trunk departures is a direct analog of spaceport feeders meeting scheduled launch slots.  

<a id="li2018"></a>**[li2018]** Li, Liu, Jian, Lu (2018). *The two-echelon distribution system considering the real-time transshipment capacity varying*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v110y2018icp239-260.html)  
Two-echelon distribution with satellites acting as cross-docks whose transshipment capacity varies in real time; MIP and heuristic (authors from recollection; venue/pages from RePEc URL, topic from result text).  
*→ Spaceport feeder design:* Time-varying transshipment capacity at satellites models launch-window-dependent hub throughput.  

<a id="marques2022"></a>**[marques2022]** Marques, Sadykov, Deschamps, Dupas (2022). *A Branch-Cut-and-Price Approach for the Single-Trip and Multi-Trip Two-Echelon Vehicle Routing Problem with Time Windows*. Transp. Sci. [10.1287/trsc.2022.1136](https://doi.org/10.1287/trsc.2022.1136)  
Exact branch-cut-and-price for 2E-CVRPTW with satellites, covering single-trip and multi-trip second-echelon variants and precedence constraints for unloading/loading freight at satellites.  
*→ Spaceport feeder design:* Multi-trip second echelon with unload/load precedence maps to reusable launch vehicles making repeated sorties with turnaround ordering at hubs.  

<a id="mhamedi2022"></a>**[mhamedi2022]** Mhamedi, Andersson, Cherkesly, Desaulniers (2022). *A Branch-Price-and-Cut Algorithm for the Two-Echelon Vehicle Routing Problem with Time Windows*. Transp. Sci. [10.1287/trsc.2021.1092](https://doi.org/10.1287/trsc.2021.1092)  
2E-VRPTW in city logistics: high-capacity vehicles depot->satellites, low-capacity vehicles satellites->customers with time windows; exact branch-price-and-cut with route-based pricing for both echelons and synchronization at satellites (authors from recollection; title, venue and DOI seen).  
*→ Spaceport feeder design:* Time-windowed echelon coupling at satellites is the analog of launch-window coupling between spoke feeders and hub launches.  

<a id="sluijk2023"></a>**[sluijk2023]** Sluijk, Florio, Kinable, Dellaert, Van Woensel (2023). *A Chance-Constrained Two-Echelon Vehicle Routing Problem with Stochastic Demands*. Transp. Sci. [10.1287/trsc.2022.1162](https://doi.org/10.1287/trsc.2022.1162)  
Two-echelon VRP with stochastic customer demands handled through chance constraints on vehicle/satellite capacity; exact-oriented solution approach.  
*→ Spaceport feeder design:* Chance-constrained capacity at satellites and trunk vehicles mirrors probabilistic payload demand against fixed launch capacity.  

### Network design under uncertainty (6 papers)

<a id="snyder2005"></a>**[snyder2005]** Snyder, Daskin (2005). *Reliability Models for Facility Location: The Expected Failure Cost Case*. Transp. Sci. [10.1287/trsc.1040.0107](https://doi.org/10.1287/trsc.1040.0107)  
Extends the P-median and uncapacitated fixed-charge location problems so that facilities fail with a common probability and each customer is assigned to an ordered list of backup facilities; the objective weights nominal transportation cost against expected post-failure cost. Solved by Lagrangian relaxation; trade-off curves show large reliability gains for small increases in nominal cost.  
*→ Spaceport feeder design:* Orbital hubs/depots that are intermittently unavailable (phasing windows, outages) map directly onto failure-prone facilities with backup-assignment levels for each spaceport.  

<a id="atamturk2007"></a>**[atamturk2007]** Atamturk, Zhang (2007). *Two-Stage Robust Network Flow and Design Under Demand Uncertainty*. Oper. Res. [10.1287/opre.1070.0428](https://doi.org/10.1287/opre.1070.0428)  
Two-stage robust network flow/design in which part of the flow decisions are deferred until demand (in a budgeted polyhedral uncertainty set) is realized. Characterizes first-stage robust decisions by exponentially many constraints, proves the separation problem NP-hard in general but tractable for totally ordered or arborescence second-stage topologies, and derives a probability bound on infeasibility; applications to lot-sizing and location-transportation.  
*→ both problems:* Gives the adjustable-robust template for committing hub/launch capacity before manifests are known and re-routing payload flows afterwards; the same recourse structure applies to flow assignment under uncertain capacity in air traffic flow management.  

<a id="lium2009"></a>**[lium2009]** Lium, Crainic, Wallace (2009). *A Study of Demand Stochasticity in Service Network Design*. Transp. Sci. [10.1287/trsc.1090.0265](https://doi.org/10.1287/trsc.1090.0265)  
Two-stage stochastic service network design on a time-space network with scenario-based demand. Compares stochastic designs with deterministic expected-value designs and shows that stochastic solutions rely on consolidation and hub-like, correlated path structures as a hedge against demand uncertainty (Transportation Science 43(2):144-157).  
*→ Spaceport feeder design:* Shows why a hub-consolidation feeder design is structurally more robust than point-to-point service when payload demand is uncertain, motivating the spaceport-to-orbital-hub architecture (  

<a id="cui2010"></a>**[cui2010]** Cui, Ouyang, Shen (2010). *Reliable Facility Location Design Under the Risk of Disruptions*. Oper. Res. [10.1287/opre.1090.0801](https://doi.org/10.1287/opre.1090.0801)  
Reliable uncapacitated fixed-charge location with site-dependent failure probabilities and customer reassignment. Proposes a compact MIP solved by Lagrangian relaxation and a continuum-approximation model as a fast near-optimal heuristic; both minimize set-up plus expected transportation cost over normal and failure scenarios.  
*→ Spaceport feeder design:* Site-dependent hub availability (different orbits/stations have different access probabilities) and the continuum approximation give a fast way to size a sparse set of orbital hubs serving many spaceports.  

<a id="peng2011"></a>**[peng2011]** Peng, Snyder, Lim, Liu (2011). *Reliable logistics networks design with facility disruptions*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v45y2011i8p1190-1211.html)  
Multi-echelon logistics network design under facility-disruption scenarios using the p-robustness criterion (bounded relative regret in every scenario) while minimizing nominal cost; MIP solved by a hybrid metaheuristic combining a genetic algorithm, local improvement and the shortest augmenting path method, outperforming CPLEX; shows reliability can be bought cheaply.  
*→ Spaceport feeder design:* p-robustness bounds the worst-scenario regret of a spaceport-to-hub feeder design when a hub or launch site is lost, a natural criterion for strategic launch infrastructure.  

<a id="bai2014"></a>**[bai2014]** Bai, Wallace, Li, Chong (2014). *Stochastic service network design with rerouting*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v60y2014icp50-65.html)  
Two-stage stochastic SND on a time-space network: first-stage service/vehicle design, second-stage integer recourse that reroutes vehicles (not just flows) once demand scenarios are revealed; scenario-based stochastic MIP, with results showing rerouting recourse lowers expected cost versus flow-only recourse and deterministic designs.  
*→ Spaceport feeder design:* Uncertain payload demand with the option to re-task launch vehicles after demand is revealed is precisely integer vehicle-rerouting recourse; the model shows how to value that flexibility in feeder design.  

### Time-window/periodic/launch scheduling (20 papers)

<a id="freeman1966"></a>**[freeman1966]** Freeman, Gogerty, Graves, Brooks (1966). *A Mathematical Model of Supply Support for Space Operations*. Oper. Res. [10.1287/opre.14.1.1](https://doi.org/10.1287/opre.14.1.1)  
Given a time-phased schedule of requirements at a space base (illustrated with a long-term lunar base), the model chooses the sequence of resupply trips, the launch date of each trip and the cargo composition of each trip so that all requirements are met over the horizon. Formulated as a nonlinear discrete programming (scheduling) problem; developed at RAND for evaluating logistics supply support of space bases.  
*→ Spaceport feeder design:* Earliest OR formulation of the spoke-to-hub launch manifest problem: capacitated trips with chosen dates and cargo mixes serving time-phased demand at an orbital/lunar hub.  

<a id="chamberlain1970"></a>**[chamberlain1970]** Chamberlain, Kingsland (1970). *A Methodology to Compare Policies for Exploring the Solar System*. Oper. Res. [10.1287/opre.18.4.593](https://doi.org/10.1287/opre.18.4.593)  
JPL methodology for quantitatively comparing alternative long-range policies (mission sequences) for exploring the solar system; part of the OR 18(4) August 1970 'Space Applications' special section.  
*→ Spaceport feeder design:* Campaign-level comparison of mission sequences is the strategic layer above spaceport-to-orbit network design (which hubs/destinations to serve, in what order).  

<a id="freeman1970"></a>**[freeman1970]** Freeman, Moore, Schilling (1970). *A Program of Astronomy Research on the Moon and its Logistics Implications*. Oper. Res. [10.1287/opre.18.4.612](https://doi.org/10.1287/opre.18.4.612)  
A mathematical logistics model analyses the implications of a post-Apollo lunar astronomy programme culminating in a lunar observatory; many interrelated input parameters are varied parametrically to measure sensitivity, and the programme is shown feasible within the constraints of planned spacecraft, boosters and launching facilities. Permits quantitative logistical comparison of alternative space missions.  
*→ Spaceport feeder design:* Treats boosters and launch facilities as the binding capacity for a multi-year lunar supply programme, i.e. the capacity side of a spaceport-to-orbit feeder network.  

<a id="waespy1970"></a>**[waespy1970]** Waespy (1970). *Linear-Programming Solutions for Orbital-Transfer Trajectories*. Oper. Res. [10.1287/opre.18.4.635](https://doi.org/10.1287/opre.18.4.635)  
Applies linear programming to compute orbital-transfer trajectories (impulsive manoeuvre schedules) between orbits; part of the OR 18(4) 1970 'Space Applications' section.  
*→ Spaceport feeder design:* Gives the arc-cost (delta-v / propellant) model for transfers between orbital hubs that a feeder network design would take as input.  

<a id="elbardai1970"></a>**[elbardai1970]** El-Bardai (1970). *Queuing Analysis of Satellite Networks*. Oper. Res. [10.1287/opre.18.4.654](https://doi.org/10.1287/opre.18.4.654)  
Models satellite communication systems as bipartite graphs with stochastic inputs and analyses them as queueing networks, taking time delay as the performance measure.  
*→ Spaceport feeder design:* Queueing-based delay at satellite (hub) nodes is the stochastic-congestion analogue for orbital-hub transfer capacity in a feeder network.  

<a id="fisher1978"></a>**[fisher1978]** Fisher, Jaikumar (1978). *An Algorithm for the Space-Shuttle Scheduling Problem*. Oper. Res. [10.1287/opre.26.1.166](https://doi.org/10.1287/opre.26.1.166)  
Models NASA shuttle mission scheduling as selecting launch times for a set of missions to minimize the number of missions flown late, subject to earliest-start (release) times and resource constraints on orbiters and ground facilities. Proposes a simple, low-computation algorithm that is optimal under restrictive assumptions and otherwise a strong heuristic.  
*→ Spaceport feeder design:* Archetypal launch-window / pad-and-vehicle-capacity scheduling model: payload missions compete for scarce reusable-vehicle and facility resources with earliest and latest launch times.  

<a id="odijk1996"></a>**[odijk1996]** Odijk (1996). *A constraint generation algorithm for the construction of periodic railway timetables*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v30y1996i6p455-464.html)  
Formulates periodic timetabling with periodic time-window constraints relating event times pairwise on a clock (PESP-type model); shows NP-completeness and solves it with a constraint generation algorithm that performs well on modest, non-trivial instances for railway performance analysis.  
*→ Spaceport feeder design:* Recurring launch windows set by orbital phasing are naturally modeled as periodic time-window constraints on a clock, exactly the PESP structure solved here.  

<a id="imai2001"></a>**[imai2001]** Imai, Nishimura, Papadimitriou (2001). *The dynamic berth allocation problem for a container port*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v35y2001i4p401-417.html)  
Assigns and sequences ships with known arrival times to a limited set of berths (dynamic arrivals) to minimize total waiting and handling time; formulated as an integer program and solved by a Lagrangian relaxation based heuristic.  
*→ Spaceport feeder design:* Launch pads and hub docking ports are berths: vehicles arrive in windows and must be sequenced on scarce shared capacity.  

<a id="kroon2003"></a>**[kroon2003]** Kroon, Peeters (2003). *A Variable Trip Time Model for Cyclic Railway Timetabling*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v37y2003i2p198-212.html)  
Extends the PESP-based cyclic timetabling model so that trip times are decision variables within intervals rather than fixed inputs; formulated as a mixed-integer program on the periodic event graph and tested on Dutch railway instances.  
*→ Spaceport feeder design:* Ascent, phasing and transfer durations to an orbital hub vary within bounds; this model shows how to keep such durations as variables inside a periodic schedule.  

<a id="imai2003"></a>**[imai2003]** Imai, Nishimura, Papadimitriou (2003). *Berth allocation with service priority*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v37y2003i5p437-457.html)  
Extends dynamic berth allocation with ship-specific service priorities (weighted waiting), formulated as a nonlinear integer program and solved with a genetic-algorithm based heuristic.  
*→ Spaceport feeder design:* Priority classes (crewed vs cargo, time-critical payloads) at shared pads or hub ports map to weighted-priority berth allocation.  

<a id="imai2005"></a>**[imai2005]** Imai, Sun, Nishimura, Papadimitriou (2005). *Berth allocation in a container port: using a continuous location space approach*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v39y2005i3p199-221.html)  
Treats the quay as a continuous resource rather than discrete berths so vessels can be placed anywhere; proposes a heuristic that builds continuous solutions from discrete-berth solutions and compares utilization.  
*→ Spaceport feeder design:* Hub capacity (mass, volume, docking length) treated as a continuous resource over time is a two-dimensional time-space packing of the same kind.  

<a id="cordeau2005"></a>**[cordeau2005]** Cordeau, Laporte, Legato, Moccia (2005). *Models and Tabu Search Heuristics for the Berth-Allocation Problem*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v39y2005i4p526-538.html)  
Formulates discrete and continuous berth allocation as a multi-depot vehicle routing problem with time windows (ships as customers, berths as depots/vehicles) and solves it with tabu search; developed for the port of Gioia Tauro.  
*→ Spaceport feeder design:* Shows how a time-windowed shared-resource scheduling problem can be recast as routing with time windows, a modeling route for pad/hub slot assignment.  

<a id="wong2008"></a>**[wong2008]** Wong, Yuen, Fung, Leung (2008). *Optimizing Timetable Synchronization for Rail Mass Transit*. Transp. Sci. [10.1287/trsc.1070.0200](https://doi.org/10.1287/trsc.1070.0200)  
Non-periodic mixed-integer program over a multi-line rail transit network that chooses run times, dwell times, headways and dispatch offsets for all trains to minimise total passenger transfer waiting time subject to safety headways and operational ranges. Solved by an optimisation-based heuristic that iteratively fixes and re-optimises integer variables with a commercial MIP solver; demonstrated on Hong Kong MTR data with substantial transfer-wait reductions.  

<a id="liebchen2008"></a>**[liebchen2008]** Liebchen (2008). *The First Optimized Railway Timetable in Practice*. Transp. Sci. [10.1287/trsc.1080.0240](https://doi.org/10.1287/trsc.1080.0240)  
Reports the PESP-based periodic timetable implemented on the Berlin Underground; uses a cycle-based integer programming formulation of PESP with integral cycle bases and a linear objective, solved by MIP, and documents measured operational benefits.  
*→ Spaceport feeder design:* Demonstrates that periodic MIP scheduling of shared infrastructure scales to practice, a template for recurring launch cadences across spaceports.  

<a id="meisel2013"></a>**[meisel2013]** Meisel, Bierwirth (2013). *A Framework for Integrated Berth Allocation and Crane Operations Planning in Seaport Container Terminals*. Transp. Sci. [link](https://prodlog.wiwi.uni-halle.de/team/ehemalige_mitarbeiter/meisel)  
Integrates berth allocation, quay crane assignment and crane scheduling through a hierarchical framework with feedback between stages, using problem-specific formulations and heuristics and quantifying the benefit of integration.  
*→ Spaceport feeder design:* Integrating pad slot assignment with ground-handling resources (integration, fueling crews) mirrors berth plus crane planning with feedback.  

<a id="kroon2014"></a>**[kroon2014]** Kroon, Peeters, Wagenaar, Zuidwijk (2014). *Flexible connections in PESP models for cyclic passenger railway timetabling*. Transp. Sci. [link](https://repub.eur.nl/pub/76844)  
Adds binary choice to PESP so the model decides which trains connect for rolling-stock and passenger connections instead of fixing pairings a priori; MIP formulation evaluated on Netherlands Railways cases.  
*→ Spaceport feeder design:* Choosing which feeder launch meets which orbital-hub departure (rendezvous pairing) is the same flexible-connection decision embedded in a periodic schedule.  

<a id="sparing2017"></a>**[sparing2017]** Sparing, Goverde (2017). *A cycle time optimization model for generating stable periodic railway timetables*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v98y2017icp198-223.html)  
Uses the minimum cycle time of a periodic timetable as a stability indicator and formulates a periodic timetabling optimization (MILP on an event-activity network) that minimizes this cycle time for heterogeneous networks; demonstrated on the central Dutch network.  
*→ Spaceport feeder design:* Gives a way to size the feasible cadence and buffer of a recurring launch schedule on shared pads and hub docking slots.  

<a id="zhang2017"></a>**[zhang2017]** Zhang, Klabjan (2017). *Optimization for gate re-assignment*. Transp. Res. B. [10.1016/j.trb.2016.11.006](https://doi.org/10.1016/j.trb.2016.11.006)  
MIP for re-assigning flights to gates after disruptions, minimizing weighted flight delay, number of re-assignments and missed passenger connections; two heuristics deliver high-quality solutions quickly on a large US carrier's data.  
*→ Spaceport feeder design:* Re-assigning launches to pads or docking slots after a scrub while protecting payload connections at the hub is the same recovery structure.  

<a id="polinder2019"></a>**[polinder2019]** Polinder, Breugem, Dollevoet, Maróti (2019). *An adjustable robust optimization approach for periodic timetabling*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v128y2019icp50-68.html)  
Defines the Robust Periodic Timetabling Problem, a PESP whose timetable can be adjusted after small periodic disturbances; solves it with adjustable robust optimization using linear decision rules, robust reformulations and cutting planes on Netherlands Railways instances, showing the efficiency-robustness trade-off.  
*→ Spaceport feeder design:* Launch windows suffer recurring small disturbances (weather holds, range conflicts); this gives a periodic schedule with built-in recourse.  

<a id="agra2022"></a>**[agra2022]** Agra, Rodrigues (2022). *Distributionally robust optimization for the berth allocation problem under uncertainty*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v164y2022icp1-24.html)  
Berth allocation with uncertain vessel arrival and handling times formulated as a distributionally robust model over an ambiguity set, with a decomposition algorithm and comparison against stochastic and robust counterparts.  
*→ Spaceport feeder design:* Launch delays and uncertain turnaround at shared pads or hub ports can be handled with the same ambiguity-set approach to time-windowed resource scheduling.  

### Transit feeder design (19 papers)

<a id="hurdle1973"></a>**[hurdle1973]** Hurdle (1973). *Minimum Cost Locations for Parallel Public Transit Lines*. Transp. Sci. [10.1287/trsc.7.4.340](https://doi.org/10.1287/trsc.7.4.340)  
Early continuous-approximation treatment of transit line spacing and headways minimising operating plus user access/wait cost under spatially varying demand;  
*→ Spaceport feeder design:* Foundational analytical sizing of parallel feeder lines, the ancestor of CA trunk-feeder design used for spoke density.  

<a id="wirasinghe1977"></a>**[wirasinghe1977]** Wirasinghe, Hurdle, Newell (1977). *Optimal Parameters for a Coordinated Rail and Bus Transit System*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v11y1977i4p359-374.html)  
Analytical model of peak CBD-bound trips where each locality is served either by direct bus or by feeder bus to a rail station; optimal rail station spacing, feeder headways and the direct/feeder boundary minimise operating plus passenger time cost.  
*→ Spaceport feeder design:* Classic trunk-feeder trade-off between direct service and feeding a trunk hub, with analytic hub spacing; transfers to direct-to-orbit vs hub-routed launches.  

<a id="hall1985"></a>**[hall1985]** Hall (1985). *Vehicle Scheduling at a Transportation Terminal with Random Delay en Route*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v19y1985i3p308-320.html)  
Analytical model of timed transfers at a terminal where feeder vehicles arrive with random (exponential) delay; derives optimal slack between scheduled feeder arrival and connecting departure as a function of mean delay and connecting headway.  
*→ both problems:* Optimal slack for feeder-to-trunk connections under random delay is the exact question for launch-window buffers at an orbital hub; also informs schedule buffers in ATFM.  

<a id="chang1991"></a>**[chang1991]** Chang, Schonfeld (1991). *Multiple period optimization of bus transit systems*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v25y1991i6p453-478.html)  
*→ Spaceport feeder design:* Multi-period joint sizing of feeder zones and fleet under a common vehicle pool mirrors launch-fleet sizing across demand seasons.  

<a id="chang1991a"></a>**[chang1991a]** Chang, Schonfeld (1991). *Optimization Models for Comparing Conventional and Subscription Bus Feeder Services*. Transp. Sci. [10.1287/trsc.25.4.281](https://doi.org/10.1287/trsc.25.4.281)  
Analytic models for fixed-route conventional and flexible-route subscription bus feeders to a single terminal; vehicle size and zone size optimised in closed form; average cost per trip decides which policy is preferable under demand density, speed and cost parameters.  
*→ Spaceport feeder design:* Closed-form comparison of scheduled vs subscription feeder policy by demand density transfers to choosing scheduled vs chartered launches per spaceport.  

<a id="wang2004"></a>**[wang2004]** Wang, Yang, Lindsey (2004). *Locating and pricing park-and-ride facilities in a linear monocentric city with deterministic mode choice*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v38y2004i8p709-731.html)  
Analytical model of P&R facility location and parking charge in a linear city with uniformly distributed residents; characterises deterministic mode-choice equilibria and compares profit-maximising and social-cost-minimising location/pricing.  
*→ Spaceport feeder design:* Access-node location with user equilibrium between direct and transfer modes informs spaceport siting and access pricing.  

<a id="quadrifoglio2006"></a>**[quadrifoglio2006]** Quadrifoglio, Hall, Dessouky (2006). *Performance and Design of Mobility Allowance Shuttle Transit Services: Bounds on the Maximum Longitudinal Velocity*. Transp. Sci. [10.1287/trsc.1050.0137](https://doi.org/10.1287/trsc.1050.0137)  
Analytical bounds on the longitudinal velocity of a hybrid fixed/flexible (MAST) shuttle that deviates from a base route to serve demand-responsive requests; used to set service capacity and slack in the fixed schedule.  
*→ Spaceport feeder design:* Analytical capacity envelope for a feeder that mixes scheduled and on-demand stops, analogous to launch vehicles with fixed hub appointments plus flexible pickup.  

<a id="daganzo2010"></a>**[daganzo2010]** Daganzo (2010). *Structure of Competitive Transit Networks*. Transp. Res. B. [10.1016/j.trb.2009.11.001](https://doi.org/10.1016/j.trb.2009.11.001)  
Continuous-approximation (CA) model of a square service region with uniform demand; a parametric family of networks spanning grid to hub-and-spoke is optimised analytically over line spacing, stop spacing and headway for agency plus user cost. Shows that the costlier the infrastructure, the more the optimal design tilts toward hub-and-spoke.  
*→ Spaceport feeder design:* Closed-form sizing of a hub-and-spoke feeder structure as a function of infrastructure cost directly transfers to deciding how many spaceport spokes should feed each orbital hub.  

<a id="badia2014"></a>**[badia2014]** Badia, Estrada, Robusté (2014). *Competitive transit network design in cities with radial street patterns*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v59y2014icp161-181.html)  
Reformulates Daganzo's (2010) hybrid CA model for radial cities: radial/circular lines in the core and hub-and-spoke in the periphery; analytical minimisation of agency plus user cost over central-area size, headway, line and stop spacing.  
*→ Spaceport feeder design:* Explicit hub-and-spoke periphery with optimised hub-zone radius is a template for sizing orbital-hub catchments.  

<a id="ouyang2014"></a>**[ouyang2014]** Ouyang, Nourbakhsh, Cassidy (2014). *Continuum approximation approach to bus network design under spatially heterogeneous demand*. Transp. Res. B. [10.1016/j.trb.2014.05.018](https://doi.org/10.1016/j.trb.2014.05.018)  
CA framework for a city-wide main grid plus nested local grids with closer spacing in high-demand neighbourhoods; a power-of-two spacing rule (from inventory theory) makes local grids nest seamlessly. Up to 8% cost savings over homogeneous grids.  
*→ Spaceport feeder design:* Hierarchical nesting of dense local feeders within a sparse main network under heterogeneous demand maps to tiered spaceport catchments feeding hubs.  

<a id="kim2014"></a>**[kim2014]** Kim, Schonfeld (2014). *Integration of conventional and flexible bus services with timed transfers*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v68y2014icp76-97.html)  
Analytical cost models for conventional and flexible-route bus zones feeding a terminal with timed transfers; integrated design (zone sizes, headways, vehicle sizes, mode per zone/period) solved with a genetic algorithm under time- and space-varying demand.  
*→ Spaceport feeder design:* Jointly choosing scheduled vs on-demand feeder service per zone and coordinating arrivals at a hub by timed transfers is the spaceport-to-hub feeder decision.  

<a id="ibarrarojas2015"></a>**[ibarrarojas2015]** Ibarra-Rojas, Delgado, Giesen, Muñoz (2015). *Planning, operation, and control of bus transport systems: A literature review*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v77y2015icp38-75.html)  
Review of the transit network planning hierarchy (network design, frequency setting, timetabling incl. synchronization, vehicle and crew scheduling) and real-time control, with the integration between stages as the organising theme.  
*→ Spaceport feeder design:* Provides the strategic-tactical-operational decomposition (design, frequency, timetable, fleet assignment) that a spaceport feeder network planning framework can mirror.  

<a id="fielbaum2016"></a>**[fielbaum2016]** Fielbaum, Jara-Díaz, Gschwender (2016). *Optimal public transport networks for a general urban structure*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v94y2016icp298-313.html)  
Parametric city model used to compare four strategic line structures (direct, exclusive, hub-and-spoke, feeder-trunk) via microeconomic agency plus user cost; identifies which structure wins as a function of centralisation, patronage and transfer penalty.  
*→ Spaceport feeder design:* Directly characterises when feeder-trunk/hub-and-spoke beats direct service as demand and transfer penalty vary; core analog for spaceport-hub structure choice.  

<a id="chen2017a"></a>**[chen2017a]** Chen, Nie (2017). *Analysis of an idealized system of demand adaptive paired-line hybrid transit*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v102y2017icp38-54.html)  
Hybrid system pairing each fixed-route line with a demand-adaptive feeder operated at a stable headway covering the line's stops; coupled design minimising agency plus user cost formulated as a MIP solved with a metaheuristic.  
*→ Spaceport feeder design:* Feeder dispatched on intervals coordinated with the trunk line is the synchronised feeder-launch concept; MIP structure transfers.  

<a id="fonseca2018"></a>**[fonseca2018]** Fonseca, van der Hurk, Roberti, Larsen (2018). *A matheuristic for transfer synchronization through integrated timetabling and vehicle scheduling*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v109y2018icp128-149.html)  
Integrated timetabling and vehicle scheduling to minimise transfer costs plus operating costs; MIP with a matheuristic (fix-and-optimise style) tested on real networks. Authors from recall; title, venue and pages corroborated by the IDEAS record.  
*→ Spaceport feeder design:* Integrating transfer synchronisation with vehicle (launcher) circulation is the integrated timetable-plus-asset problem for feeder launches meeting hub departures.  

<a id="steiner2018"></a>**[steiner2018]** Steiner, Irnich (2018). *Schedule-Based Integrated Intercity Bus Line Planning via Branch-and-Cut*. Transp. Sci. [10.1287/trsc.2017.0763](https://doi.org/10.1287/trsc.2017.0763)  
Schedule-based (timetabled service) line planning for intercity buses integrating station location, service times and time-dependent demand on a given corridor; MIP solved by branch-and-cut; shows results differ markedly from frequency-based planning.  
*→ Spaceport feeder design:* Low-frequency timetabled services where customers choose specific departures mirror launch-slot choice; integrated stop (spaceport) selection and timing with exact B&C.  

<a id="pinto2020"></a>**[pinto2020]** Pinto, Hyland, Mahmassani, Verbas (2020). *Joint design of multimodal transit networks and shared autonomous mobility fleets*. Transp. Res. C. [10.1016/j.trc.2019.06.010](https://doi.org/10.1016/j.trc.2019.06.010)  
Bi-level design allocating resources between fixed transit and shared autonomous vehicle fleets as first/last-mile feeders in a large metro area; agent-based evaluation shows reduced traveller wait times versus the base network. DOI from UCI ITS page.  
*→ Spaceport feeder design:* Joint design of trunk network and feeder fleet size is the two-tier spaceport-hub resource allocation problem.  

<a id="bertsimas2021"></a>**[bertsimas2021]** Bertsimas, Ng, Yan (2021). *Data-Driven Transit Network Design at Scale*. Oper. Res. [10.1287/opre.2020.2057](https://doi.org/10.1287/opre.2020.2057)  
Holistic transit network design (routes and frequencies) as a large-scale optimisation solved by column generation that scales to hundreds of stops; demonstrated on Boston data.  
*→ Spaceport feeder design:* Column-generation machinery for simultaneous route and frequency design transfers to generating feeder routes/cadences over many spaceports.  

<a id="trb-bus2023"></a>**[trb-bus2023]** (authors not captured) (2023). *The bus synchronization timetabling problem with dwelling times*. Transp. Res. B. [link](https://www.sciencedirect.com/science/article/pii/s0191261523000905)  
Timetabling to maximise synchronised arrivals at transfer nodes while modelling dwell times; TR-B 174 (2023). From result listing only.  
*→ Spaceport feeder design:* Recent synchronization IP variant; adds dwell (turnaround) time, which is the pad/docking occupancy in a hub-feeder launch schedule.  

### Emerging-tech network design (17 papers)

<a id="berman1992"></a>**[berman1992]** Berman, Larson, Fouska (1992). *Optimal Location of Discretionary Service Facilities*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v26y1992i3p201-211.html)  
Classic flow-interception model: demand is origin-destination vehicle flow on a network, and m facilities are located on paths to intercept maximum flow; also finds the minimum number of facilities to capture a target fraction of flow. Foundation of flow-capturing and flow-refuelling location models (TS 26(3):201-211).  
*→ Spaceport feeder design:* Path-flow-based facility location is the root of refuelling/charging-hub location used as the capacity-hub analog for spaceport feeder design.  

<a id="berman1995"></a>**[berman1995]** Berman, Bertsimas, Larson (1995). *Locating Discretionary Service Facilities, II: Maximizing Market Size, Minimizing Inconvenience*. Oper. Res. [10.1287/opre.43.4.623](https://doi.org/10.1287/opre.43.4.623)  
Extends flow-interception location to allow customers to deviate from preplanned paths at a cost; models market size versus inconvenience trade-off and gives formulations and approximation algorithms (OR 43(4):623-632).  
*→ Spaceport feeder design:* Deviation-tolerant interception models underlie later range-limited refuelling and charging-hub location, the hub-with-capacity analog for feeder networks.  

<a id="arslan2018"></a>**[arslan2018]** Arslan, Karaşan, Mahjoub, Yaman (unverified) (2018). *A Branch-and-Cut Algorithm for the Alternative Fuel Refueling Station Location Problem with Routing*. Transp. Sci. [10.1287/trsc.2018.0869](https://doi.org/10.1287/trsc.2018.0869)  
Locates refuelling stations for range-limited vehicles while allowing drivers to deviate from shortest paths (routing); branch-and-cut on a natural formulation with path/range feasibility cuts. From URL/title only; DOI in the 2018 series (likely published 2019).  
*→ Spaceport feeder design:* Locating replenishment nodes so that range-limited vehicles can complete paths is the terrestrial analog of placing staging/refuelling hubs along spoke-to-orbit chains.  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="agatz2018"></a>**[agatz2018]** Agatz, Bouman, Schmidt (2018). *Optimization Approaches for the Traveling Salesman Problem with Drone*. Transp. Sci. [10.1287/trsc.2017.0791](https://doi.org/10.1287/trsc.2017.0791)  
Introduces the TSP with Drone (TSP-D): a truck and a drone jointly serve customers, the drone launching from and returning to the truck under a flight-range limit. MIP formulation plus route-first, cluster-second heuristics based on local search and dynamic programming; shows substantial savings over truck-only delivery.  
*→ Spaceport feeder design:* Fast range-limited vehicle synchronized with a slower high-capacity carrier is the structural analog of launch vehicles with limited windows feeding from ground spokes.  

<a id="cheng2020"></a>**[cheng2020]** Cheng, Adulyasak, Rousseau (2020). *Drone routing with energy function: Formulation and exact algorithm*. Transp. Res. B. [10.1016/j.trb.2020.06.011](https://doi.org/10.1016/j.trb.2020.06.011)  
Multi-trip drone routing from a depot where energy consumption is a nonlinear function of payload and distance; 2-index and 3-index formulations with logic-based cuts, solved by branch-and-cut; shows the value of modelling the energy function explicitly (TR-B 139:364-387).  
*→ Spaceport feeder design:* Payload-dependent energy/range of a vehicle returning to a hub is a direct analog of payload-dependent launch-vehicle capacity and delta-v budgets.  

<a id="ts-exact2020"></a>**[ts-exact2020]** (authors not captured) (2020). *Exact and Heuristic Algorithms for the Carrier–Vehicle Traveling Salesman Problem*. Transp. Sci. [10.1287/trsc.2020.0999](https://doi.org/10.1287/trsc.2020.0999)  
Carrier-vehicle TSP: a slow, long-range carrier (e.g., ship) transports a fast, range-limited vehicle (e.g., helicopter) that visits targets and returns to the carrier; exact and heuristic algorithms. From URL/title only; DOI in the 2020 series (likely published 2021).  
*→ Spaceport feeder design:* Mothership-and-satellite routing is the closest routing analog to a reusable launcher staging from a carrier hub with limited sortie range.  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="dayarian2020"></a>**[dayarian2020]** Dayarian, Savelsbergh, Clarke (2020). *Same-Day Delivery with Drone Resupply*. Transp. Sci. [10.1287/trsc.2019.0944](https://doi.org/10.1287/trsc.2019.0944)  
Introduces the vehicle routing problem with drone resupply: delivery trucks are resupplied in the field by drones from the depot whenever stationary, so trucks need not return. Dynamic same-day setting; optimization-based heuristics evaluated in simulation show reductions in delivery time and fleet size (TS 54(1):229-249).  
*→ Spaceport feeder design:* Hub-to-vehicle resupply with time-limited rendezvous is an analog of feeding payload to a launch asset within a time window rather than returning to the hub.  

<a id="ts-charging2021"></a>**[ts-charging2021]** (authors not captured) (2021). *Charging Station Location and Sizing for Electric Vehicles Under Congestion*. Transp. Sci. [10.1287/trsc.2021.0494](https://doi.org/10.1287/trsc.2021.0494)  
Joint location and sizing of charging stations with queueing/congestion at stations (capacitated facilities with waiting), formulated and solved as a capacitated location model with congestion terms. From URL/title only; DOI in the 2021 series (likely published 2022-2023).  
*→ both problems:* Hub-with-capacity-and-congestion location is the generic form of both vertiport charging-pad sizing and orbital/ground hub docking capacity.  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="ts-coordinated2021"></a>**[ts-coordinated2021]** (authors not captured) (2021). *Coordinated Logistics with a Truck and Multiple Sidekicks*. Transp. Sci. [10.1287/trsc.2021.0485](https://doi.org/10.1287/trsc.2021.0485)  
Truck coordinated with multiple drones (sidekicks); extends the single-drone coordinated-logistics analysis to several range-limited satellite vehicles. From URL/title only; DOI in the 2021 series (likely published 2022).  
*→ Spaceport feeder design:* One carrier serving many range-limited satellites approximates one orbital hub served by several limited-capacity launch vehicles.  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="roberti2021"></a>**[roberti2021]** Roberti, Ruthmair (2021). *Exact Methods for the Traveling Salesman Problem with Drone*. Transp. Sci. [10.1287/trsc.2020.1017](https://doi.org/10.1287/trsc.2020.1017)  
Exact solution of TSP-D variants (truck with large capacity and low urban speed; drone fast, off-network, range- and payload-limited). Compact MIP and a branch-and-price approach with ng-route-type relaxations and dynamic programming pricing; solves larger instances than earlier exact methods (TS 55(2):315-335).  
*→ Spaceport feeder design:* Exact decomposition for synchronized carrier/satellite-vehicle schedules transfers to synchronized spoke-to-launcher feeding with capacity and range limits.  

<a id="dukkanci2021"></a>**[dukkanci2021]** Dukkanci, Kara, Bektaş (2021). *Minimizing energy and cost in range-limited drone deliveries with speed optimization*. Transp. Res. C. [10.1016/j.trc.2021.102985](https://doi.org/10.1016/j.trc.2021.102985)  
Energy Minimizing and Range Constrained Drone Delivery Problem: trucks act as launch bases for drones; nonlinear model minimizing operating plus energy cost with drone speed as a decision, service-time bounds and range limits; solved via second-order cone reformulation and heuristics. Published in TR-C 125 (the facet brief listed TR-B).  
*→ Spaceport feeder design:* Jointly choosing launch bases and vehicle speed/energy under range limits parallels choosing spaceport staging and trajectory energy budgets.  

<a id="ts-cooperative2022"></a>**[ts-cooperative2022]** (authors not captured) (2022). *Cooperative Learning for Smart Charging of Shared Autonomous Vehicle Fleets*. Transp. Sci. [10.1287/trsc.2022.1187](https://doi.org/10.1287/trsc.2022.1187)  
Operational charging control for shared autonomous (electric) vehicle fleets using cooperative/multi-agent learning to decide when and where vehicles charge given station capacity. From URL/title only; DOI in the 2022 series.  
*→ both problems:* Fleet-level charging/turnaround coordination at capacitated stations is the operational counterpart of RAM aircraft charging slots (A) and reusable-vehicle turnaround scheduling (B).  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="ts-robust2022"></a>**[ts-robust2022]** (authors not captured) (2022). *Robust Charging Network Planning for Metropolitan Taxi Fleets*. Transp. Sci. [10.1287/trsc.2022.0207](https://doi.org/10.1287/trsc.2022.0207)  
Plans a charging-station network (locations and charger counts) for an electric taxi fleet under uncertain demand using robust optimization. From URL/title only; DOI in the 2022 series (likely published 2023-2024).  
*→ both problems:* Robust sizing of capacitated energy-replenishment hubs for a fleet transfers to vertiport/airport charging capacity (A) and to turnaround capacity at spaceport hubs under demand uncertainty (B).  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="ts-traveling2022"></a>**[ts-traveling2022]** (authors not captured) (2022). *The Traveling Salesman Problem with Drones: The Benefits of Retraversing the Arcs*. Transp. Sci. [10.1287/trsc.2022.0230](https://doi.org/10.1287/trsc.2022.0230)  
TSP with drones in which the truck may retraverse arcs; quantifies the benefit of allowing repeated arc use for truck-drone synchronization. From URL/title only; DOI in the 2022 series (likely TS 57, 2023; an IDEAS handle ortrsc/v57y2023i5p1340-1358 appeared in the same result set).  
*→ Spaceport feeder design:* Shows how relaxing path structure of the carrier improves synchronized satellite operations, relevant to flexible routing of feeder legs to launch sites.  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="ts-orienteering2023"></a>**[ts-orienteering2023]** (authors not captured) (2023). *The Orienteering Problem with Drones*. Transp. Sci. [10.1287/trsc.2023.0003](https://doi.org/10.1287/trsc.2023.0003)  
Orienteering (profit-collecting, time-limited) variant with a truck and drones; selects which customers to serve within a time budget subject to drone range and synchronization. From URL/title only; DOI in the 2023 series (likely published 2024).  
*→ Spaceport feeder design:* Selective service under a hard time budget with range-limited satellites maps to choosing which spokes a launch window can serve.  
*(year taken from DOI (submission year); publication may be one year later)*  

<a id="mahmutogullari2024"></a>**[mahmutogullari2024]** Mahmutoğulları, Yaman (2024). *Mathematical formulations for the multi-period alternative fuel refueling station location problem with routing under decision-dependent flow dynamics*. Transp. Res. B. [10.1016/j.trb.2024.102999](https://doi.org/10.1016/j.trb.2024.102999)  
Multi-period location of alternative-fuel refuelling stations where range-limited vehicles may deviate from shortest paths and the flow (adoption) in each period depends on the stations already opened (decision-dependent dynamics).  
*→ Spaceport feeder design:* Phased infrastructure roll-out where demand responds to opened facilities parallels staged spaceport/hub capacity expansion under adoption-dependent demand.  

<a id="zhen2025"></a>**[zhen2025]** Zhen et al. (co-authors not captured) (2025). *Optimizing an On-Demand Delivery Mode Based on Trucks and Drones*. Transp. Sci. [10.1287/trsc.2024.0693](https://doi.org/10.1287/trsc.2024.0693)  
A fleet of trucks, each carrying several drones, circulates on closed-loop routes; drones pick up and deliver parcels and parcels can transship between routes. MIP for the multi-route network with transshipment; studies number of drones, speed, endurance, penalty cost and spatial order distribution (TS 59(5):1008-1031).  
*→ Spaceport feeder design:* Cyclic trunk routes with drone spokes and inter-route transshipment mirror periodic launch cycles fed by spokes with transfer at hubs.  

### Fleet sizing & capacity expansion (45 papers)

<a id="fong1981"></a>**[fong1981]** Fong, Srinivasan (1981). *The Multiregion Dynamic Capacity Expansion Problem, Part I*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v29y1981i4p787-799.html)  
Multi-region, multi-period capacity expansion with inter-regional transportation: when and where to add capacity to satisfy growing regional demands; heuristic based on single-region DP subproblems.  
*→ Spaceport feeder design:* Where/when to add launch or hub capacity across regions with transshipment between them.  

<a id="fong1981a"></a>**[fong1981a]** Fong, Srinivasan (1981). *The Multiregion Dynamic Capacity Expansion Problem, Part II*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v29y1981i4p800-816.html)  
Companion paper refining the multiregion dynamic capacity expansion solution approach and reporting computational results.  
*→ Spaceport feeder design:* Same transfer as Part I.  

<a id="luss1982"></a>**[luss1982]** Luss (1982). *Operations Research and Capacity Expansion Problems: A Survey*. Oper. Res. [10.1287/opre.30.5.907](https://doi.org/10.1287/opre.30.5.907)  
Unifying survey of capacity expansion models: single/multi-facility, deterministic and stochastic demand growth, timing and sizing of expansions, economies of scale; DP, network and heuristic algorithms and applications.  
*→ Spaceport feeder design:* Foundational taxonomy for expanding spaceport/hub capacity over time under demand growth.  

<a id="turnquist1986"></a>**[turnquist1986]** Turnquist, Jordan (1986). *Fleet Sizing under Production Cycles and Uncertain Travel Times*. Transp. Sci. [10.1287/trsc.20.4.227](https://doi.org/10.1287/trsc.20.4.227)  
Analytical/stochastic model of the number of reusable containers (vehicles) needed to sustain a cyclic production-shipment loop when travel/turnaround times are uncertain; fleet size follows from cycle time distribution and service-level targets.  
*→ Spaceport feeder design:* Direct analog for sizing a reusable launch-vehicle fleet whose turnaround (refurbishment + return) time is uncertain and whose service runs on a repeating cycle.  

<a id="dejax1987"></a>**[dejax1987]** Dejax, Crainic (1987). *Survey Paper—A Review of Empty Flows and Fleet Management Models in Freight Transportation*. Transp. Sci. [10.1287/trsc.21.4.227](https://doi.org/10.1287/trsc.21.4.227)  
Taxonomy and literature review of empty-vehicle flow and fleet management models (strategic fleet sizing, tactical allocation, operational dispatching; deterministic vs stochastic; network-flow and DP formulations).  
*→ Spaceport feeder design:* Organizing framework for the empty-return (vehicle repositioning) layer of a spaceport feeder network with reusable vehicles.  

<a id="beaujon1991"></a>**[beaujon1991]** Beaujon, Turnquist (1991). *A Model for Fleet Sizing and Vehicle Allocation*. Transp. Sci. [10.1287/trsc.25.1.19](https://doi.org/10.1287/trsc.25.1.19)  
Joint optimization of fleet size and dynamic allocation of loaded/empty vehicles over a time-space network with uncertain demand; expected-value nonlinear network model in which fleet size and utilization interact, solved by an iterative network-optimization procedure. Shows fleet sizing and empty allocation must be decided together.  
*→ Spaceport feeder design:* Template for jointly choosing the launch-vehicle fleet size and the repositioning of empty vehicles among spaceports under uncertain payload demand.  

<a id="bean1992"></a>**[bean1992]** Bean, Higle, Smith (1992). *Capacity Expansion Under Stochastic Demands*. Oper. Res. [link](https://ideas.repec.org/a/inm/oropre/v40y1992i3-supplement-2ps210-s216.html)  
Shows that capacity expansion under certain stochastic demand processes can be transformed into an equivalent deterministic problem by rescaling time/discount rate, enabling deterministic expansion algorithms.  
*→ Spaceport feeder design:* Simplifies hub/launch-capacity expansion timing under uncertain demand growth.  

<a id="crainic1993"></a>**[crainic1993]** Crainic, Gendreau, Dejax (1993). *Dynamic and Stochastic Models for the Allocation of Empty Containers*. Oper. Res. [10.1287/opre.41.1.102](https://doi.org/10.1287/opre.41.1.102)  
Dynamic deterministic and stochastic network models for allocating empty containers among depots/ports over a multi-period horizon, including substitution between container types and uncertain supplies/demands; time-space multicommodity flow formulations. Seen only as a citation in a result (no publisher URL).  
*→ Spaceport feeder design:* Foundational time-expanded asset-balancing formulation; the spaceport analogue is repositioning reusable vehicles and containers among spokes.  

<a id="cordeau1998"></a>**[cordeau1998]** Cordeau, Toth, Vigo (1998). *A Survey of Optimization Models for Train Routing and Scheduling*. Transp. Sci. [link](https://pubsonline.informs.org/doi/references/10.1287/trsc.1050.0115)  
Survey of optimization models for rail routing and scheduling including locomotive and rolling-stock assignment and rotation. Seen only in a reference list (TS 32:380-404).  
*→ Spaceport feeder design:* Background for cyclic asset-rotation models applicable to reusable vehicle turnaround.  

<a id="holmberg1998a"></a>**[holmberg1998a]** Holmberg, Joborn, Lundgren (1998). *A Tactical Decision Support System for Empty Railcar Management*. Transp. Sci. [10.1287/trsc.32.4.306](https://doi.org/10.1287/trsc.32.4.306)  
Multicommodity network flow model on a time-space network for tactical distribution of empty railcars with train-capacity constraints and substitution between car types; solved by Lagrangian-relaxation-based heuristics for a national railway.  
*→ Spaceport feeder design:* Capacitated time-space repositioning of reusable assets with substitutable types resembles returning launch vehicles/capsules through capacitated scheduled links.  

<a id="cheung1998"></a>**[cheung1998]** Cheung, Chen (1998). *A Two-Stage Stochastic Network Model and Solution Methods for the Dynamic Empty Container Allocation Problem*. Transp. Sci. [10.1287/trsc.32.2.142](https://doi.org/10.1287/trsc.32.2.142)  
Two-stage stochastic network model on a time-space network: stage-one supplies, demands and ship capacities deterministic, stage-two random; exploits network structure to apply stochastic quasi-gradient and stochastic hybrid approximation procedures.  
*→ Spaceport feeder design:* Stochastic time-expanded repositioning of reusable assets with capacitated, scheduled links (ships ~ launch slots) maps directly onto the spaceport feeder problem.  

<a id="powell1998"></a>**[powell1998]** Powell, Carvalho (1998). *Dynamic Control of Logistics Queueing Networks for Large-Scale Fleet Management*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v32y1998i2p90-109.html)  
Formulates dynamic fleet management as an optimal control problem over a Logistics Queueing Network, replacing one large time-space LP by a sequence of small local problems with value-based gradients; achieves solutions within a few percent of global optimum with much more modeling flexibility.  
*→ Spaceport feeder design:* Scalable decomposition for dispatching reusable vehicles among many spokes when demand arrives dynamically.  

<a id="carvalho2000"></a>**[carvalho2000]** Carvalho, Powell (2000). *A Multiplier Adjustment Method for Dynamic Resource Allocation Problems*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v34y2000i2p150-164.html)  
Multiplier (dual) adjustment method for dynamic resource allocation on time-space networks, building on the LQN framework to approximate the value of resources in future periods. Title seen on a Princeton page; volume/pages matched via IDEAS (TS 34(2):150-164).  
*→ Spaceport feeder design:* Dual-price based coordination of vehicle allocation across periods/locations is reusable for launch-vehicle allocation.  

<a id="godfrey2002"></a>**[godfrey2002]** Godfrey, Powell (2002). *An Adaptive Dynamic Programming Algorithm for Dynamic Fleet Management, I: Single Period Travel Times*. Transp. Sci. [10.1287/trsc.36.1.21.570](https://doi.org/10.1287/trsc.36.1.21.570)  
Approximate dynamic programming for stochastic dynamic fleet management: piecewise-linear concave, separable value-function approximations of future resource value are learned adaptively from sample gradients and naturally yield integer solutions to the per-period network subproblems.  
*→ Spaceport feeder design:* ADP with concave value functions handles stochastic payload demand and vehicle repositioning decisions over many periods in the feeder network.  

<a id="godfrey2002a"></a>**[godfrey2002a]** Godfrey, Powell (2002). *An Adaptive Dynamic Programming Algorithm for Dynamic Fleet Management, II: Multiperiod Travel Times*. Transp. Sci. [10.1287/trsc.36.1.40.572](https://doi.org/10.1287/trsc.36.1.40.572)  
Extends Part I to multiperiod travel times, where the basic algorithm performed poorly; a modified algorithm that accounts for vehicles in transit restores near-Part-I performance.  
*→ Spaceport feeder design:* Launch-and-return trips span multiple periods (orbital phasing, refurbishment), exactly the in-transit resource issue solved here.  

<a id="ahmed2003"></a>**[ahmed2003]** Ahmed, Sahinidis (2003). *An Approximation Scheme for Stochastic Integer Programs Arising in Capacity Expansion*. Oper. Res. [10.1287/opre.51.3.461.14960](https://doi.org/10.1287/opre.51.3.461.14960)  
Multi-stage stochastic integer program for capacity expansion over a scenario tree; LP-relaxation-based heuristic shown to be asymptotically optimal as the number of periods grows.  
*→ Spaceport feeder design:* Multi-stage expansion of launch/hub capacity under demand scenarios.  

<a id="wu2005"></a>**[wu2005]** Wu, Hartman, Wilson (2005). *An Integrated Model and Solution Approach for Fleet Sizing with Heterogeneous Assets*. Transp. Sci. [10.1287/trsc.1030.0050](https://doi.org/10.1287/trsc.1030.0050)  
LP on a time-space network that integrates operational decisions (demand allocation, empty repositioning) with tactical asset procurement/sale decisions for assets of different ages with age-dependent costs, yielding optimal fleet size and mix; two-phase solution approach for large instances (truck rental).  
*→ Spaceport feeder design:* Shows how fleet size/mix and vehicle acquisition-retirement (finite reuse life of launch vehicles) can be embedded in a time-expanded repositioning model.  

<a id="ahuja2005"></a>**[ahuja2005]** Ahuja, Liu, Orlin, Sharma, Shughart (2005). *Solving Real-Life Locomotive-Scheduling Problems*. Transp. Sci. [10.1287/trsc.1050.0115](https://doi.org/10.1287/trsc.1050.0115)  
Weekly locomotive assignment as a multicommodity flow on a space-time network with consist constraints; solved by problem decomposition, integer programming and very large-scale neighborhood search within 30 minutes for U.S. railroads.  
*→ Spaceport feeder design:* Assigning reusable propulsion assets to scheduled services with consistency constraints, a close analog of launch-vehicle-to-launch assignment.  

<a id="diana2006"></a>**[diana2006]** Diana, Dessouky, Xia (2006). *A model for the fleet sizing of demand responsive transportation services with time windows*. Transp. Res. B. [10.1016/j.trb.2005.09.005](https://doi.org/10.1016/j.trb.2005.09.005)  
Probabilistic model to determine the number of vehicles needed for a demand-responsive service with prescribed quality (waiting time and maximum detour), requiring only the spatial demand distribution and pickup/delivery time windows; positioned as a lighter alternative to simulation when detailed demand data are lacking.  
*→ both problems:* Analytical fleet-sizing under time-window quality targets applies to RAM on-demand fleets and feeder vehicle counts.  

<a id="topaloglu2007"></a>**[topaloglu2007]** Topaloglu, Powell (2007). *Incorporating Pricing Decisions into the Stochastic Dynamic Fleet Management Problem*. Transp. Sci. [10.1287/trsc.1070.0196](https://doi.org/10.1287/trsc.1070.0196)  
Joint pricing and fleet management: ADP value function approximations for the stochastic dynamic fleet problem are combined with price-dependent demand so that prices and vehicle allocations are optimized together.  
*→ Spaceport feeder design:* Suggests coupling launch pricing with fleet repositioning in the feeder network under demand uncertainty.  

<a id="topaloglu2007a"></a>**[topaloglu2007a]** Topaloglu, Powell (2007). *Sensitivity Analysis of a Dynamic Fleet Management Model Using Approximate Dynamic Programming*. Oper. Res. [10.1287/opre.1060.0347](https://doi.org/10.1287/opre.1060.0347)  
Tractable algorithms to compute the marginal value of an additional vehicle or load in a stochastic dynamic fleet management model solved by ADP, without re-simulation; numerically accurate and cheap.  
*→ Spaceport feeder design:* Gives the marginal value of one more reusable vehicle, i.e., a fleet-sizing signal, directly from the operational model.  

<a id="fugenschuh2008"></a>**[fugenschuh2008]** Fügenschuh, Homfeld, Huck, Martin, Yuan (2008). *Scheduling Locomotives and Car Transfers in Freight Transport*. Transp. Sci. [10.1287/trsc.1080.0248](https://doi.org/10.1287/trsc.1080.0248)  
MIP for simultaneous locomotive scheduling and car-transfer planning in freight rail with cyclic timetable; solved with commercial MIP plus problem-specific cuts/heuristics.  
*→ Spaceport feeder design:* Coupled vehicle and cargo transfer scheduling resembles coupling vehicle cycles with payload consolidation at spaceports.  

<a id="vaidyanathan2008"></a>**[vaidyanathan2008]** Vaidyanathan, Ahuja, Orlin (2008). *The Locomotive Routing Problem*. Transp. Sci. [10.1287/trsc.1080.0244](https://doi.org/10.1287/trsc.1080.0244)  
Routes individual locomotive units through a train network so that fueling and maintenance constraints are met; network-based IP formulations on a time-space network with decomposition heuristics.  
*→ Spaceport feeder design:* Vehicle-level routing with mandatory maintenance (refurbishment) visits mirrors reusable launcher cycles.  

<a id="simao2009"></a>**[simao2009]** Simao, Day, George, Gifford, Nienow, Powell (2009). *An Approximate Dynamic Programming Algorithm for Large-Scale Fleet Management: A Case Application*. Transp. Sci. [10.1287/trsc.1080.0238](https://doi.org/10.1287/trsc.1080.0238)  
ADP model simulating more than 6,000 drivers for Schneider National: high-dimensional multi-attribute resource allocation solved by merging math programming with machine-learned value function approximations; calibrated against historical performance.  
*→ Spaceport feeder design:* Demonstrates ADP scaling to heterogeneous reusable assets with many attributes (vehicle type, state, location) relevant to launch fleet planning.  

<a id="singh2009"></a>**[singh2009]** Singh, Philpott, Wood (2009). *Dantzig-Wolfe Decomposition for Solving Multistage Stochastic Capacity-Planning Problems*. Oper. Res. [10.1287/opre.1080.0678](https://doi.org/10.1287/opre.1080.0678)  
Multistage stochastic MIP for capacity expansion with a scenario tree; variable splitting plus Dantzig-Wolfe gives a master problem with far stronger LP relaxation that tends to yield integer solutions; solved 6-stage, 243-scenario electricity-network instance.  
*→ Spaceport feeder design:* Decomposition recipe for multistage expansion of a capacitated network under uncertain demand.  

<a id="huang2009"></a>**[huang2009]** Huang, Ahmed (2009). *The Value of Multistage Stochastic Programming in Capacity Planning Under Uncertainty*. Oper. Res. [10.1287/opre.1080.0623](https://doi.org/10.1287/opre.1080.0623)  
Analyzes the value of multistage over two-stage stochastic programming for capacity planning, deriving bounds on the gap and conditions under which multistage models matter; semiconductor capacity case.  
*→ Spaceport feeder design:* Helps decide whether phased spaceport capacity decisions need a full multistage model.  

<a id="andersen2011"></a>**[andersen2011]** Andersen, Christiansen, Crainic, Gronhaug (2011). *Branch and Price for Service Network Design with Asset Management Constraints*. Transp. Sci. [10.1287/trsc.1100.0333](https://doi.org/10.1287/trsc.1100.0333)  
Scheduled service network design on a cyclic time-space network with asset-balance constraints that force each vehicle to follow a closed rotation; the model is written with cycle-based (vehicle-rotation) variables and solved by branch-and-price with column generation over asset cycles, which outperforms arc- and path-based formulations.  
*→ Spaceport feeder design:* Launch vehicles cycling between spaceports and orbital hubs are exactly the assets whose rotations the cycle variables enumerate; the number of cycles selected is the fleet size, and turnaround is a minimum ground-arc duration.  

<a id="chow2011"></a>**[chow2011]** Chow, Regan (2011). *Network-based real option models*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v45y2011i4p682-695.html)  
Network option design problem maximizing expanded NPV with the option to defer investment, shown to generalize network design and multi-period network design; second model decomposes the deferral option into link/project-level options as project selection under uncertainty.  
*→ Spaceport feeder design:* Flexible timing of spaceport/link investments under uncertain demand growth.  

<a id="contreras2011a"></a>**[contreras2011a]** Contreras, Cordeau, Laporte (2011). *The Dynamic Uncapacitated Hub Location Problem*. Transp. Sci. [link](https://ideas.repec.org/a/inm/ortrsc/v45y2011i1p18-32.html)  
Multi-period (dynamic) uncapacitated multiple-allocation hub location: hubs are opened and closed over a planning horizon with time-varying demand to minimize discounted set-up, closing and routing costs; MIP formulation solved by a Lagrangian relaxation embedded in branch-and-bound. Index page corroborates TS 45(1):18-32, 2011 and the search summary lists 'dynamic hub location problems' among TS hub papers; title and author order from recollection and should be reconfirmed.  
*→ Spaceport feeder design:* Phased commissioning of orbital depots over a multi-year horizon, with spaceport assignments re-optimized per period, is exactly a dynamic hub location problem.  

<a id="zhu2014"></a>**[zhu2014]** Zhu, Crainic, Gendreau (2014). *Scheduled Service Network Design for Freight Rail Transportation*. Oper. Res. [10.1287/opre.2013.1254](https://doi.org/10.1287/opre.2013.1254)  
Scheduled service network design that integrates service selection and scheduling, car blocking and train make-up on a cyclic three-layer time-space network (services, blocks, cars). Solved with a matheuristic combining tabu/ellipsoidal search with slope scaling and long-term memory; demonstrated on realistic freight-rail instances (Operations Research 62(2):383-400).  
*→ Spaceport feeder design:* Launch-vehicle services can be modelled as cyclic, scheduled time-space services with payload consolidation (blocking) at orbital hubs and vehicle make-up constraints, exactly the three-layer structure solved here (  

<a id="jena2015"></a>**[jena2015]** Jena, Cordeau, Gendron (2015). *Dynamic Facility Location with Generalized Modular Capacities*. Transp. Sci. [10.1287/trsc.2014.0575](https://doi.org/10.1287/trsc.2014.0575)  
Unifying MIP for multi-period facility location where costs for changing capacity are defined for every pair of capacity levels (opening, closing, expansion, reduction, temporary closure); strong formulation solves 100-facility/1,000-customer instances faster than specialized models.  
*→ Spaceport feeder design:* Direct template for multi-period opening and resizing of spaceports/hubs with modular capacity steps.  

<a id="sun2015"></a>**[sun2015]** Sun, Schonfeld (2015). *Stochastic capacity expansion models for airport facilities*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v80y2015icp1-18.html)  
Stochastic models for timing and sizing airport facility (e.g., runway/terminal) capacity expansions under uncertain demand growth, trading off construction economies of scale against delay costs.  
*→ both problems:* Capacity expansion timing for airports (RAM) and for launch/hub facilities (spaceports).  

<a id="crainic2016a"></a>**[crainic2016a]** Crainic, Hewitt, Toulouse, Vu (2016). *Service Network Design with Resource Constraints*. Transp. Sci. [10.1287/trsc.2014.0525](https://doi.org/10.1287/trsc.2014.0525)  
Scheduled service network design in which vehicles (resources) are anchored to home terminals, must complete a closed cycle within the schedule period and are limited in number per terminal; MIP on a time-space network solved by a column-generation and slope-scaling based matheuristic with intensification and diversification phases.  
*→ Spaceport feeder design:* Models a bounded number of reusable vehicles based at each spaceport that must return home within the planning cycle, the core resource structure of spaceport-to-orbit feeder scheduling.  

<a id="barmann2017"></a>**[barmann2017]** Bärmann, Martin, Schuelldorf (2017). *A Decomposition Method for Multiperiod Railway Network Expansion—With a Case Study for Germany*. Transp. Sci. [link](https://cris.fau.de/publications/118144224?lang=en_GB)  
Multiperiod MIP for expanding the German rail network until 2030 under growing demand; novel multiple-knapsack decomposition used as heuristic and as exact method. Venue shown on university page only.  
*→ Spaceport feeder design:* Phased capacity expansion of a transportation network under demand growth, analog of staged spaceport/hub build-out.  

<a id="ho2017"></a>**[ho2017]** Ho, Szeto (2017). *A hybrid large neighborhood search for the static multi-vehicle bike-repositioning problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v95y2017icp340-363.html)  
Static multi-vehicle bike repositioning as a routing MIP; hybrid LNS with tabu search.  
*→ Spaceport feeder design:* Rebalancing routing heuristics; peripheral to fleet sizing.  

<a id="zhang2017a"></a>**[zhang2017a]** Zhang, Yu, Desai, Lau, Srivathsan (2017). *A time-space network flow approach to dynamic repositioning in bicycle sharing systems*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v103y2017icp188-207.html)  
Dynamic bike repositioning modeled as a MIP on a time-space network with vehicle routes and bike flows; heuristic for large instances; significantly fewer rejected user requests than existing methods on standard test beds.  
*→ Spaceport feeder design:* Time-expanded repositioning of shared assets under time-varying demand, analogous to repositioning vehicles among spaceports.  

<a id="szeto2018"></a>**[szeto2018]** Szeto, Shui (2018). *Exact loading and unloading strategies for the static multi-vehicle bike repositioning problem*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v109y2018icp176-211.html)  
Static multi-vehicle repositioning with exact loading/unloading quantity determination given routes; enhanced heuristic framework.  
*→ Spaceport feeder design:* Rebalancing methods; peripheral to facet.  

<a id="hewitt2019a"></a>**[hewitt2019a]** Hewitt, Crainic, Nowak, Rei (2019). *Scheduled service network design with resource acquisition and management under uncertainty*. Transp. Res. B. [10.1016/j.trb.2019.08.008](https://doi.org/10.1016/j.trb.2019.08.008)  
Scheduled service network design with vehicle (resource) acquisition and management under demand uncertainty, posed as a two-stage stochastic program on a time-expanded network: the first stage selects services and acquires/positions resources subject to asset-balance (cyclic) design constraints, the second stage routes stochastic demand with recourse. Solved with a decomposition-based approach and used to quantify the value of jointly deciding fleet acquisition and schedule (Transportation Research Part B 128:324-343).  
*→ Spaceport feeder design:* Directly matches reusable launch-vehicle fleet acquisition, turnaround/positioning and launch scheduling under uncertain demand with vehicle balance across the cycle (  

<a id="trb-hybrid2020"></a>**[trb-hybrid2020]** (authors not captured) (2020). *A hybrid algorithm for the static bike-sharing re-positioning problem based on an effective clustering strategy*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v140y2020icp1-21.html)  
Clustering-based hybrid algorithm for static bike repositioning in large systems. From title only.  
*→ Spaceport feeder design:* Repositioning heuristics; peripheral.  

<a id="vanlieshout2021"></a>**[vanlieshout2021]** Van Lieshout (2021). *Integrated Periodic Timetabling and Vehicle Circulation Scheduling*. Transp. Sci. [10.1287/trsc.2020.1024](https://doi.org/10.1287/trsc.2020.1024)  
Jointly optimizes a PESP periodic timetable and the circulation of vehicles that operate it, so vehicle count and turnaround are decided with event times; integrated MIP formulations and solution approaches are compared against sequential planning on public transport instances.  

<a id="trb-operations2022"></a>**[trb-operations2022]** (authors not captured) (2022). *Operations design for high-velocity intra-city package service*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v161y2022icp150-168.html)  
Service network design for high-velocity intra-city package shuttles using rate-based (continuous flow) models that build repeatable cyclic vehicle routes subject to capacity and timing requirements, producing cost-effective designs.  
*→ Spaceport feeder design:* Repeatable cyclic shuttle routes under capacity and timing constraints are a close analog of periodic launch rotations between spaceports and orbital hubs; rate-based modeling sidesteps full time expansion.  

<a id="shehadeh2023"></a>**[shehadeh2023]** Shehadeh (2023). *Distributionally Robust Optimization Approaches for a Stochastic Mobile Facility Fleet Sizing, Routing, and Scheduling Problem*. Transp. Sci. [10.1287/trsc.2022.1153](https://doi.org/10.1287/trsc.2022.1153)  
Two-stage DRO models (moment- and Wasserstein-based ambiguity sets) and a stochastic program choosing fleet size plus route and time schedule for mobile facilities under time-dependent random demand; decomposition algorithms; computational comparison of DRO vs SP.  
*→ Spaceport feeder design:* Recent fleet-sizing-under-uncertainty template with schedule decisions, suitable for sizing launch fleets against ambiguous demand distributions.  

<a id="gong2023"></a>**[gong2023]** Gong, Zhang, Liu, Graham (2023). *The effects of airport capacity expansion under responsive airlines and elastic passenger demand*. Transp. Res. B. [link](https://ideas.repec.org/a/eee/transb/v170y2023icp48-76.html)  
Equilibrium model of airport capacity expansion in which airlines respond to capacity and passenger demand is elastic; analyzes welfare and congestion effects of expansion.  
*→ both problems:* Capacity expansion with responsive carriers/elastic demand informs hub capacity decisions in both topics.  

<a id="or-budget2025"></a>**[or-budget2025]** (authors not captured) (2025). *Budget-Driven Multiperiod Hub Location: A Robust Time-Series Approach*. Oper. Res. [10.1287/opre.2022.0319](https://doi.org/10.1287/opre.2022.0319)  
Multiperiod hub location under uncertain time-dependent demand: budget-driven distributionally robust model with a nested ambiguity set built from VAR/VARMA time-series models; constrains expected periodic cost within budgets while maximising robustness (Sharpe-ratio-type criterion over the worst period); uncapacitated case solved by bisection over mixed-integer conic programs, capacitated case via decision rules (OR 73(2):613-631).  
*→ Spaceport feeder design:* Phased build-out of orbital hubs under a capital budget with demand that evolves over time is a multi-period hub location problem; a time-series robust model fits launch-demand forecasts.  

<a id="ts-dynamic2025"></a>**[ts-dynamic2025]** (authors not captured) (2025). *Dynamic Facility Location Under Cumulative Customer Demand*. Transp. Sci. [10.1287/trsc.2025.0104](https://doi.org/10.1287/trsc.2025.0104)  
Multi-period facility location where customer demand accumulates over time if unserved; formulations and solution approach for dynamic location/relocation. From title only.  
*→ Spaceport feeder design:* Recent dynamic location model relevant to phased hub/spaceport deployment with backlogged payload demand.


## Appendix A: counts by venue, period and family

Total verified in-scope papers: **453**. Relevance: A = 138, B = 237, both = 78.

| Venue | pre-2000 | 2000-2009 | 2010-2019 | 2020-2026 | Total |
|---|---|---|---|---|---|
| Operations Research | 34 | 18 | 18 | 6 | 76 |
| Transportation Science | 48 | 58 | 80 | 52 | 238 |
| Transportation Research Part B | 15 | 17 | 48 | 21 | 101 |
| Transportation Research Part C | 0 | 0 | 14 | 24 | 38 |
| **Total** | 97 | 93 | 160 | 103 | 453 |

| Methodology family | Papers | OR | TS | TR-B | TR-C | 2020-2026 |
|---|---|---|---|---|---|---|
| Deterministic ATFM IP | 14 | 4 | 8 | 1 | 1 | 3 |
| Stochastic/robust ATFM | 13 | 2 | 8 | 3 | 0 | 4 |
| Equity/CDM/slot allocation | 28 | 1 | 14 | 7 | 6 | 7 |
| Decomposition & large-scale methods | 6 | 3 | 1 | 2 | 0 | 3 |
| Trajectory-based ops & airspace | 16 | 0 | 8 | 1 | 7 | 2 |
| Airport/runway/terminal scheduling | 15 | 6 | 8 | 0 | 1 | 1 |
| UAM/AAM traffic management | 18 | 0 | 4 | 0 | 14 | 15 |
| AAM demand & network planning | 8 | 0 | 2 | 2 | 4 | 5 |
| Airline scheduling & recovery | 45 | 5 | 35 | 3 | 2 | 7 |
| Dynamic network flows | 39 | 9 | 18 | 11 | 1 | 6 |
| Hub location | 39 | 7 | 16 | 16 | 0 | 8 |
| Service network design | 20 | 5 | 14 | 1 | 0 | 4 |
| Liner/feeder shipping | 26 | 4 | 12 | 10 | 0 | 5 |
| Air cargo/express network design | 29 | 4 | 17 | 8 | 0 | 6 |
| Multi-echelon & synchronization | 30 | 5 | 22 | 3 | 0 | 3 |
| Network design under uncertainty | 6 | 2 | 2 | 2 | 0 | 0 |
| Time-window/periodic/launch scheduling | 20 | 6 | 6 | 8 | 0 | 1 |
| Transit feeder design | 19 | 1 | 6 | 11 | 1 | 3 |
| Emerging-tech network design | 17 | 1 | 13 | 2 | 1 | 13 |
| Fleet sizing & capacity expansion | 45 | 11 | 24 | 10 | 0 | 7 |

Annotation basis: abstract snippet = 0, reviewer knowledge = 0, finder snippet only = 453.
Venue evidence: DOI seen in a real search result = 305, publisher/IDEAS URL signature = 134, title matched to a search result = 14.
Unconfirmed leads (not included): 83. Exists-but-other-venue: 1.


## Appendix B: search protocol, verification and limitations

### Search facets

| Problem | Facets searched |
|---|---|
| RAM air-traffic-flow problem | deterministic ATFM integer programs; stochastic and robust ATFM; equity, collaborative decision making and slots; large-scale solution methods; trajectory-based operations and airspace; airport, runway and terminal scheduling; UAM, AAM and RAM traffic management (two passes); RAM demand and network planning; airline scheduling and recovery; dynamic network flows; recent ATFM in TR-B and TR-C |
| Spaceport-to-Orbit feeder design | hub location; service network design; liner and feeder shipping; air cargo, express and airline networks; multi-echelon and synchronisation; network design under uncertainty; periodic, time-window and launch scheduling; transit feeder design; emerging-technology network design; fleet sizing and capacity expansion; in-venue space and launch papers |

### Process

1. **Search.** Each facet was assigned to an agent with a quota of about 28 web searches. Queries combined method phrases, author surnames, venue names and DOI prefixes. A first round of automated sweeps ran into a shared per-turn search limit, so several facets were re-run in later rounds with explicit quotas. In total, 847 searches returned results and 462 were refused by the limit. Refused searches produced no papers.
2. **Venue oracle.** Every link in every real search result was parsed. A link counted as proof of venue only if it was a DOI or publisher URL with a journal-identifying prefix, or an IDEAS/RePEc journal page. This produced 810 in-scope links.
3. **Consolidation.** Candidates from all agents were merged by DOI and title. A candidate was accepted only if its DOI was seen in a real search result, or its URL carried a venue signature. Candidates with a typed DOI that never appeared in a result were held back as leads.
4. **Lead resolution.** One partial round of targeted re-searches confirmed additional leads. It was cut short by a usage limit. The remaining leads are in Appendix C.
5. **Cleanup.** Placeholder author strings were removed, duplicate entries merged, and families reassigned by title keywords where the facet label was misleading.
6. **Synthesis.** Sections 1 to 6 cite only keys in the verified bibliography. A build check rejects any unknown key.

### Files

- `bibliography.csv` has one row per paper, with family, scope, summary and transfer note.
- `bibliography.bib` is BibTeX. Author fields hold surnames only, so complete them from the DOI.
- `data/papers.json` holds full records, including the evidence type for each venue decision.
- `data/leads_unconfirmed.json` and `data/papers_secondary.json` hold excluded items.
- `search-log/` holds every agent's query log and candidate notes.


## Appendix C: unconfirmed leads and out-of-venue sightings

**Unconfirmed leads (83).** Search agents recorded these titles with medium or low confidence, but no search result showed a publisher page in one of the four venues, so they are excluded from the counts above. They are listed so a reader can check them manually.

- Nilim, El Ghaoui (2005). Robust Control of Markov Decision Processes with Uncertain Transition Matrices. *claimed venue:* Operations Research; *confidence:* medium
- Zhu, Belieres, Hewitt, Wu (2026). Joint fleet scheduling and cargo flow allocation for air cargo services. *claimed venue:* Transportation Research Part B; *confidence:* high
- Landete, Muñoz-Ocaña, Rodríguez-Chía, Saldanha-da-Gama (2024). Uncapacitated Single-Allocation Hub Median Location with Edge Upgrading: Models and Exact Solution Algorithms. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Taherkhani, Hosseini, Alumur (2024). Sustainable hub location under uncertainty. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Ghaffarinasab, Çavuş, Kara (2023). A mean-CVaR approach to the risk-averse single allocation hub location problem with flow-dependent economies of scale. *claimed venue:* Transportation Research Part B; *confidence:* medium
- (authors not shown in result; PolyU repository) (2023). An Exact Algorithm for the Pickup and Delivery Problem with Crowdsourced Bids and Transshipment. *claimed venue:* Transportation Research Part B; *confidence:* medium
- not shown in result (2023). A branch-and-price-and-cut algorithm for the vehicle routing problem with load-dependent drones. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Zhou et al. (co-authors not shown) (2023). An exact algorithm for the two-echelon vehicle routing problem with drones. *claimed venue:* Transportation Research Part B; *confidence:* medium
- authors not shown in search snippet (PolyU-affiliated) (2022). Integrated berth and yard space allocation under uncertainty. *claimed venue:* Transportation Research Part B; *confidence:* low
- Guo, Hu, Zou, Hansen, Zhang, Xie (2022). Air Traffic Flow Management Integrating Separation Management and Ground Holding: An Efficiency-Equity Bi-objective Perspective. *claimed venue:* Transportation Research Part B; *confidence:* medium
- not shown in result (TU Dresden; likely Tamke, Buscher) (2021). A branch-and-cut algorithm for the vehicle routing problem with drones. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Li, Wang, Chen, Bai (2020). Two-echelon vehicle routing problem with time windows and mobile satellites. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Abdolmaleki, Masoud, Yin (2020). Transit timetable synchronization for transfer time minimization. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Wang, Sheu (2019). Vehicle routing problem with drones. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Kim, Levy, Schonfeld (2019). Optimal zone sizes and headways for flexible-route bus services. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Dell'Amico, Iori, Novellani, Subramanian (2018). The Bike sharing Rebalancing Problem with Stochastic Demands. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Çelebi, Yörüsün, Işık (2018). Bicycle sharing system design with capacity allocations. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Chen, Nie (2017). Connecting e-hailing to mass transit platform: Analysis of relative spatial position. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Demir, Burgholzer, Hrušovský, Arıkan, Jammernegg, Van Woensel (2016). A green intermodal service network design problem with travel time uncertainty. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Wu, Liu, Jin (2016). Designing robust schedule coordination scheme for transit networks with safety control margins. *claimed venue:* Transportation Research Part B; *confidence:* medium
- An, Lo (2016). Two-phase stochastic program for transit network design under demand uncertainty. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Forma, Raviv, Tzur (2015). A 3-step math heuristic for the static repositioning problem in bike-sharing systems. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Chen, Gu, Cassidy, Daganzo (2015). Optimal transit service atop ring-radial and grid street networks: A continuum approximation design method and comparisons. *claimed venue:* Transportation Research Part B; *confidence:* medium
- He, Wu, Yin, Guan (2013). Optimal deployment of public charging stations for plug-in hybrid electric vehicles. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Swaroop, Zou, Ball, Hansen (2012). Do more US airports need slot controls? A welfare based approach to determine slot levels. *claimed venue:* Transportation Research Part B; *confidence:* high
- Ibarra-Rojas, Rios-Solis (2012). Synchronization of bus timetabling. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Ban, Pang, Liu, Ma (2012). Continuous-time point-queue models in dynamic network loading. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Ban, Pang, Liu, Ma (2012). Modeling and solving continuous-time instantaneous dynamic user equilibria: A differential complementarity systems approach. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Nourbakhsh, Ouyang (2012). A structured flexible transit system for low demand areas. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Quadrifoglio, Li (2009). A methodology to derive the critical demand density for designing and operating feeder transit services. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Lo, Szeto (2002). A cell-based variational inequality formulation of the dynamic user optimal assignment problem. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Ceder, Wilson (1986). Bus network design. *claimed venue:* Transportation Research Part B; *confidence:* medium
- Szwed, Skrzyński, Wąs (2026). A ranking-based optimization algorithm for the vehicle relocation problem in car sharing services. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Authors not captured in search snippets (arXiv 2509.18492; listing attributes to Wu, Li - unverified) (2025). Integrated Prediction and Distributionally Robust Optimization for Air Traffic Management. *claimed venue:* Transportation Research Part C; *confidence:* low
- not shown (Beihang University group) (2025). Machine learning assisted dynamic copy generation approach for integrated aircraft and passenger recovery problem. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Waltz, Okhrin, Schultz (2024). Self-organized free-flight arrival for urban air mobility. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Barea, de Celis, Cadarso (2024). An integrated model for airport runway assignment and aircraft trajectory optimisation. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown) (2024). Text-Enriched Air Traffic Flow Modeling and Prediction Using Transformers. *claimed venue:* Transportation Research Part C; *confidence:* low
- He, Jin, Trépanier, Schulte (2024). A column-generation matheuristic approach for optimizing first-mile ridesharing services with publicly- and privately-owned autonomous vehicles. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Cummings, Mahmassani (2024). Airspace congestion, flow relations, and 4-d fundamental diagrams for advanced urban air mobility. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Kamo, Rosenow, Fricke, Soler (2023). Robust optimization integrating aircraft trajectory and sequence under weather forecast uncertainty. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Katsigiannis, Zografos (2023). Multi-objective airport slot scheduling incorporating operational delays and multi-stakeholder preferences. *claimed venue:* Transportation Research Part C; *confidence:* medium
- authors not shown in result (2023). Capacity of a constrained urban airspace: Influencing factors, analytical modelling and simulations. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown; Cranfield/BUAA group) (2023). General multi-agent reinforcement learning integrating heuristic-based delay priority strategy for demand and capacity balancing. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown; ASU group) (2023). Air traffic density prediction using Bayesian ensemble graph attention network (BEGAN). *claimed venue:* Transportation Research Part C; *confidence:* medium
- Ye et al. (co-authors not shown) (2022). Data-driven distributionally robust generation of time-varying flow corridor networks under demand uncertainty. *claimed venue:* Transportation Research Part C; *confidence:* low
- not shown in result (2022). Passenger-centric Urban Air Mobility: Fairness trade-offs and operational efficiency. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Wang, Brownlee, Weiszer, Woodward, Mahfouf, Chen (2021). A chance-constrained programming model for airport ground movement optimisation with taxi time uncertainties. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown; Zografos group, HW/Lancaster) (2021). A decision making framework for incorporating fairness in allocating slots at capacity-constrained airports. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Lin, Li, Ren, Wang, Szeto (2021). From aircraft tracking data to network delay model: A data-driven approach. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Prats (et al.; co-authors not shown; LiU/UPC group) (2021). Automated sequencing and merging with dynamic aircraft arrival routes and speed management for continuous descent operations. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown in result) (2021). A framework for railway transit network design with first-mile shared autonomous vehicles. *claimed venue:* Transportation Research Part C; *confidence:* medium
- authors not shown in result (2021). Identification and prediction of urban airspace availability for emerging air mobility operations. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Justin, Payan, Briceno, German, Mavris (2020). Power optimized battery swap and recharge strategies for electric aircraft operations. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Murray, Raj (2020). The multiple flying sidekicks traveling salesman problem: Parcel delivery with multiple drones. *claimed venue:* Transportation Research Part C; *confidence:* medium
- not shown in result (likely Moshref-Javadi, Hemmati, Winkenbach) (2020). Truck-Drone Team Logistics: A Heuristic Approach to Multi-Drop Route Planning. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Salama, Srinivas (2020). Joint optimization of customer location clustering and drone-based routing for last-mile deliveries. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Zografos, Jiang (2019). A bi-objective efficiency-fairness model for scheduling slots at congested airports. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Alkaabneh, Diabat, Elhedhli (2019). A Lagrangian heuristic and GRASP for the hub-and-spoke network system with economies-of-scale and congestion. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Chauhan, Unnikrishnan, Figliozzi (2019). Maximum coverage capacitated facility location problem with range constrained drones. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Samà, D'Ariano, Corman, Pacciarelli (2017). Metaheuristics for efficient aircraft scheduling and re-routing at busy terminal control areas. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Sidiropoulos, Han, Majumdar, Ochieng (2017). Robust identification of air traffic flow patterns in Metroplex terminal areas under demand uncertainty. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Evertse, Visser (2017). Real-time airport surface movement planning: Minimizing aircraft emissions. *claimed venue:* Transportation Research Part C; *confidence:* low
- Puerto, Ramos, Rodríguez-Chía, Sánchez-Gil (2016). Ordered median hub location problems with capacity constraints. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown in result; verify) (2015). Operating cost sensitivity to required time of arrival commands to ensure separation in optimal aircraft 4D trajectories. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Feng, Li, Shen (2015). Air cargo operations: Literature review and comparison with practices. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Murray, Chu (2015). The flying sidekick traveling salesman problem: Optimization of drone-assisted parcel delivery. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Sölveling, Clarke (2014). Scheduling of airport runway operations using stochastic branch and bound methods. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Pyrgiotis, Malone, Odoni (authors not shown in snippet; from the known TR-C paper) (2013). Modelling delay propagation within an airport network. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Buxi, Hansen (2013). Generating day-of-operation probabilistic capacity scenarios from weather forecasts. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Kim, Hansen (2013). A framework for the assessment of collaborative en route resource allocation strategies. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Zhu, Ukkusuri (2013). A cell based dynamic system optimum model with non-holding back flows. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Castelli, Labbé, Violin (2013). A Network Pricing Formulation for the revenue maximization of European Air Navigation Service Providers. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Zografos, Salouras, Madas (2012). Dealing with the efficient allocation of scarce resources at congested airports. *claimed venue:* Transportation Research Part C; *confidence:* low
- Castelli, Pesenti, Ranieri (authors not shown in snippet; from the known TR-C paper) (2011). The design of a market mechanism to allocate Air Traffic Flow Management slots. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Norstad, Fagerholt, Laporte (2011). Tramp ship routing and scheduling with speed optimization. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown in result; verify) (2010). Air traffic control complexity as workload driver. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Li, Quadrifoglio (2010). Feeder transit services: Choosing between fixed and demand responsive policy. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Andersen, Crainic, Christiansen (2009). Service network design with asset management: Formulations and comparative analyses. *claimed venue:* Transportation Research Part C; *confidence:* low
- Waller, Ziliaskopoulos (2006). A chance-constrained based stochastic dynamic traffic assignment model: Analysis, formulation and solution algorithms. *claimed venue:* Transportation Research Part C; *confidence:* medium
- Baaj, Mahmassani (1995). Hybrid route generation heuristic algorithm for the design of transit networks. *claimed venue:* Transportation Research Part C; *confidence:* medium
- (authors not shown; arXiv 1908.02917) (n.d.). Stochastic and Simulation-based Models for Setting Flow Rates in Collaborative Trajectory Options Program (CTOP). *claimed venue:* Transportation Research Part C; *confidence:* medium
- Delahaye (et al.; co-authors not shown; ENAC group) (n.d.). Integrated optimization of terminal maneuvering area and airport at the macroscopic level. *claimed venue:* Transportation Research Part C; *confidence:* medium

**Exists, but in another journal (1).** Found during the search with a DOI or URL proving a venue outside the four journals; kept here because they are closely related.

- Wang, Jacquillat, Vaze (2022). Vertiport Planning for Urban Aerial Mobility: An Adaptive Discretization Approach. *Manufacturing & Service Operations Management*. https://doi.org/10.1287/msom.2022.1148
