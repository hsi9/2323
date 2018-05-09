# Jupyter

kernel: It is the code that is running. You can interupt, restart and reconnect.

Shift + Enter == Running a cell

Tab will show a pop up of methods on an object

numpy to create arrays:

    import numpy as np
    to make identity matrix of 5:  np.eye(5) 

fancy indexing:  it will pick up the arrays you need

    array([[ 0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.],
           [ 1.,  1.,  1.,  1.,  1.,  1.,  1.,  1.,  1.,  1.],
           [ 2.,  2.,  2.,  2.,  2.,  2.,  2.,  2.,  2.,  2.],
           [ 3.,  3.,  3.,  3.,  3.,  3.,  3.,  3.,  3.,  3.],
           [ 4.,  4.,  4.,  4.,  4.,  4.,  4.,  4.,  4.,  4.],
           [ 5.,  5.,  5.,  5.,  5.,  5.,  5.,  5.,  5.,  5.],
           [ 6.,  6.,  6.,  6.,  6.,  6.,  6.,  6.,  6.,  6.],
           [ 7.,  7.,  7.,  7.,  7.,  7.,  7.,  7.,  7.,  7.],
           [ 8.,  8.,  8.,  8.,  8.,  8.,  8.,  8.,  8.,  8.],
           [ 9.,  9.,  9.,  9.,  9.,  9.,  9.,  9.,  9.,  9.]])
           
    call: arr2d[[2,4,6,8]]
    we get: array([[ 2.,  2.,  2.,  2.,  2.,  2.,  2.,  2.,  2.,  2.],
                  [ 4.,  4.,  4.,  4.,  4.,  4.,  4.,  4.,  4.,  4.],
                  [ 6.,  6.,  6.,  6.,  6.,  6.,  6.,  6.,  6.,  6.],
                  [ 8.,  8.,  8.,  8.,  8.,  8.,  8.,  8.,  8.,  8.]])
