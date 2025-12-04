# pypomp

This organization supports modeling and inference using partially observed Markov process (POMP) models.

A core goal is the development of the [**pypomp** Python package](https://pypi.org/project/pypomp/). This seeks inspiration from the [**pomp** R package](https://kingaa.github.io/pomp/) while incorporating automatic differentiation and parallelization using [JAX](https://jax.readthedocs.io/en/latest/).

### Current priorities

1. To support the methodology explored by Tan, K., Ionides, E. L. and Hooker, G. (2024), Accelerated inference for partially observed Markov processes using automatic differentiation, [arxiv:2407.03085](https://arxiv.org/abs/2407.03085), based on the code for this project at [zenodo.13356896](https://zenodo.org/doi/10.5281/zenodo.13356896). 

2. To provide state-of-the-art alternative methods, including iterated filtering algorithms. Most methods have the plug-and-play property, i.e., they require the dynamic model to be specified by coding a simulator not a function to evaluate the transition density.

3. To include tools for investigation of panel data, i.e., collections of time series.

### Expected users

* Scientists wanting to perform data analysis on a dynamic system via partially observed Markov processes (POMP), also  called state-space models (SSM) or hidden Markov models (HMM).

* Many of the expected use cases and motivating examples of this package can be found on the [**pomp** R package bibliography page](https://kingaa.github.io/pomp/biblio.html).

* Researchers wishing to develop novel inference methodology for POMP models.

### Contributors

* This organization is collaborative. All interested individuals are welcome to contribute to existing projects or to propose new projects.

* The organization is led by the [core development team](Governance.md), guided by some [basic democratic rules](Governance.md).

* Those wishing to contribute can either contact the core development team or simply propose a coding contribution via a pull request.




