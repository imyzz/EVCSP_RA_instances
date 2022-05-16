# EVCSP_RA_instances
This repository contains the instances used for electric vehicle charging scheduling problem presented at paper "Electric Vehicle Charging Scheduling Problem: Heuristics and Metaheuristic approaches".

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


## Instances Description
An instance represents the charging demands during one day and have been generated as described [below](#instances-generation). All instances files are `.csv` files. Each row represents an electric vehicle. For each vehicle we have:
- Column `arrival_time` indicates the desired arrival time to the charging station in hours.
-  Column `departure_time` gives the departure time in hours.
-  Column `initial_SOC` displays the initial state of charge (SoC) of the battery expressed as a percentage.
-  Column `desired_SOC` indicates the requested state of charge (SoC) by the driver, expressed as a percentage.
- Column `battery_capacity` gives the battery capacity in (kWh) which is the maximum energy that can be stored in the battery.

## Instances generation
-Electric vehicle arrivals are randomly occurring and independent events. Therefore, the arrival time is modeled using a non-homogeneous Poisson Process with an arrival rate that varies at each hour h={1,...,24}. 
- The parking duration follows an exponential distribution with a mean parking duration that also varies over time. The departure time of each electric vehicle can be directly obtained as the sum of the arrival time and the parking duration. 
- The initial state-of-charge is considered uniformly distributed in the range of [0.2,0.7] of the capacity of the vehicle's battery. 
- The desired state-of-charge of each electric vehicle is uniformly chosen from [the initial SoC,1]. 
- The battery capacities are randomly chosen from the list of current real-world electric vehicle battery capacities 
 

## Instanes with 10 vehicles
This folder contains 15 instances generated with a number of vehicles limited to 10.

## Instanes with vehicles

| File                | Number of vehicles           |
|:--------------------|:---------------------------|


