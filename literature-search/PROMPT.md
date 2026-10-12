# Prompt: reuse the verified recent literature

Copy everything inside the box below into a new chat. It gives that chat the 103 verified 2020 to 2026 papers from the literature search, plus rules so it cites them correctly. The full 453-paper set, with summaries, is at https://github.com/kamng0222/kamng0222.github.io/tree/claude/github-literature-search-enjrbq/literature-search

---

````text
You are helping me with operations research modelling for two problems:

A. Regional Air Mobility (RAM) air traffic flow management. Small electric or hybrid aircraft fly scheduled or on-demand between many regional airports and vertiports. The model assigns departure times, routes, speeds and ground or airborne holds, subject to per-period capacity at airports and vertiports, in airspace sectors or corridors, and at chargers, with turnaround that depends on state of charge. It may include weather and capacity uncertainty and fairness among operators. The base formulation is the time-indexed 0-1 model of Bertsimas and Stock Patterson (Operations Research 1998, doi:10.1287/opre.46.3.406), with rerouting (Transportation Science 2000, doi:10.1287/trsc.34.3.239.12300) and large-scale extension (Operations Research 2011).

B. Spaceport-to-Orbit feeder network design. Many ground spaceports (spokes) feed payload or passengers to a few orbital hubs, using reusable launch vehicles with limited, time-windowed capacity (launch windows, orbital phasing), turnaround times, hub capacity and uncertain demand. There is almost no direct literature in the four target journals; the only in-venue space papers are six Operations Research papers from 1966 to 1978 (for example Fisher and Jaikumar 1978, Space Shuttle scheduling, doi:10.1287/opre.26.1.166). So the methodology comes from analogs: hub location, scheduled service network design with asset balance on time-expanded networks, dynamic discretization discovery, liner and feeder shipping, express air cargo networks, two-echelon routing with synchronization, periodic event scheduling for launch windows, fleet sizing and capacity expansion.

Target journals: INFORMS Operations Research (OR), INFORMS Transportation Science (TS), Transportation Research Part B (TR-B), Transportation Research Part C (TR-C).

Below is a verified list of recent (2020 to 2026) papers. Each one's journal was confirmed from a DOI or publisher link. Rules for using it:
1. When you cite recent literature from these journals, cite from this list and give the key in square brackets, for example [levin2023], plus the DOI.
2. Do not invent papers, authors, DOIs, volumes or page numbers. If you mention a paper that is not on this list, label it "(not in the verified list, please check)".
3. Some entries say "authors not captured" or list only the first author. Do not fill in authors from memory; tell me to complete them from the DOI.
4. Years for a few Transportation Science entries come from the DOI and may be one year early.
5. Relevance tags: RAM = problem A, Spaceport = problem B, Both = both.

