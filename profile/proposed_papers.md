
# Current projects related to pypomp

* This list is updated as of 25-07-15. 

* It is designed to help coordinate the researchers involved in pypomp. Titles and author lists of working papers are open to changes. Author lists are based in part on expected future contributions as well as past contributions - when the papers are completed, we can make any necessary changes if we agree that there is a big mismatch between the preliminary author list and the actual contributions.

* If you want to join a project, speak up! If you think the author order is wrong, speak up! If you want to take over the lead on a project that has stalled, speak up! That is the purpose of writing this down.

* A responsibility of the first author is to stick with the project through to publication. Kevin mentioned that some groups use a principle of "last touch gets first author" which is an interesting idea: if someone picks up a project and runs with it across the line, they get first position. This disincentivizes dropping the ball when you are currently in first position, which is good for the whole team! Of course, it is not okay to grab the ball from a team-mate and run off with it.


## Working papers

* **Accelerated inference for partially observed Markov processes using automatic differentiation**.  
Kevin Tan, Giles Hooker and Ed Ionides.  
STATUS: in review

* **pypomp: Inference for partially observed Markov processes with automatically differentiable particle filters and GPU support**.  
Aaron Abkemeier, Jun Chen, Kevin Tan, Jesse Wheeler, Bo Yang, Kunyang He, Aaron King, Ed Ionides.    
STATUS: AJA and Jun are provisionally assigned as joint first author. The assumption that AJA will continue to lead the code development and the paper writing; Jun led code development until April 2025 and is expected to actively continue with writing and code development.  
NOTE: all core developers can be included in this. Giles Hooker could join if he wants to, due to his role mentoring Kevin.   
TARGET JOURNAL: J. Stat. Software


* **Fitting dynamic models to panel data via automatically differentiable particle filters: A mesocosm case study**.  
    + This paper proposal is short of a leader. Sign up for it if you want to do it.
    + Jun has decided to focus on the pypomp paper.
    + Kunyang would rather write an Annals of Applied Statistics style paper that is rather different; less tutorial and more applied stats methodology.
    + AJA will probably focus on the pypomp, DPOP and measles papers.
    + Bo or Ed could take the lead on this paper, but it may be a low priority if an overlapping applied stats pypomp.panel paper gets written. There is still room for both, since the communities are different, but the motivation is reduced.  

  POTENTIAL CONTRIBUTORS. Jun Chen, Bo Yang, Aaron Abkemeier, Kevin Tan, Kunyang He, [...], Giles Hooker, Ed Ionides.   
  NOTE: The plan here is very provisional. BY and ELI discussed it on a zoom call on 25-07-02. The idea is that there might be considerable scientific interest in a paper in Methods in Ecology & Evolution, or a similar journal, comparing pypomp.panel with R-pomp for an ecological system (i.e., showing that autodiff is helpful). Jun and Bo have already developed and tested a pypomp version of Bo's Daphnia mesocosm model. There is a small amount of method development for pypomp.panel (concerning mini-batch size for SGD) but there is maybe nothing hugely insightful specific to the PanelPOMP case, so focusing on practical relevance may be a better strategy. I'm supposing that Kevin will be helpful on this, since he has already experimented with some panel-adpf algorithms. AJA has already contributed panelPomp_class.py to pypomp, though this is just a starting point.    
  MENTORING: Jun will be mentored by Ed, Bo and Kevin. Kunyang is anticipated to help Jun, and he will be mentored by Jun and Ed.  
  TARGET JOURNAL: Methods in Ecology & Evolution.  
  OTHER COAUTHORS: If we agree on MEE as a target journal, maybe bring in one or more of Aaron King and Meg Duffy, to include ecological expertise. Giles already has two MEE papers.


* **Panel data analysis via automatically differentiable particle filters**.
This is a reworking of the proposed pypomp.panel MEE paper, but targeted at an applied statistics journal.  
POTENTIAL CONTRIBUTORS. Kunyang He, Aaron Abkemeier, Kevin Tan, Jun Chen, [...], Ed Ionides.
NOTE: This could be written with or without DPOP. It would be stronger with DPOP, but the decision will depend on how the logjam of papers plays out. The idea is to show multiple examples of pypomp.panel, highlighting the capabilities of IFAD. This has some overlap with the "Data mining for panel time series via mechanistic models" plan. The latter idea is focused on measles, and emphasizes scalability issues to large panels. The plan is based on something Kunyang would like to write, since it would give him practice writing for an applied stats audience, and it is also a step toward a potential pypomp.spat.  
TARGET JOURNAL: Annals of Applied Statistics.  
OTHER COAUTHORS: If this becomes the first pypomp.panel paper, it would include all nontrivial contributors to that agenda.


* **Differentiable particle filters for overdispersed discrete-state continuous-time partially observed Markov processes models**. Aaron Abkemeier, Kevin Tan, [...], Ed Ionides.  
TARGET JOURNAL: JCGS or Statistics and Computing.  
NOTE: DPOP is critical for many of the data analysis tasks we want to be able to do. It is also a relatively straightforward paper to write at this point: DPOP and the worked Haiti cholera example have already been developed by Kevin. A relevant question is whether to bundle this with another paper (e.g., measles panel, see below) or write a stand-alone paper. We don't have to decide quite yet. If the contribution is considered big enough for JCGS or S&C (which it justly should be) then publishing it as a step forward may make sense. 

* **Data mining for panel time series via mechanistic models: Measles in England and Wales**.  
Aaron Abkemeier, Kevin Tan, [...], Ed Ionides.  
NOTE: This is a provisional idea to develop a paper that AJA already has some work on. DPOP is not clearly worth a major theory paper (the theory is a fairly direct extension of DMOP) but maybe it could be included in a major applied stats paper? It has been a longstanding methodological challenge to fit POMP models with shared and unit-specific parameters to large datasets (100-1000 units, each with 100-1000 data points). R-panelPomp is not powerful enough for this, in practice. ADPF methods scale much better, not just because they're quicker per unit, but more critically because they avoid the dependence between units introduced by iterated filtering (or Bayesian methods) and so they entirely avoid the curse of dimensionality.  
TARGET JOURNAL: AoAS -> PLOS Comp Bio. DPOP can also be partitioned out to JCGS or Statistics and Computing, but in that case the measles paper may be a better fit for PLOS Comp Bio than AoAS.
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
    + Translating "Simulation-based inference for epidemiological dynamics" into pypomp. Currently being done by Kunyang.
    + pypomp documentation for beginners, R-pomp users, and developers   






