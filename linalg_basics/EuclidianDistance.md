# Euclidian Distance
- a similarity metric for vectors
- identifies how far two vectors or points are from eachother
- length of the straight line between points
- heigher dimenstions

$$ d(\vec v,\vec w)  = \sqrt {\sum_{i=1}^{n} (v_i-w_i) ^ 2}$$


### In numpy

    np.linalg.norm(v-w)