### UAM/AAM traffic management
- [trc-pre2026] authors not captured (2026). Pre-planned air routes or dynamic 4D trajectories? A comparative study of UTM ConOps. TR-C. sciencedirect pii:S0968090X26003797. Relevance: RAM.
- [trc-conflict2025] authors not captured (2025). Conflict probability based strategic conflict resolution for UAS traffic management considering Reasonable-Time-To-Act principle. TR-C. sciencedirect pii:S0968090X25002803. Relevance: RAM.
- [trc-demand2025] authors not captured (2025). On-demand ridesharing based on dynamic scheduling in urban air mobility. TR-C. sciencedirect pii:S0968090X25001159. Relevance: RAM.
- [trc-real2025] authors not captured (2025). Real-time traffic simulation and management for large-scale urban air mobility: Integrating route guidance and collision avoidance. TR-C. sciencedirect pii:S0968090X25004814. Relevance: RAM.
- [trc-chance2024] authors not captured (2024). Chance-constrained UAM traffic flow optimization with fast disruption recovery under uncertain waypoint occupancy time. TR-C. sciencedirect pii:S0968090X24000688. Relevance: RAM.
- [wang2023] Wang, Delahaye, Farges, Alam (2023). A quasi-dynamic air traffic assignment model for mitigating air traffic complexity and congestion for high-density UAM operations. TR-C. sciencedirect pii:S0968090X23002681. Relevance: RAM.
- [levin2023] Levin, Rey (2023). Branch-and-Price for Drone Delivery Service Planning in Urban Airspace. TS. doi:10.1287/trsc.2022.1175. Relevance: RAM.
- [trc-spacetime2022] authors not captured (2022). A space–time-energy flow-based integer programming model to design and operate a regional shared automated electric vehicle (SAEV) system and corresponding charging network. TR-C. sciencedirect pii:S0968090X22004107. Relevance: Both.
- [wang2022] Wang, Delahaye, Farges, Alam (2022). Complexity optimal air traffic assignment in multi-layer transport network for Urban Air Mobility operations. TR-C. sciencedirect pii:S0968090X22002054. Relevance: RAM.
- [wang2022a] Wang, Delahaye, Farges, Alam (2022). Complexity optimal air traffic assignment in multi-layer transport networks for Urban Air Mobility operations. TR-C. https://hal-enac.archives-ouvertes.fr/hal-03701655. Relevance: RAM.
- [justin2022] Justin, Payan, Mavris (authors per facet brief; not displayed in result) (2022). Integrated fleet assignment and scheduling for environmentally friendly electrified regional air mobility. TR-C. sciencedirect pii:S0968090X22000158. Relevance: RAM.
- [trc-traffic2022] authors not captured (2022). Traffic management and resource allocation for UAV-based parcel delivery in low-altitude urban space. TR-C. sciencedirect pii:S0968090X22002339. Relevance: RAM.
- [tang2021] Tang et al. (2021). Automated flight planning of high-density urban air mobility. TR-C. sciencedirect pii:S0968090X21003302. Relevance: RAM.
- [song2021] Song, Yeo (2021). Development of optimal scheduling strategy and approach control model of multicopter VTOL aircrafts for urban air mobility (UAM) operation. TR-C. doi:10.1016/j.trc.2021.103181. Relevance: RAM.
- [shao2021] Shao, Shao, Lu (2021). Terminal area control rules and eVTOL adaptive scheduling model for multi-vertiport system in urban air Mobility. TR-C. sciencedirect pii:S0968090X21003843. Relevance: RAM.

### AAM demand & network planning
- [trb-integrated2025] authors not captured (2025). Integrated air-rail scheduling: A branch-and-price approach for adaptive passenger-centric planning. TR-B. sciencedirect pii:S0191261525002127. Relevance: RAM.
- [trc-optimizing2023] authors not captured (2023). Optimizing the battery charging and swapping infrastructure for electric short-haul aircraft—The case of electric flight in Norway. TR-C. sciencedirect pii:S0968090X23003029. Relevance: RAM.
- [willey2021] Willey, Salmon (2021). A method for urban air mobility network design using hub location and subgraph isomorphism. TR-C. doi:10.1016/j.trc.2021.102997. Relevance: Both.
- [haan2021] Haan, Garrow, Marzuoli, Roy, Bierlaire (2021). Are commuter air taxis coming to your city? A case study for 40 cities in the United States. TR-C. doi:10.1016/j.trc.2021.103392. Relevance: RAM.
- [garrow2021] Garrow, German, Leonard (2021). Urban air mobility: A comprehensive review and comparative analysis with autonomous and electric ground transportation for informing future research. TR-C. doi:10.1016/j.trc.2021.103377. Relevance: RAM.

### Deterministic ATFM IP
- [degiovanni2024] De Giovanni, Lancia, Lulli (2024). Data-Driven Optimization for Air Traffic Flow Management with Trajectory Preferences. TS. doi:10.1287/trsc.2022.0309. Relevance: RAM.
- [hamdan2022] Hamdan, Cheaitou, Jouini, Andersson Granberg, Jemai, Alsyouf, Bettayeb, Josefsson (2022). Central Authority-Controlled Air Traffic Flow Management: An Optimization Approach. TS. doi:10.1287/trsc.2021.1087. Relevance: RAM.
- [jacquillat2022] Jacquillat (2022). Predictive and Prescriptive Analytics Toward Passenger-Centric Ground Delay Programs. TS. doi:10.1287/trsc.2021.1081. Relevance: RAM.

