# EVCSP_RA_instances
This repository contains the instances used for electric vehicle charging scheduling problem.

This research was done at the [laboratoire lorrain de recherche en informatique et ses applications (LORIA)](https://www.loria.fr/en/) laboratory of the [Université de Lorraine](https://www.univ-lorraine.fr/), [OPTIMIST](https://optimist.loria.fr/) Team. and the [Institut de Recherche en Informatique, Mathématiques, Automatique et Signal (IRIMAS)](https://www.irimas.uha.fr/) laboratory of the [Université de Haute-Alsace (UHA)](https://www.uha.fr/).

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


## Instances
All instances files are `.csv` files. Each row represents an electric vehicle. For each vehicle we have:
- Column `arrival_time` arrival time to the charging station in hours.
-  Column `departure_time` departure time in hours.
-  Column `initial_SOC` battery initial state of charge (SoC) (%).
-  Column `desired_SOC` battery initial state of charge (SoC) (%).
- Column `battery_capacity` battery capacity in (kWh).
- 
## Instances generation
Electric vehicle arrivals are randomly occurring and independent events. Therefore, the arrival time is modeled using a non-homogeneous Poisson Process with an arrival rate that varies $\lambda (h)$ at each hour $h=\{1,...,24\}$. 

<img src="https://latex.codecogs.com/svg.latex?\Large&space; h=\{1,...,24\}" />
The arrivals are likely high in the morning and low in the afternoon. 
The parking duration follows an exponential distribution with a mean parking duration that also varies over time. There is no correlation between the arrival time and the parking duration so the two variables can be generated independently. The departure time $d_j$ of each electric vehicle can be directly obtained with the formula $d_j = r_j + pr_j $. The initial state-of-charge $e^0_j$ at the arrival $r_j$ is considered uniformly distributed in the range of [0.2,0.7] of the capacity of the vehicle's battery. The desired state-of-charge $e^{d}_j$  of each electric vehicle $j$ is uniformly chosen from [$e^0_j$,1]. The battery capacities are randomly chosen from the list of current real-world electric vehicle battery capacities \cite{EV_Database_2020}. We generate $15$ scenarios for each case. In the first 10 scenarios of each case, the chromatic number $k$ of the interval graph corresponding to the electric vehicle charging demand instance is greater than the number of chargers, while it is less or equal in the last five scenarios. 

## Instanes with 10 vehicles

## Instanes with vehicles

| File              | Number of vehicles                     |
|:--------------------|:---------------------------|


