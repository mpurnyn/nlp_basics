# Linear Algebra Terms

#### Dot Product

The dot product or scalar product or inner product between two vectors $\vec a$ and $\vec b$ of the same size is defined as:
$$\vec a \cdot \vec b = \sum_{i=1}^{n} a_i b_i$$

The dot product takes two vectors and returns a single number.

    nparray1 = np.array([0, 1, 2, 3]) # Define an array
    nparray2 = np.array([4, 5, 6, 7]) # Define an array

    flavor1 = np.dot(nparray1, nparray2) # Recommended way
    print(flavor1)

    flavor2 = np.sum(nparray1 * nparray2) # Ok way
    print(flavor2)

    flavor3 = nparray1 @ nparray2         # Geeks way
    print(flavor3)

    # As you never should do:             # Noobs way
    flavor4 = 0
    for a, b in zip(nparray1, nparray2):
        flavor4 += a * b
        
    print(flavor4)

#### Transpose of a Matrix
In linear algebra, the transpose of a matrix is an operator that flips a matrix over its diagonal, i.e., the transpose operator switches the row and column indices of the matrix producing another matrix. If the original matrix dimension is n by m, the resulting transposed matrix will be m by n.

    print(nparray.T)

#### Norm of Vector
In linear algebra, the norm of an n-dimensional vector 𝑎⃗ 

is defined as:

$$ norm(\vec a) = ||\vec a|| = \sqrt {\sum_{i=1}^{n} a_i ^ 2}$$

Calculating the norm of vector or even of a matrix is a general operation when dealing with data. 

Numpy has a set of functions for linear algebra in the subpackage linalg, including the norm function. Note that without any other parameter, the norm function treats the matrix as being just an array of numbers. However, it is possible to get the norm by rows or by columns. The axis parameter controls the form of the operation:

- axis=0 means get the norm of each column
- axis=1 means get the norm of each row.

    normByCols = np.linalg.norm(nparray2, axis=0) # Get the norm for each column. Returns 2 elements
    normByRows = np.linalg.norm(nparray2, axis=1) # get the norm for each row. Returns 3 elements

Finally, note that the norm is the square root of the dot product of the vector with itself. That gives many options to write that function:

$$ norm(\vec a) = ||\vec a|| = \sqrt {\sum_{i=1}^{n} a_i ^ 2} = \sqrt {a \cdot a}$$

#### Mean of Vector

As with the sums, one can get the **mean** by rows or columns using the **axis** parameter. Just remember that the mean is the sum of the elements divided by the length of the vector
$$ mean(\vec a) = \frac {{\sum_{i=1}^{n} a_i }}{n}$$

nparray2 = np.array([[1, -1], [2, -2], [3, -3]]) # Define a 3 x 2 matrix. Chosen to be a matrix with 0 mean

mean = np.mean(nparray2) # Get the mean for the whole matrix
meanByCols = np.mean(nparray2, axis=0) # Get the mean for each column. Returns 2 elements
meanByRows = np.mean(nparray2, axis=1) # get the mean for each row. Returns 3 elements

    print('Matrix mean: ')
    print(mean)
    print('Mean by columns: ')
    print(meanByCols)
    print('Mean by rows:')
    print(meanByRows)

#### Center a matrix (subtract the mean)

Centering the attributes of a data matrix is another essential preprocessing step. Centering a matrix means to remove the column mean to each element inside the column. The mean by columns of a centered matrix is always 0.

    nparrayCentered = nparray2 - np.mean(nparray2, axis=0) # Remove the mean for each column
