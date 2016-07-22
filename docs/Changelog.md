## LuST Scenario v2.0
The scenario has been tested with **SUMO 0.26.0**

#### Network:
* fixed various intersections and eges.
* changed the TLS to actuaded in the main net file.
* added an additional file with the static TLS.

#### Traffic demand:
* mobility over 24 hours
  * shortest path (same for both static and actuated TLS)
  * dynamic user equilibrium for static TLS
  * dynamic user equilibrium for actuated TLS

## LuST Scenario v1.1
The scenario has been tested with **SUMO 0.23.0**

**IMPORTANT:** We decided to keep the configuration file with **threads**, however we are incurring in several random crashes of the simulation while using the thread option. We already asked to the SUMO developers about it, and they confirmed that SUMO suses libfox1.6 to implement the threads so different packages of the library may result in different behaviours in different system. We tested it with Mac OSX 10.10.3 and Ubuntu 14.04.2 LTS and in both cases we had random crashes. You are welcome to try on your system and report the outcome.

#### Traffic demand:
* the new traffic demand improves the three rush hours (morning, lunch and evening).
* the **internal mobility** represent:
  * the local traffic (source and destination are internal);
  * the incoming traffic (source is outside the city, destination is inside the city);
  * the outgoing traffic (source is inside the city, destination is outside the city).
* the **external mobility** represent that portion of traffic with both source and destination outside the city. (Note: the external mobility alone is not representative of the traffic on the highways.)

#### Polygons:
* fixed the position of more polygons.
