# EVCSP_RA_instances
This repository contains the instances used for electric vehicle charging scheduling problem presented at paper "Electric Vehicle Charging Scheduling Problem: Heuristics and Metaheuristic approaches".

This research was done at the [laboratoire lorrain de recherche en informatique et ses applications (LORIA)](https://www.loria.fr/en/) laboratory of the [Université de Lorraine](https://www.univ-lorraine.fr/), [OPTIMIST](https://optimist.loria.fr/) Team. and the [Institut de Recherche en Informatique, Mathématiques, Automatique et Signal (IRIMAS)](https://www.irimas.uha.fr/) laboratory of the [Université de Haute-Alsace (UHA)](https://www.uha.fr/) by:

| Name                | Email                      | Institute |
|:--------------------|:---------------------------|:---------:|
| Imene Zaidi         | imene.zaidi@loria.fr       |    1,2    |
| Ammar Oulamara      | ammar.oulamara@loria.fr    |    1      |
| Lhassane Idoumghar  | lhassane.idoumghar@uha.fr  |    2      |
| Michel Basset       | michel.basset@uha.fr       |    2      |

| Ref. | Institute                                                            |
|:----:|:---------------------------------------------------------------------|
|  1   |  LORIA Laboratory UMR7503, Université de Lorraine Nancy, France      |
|  2   |  IRIMAS UR 7499, F-68100, Université de Haute-Alsace Mulhouse, France |


## Instances Description
An instance represents the charging demands during one day and have been generated as described [below](#instances-generation). All instances files are `.csv` files. Each row represents an electric vehicle. For each vehicle we have:
- Column `arrival_time` indicates the desired arrival time to the charging station in hours.
-  Column `departure_time` gives the departure time in hours.
-  Column `initial_SOC` displays the initial state of charge (SoC) of the battery expressed as a percentage.
-  Column `desired_SOC` indicates the requested state of charge (SoC) by the driver, expressed as a percentage.
- Column `battery_capacity` gives the battery capacity in (kWh) which is the maximum energy that can be stored in the battery.

## Instances generation
Electric vehicle arrivals are randomly occurring and independent events. Therefore, the arrival time is modeled using a non-homogeneous Poisson Process with an arrival rate that varies at each hour h={1,...,24}. 
- The parking duration follows an exponential distribution with a mean parking duration that also varies over time. The departure time of each electric vehicle can be directly obtained as the sum of the arrival time and the parking duration. 
- The initial state-of-charge is considered uniformly distributed in the range of [0.2,0.7] of the capacity of the vehicle's battery. 
- The desired state-of-charge of each electric vehicle is uniformly chosen from [the initial SoC,1]. 
- The battery capacities are randomly chosen from the list of current real-world electric vehicle battery capacities 
 

## Instanes with 10 vehicles
`Instances_10_EVs ` folder contains 15 instances generated with a number of vehicles limited to 10.

## Instanes with vehicles
`Instances` folder contains 45 instances.

| File                 |Number of vehicles|
|:---------------------|:-----------------|
|			scenario_1.csv 				|20																|
|			scenario_2.csv 				|29																|
|			scenario_3.csv 				|24																|
|			scenario_4.csv 				|25																|
|			scenario_5.csv 				|30																|
|			scenario_6.csv 				|27																|
|			scenario_7.csv 				|29																|
|			scenario_8.csv 				|26																|
|			scenario_9.csv 				|22																|
|			scenario_10.csv 			|22																|
|			scenario_11.csv 			|27																|
|			scenario_12.csv 			|25																|
|			scenario_13.csv 			|20																|
|			scenario_14.csv 			|23																|
|			scenario_15.csv 			|22																|
|			scenario_16.csv 			|48																|
|			scenario_17.csv 			|50																|
|			scenario_18.csv 			|59																|
|			scenario_19.csv 			|66																|
|			scenario_20.csv 			|51																|
|			scenario_21.csv 			|58																|
|			scenario_22.csv 			|53																|
|			scenario_23.csv 			|68																|
|			scenario_24.csv 			|52																|
|			scenario_25.csv 			|54																|
|			scenario_26.csv 			|40																|
|			scenario_27.csv 			|40																|
|			scenario_28.csv 			|37																|
|			scenario_29.csv 			|33																|
|			scenario_30.csv 			|39																|
|			scenario_31.csv 			|93																|
|			scenario_32.csv 			|99																|
|			scenario_33.csv 			|79																|
|			scenario_34.csv 			|102															|
|			scenario_35.csv 			|93																|
|			scenario_36.csv 			|96																|
|			scenario_37.csv 			|96																|
|			scenario_38.csv 			|112															|
|			scenario_39.csv 			|95																|
|			scenario_40.csv 			|78																|
|			scenario_41.csv 			|85																|
|			scenario_42.csv 			|82																|
|			scenario_43.csv 			|88																|
|			scenario_44.csv 			|91																|
|			scenario_45.csv 			|79																|

## License

<img align="right" src="http://opensource.org/trademarks/opensource/OSI-Approved-License-100x137.png">

USCP is licensed under the [MIT License](http://opensource.org/licenses/MIT):

Copyright &copy; 2022 [Imene ZAIDI](https://github.com/imyzz)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
