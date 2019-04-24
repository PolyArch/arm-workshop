---
layout: default
title: Hi There!
---
<!--
Text can be **bold**, _italic_, or ~~strikethrough~~.
[Link to another page](./another-page.html).
-->

# Renegotiating the Levels of Abstraction for the Post Moore's Law Era

Several industrial trends are conspiring together to threaten the traditionally expected generational scaling of compute performance: the exponential growth in the scale of data, the commensurate rise in computationally intensive techniques to extract meaning from this deluge (e.g. ML, CV, Graph Analytics), and most of all, the impending end of Moore’s Law.

Given this, there is abundant pressure across the traditional levels of abstraction: new domain-specific languages can expose parallelism that is otherwise difficult for compilers to analyze. Similarly, new compilers and IRs are emerging to facilitate deployment of custom hardware and programmable accelerators.  These in turn rely on non-traditional, explicitly concurrent, non-Von-Neumann execution models, often exposing much more of their microarchitectural mechanisms in order to maximize throughput, compute efficiency and density.

As with other such disruptive moments, this one is also characterized by a gold-rush attempt to provide spot-fixes to a diverse set of problems, in isolation, and often in incompatible ways - languages may be developed with little attention paid to their execution efficiency, while programmable accelerators may be designed with limited insight into the difficulty of compiling/porting their target applications to run on them.

This workshop will attempt to bring together researchers who are working across the various levels of abstraction into the same room, in the hope that people working in different levels may gain insight into the objectives, constraints, and expectations of the others.


This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

<table class="c20"><tbody><tr class="c30"><td class="c31" colspan="1" rowspan="1"><p class="c15"><span class="c1">&hellip;</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">Yesterday</span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">Today &amp; Tomorrow?</span></p></td></tr><tr class="c10"><td class="c27" colspan="1" rowspan="1"><p class="c15"><span class="c1">Applications &amp; Algorithms</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">Abstracted from hardware, parallelism the primary concern </span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">Codesigned for the underlying hardware execution model </span></p></td></tr><tr class="c29"><td class="c21" colspan="1" rowspan="1"><p class="c15"><span class="c1">Languages</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">Imperative, shared memory, C, C++, OpenCL, OpenMP</span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">Functional, DSLs, </span></p><p class="c15"><span class="c1">partitioned memory</span></p></td></tr><tr class="c35"><td class="c31 c33" colspan="1" rowspan="1"><p class="c15"><span class="c1">Compilers &amp; IRs</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">LLVM, GCC</span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">Relay, NNVM, MLIR, GLOW, HPVM, DLVM&hellip;</span></p></td></tr><tr class="c32"><td class="c17" colspan="1" rowspan="1"><p class="c15"><span class="c1">Execution Models &amp; Runtimes</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">Imperative, SIMD, SIMT</span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">BSP, Dataflow, FSM, Streaming Task Graphs...</span></p></td></tr><tr class="c23"><td class="c28" colspan="1" rowspan="1"><p class="c15"><span class="c1">Architectures</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">Von Neumann, threaded, Warp-based, shared memory</span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">&ldquo;non-Von Neumann&rdquo;: Decentralized, explicitly parallel, communication-centric, task parallel, restricted Von-Neumann, Heterogeneous...</span></p></td></tr><tr class="c26"><td class="c19" colspan="1" rowspan="1"><p class="c15"><span class="c1">Micro-architectures</span></p></td><td class="c14" colspan="1" rowspan="1"><p class="c15"><span class="c1">Pipelined, restricted dynamic dataflow; SIMT/Warp-based</span></p></td><td class="c24" colspan="1" rowspan="1"><p class="c15"><span class="c1">&ldquo;Spatial&rdquo;: MPPAs, CGRAs, FPGAs, custom hardware...</span></p></td></tr></tbody></table>

# Goals:
Broadly our goal is to bring together researchers doing work across DSLs, compilers, architecture, and accelerator communities.  

* What is the nature of the key applications (incl. algorithms, and datastructures) looking forward over the next decade?
* What are the compute, memory, interconnect, bandwidth, scaling etc. requirements?
* What is the right compiler IR for accelerators?  (how general, how to deal with heterogeneous architecture capabilities)
* What are the principles around designing accelerators ISAs?
* Is design space exploration across all levels possible/valuable?
* How do these insights help us... 
    * Renegotiate the levels of abstraction, design the appropriate DSLs, Compilers & IRs, Runtimes, Architectures and Microarchitectures, with the goal of continuing with traditional expectations of ease-of-use and productivity
    * … while also providing energy efficiency, performance density and scalability, post Moore’s law?

