.. toctree::
   :maxdepth: 2
   :caption: Contents:
   
   model_storage
   models_op
   optimizer
   valuation_optimizer
   constraints

This is a Python module that uses the Pyomo optimization modeling language to construct a linear program for the valuation of an energy storage device in a given electricity market.

The valuation of an electricity storage device is based on the expected future cash flow generated by the device. The optimization problems built using this module estimate the maximum potential revenue of an energy storage system based on historical data. The model is based on a linear program that seeks to maximize revenue using the compensation model of the market subject to physical constraints of the energy storage system such as storage and ramping limits. Historical data including regulation market results and locational marginal prices are used to determine the optimal policy for the horizon covered by the provided data. The strategy is determined using perfect knowledge and thus results in an upper bound on the revenue that would have been obtained during the optimization horizon. 

Requirements
------------

In order for this software to function, the following modules and tools must be installed:

* Python 3.6 or higher
* The Pyomo, Pandas, NumPy, and Six Python modules
* GLPK, Gurobi, or any other solver for linear programming problems compatible with Pyomo

Solvers
=======

For Pyomo to operate, a solver with linear program solving capabilities must be installed and included in the system path. Two examples of capable solvers are GLPK and IPOPT. Commercial solvers such as Gurobi are alternative choices. The COIN-OR Optimization Suite contains a collection of solvers for optimization problems. It can be downloaded for free at:

http://projects.coin-or.org/CoinBinary

Please see installation instructions for each solver.

Acknowledgment
--------------

The authors would like to thank Dr. Imre Gyuk and his colleagues at the Energy Storage Program at the U.S. Department of Energy for funding this research. Sandia National Laboratories is a multimission laboratory managed and operated by National Technology and Engineering Solutions of Sandia, LLC, a wholly owned subsidiary of Honeywell International, Inc., for the U.S. Department of Energy's National Nuclear Security Administration under contract DE-NA0003525.

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
