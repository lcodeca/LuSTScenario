## How To:
LuST Scenario can be lunched directly with four configuration files.
* Mobility: shortest path with rerouting.
  * `sumo -c dua.static.sumocfg` with static traffic lights.
  * `sumo -c dua.actuated.sumocfg` with actuated traffic lights.
* Mobility: Dynamic user equilibrium.
  * `sumo -c due.static.sumocfg` with static traffic lights.
  * `sumo -c due.actuated.sumocfg` with actuated traffic lights.

### Simulations summary

```
SUMO Version 0.27.0
 Build features: x86_64-apple-darwin15.5.0 InternalLanes DoublePrecision TRACI PROJ GDAL GUI Python
 Copyright (C) 2001-2016 DLR and contributors; http://sumo.dlr.de
 License GPLv3+: GNU GPL Version 3 or later <http://gnu.org/licenses/gpl.html>
 Use --help to get the list of options.
```

##### sumo -c dua.static.sumocfg
```
Simulation ended at time: 88161.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 3219155ms
 Real time factor: 27.3864
 UPS: 60050.936969
Vehicles:
 Inserted: 287034 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 55 (Collisions: 12, Jam: 25, Yield: 5, Wrong Lane: 13)
Emergency Stops: 2

DijkstraRouterTT answered 533322 queries and explored 1862.17 edges on average.
DijkstraRouterTT spent 422135ms answering queries (0.79ms on average).
```

##### sumo -c dua.actuated.sumocfg
```
Simulation ended at time: 87939.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 3227580ms
 Real time factor: 27.2461
 UPS: 60118.433006
Vehicles:
 Inserted: 286987 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 24 (Collisions: 15, Yield: 1, Wrong Lane: 8)
Emergency Stops: 3

DijkstraRouterTT answered 540635 queries and explored 1861.34 edges on average.
DijkstraRouterTT spent 427299ms answering queries (0.79ms on average).
```

##### sumo -c due.static.sumocfg
```
Simulation ended at time: 88226.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2288601ms
 Real time factor: 38.5502
 UPS: 86078.456227
Vehicles:
 Inserted: 284184 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 102 (Collisions: 9, Jam: 37, Yield: 45, Wrong Lane: 11)
```

##### sumo -c due.actuated.sumocfg
```
Simulation ended at time: 88375.00
Reason: All vehicles have left the simulation.
Performance:
 Duration: 2326824ms
 Real time factor: 37.981
 UPS: 87747.148474
Vehicles:
 Inserted: 284349 (Loaded: 288250)
 Running: 0
 Waiting: 0
Teleports: 767 (Collisions: 7, Jam: 224, Yield: 378, Wrong Lane: 158)
```

## LuST Scenario Files
#### Configuration files:
* [dua.actuated.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/dua.actuated.sumocfg): SUMO configuration file that uses the shortest path traces with rerouting and actuated traffic lights.
* [dua.static.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/dua.static.sumocfg): SUMO configuration file that uses the shortest path traces with rerouting and static traffic lights.
* [due.actuated.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/due.actuated.sumocfg): SUMO configuration file that uses the dynamic user equilibrium traces with rerouting and actuated traffic lights.
* [due.static.sumocfg](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/due.static.sumocfg): SUMO configuration file that uses the dynamic user equilibrium traces with rerouting and static traffic lights.

#### Network files:
* [lust.net.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/lust.net.xml) is the SUMO net file with actuated traffic lights.
* [tll.static.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/tll.static.xml) is the alternative file with static traffic lights.

#### Mobility files:
* [buslines.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/buslines.rou.xml) contains the routes for the buses.
* [transit.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/transit.rou.xml) contain the routes for the vehicles (no buses) with origin and destination outside to the city.
* [DUARoutes/local.*.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/DUARoutes) contain the shortest path routes for the vehicles (no buses) with origin, destination, or both of them, internal to the city.
* [DUERoutes/local.actuated.*.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/DUERoutes) contain the dynamic user equilibrium routes (with actuated traffic lights) for the vehicles (no buses) with origin, destination, or both of them, internal to the city.
* [DUERoutes/local.static.*.rou.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/DUERoutes) contain the dynamic user equilibrium routes (with static traffic lights) for the vehicles (no buses) with origin, destination, or both of them, internal to the city.

#### Additional files:
* [vtypes.add.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/vtypes.add.xml) contains the vehicles definition.
* [busstops.add.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/busstops.add.xml) contains the bus stops definition.
* [e1detectors.add.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/e1detectors.add.xml) contains the inductive loops definition.
* [lust.poly.xml](https://github.com/lcodeca/LuSTScenario/blob/master/scenario/lust.poly.xml) contains the polygons definition (buildings and parking lots).

#### Miscellanea:
* [lust.legacy.scenario.osm](https://github.com/lcodeca/LuSTScenario/blob/master/misc/lust.legacy.scenario.osm) contains the definition of the network in OpenStreetMap fromat.
* [lust.polygons.osm](https://github.com/lcodeca/LuSTScenario/blob/master/misc/lust.polygons.osm) contains the definition of the polygons in OpenStreetMap format.

* [polygonTypes.xml](https://github.com/lcodeca/LuSTScenario/blob/master/misc/polygonTypes.xml) contains the definition of the polygons types for *polyconvert*.
