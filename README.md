## Luxembourg SUMO Traffic (LuST) Scenario

Contacts: Lara CODECA [codeca@gmail.com], VehicularLab [vehicular-lab@uni.lu]

This project is licensed under the terms of the MIT license.

#### Publication:

Lara CODECA, Raphael FRANK, Thomas ENGEL. December 2015. *Luxembourg SUMO Traffic (LuST) Scenario: 24 Hours of Mobility for Vehicular Networking Research* in Proceedings of the 7th IEEE Vehicular Networking Conference (VNC15).

[Get BibTeX](https://github.com/lcodeca/LuSTScenario/BibTeX.bib)

#### How To:
LuST Scenario can be lunched directly with four configuration files.
* Mobility: shortest path with rerouting.
  * `sumo -c LuSTScenario.dua.complete.mobility.static.sumocfg` with static traffic lights.
  * `sumo -c LuSTScenario.dua.complete.mobility.actuated.sumocfg` with actuated traffic lights.
* Mobility: Dynamic user equilibrium.
  * `sumo -c LuSTScenario.due.complete.mobility.static.sumocfg` with static traffic lights.
  * `sumo -c LuSTScenario.due.complete.mobility.actuated.sumocfg` with actuated traffic lights.

*A special thanks to Matěj Kubička [matej@matejk.cz] for his contribution to the network topology.*
