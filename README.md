## Luxembourg SUMO Traffic (LuST) Scenario

Contacts: Lara CODECA [codeca@gmail.com], VehicularLab [vehicular-lab@uni.lu]

This project is licensed under the terms of the MIT license.

### Important Note:
_LuST Scenario has been generated with *SUMO version 0.26* and validated with real data._
_Although it's possible to use it with more recent versions of SUMO, the resulting mobility cannot be considered validated._

#### If you need a realistic mobility scenario compatible with the new versions of SUMO, please use [MoST Scenario](https://github.com/lcodeca/MoSTScenario)

### Publications:

L. Codeca, R. Frank, S. Faye and T. Engel,
*"Luxembourg SUMO Traffic (LuST) Scenario: Traffic Demand Evaluation"*
in IEEE Intelligent Transportation Systems Magazine, vol. 9, no. 2, pp. 52-63, Summer 2017.
DOI: 10.1109/MITS.2017.2666585
URL: http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7906642&isnumber=7904753

[Get BibTeX](https://github.com/lcodeca/LuSTScenario/blob/master/BibTeX.bib)

Best paper award of VNC 2015 to Lara CODECA, Raphael FRANK, Thomas ENGEL,
*Luxembourg SUMO Traffic (LuST) Scenario: 24 Hours of Mobility for Vehicular Networking Research*
in Proceedings of the 7th IEEE Vehicular Networking Conference (VNC15), December 2015.

### How To:
LuST Scenario can be lunched directly with four configuration files.
* Mobility: shortest path with rerouting.
  * `sumo -c dua.static.sumocfg` with static traffic lights.
  * `sumo -c dua.actuated.sumocfg` with actuated traffic lights.
* Mobility: Dynamic user equilibrium.
  * `sumo -c due.static.sumocfg` with static traffic lights.
  * `sumo -c due.actuated.sumocfg` with actuated traffic lights.

*A special thanks to Matěj Kubička [matej@matejk.cz] for his contribution to the network topology.*