### Stochastic/robust ATFM
- [starita2023] Starita, Strauss, Fei, Jovanović, Ivanov, Pavlović, Fichert (2023). Cross-Border Capacity Planning in Air Traffic Management Under Uncertainty. TS. https://ideas.repec.org/a/inm/ortrsc/v57y2023i4p999-1018.html. Relevance: Both.
- [wang2020] Wang, Jacquillat (2020). A Stochastic Integer Programming Approach to Air Traffic Scheduling and Operations. OR. doi:10.1287/opre.2020.1985. Relevance: Both.
- [starita2020] Starita, Strauss, Fei, Jovanović, Ivanov, Pavlović, Fichert (2020). Air Traffic Control Capacity Planning Under Demand and Capacity Provision Uncertainty. TS. doi:10.1287/trsc.2019.0962. Relevance: Both.
- [khassiba2020] Khassiba, Bastin, Cafieri, Gendron, Mongeau (2020). Two-Stage Stochastic Mixed-Integer Programming with Chance Constraints for Extended Aircraft Arrival Management. TS. https://ideas.repec.org/a/inm/ortrsc/v54y2020i4p897-919.html. Relevance: RAM.

### Equity/CDM/slot allocation
- [gasparin2025] Gasparin et al. (2025). A User-Driven Prioritisation Process implementation and optimisation for ATFM hotspot resolution. TR-C. doi:10.1016/j.trc.2024.104894. Relevance: RAM.
- [keskin2023] Keskin, Zografos (2023). Optimal network-wide adjustments of initial airport slot allocations with connectivity and fairness objectives. TR-B. doi:10.1016/j.trb.2023.102801. Relevance: RAM.
- [birolini2023] Birolini, Jacquillat, Schmedeman, Ribeiro (2023). Passenger-Centric Slot Allocation at Schedule-Coordinated Airports. TS. doi:10.1287/trsc.2022.1165. Relevance: RAM.
- [fairbrother2020] Fairbrother et al. (2020). A Slot-Scheduling Mechanism at Congested Airports that Incorporates Efficiency, Fairness, and Airline Preferences. TS. doi:10.1287/trsc.2019.0926. Relevance: RAM.
- [xu2020] Xu, Dalmau, Melgosa, Montlaur, Prats (2020). A framework for collaborative air traffic flow management minimizing costs for airspace users: Enabling trajectory options and flexible pre-tactical delay management. TR-B. https://ideas.repec.org/a/eee/transb/v134y2020icp229-255.html. Relevance: RAM.
- [estes2020] Estes, Ball (2020). Equity and Strength in Stochastic Integer Programming Models for the Dynamic Single Airport Ground-Holding Problem. TS. doi:10.1287/trsc.2020.0975. Relevance: RAM.
- [xu2020a] Xu, Prats, Delahaye (2020). Synchronised demand-capacity balancing in collaborative air traffic flow management. TR-C. doi:10.1016/j.trc.2020.02.007. Relevance: RAM.

### Decomposition & large-scale methods
- [starita2022] Starita, Strauss, Fei, Jovanović, Ivanov, Pavlović, Fichert (2022). The value of flexible flight-to-route assignments in pre-tactical air traffic management. TR-B. https://ideas.repec.org/a/eee/transb/v160y2022icp76-96.html. Relevance: RAM.
- [crainic2021] Crainic, Hewitt, Maggioni, Rei (2021). Partial Benders Decomposition: General Methodology and Application to Stochastic Network Design. TS. doi:10.1287/trsc.2020.1022. Relevance: Both.
- [rahmaniani2020] Rahmaniani, Ahmed, Crainic, Gendreau, Rei (2020). The Benders Dual Decomposition Method. OR. doi:10.1287/opre.2019.1892. Relevance: Both.

