# Biobjective_Instances


This library contains instances for biobjective pure integer problems.

## Linear Integer Instances

  **linear_integer.zip** contains biobjective integer linear instances in **.dat** format. 
   
   
   The name of each file is in the format `added_instance_p-2_n-X_m-Y.lp` where `X` is the number of integer variables and `Y` is the number of constraints.

   The **.dat** are organized as follows:

   1. [line 1] number of objectives (always 2)
   2. [line 2] number of variables
   3. [line 3] number of constraints m
   4. [line 4 - 5] A matrix such that the first row is the first objective c1 and the second row is the second objective c2.
     
        It appears in the format 
           [[ c1 ],
           [  c2 ]]
   5. [line 6-(6+m)] The constraint matrix, where each row is a constraint.
     
        The matrix is in the format [[ row_1 ],[ row_2 ],[ row_3 ], ... , [ row_m ]]
   6. [line (6+m+1)] The rhs coefficients. They appear in the format [ rhs_1, rhs_2, ... , rhs_m ]
  
   
   Coefficients have been chosen accordingly to the following
   
   1. c1_j and c2_j are integers with value in the range [-100, -1] with probability 0.2 and in the range [0, 100] with probability 0.8
   2. row_1_j, ... , row_m_j are generated in the range [-100,-1] with probability 0.05,
in [1,100] with probability 0.9 and they are set to zero with probability 0.05.

   3. rhs_1, ... , rhs_m are generated in the range [0, tot], where tot is the sum of all the elments of the constraints matrix
   
   **Remark** all the variables are non negatives and integers.
   
   **Remark** the objectives have to be **maximized**


   **Remark**The new instances are 97. 58 problems have a number of constraints which is the 83% of the number of variables, the remaining 39 ones have exactly 10 constraints each.
   
   
## Linearly Constrained Quadratic Instances

   **quadratic_integer.zip** contains biobjective integer linearly constrained quadratic instances in **.lp** format. 

   **Remark** The first constraint (the only quadratic one) is the second objective.
   
   
   The name of each file is in the format `QuadraticILP_p-Z_n-X_m-Y.lp` where `X` is the number of integer variables, `Y` is the number of constraints. `Z` has not to be taken into consideration since it is inherited from [moolibrary](http://home.ku.edu.tr/~moolibrary/).
   
   The constraints matrix and the rhs vector are the same as in [moolibrary](http://home.ku.edu.tr/~moolibrary/).
   
   To generate the positive semidefinite quadratic functions Q1 and Q2 we firstly generated the Gramian complements L1 and L2 randomply and then we simply put Q1 = L1 L1' and Q2 = L2 L2'. The generic element Lij of the matrix L (L1 or L2) is chosen in {0, 1} with equal probability.
