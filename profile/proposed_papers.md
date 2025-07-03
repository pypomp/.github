
# Current projects related to pypomp

* This list is updated as of 25-07-02. 

* It is designed to help coordinate the researchers involved in pypomp. Titles and author lists of working papers are open to changes. Author lists are based in part on expected future contributions as well as past contributions - when the papers are completed, we can make any necessary changes if we agree that there is a big mismatch between the preliminary author list and the actual contributions.

* If you want to join a project, speak up! If you think the author order is wrong, speak up! That is the purpose of writing this down.

## Working papers

* **Accelerated inference for partially observed Markov processes using automatic differentiation**.  
Kevin Tan, Giles Hooker and Ed Ionides.  
STATUS: in review

* **pypomp: Inference for partially observed Markov processes with automatically differentiable particle filters and GPU support**.  
Aaron Abkemeier, Jun Chen, Kevin Tan, Jesse Wheeler, Bo Yang, Kunyang He and Ed Ionides.  
STATUS: AJA's draft thesis chapter is work in progress toward a software paper. The author order here is based on the assumption that AJA will continue to lead the code development and the paper writing, even though Jun led code development until April 2025.  
NOTE: all core developers can be included in this. I've invited Aaron King to join, since pypomp borrows heavily from pomp so Aaron deserved recognition and he is in a strong position to give us good advice. Giles Hooker could join if he wants to, due to his role mentoring Kevin. We expect that Kunyang will join the core development team soon.  
TARGET JOURNAL: J. Stat. Sofware

* **Fitting dynamic models to panel data via automatically differentiable particle filters: A mesocosm case study**.  
Jun Chen, Bo Yang, Aaron Abkemeier, Kevin Tan, Kunyang He, [...], Ed Ionides.  
NOTE: The plan here is very provisional. BY and ELI discussed it on a zoom call today (25-07-02). The idea is that there might be considerable scientific interest in a paper in Methods in Ecology & Evolution, or a similar journal, comparing pypomp.panel with R-pomp for an ecological system (i.e., showing that autodiff is helpful). Jun and Bo have already developed and tested a pypomp version of Bo's Daphnia mesocosm model. There is a small amount of method development for pypomp.panel (concerning mini-batch size for SGD) but there is maybe nothing hugely insightful specific to the PanelPOMP case, so focusing on practical relevance may be a better strategy. I'm supposing that Kevin will be helpful on this, since he has already experimented with some panel-adpf algorithms. AJA has already contributed panelPomp_class.py to pypomp, though this is just a starting point.  
MENTORING: Jun will be mentored by Ed, Bo and Kevin. Kunyang is anticipated to help Jun, and he will be mentored by Jun and Ed.  
TARGET JOURNAL: Methods in Ecology & Evolution.  
OTHER COAUTHORS: If we agree on MEE as a target journal, it will be good to bring in one or more of Aaron King and Meg Duffy, to include ecological expertise. Giles should be invited, as Kevin's mentor, but he will only agree if he expects to contribute to the development of the manuscript.

* **Data mining for panel time series via mechanistic models: Measles in England and Wales**.  
Aaron Abkemeier, Kevin Tan, [...], Ed Ionides.  
NOTE: This is a provisional idea to develop a paper that AJA already has some work on. DPOP is not clearly worth a major theory paper (the theory is a fairly direct extension of DMOP) but maybe it could be included in a major applied stats paper? It has been a longstanding methodological challenge to fit POMP models with shared and unit-specific parameters to large datasets (100-1000 units, each with 100-1000 data points). R-panelPomp is not powerful enough for this, in practice. ADPF methods scale much better, not just because they're quicker per unit, but more critically because they avoid the dependence between units introduced by iterated filtering (or Bayesian methods) and so they entirely avoid the curse of dimensionality.  
TARGET JOURNAL: AoAS.  
NOTE: Anybody else who ends up making large contributions to pypomp.panel or DPOP should be included in this paper (maybe, Jun or Kunyang?). Aaron could include anyone else who is helpful for getting the paper finished, e.g., Jesse? We have enough measles expertise not to require a scientific collaborator, but if AAK wants to join, he could contribute additional measles insights.


## Non-publishable tasks:

There are things that we can do to help the pypomp project that will help all related papers. People who contribute to these tasks should be welcomed into publishable projects whenever we can find a way for them to join usefully.

* Core code development (https://github.com/pypomp/pypomp)
    + New features
    + Bug fixes
    + Performance improvement

* Quantitative tests (https://github.com/pypomp/quant)
    + Quality control, benchmarking against R-pomp and analytic results
    + Performance measuring and comparisons

* Tutorials (https://github.com/pypomp/tutorials)
    + Translating "Simulation-based inference for epidemiological dynamics" into pypomp
    + pypomp documentation for beginners, R-pomp users, and developers   






