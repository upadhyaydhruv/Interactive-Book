---
layout: default
title:  Interactive FSM
comments: true
nav_order: 18
---

# Interactive FSM

In this module, we will learn how to implement a final state machine(FSM) that describes the functionality of a Soda vending machine:

## Problem
Suppose we have a vending machine that sells soda cans that costs a 15¢ each.
Moreover we have only 2 types of coins: 10¢ and 5¢.

Our objective is to design a state machine that determines when to dispense a can, how to return the change.
```
Note: in this design we will ignore the capacity of the stock, which means, we’ll assume that there will always be can in the vending machine.
Also, we can assume that only one action could be made in every “clock cycle” or state
```
## RULES

First give back the change then dispense the can.

## Understanding the possibilities 
There are quite few options:
1. entering no money
2. putting 5¢ followed by another 10¢ => getting the can
3. putting 10¢ followed by 10¢ => receiving  change => getting a can
4. putting 5¢ followed by 5¢ followed by followed by 10¢=> receiving  change => getting a can
5. putting 10¢ followed by 5¢ and getting the can
6. putting 5$ followed by 5¢ followed by 5¢ => getting a can.

## FSM diagram
Basically, what we’ll do now is translating the options we stated above into a flow chart/FSM diagram:

{% include fsm.html %}

Lets try the soda can vending machine and look for the corresponding state changes FSM diagram in each of the above mentioned possibilities.

{% include disqus.html %}