### Trajectory-based ops & airspace
- [pelegrin2022] Pelegrín, D'Ambrosio (2022). Aircraft Deconfliction via Mathematical Programming: Review and Insights. TS. doi:10.1287/trsc.2021.1056. Relevance: RAM.
- [trc-free2020] authors not captured (2020). From free-route air traffic to an adapted dynamic main-flow system. TR-C. sciencedirect pii:S0968090X19304218. Relevance: RAM.

### Airport/runway/terminal scheduling
- [ng2024] Ng, Ribeiro, Jorge (2024). An optimization approach for the terminal airspace scheduling problem. TR-C. doi:10.1016/j.trc.2024.104856. Relevance: RAM.

### Airline scheduling & recovery
- [hizir2026] Hizir, Barnhart, Vaze (2026). Large-Scale Airline Crew Recovery Using Mixed-Integer Optimization and Supervised Machine Learning. TS. doi:10.1287/trsc.2025.0105. Relevance: RAM.
- [bayram2023] Bayram, Yıldız, Farham (2023). Hub Network Design Problem with Capacity, Congestion, and Stochastic Demand Considerations. TS. doi:10.1287/trsc.2022.0112. Relevance: Spaceport.
- [cadarso2023] Cadarso, Vaze (2023). Passenger-Centric Integrated Airline Schedule and Aircraft Recovery. TS. doi:10.1287/trsc.2022.1174. Relevance: RAM.
- [wei2022] Wei, Vaze, Jacquillat (2022). Choice-Based Airline Schedule Design and Fleet Assignment: A Decomposition Approach. TS. doi:10.1287/trsc.2022.1141. Relevance: Both.
- [birolini2021] Birolini et al. (2021). Integrated Flight Scheduling and Fleet Assignment with Improved Supply-Demand Interactions. TR-B. https://ideas.repec.org/a/eee/transb/v149y2021icp162-180.html. Relevance: Both.
- [wei2020] Wei, Vaze, Jacquillat (2020). Airline Timetable Development and Fleet Assignment Incorporating Passenger Choice. TS. doi:10.1287/trsc.2019.0924. Relevance: Spaceport.
- [lee2020] Lee, Marla, Jacquillat (2020). Dynamic Disruption Management in Airline Networks Under Airport Operating Uncertainty. TS. doi:10.1287/trsc.2020.0983. Relevance: RAM.

### Dynamic network flows
- [ts-cost2025] authors not captured (2025). Cost Function Approximation for the Dynamic Scheduled Service Network Design Problem. TS. doi:10.1287/trsc.2025.0428. Relevance: Both.
- [ts-cross2025] authors not captured (2025). Cross-Dock Trailer Scheduling with Workforce Constraints: A Dynamic Discretization Discovery Approach. TS. doi:10.1287/trsc.2023.0406. Relevance: Both.
- [hewitt2023] Hewitt, Lehuede (2023). New formulations for the Scheduled Service Network Design Problem. TR-B. https://ideas.repec.org/a/eee/transb/v172y2023icp117-133.html. Relevance: Both.
- [marshall2021] Marshall, Boland, Savelsbergh, Hewitt (2021). Interval-Based Dynamic Discretization Discovery for Solving the Continuous-Time Service Network Design Problem. TS. doi:10.1287/trsc.2020.0994. Relevance: Both.
- [vu2020] Vu, Hewitt, Boland, Savelsbergh (2020). Dynamic Discretization Discovery for Solving the Time-Dependent Traveling Salesman Problem with Time Windows. TS. doi:10.1287/trsc.2019.0911. Relevance: Both.
- [scherr2020] Scherr, Hewitt, Neumann-Saavedra, Mattfeld (2020). Dynamic discretization discovery for the service network design problem with mixed autonomous fleets. TR-B. doi:10.1016/j.trb.2020.09.009. Relevance: Both.

