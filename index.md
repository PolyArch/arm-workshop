---
layout: default
title: Hi There!
---
<!-->
Text can be **bold**, _italic_, or ~~strikethrough~~.
[Link to another page](./another-page.html).
<!-->

# Renegotiating the Levels of Abstraction for the Post Moore's Law Era

Several industrial trends are conspiring together to threaten the traditionally expected generational scaling of compute performance: the exponential growth in the scale of data, the commensurate rise in computationally intensive techniques to extract meaning from this deluge (e.g. ML, CV, Graph Analytics), and most of all, the impending end of Moore’s Law.

Given this, there is abundant pressure across the traditional levels of abstraction: new domain-specific languages can expose parallelism that is otherwise difficult for compilers to analyze. Similarly, new compilers and IRs are emerging to facilitate deployment of custom hardware and programmable accelerators.  These in turn rely on non-traditional, explicitly concurrent, non-Von-Neumann execution models, often exposing much more of their microarchitectural mechanisms in order to maximize throughput, compute efficiency and density.

As with other such disruptive moments, this one is also characterized by a gold-rush attempt to provide spot-fixes to a diverse set of problems, in isolation, and often in incompatible ways - languages may be developed with little attention paid to their execution efficiency, while programmable accelerators may be designed with limited insight into the difficulty of compiling/porting their target applications to run on them.

This workshop will attempt to bring together researchers who are working across the various levels of abstraction into the same room, in the hope that people working in different levels may gain insight into the objectives, constraints, and expectations of the others.


This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

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

