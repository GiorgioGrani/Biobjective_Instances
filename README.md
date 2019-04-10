# Biobjective_Instances


This library contains instances for biobjective pure integer problems:

* **linear_integer.zip** contains biobjective integer linear instances in **.dat** format. 
   The name of each file is in the format `added_instance_p-2_n-X_m-Y.lp` where `X` is the number of integer variables and `Y` is the number of constraints.
We have $c_i\in \Z^n$, $i=1,2$;\; $A\in \Z^{m\times n}$ and $b\in \Z^m$.
In particular, $c_{ij}$ is generated in the ranges $[-100,-1]$ with probability $0.2$ and $[0,100]$ with probability $0.8$,
$j=1,\ldots,n$; $i=1,2$. The coefficients $a_{kl}$ are generated in the ranges $[-100,-1]$ with probability $0.05$,
$[1,100]$ with probability $0.9$ and $a_{kl}=0$ with probability $0.05$.
The right-hand side $b_k$ is generated randomly in the range $[0,\sum_{l=1}^n a_{kl}]$.
The new instances are $97$. $58$ problems have a number of constraints which is the $83\%$ of the number of variables, the remaining $39$ ones have exactly $10$ constraints each.

*  **quadratic_integer.zip** contains biobjective integer linearly constrained quadratic instances in **.lp** format. 
   The first constraint is the second objective.
   The name of each file is in the format `QuadraticILP_p-Z_n-X_m-Y.lp` where `X` is the number of integer variables, `Y` is the number of constraints. `Z` has not to be taken into consideration since it is inherited from [moolibrary](http://home.ku.edu.tr/~moolibrary/).