### Hub location
- [ts-demand2025] authors not captured (2025). Demand-Driven Hub Network Design Under Uncertainty for Less-Than-Truckload Carriers. TS. doi:10.1287/trsc.2025.0180. Relevance: Spaceport.
- [rostami2022] Rostami, Chitsaz, Arslan, Laporte, Lodi (2022). Single Allocation Hub Location with Heterogeneous Economies of Scale. OR. doi:10.1287/opre.2021.2185. Relevance: Spaceport.
- [ghaffarinasab2022] Ghaffarinasab, Kara, Campbell (2022). The stratified p-hub center and p-hub maximal covering problems. TR-B. https://ideas.repec.org/a/eee/transb/v157y2022icp120-148.html. Relevance: Spaceport.
- [wandelt2022] Wandelt, Dai, Zhang, Sun (2022). Toward a Reference Experimental Benchmark for Solving Hub Location Problems. TS. doi:10.1287/trsc.2021.1094. Relevance: Spaceport.
- [yildiz2021] Yıldız, Yaman, Karaşan (2021). Hub Location, Routing, and Route Dimensioning: Strategic and Tactical Intermodal Transportation Hub Network Design. TS. https://ideas.repec.org/a/inm/ortrsc/v55y2021i6p1351-1369.html. Relevance: Spaceport.
- [taherkhani2021] Taherkhani, Alumur, Hosseini (2021). Robust Stochastic Models for Profit-Maximizing Hub Location Problems. TS. doi:10.1287/trsc.2021.1064. Relevance: Spaceport.
- [taherkhani2020] Taherkhani, Alumur, Hosseini (2020). Benders Decomposition for the Profit Maximizing Capacitated Hub Location Problem with Multiple Demand Classes. TS. doi:10.1287/trsc.2020.1003. Relevance: Spaceport.
- [wang2020a] Wang, Chen, Liu (2020). Distributionally Robust Hub Location. TS. doi:10.1287/trsc.2019.0948. Relevance: Spaceport.

### Service network design
- [malik2026] Malik, Chakraborty, Jayaswal (2026). E-Commerce Middle-Mile Network Design with Delivery Speed Choices and Service Level Constraints. TS. doi:10.1287/trsc.2024.0930. Relevance: Spaceport.
- [shu2024] Shu, Xu, Baldacci (2024). Incorporating Holding Costs in Continuous-Time Service Network Design: New Model, Relaxation, and Exact Algorithm. TS. doi:10.1287/trsc.2022.0104. Relevance: Spaceport.
- [hewitt2022] Hewitt (2022). The Flexible Scheduled Service Network Design Problem. TS. doi:10.1287/trsc.2021.1114. Relevance: Spaceport.
- [ts-robust2020] authors not captured (2020). Robust Service Network Design Under Demand Uncertainty. TS. doi:10.1287/trsc.2019.0935. Relevance: Spaceport.

### Liner/feeder shipping
- [xia2025] Xia, Xu, Baldacci (2025). A Simultaneous Column-and-Row Generation Solution Method for Liner Shipping Network Design. OR. doi:10.1287/opre.2020.0458. Relevance: Spaceport.
- [zhang2025] Zhang, Wang, Xin (2025). Liner fleet deployment and slot allocation problem: a distributionally robust optimization model with joint chance constraints. TR-B. doi:10.1016/j.trb.2025.103236. Relevance: Spaceport.
- [zhang2022] Zhang, Zheng, Teo (2022). Schedule reliability in liner shipping timetable design: a convex programming approach. TR-B. doi:10.1016/j.trb.2021.11.010. Relevance: Spaceport.
- [jin2021] Jin, Meng, Wang (2021). Feeder vessel routing and transshipment coordination at a congested hub port. TR-B. doi:10.1016/j.trb.2021.07.002. Relevance: Spaceport.
- [koza2020] Koza, Desaulniers, Ropke (2020). Integrated Liner Shipping Network Design and Scheduling. TS. doi:10.1287/trsc.2018.0888. Relevance: Spaceport.

