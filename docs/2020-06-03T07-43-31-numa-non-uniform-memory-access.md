---
date: 2020-06-03T07:43:31-07:00
title: NUMA (Non-uniform Memory Access)
tags: technology
---

# NUMA (Non-uniform Memory Access)

more correctly Cache-Coherent Numa (ccNUMA). In this architecture each processor has a local bank of memory, to which it has a much closer (lower latency) access. Mean, we divide the complete available memory to each individual CPU, which will become their own local memory. In case, any CPU wants more memory, it can still access memory from other CPU, but with little higher latency.

* To compensate for memory latency effects due to some memory being closer to the processor than others.
* Useful to scale the VM for large amounts of memory
* I/O optimizations due to device NUMA effects

http://www.techplayon.com/what-is-numa-non-uniform-memory-access/