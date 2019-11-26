# cache-cpi-experiments
Experiments to simulate multiple cache hierarchies, L1/L2 set-associativities, block sizes using DineroIV, and measure impact on Cycles Per Instruction (CPI) and Average Memory Access Time (AMAT).

# Prerequisites

* Python3 (tested on 3.7)
	- Install `terminaltables` using `pip3 install terminaltables`
* DineroIV binary in the current working directory

# Simulations
The first part of the simulation uses a split 64K `n`-way associative L1 cache with a block size of `b`. `n` is varied between (1, 2, 4) and `b` is varied between `(32, 64)`B. 

The second part of the simulation adds a unified 128K `n`-way associated L2 cache with a block size of `b`. `n` is varied between (1, 2, 4) and `b` is varied between `(32, 64)`. Each combination of L2 is simulated for each combination of L1 discussed above.

In each case, cycles per instruction is calculated.

# License
MIT