### Air cargo/express network design
- [erera2025] Erera et al. (2025). Outbound Load Planning in Parcel Delivery Service Networks Using Machine Learning and Optimization. TS. doi:10.1287/trsc.2024.0672. Relevance: Spaceport.
- [kinene2024] Kinene, Birolini (full author list unconfirmed) (2024). Optimization of subsidized air transport networks using electric aircraft. TR-B. sciencedirect pii:S0191261524001899. Relevance: Both.
- [greening2023] Greening, Dahan, Erera (2023). Lead-Time-Constrained Middle-Mile Consolidation Network Design with Fixed Origins and Destinations. TR-B. sciencedirect pii:S0191261523001078. Relevance: Spaceport.
- [baubaid2023] Baubaid, Boland, Savelsbergh (2023). The Dynamic Freight Routing Problem for Less-Than-Truckload Carriers. TS. doi:10.1287/trsc.2022.1190. Relevance: Spaceport.
- [birolini2021a] Birolini, Jacquillat, Cattaneo, Antunes (2021). Airline Network Planning: Mixed-Integer Non-convex Optimization with Demand-Supply Interactions. TR-B. doi:10.1016/j.trb.2021.09.003. Relevance: Both.
- [baubaid2021] Baubaid, Boland, Savelsbergh (2021). The Value of Limited Flexibility in Service Network Designs. TS. doi:10.1287/trsc.2020.1009. Relevance: Spaceport.

### Multi-echelon & synchronization
- [sluijk2023] Sluijk, Florio, Kinable, Dellaert, Van Woensel (2023). A Chance-Constrained Two-Echelon Vehicle Routing Problem with Stochastic Demands. TS. doi:10.1287/trsc.2022.1162. Relevance: Spaceport.
- [marques2022] Marques, Sadykov, Deschamps, Dupas (2022). A Branch-Cut-and-Price Approach for the Single-Trip and Multi-Trip Two-Echelon Vehicle Routing Problem with Time Windows. TS. doi:10.1287/trsc.2022.1136. Relevance: Spaceport.
- [mhamedi2022] Mhamedi, Andersson, Cherkesly, Desaulniers (2022). A Branch-Price-and-Cut Algorithm for the Two-Echelon Vehicle Routing Problem with Time Windows. TS. doi:10.1287/trsc.2021.1092. Relevance: Spaceport.

### Time-window/periodic/launch scheduling
- [agra2022] Agra, Rodrigues (2022). Distributionally robust optimization for the berth allocation problem under uncertainty. TR-B. https://ideas.repec.org/a/eee/transb/v164y2022icp1-24.html. Relevance: Spaceport.

### Transit feeder design
- [trb-bus2023] authors not captured (2023). The bus synchronization timetabling problem with dwelling times. TR-B. sciencedirect pii:S0191261523000905. Relevance: Spaceport.
- [bertsimas2021] Bertsimas, Ng, Yan (2021). Data-Driven Transit Network Design at Scale. OR. doi:10.1287/opre.2020.2057. Relevance: Spaceport.
- [pinto2020] Pinto, Hyland, Mahmassani, Verbas (2020). Joint design of multimodal transit networks and shared autonomous mobility fleets. TR-C. doi:10.1016/j.trc.2019.06.010. Relevance: Spaceport.

