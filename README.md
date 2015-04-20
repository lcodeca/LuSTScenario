# LuSTScenario
Luxembourg SUMO Traffic (LuST) Scenario

Author: Lara CODECA [lara.codeca@uni.lu]

The MIT License (MIT)

Copyright (c) 2015 Lara CODECA [lara.codeca@uni.lu], VehicularLab [vehicular-lab@uni.lu]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


#How To Use:
LuST Scenario can be used as any other standard SUMO (SUMO version 0.23.0) scenario.
The conf_complete_LuSTScenario.sumo.cfg file contains all the configuration information and can be used with sumo -c conf_complete_LuSTScenario.sumo.cfg.

Concerning the files:
- LuSTScenario.net.xml is the SUMO net file.
- LuSTScenario.vehOnly.rou.xml contains the routes for the vehicles (no buses).
- LuSTScenario.duarouter.busLines.rou.xml contains the routes for the buses.
- vtypes.add.xml contains the vehicles definition.
- LuSTScenario.busStops.xml contains the bus stops definition.
- LuSTScenario.indLoops.xml contains the inductive loops definition.
- LuSTScenario.poly.xml contains the polygons definition (buildings and parking lots).