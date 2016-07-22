## How To:
LuST Scenario can be lunched directly with four configuration files.
* Mobility: shortest path with rerouting.
  * `sumo -c LuSTScenario.dua.complete.mobility.static.sumocfg` with static traffic lights.
  * `sumo -c LuSTScenario.dua.complete.mobility.actuated.sumocfg` with actuated traffic lights.
* Mobility: Dynamic user equilibrium.
  * `sumo -c LuSTScenario.due.complete.mobility.static.sumocfg` with static traffic lights.
  * `sumo -c LuSTScenario.due.complete.mobility.actuated.sumocfg` with actuated traffic lights.

### Simulations summary

```
SUMO Version 0.26.0
 Build features: x86_64-apple-darwin15.4.0 InternalLanes DoublePrecision TRACI PROJ GDAL GUI Python
 Copyright (C) 2001-2016 DLR and contributors; http://sumo.dlr.de
```

##### sumo -c LuSTScenario.dua.complete.mobility.static.sumocfg
```
Simulation ended at time: 87475.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2464790ms
 Real time factor: 35.4898
 UPS: 80800.560291
Vehicles:
 Inserted: 286990 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 1706 (Collisions: 179, Jam: 877, Yield: 373, Wrong Lane: 277)
Emergency Stops: 1170

DijkstraRouterTT answered 621923 queries and explored 1757.04 edges on average.
DijkstraRouterTT spent 335328ms answering queries (0.54ms on average).
```

##### sumo -c LuSTScenario.dua.complete.mobility.actuated.sumocfg
```
Simulation ended at time: 87356.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2049967ms
 Real time factor: 42.6134
 UPS: 76293.166670
Vehicles:
 Inserted: 287190 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 148 (Collisions: 117, Jam: 20, Wrong Lane: 11)
Emergency Stops: 577

DijkstraRouterTT answered 544744 queries and explored 1799.94 edges on average.
DijkstraRouterTT spent 279218ms answering queries (0.51ms on average).
```

##### sumo -c LuSTScenario.due.complete.mobility.static.sumocfg
```
Simulation ended at time: 87438.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 1492003ms
 Real time factor: 58.6044
 UPS: 103749.562836
Vehicles:
 Inserted: 285852 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 181 (Collisions: 118, Jam: 21, Yield: 15, Wrong Lane: 27)
Emergency Stops: 672
```

##### sumo -c LuSTScenario.due.complete.mobility.actuated.sumocfg
```
Simulation ended at time: 87237.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 1722387ms
 Real time factor: 50.6489
 UPS: 81932.401371
Vehicles:
 Inserted: 287050 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 111 (Collisions: 66, Jam: 8, Yield: 7, Wrong Lane: 30)
Emergency Stops: 409
```
## LuST Scenario Files
#### Configuration files:
* [LuSTScenario.dua.complete.mobility.actuated.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.dua.complete.mobility.actuated.sumocfg): SUMO configuration file that uses the shortest path traces with rerouting and actuated traffic lights.
* [LuSTScenario.dua.complete.mobility.static.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.dua.complete.mobility.static.sumocfg): SUMO configuration file that uses the shortest path traces with rerouting and static traffic lights.
* [LuSTScenario.due.complete.mobility.actuated.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.due.complete.mobility.actuated.sumocfg): SUMO configuration file that uses the dynamic user equilibrium traces with rerouting and actuated traffic lights.
* [LuSTScenario.due.complete.mobility.static.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.due.complete.mobility.static.sumocfg): SUMO configuration file that uses the dynamic user equilibrium traces with rerouting and static traffic lights.

#### Network files:
* [LuSTScenario.net.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.net.xml) is the SUMO net file with actuated traffic lights.
* [LuSTScenario.tll.static.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.tll.static.xml) is the alternative file with static traffic lights.

#### Mobility files:
* [LuSTScenario.busLines.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.busLines.rou.xml) contains the routes for the buses.
* [LuSTScenario.transit.mobility.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.transit.mobility.rou.xml) contain the routes for the vehicles (no buses) with origin and destination outside to the city.
* [DUARoutes/LuSTScenario.local.mobility.*.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/DUARoutes) contain the shortest path routes for the vehicles (no buses) with origin, destination, or both of them, internal to the city.
* [DUERoutes/LuSTScenario.local.mobility.*.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/DUERoutes) contain the dynamic user equilibrium routes (with actuated traffic lights) for the vehicles (no buses) with origin, destination, or both of them, internal to the city.
* [DUERoutes/LuSTScenario.local.mobility.*.static.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/DUERoutes) contain the dynamic user equilibrium routes (with static traffic lights) for the vehicles (no buses) with origin, destination, or both of them, internal to the city.

#### Additional files:
* [LuSTScenario.vtypes.add.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.vtypes.add.xml) contains the vehicles definition.
* [LuSTScenario.busStops.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.busStops.xml) contains the bus stops definition.
* [LuSTScenario.indLoops.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.indLoops.xml) contains the inductive loops definition.
* [LuSTScenario.poly.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/LuSTScenario.poly.xml) contains the polygons definition (buildings and parking lots).

#### Miscellanea:
* [LuSTScenario.osm](https://github.com/lcodeca/LuSTScenario/blob/master/misc/LuSTScenario.osm) contains the OpenStreetMap definition of the network.
* [LuST.polygons.osm](https://github.com/lcodeca/LuSTScenario/blob/master/misc/LuST.polygons.osm) contains the OpenStreetMap definition of the polygons.
