## Pypomp: Modeling and inference for partially observed Markov processes

The Pypomp organization supports data analysis using partially observed Markov process (POMP) models. A core produce is the [**pypomp** Python package](https://pypi.org/project/pypomp/). This is supported by [documentation](https://pypomp.readthedocs.io), [tutorials](https://pypomp.github.io/tutorials), [extended quantitative tests](https://pypomp.github.io/quant), and other [case study repositories](https://github.com/orgs/pypomp/repositories). The Pypomp library draws inspiration from the [**pomp** R package](https://kingaa.github.io/pomp/) while incorporating automatic differentiation and parallelization for GPU and CPU using [JAX](https://jax.readthedocs.io/en/latest/).

### Pypomp capabilities

1. Method development. Pypomp provides state-of-the-art methods, including iterated filtering algorithms and [automatically differentiable particle filters](https://arxiv.org/abs/2407.03085). Most methods have the plug-and-play property, i.e., they require the dynamic model to be specified by coding a simulator not a function to evaluate the transition density.

2. Panel data. Pypomp supports analysis of collections of time series, via PanelPOMP models.  

3. Application to infectious disease dynamics. A tutorial provides an [introduction to infectious disease modeling and inference using Pypomp](https://pypomp.github.io/tutorials/sbied). There are also case studies using Pypomp to analyze [historical cholera transmission](https://pypomp.github.io/tutorials/dhaka/dhaka_tutorial.html) and a panel study of [historical measles dynamics](https://pypomp.github.io/tutorials/big_measles/big_measles_tutorial.html).

4. Application to ecological dynamics. A case study of [population dynamics for four interacting species](https://pypomp.github.io/Daphnia-tutorial/).

5. Other applications. Pypomp has been tested on a range of data analysis tasks in [final projects for a Master level time series class](https://ionides.github.io/531w26/final_project/index.html). 

6. Other motivating examples can be found on the [**pomp** R package bibliography page](https://kingaa.github.io/pomp/biblio.html).


### Contributors

* This organization is collaborative. All interested individuals are welcome to contribute to existing projects or to propose new projects.

* The organization is led by the [core development team](Governance.md), guided by some [basic democratic rules](Governance.md).

* Those wishing to contribute can either contact the core development team or simply propose a coding contribution via a pull request.




