# Middlebox_Routing
## Introduction
The document here mainly includes .py files for generating the information (eg, source, destination and SFC links) of each flow and the information (eg, maximum link load and the load rate) of the links in the network. Moreover, we also generated the information of the other two benchmarks for the comparison.

## The file generated by nfv_distribution_LP.py:
### Description
**Flow_vnf.txt:** Source, SFC, destination, and traffic information for each stream.

**Flow_feasible_vnf.txt:** three possible sfc links per stream

**Alg1_NF_load.txt:** alg1 algorithm for traffic on each NF

**Alg1_max_NF:** The maximum NF load of the lag1 algorithm

## The file generated by retoute.py:
### Description
**Alg0.json:** maximum link load rate for linear solutions

**Alg1_ce.json:** the load rate of each link of the rounding solution

**Alg1_lambda.json:** maximum link load rate for rounding solution

**Alg1_entries.json:** rounding solves the flow entries used by each switch

**Alg1_max_entries.json:** rounding solution maximum switch use flow table entry

**Alg1_path.txt:** the selected path information for each stream of the rounding solution

## The file generated by retoute_compare_alg.py:
### Description
**PDA_lambda.json:** Maximum link load rate for PDA solution

**SIMPLE_lambda.json:** Maximum link load rate for PDA solution

<br/>

**PDA_ce.json:** Load rate per link for PDA solution

**SIMPLE_ce.json:** SIMPLE solution load rate per link

<br/>

**PDA_entries.json:** PDA solves the flow entries used by each switch

**SIMPLE_entries.json:** SIMPLE solves the flow entries used by each switch.

<br/>

**PDA_max_entries.json:** PDA solves the maximum switch using flow table entries

**SIMPLE_max_entries.json:** PDA solves the maximum switch using flow table entries

<br/>

**PDA_path.txt:** The selected path information for each stream of the PDA solution

**SIMPLE_path.txt:** Selected path information for each stream of the SIMPLE solution

## Summary of Workflow
First, we establish the three feasible paths for each flow in the network, including the information of SFC. Then, SIMPLE greedily finds the path with the lightest link load, and PDA greedily finds the path with the least number of flow entries.
