---
layout: default
title: RAAW
---
<!--
Text can be **bold**, _italic_, or ~~strikethrough~~.
[Link to another page](./another-page.html).
-->

# Renegotiating the Levels of Abstraction for the Post Moore's Law Era
### A Workshop at the ARM Research Summit, September 15-19, 2019

Several industrial trends are conspiring together to threaten the traditionally expected generational scaling of compute performance: the exponential growth in the scale of data, the commensurate rise in computationally intensive techniques to extract meaning from this deluge (e.g. ML, CV, Graph Analytics), and most of all, the impending end of Moore’s Law.

Given this, there is abundant pressure across the traditional levels of abstraction: new domain-specific languages can expose parallelism that is otherwise difficult for compilers to analyze. Similarly, new compilers and IRs are emerging to facilitate deployment of custom hardware and programmable accelerators.  These in turn rely on non-traditional, explicitly concurrent, non-Von-Neumann execution models, often exposing much more of their microarchitectural mechanisms in order to maximize throughput, compute efficiency and density.

As with other such disruptive moments, this one is also characterized by a gold-rush attempt to provide spot-fixes to a diverse set of problems, in isolation, and often in incompatible ways - languages may be developed with little attention paid to their execution efficiency, while programmable accelerators may be designed with limited insight into the difficulty of compiling/porting their target applications to run on them.

This workshop will attempt to bring together researchers who are working across the various levels of abstraction into the same room, in the hope that people working in different levels may gain insight into the objectives, constraints, and expectations of the others.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-top-width:1px;border-bottom-width:1px;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-top-width:1px;border-bottom-width:1px;border-color:black;}
.tg .tg-4fps{background-color:#efefef;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-cl49{background-color:#f7f793;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-o7qv{background-color:#c2d69b;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-zefg{background-color:#c0c0c0;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-pylb{background-color:#b2a1c7;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-yp4f{background-color:#b3d7ff;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-as4m{background-color:#fabf8f;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
.tg .tg-5v9j{background-color:#d99594;color:#000000;border-color:#000000;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-zefg">Abstractions</th>
    <th class="tg-zefg">Yesterday</th>
    <th class="tg-zefg">Today &amp; Tomorrow?</th>
  </tr>
  <tr>
    <td class="tg-pylb">Applications &amp; Algorithms</td>
    <td class="tg-4fps">Abstracted from hardware, parallelism the primary concern</td>
    <td class="tg-4fps">Codesigned for the underlying hardware execution model</td>
  </tr>
  <tr>
    <td class="tg-yp4f">Languages</td>
    <td class="tg-4fps">Imperative, shared memory, C, C++, OpenCL, OpenMP</td>
    <td class="tg-4fps">Functional, DSLs,partitioned memory</td>
  </tr>
  <tr>
    <td class="tg-o7qv">Compilers &amp; IRs</td>
    <td class="tg-4fps">LLVM, GCC</td>
    <td class="tg-4fps">Relay, NNVM, MLIR, GLOW, HPVM, DLVM…</td>
  </tr>
  <tr>
    <td class="tg-cl49">Execution Models &amp; Runtimes</td>
    <td class="tg-4fps">Imperative, SIMD, SIMT</td>
    <td class="tg-4fps">BSP, Dataflow, FSM, Streaming Task Graphs...</td>
  </tr>
  <tr>
    <td class="tg-as4m">Architectures</td>
    <td class="tg-4fps">Von Neumann, threaded, Warp-based, shared memory</td>
    <td class="tg-4fps">“non-Von Neumann”: Decentralized, explicitly parallel, communication-centric, task parallel, restricted Von-Neumann, Heterogeneous...</td>
  </tr>
  <tr>
    <td class="tg-5v9j">Micro-architectures</td>
    <td class="tg-4fps">Pipelined, restricted dynamic dataflow; SIMT/Warp-based</td>
    <td class="tg-4fps">“Spatial”: MPPAs, CGRAs, FPGAs, custom hardware...</td>
  </tr>
</table>

# Goals:
Broadly our goal is to bring together researchers doing work across DSLs, compilers, architecture, and accelerator communities.  We hope to spark interest in some open cross-cutting questions, for example:

* What is the nature of the key applications (incl. algorithms, and datastructures) looking forward over the next decade?
* What are the compute, memory, interconnect, bandwidth, scaling etc. requirements?
* What is the right compiler IR for accelerators?  (how general, how to deal with heterogeneous architecture capabilities)
* What are the principles around designing accelerators ISAs?
* Is design space exploration across all levels possible/valuable?
* How do these insights help us... 
    * Renegotiate the levels of abstraction, design the appropriate DSLs, Compilers & IRs, Runtimes, Architectures and Microarchitectures, with the goal of continuing with traditional expectations of ease-of-use and productivity
    * … while also providing energy efficiency, performance density and scalability, post Moore’s law?