### Emerging-tech network design
- [zhen2025] Zhen et al. (2025). Optimizing an On-Demand Delivery Mode Based on Trucks and Drones. TS. doi:10.1287/trsc.2024.0693. Relevance: Spaceport.
- [mahmutogullari2024] Mahmutoğulları, Yaman (2024). Mathematical formulations for the multi-period alternative fuel refueling station location problem with routing under decision-dependent flow dynamics. TR-B. doi:10.1016/j.trb.2024.102999. Relevance: Spaceport.
- [ts-orienteering2023] authors not captured (2023). The Orienteering Problem with Drones. TS. doi:10.1287/trsc.2023.0003. Relevance: Spaceport.
- [ts-cooperative2022] authors not captured (2022). Cooperative Learning for Smart Charging of Shared Autonomous Vehicle Fleets. TS. doi:10.1287/trsc.2022.1187. Relevance: Both.
- [ts-robust2022] authors not captured (2022). Robust Charging Network Planning for Metropolitan Taxi Fleets. TS. doi:10.1287/trsc.2022.0207. Relevance: Both.
- [ts-traveling2022] authors not captured (2022). The Traveling Salesman Problem with Drones: The Benefits of Retraversing the Arcs. TS. doi:10.1287/trsc.2022.0230. Relevance: Spaceport.
- [ts-charging2021] authors not captured (2021). Charging Station Location and Sizing for Electric Vehicles Under Congestion. TS. doi:10.1287/trsc.2021.0494. Relevance: Both.
- [ts-coordinated2021] authors not captured (2021). Coordinated Logistics with a Truck and Multiple Sidekicks. TS. doi:10.1287/trsc.2021.0485. Relevance: Spaceport.
- [roberti2021] Roberti, Ruthmair (2021). Exact Methods for the Traveling Salesman Problem with Drone. TS. doi:10.1287/trsc.2020.1017. Relevance: Spaceport.
- [dukkanci2021] Dukkanci, Kara, Bektaş (2021). Minimizing energy and cost in range-limited drone deliveries with speed optimization. TR-C. doi:10.1016/j.trc.2021.102985. Relevance: Spaceport.
- [cheng2020] Cheng, Adulyasak, Rousseau (2020). Drone routing with energy function: Formulation and exact algorithm. TR-B. doi:10.1016/j.trb.2020.06.011. Relevance: Spaceport.
- [ts-exact2020] authors not captured (2020). Exact and Heuristic Algorithms for the Carrier–Vehicle Traveling Salesman Problem. TS. doi:10.1287/trsc.2020.0999. Relevance: Spaceport.
- [dayarian2020] Dayarian, Savelsbergh, Clarke (2020). Same-Day Delivery with Drone Resupply. TS. doi:10.1287/trsc.2019.0944. Relevance: Spaceport.

### Fleet sizing & capacity expansion
- [or-budget2025] authors not captured (2025). Budget-Driven Multiperiod Hub Location: A Robust Time-Series Approach. OR. doi:10.1287/opre.2022.0319. Relevance: Spaceport.
- [ts-dynamic2025] authors not captured (2025). Dynamic Facility Location Under Cumulative Customer Demand. TS. doi:10.1287/trsc.2025.0104. Relevance: Spaceport.
- [shehadeh2023] Shehadeh (2023). Distributionally Robust Optimization Approaches for a Stochastic Mobile Facility Fleet Sizing, Routing, and Scheduling Problem. TS. doi:10.1287/trsc.2022.1153. Relevance: Spaceport.
- [gong2023] Gong, Zhang, Liu, Graham (2023). The effects of airport capacity expansion under responsive airlines and elastic passenger demand. TR-B. https://ideas.repec.org/a/eee/transb/v170y2023icp48-76.html. Relevance: Both.
- [trb-operations2022] authors not captured (2022). Operations design for high-velocity intra-city package service. TR-B. https://ideas.repec.org/a/eee/transb/v161y2022icp150-168.html. Relevance: Spaceport.
- [vanlieshout2021] Van Lieshout (2021). Integrated Periodic Timetabling and Vehicle Circulation Scheduling. TS. doi:10.1287/trsc.2020.1024. Relevance: Spaceport.
- [trb-hybrid2020] authors not captured (2020). A hybrid algorithm for the static bike-sharing re-positioning problem based on an effective clustering strategy. TR-B. https://ideas.repec.org/a/eee/transb/v140y2020icp1-21.html. Relevance: Spaceport.
````
