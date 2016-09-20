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
SUMO Version 0.27.0
 Build features: x86_64-apple-darwin15.5.0 InternalLanes DoublePrecision TRACI PROJ GDAL GUI Python
 Copyright (C) 2001-2016 DLR and contributors; http://sumo.dlr.de
 License GPLv3+: GNU GPL Version 3 or later <http://gnu.org/licenses/gpl.html>
 Use --help to get the list of options.
```

##### sumo -c LuSTScenario.dua.complete.mobility.static.sumocfg
```
Simulation ended at time: 88073.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2803119ms
 Real time factor: 31.4196
 UPS: 68748.496229
Vehicles:
 Inserted: 287015 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 73 (Collisions: 12, Jam: 47, Wrong Lane: 14)
Emergency Stops: 3

DijkstraRouterTT answered 634608 queries and explored 1632.82 edges on average.
DijkstraRouterTT spent 344611ms answering queries (0.54ms on average).
```

##### sumo -c LuSTScenario.dua.complete.mobility.actuated.sumocfg
```
Simulation ended at time: 87647.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2472924ms
 Real time factor: 35.4427
 UPS: 68029.329247
Vehicles:
 Inserted: 287239 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 37 (Collisions: 8, Jam: 24, Yield: 1, Wrong Lane: 4)
Emergency Stops: 2

DijkstraRouterTT answered 571809 queries and explored 1637.87 edges on average.
DijkstraRouterTT spent 316620ms answering queries (0.55ms on average).
```

##### sumo -c LuSTScenario.due.complete.mobility.static.sumocfg
```
Simulation ended at time: 88746.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2102590ms
 Real time factor: 42.2079
 UPS: 91152.355904
Vehicles:
 Inserted: 284208 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 169 (Collisions: 26, Jam: 49, Yield: 36, Wrong Lane: 58)
```

##### sumo -c LuSTScenario.due.complete.mobility.actuated.sumocfg
```
Simulation ended at time: 87557.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 1966648ms
 Real time factor: 44.5209
 UPS: 95726.369437
Vehicles:
 Inserted: 286007 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 468 (Collisions: 14, Jam: 246, Yield: 165, Wrong Lane: 43)
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
