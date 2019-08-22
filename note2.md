# note2:

1. **[Diagonal Matrix](https://en.wikipedia.org/wiki/Diagonal_matrix)**: In linear algebra, a diagonal matrix is a matrix in which the entries outside the main diagonal are all zero. Also note that diagonal matrix usually refers to square matrices.

    1.1: then we want to know what a [main diagonal](https://en.wikipedia.org/wiki/Main_diagonal) is: In linear algebra, the main diagonal of a matrix A is the collection of entries **A{i, j}** where **i = j**. Note that this  **main diagonal** definition applies to any matrix based on Wiki. See the three different main diagonals in the link above.

    1.2: Then, based on main diagonal, we have another concept called the **Antidiagonal**, definition here: The antidiagonal of a dimension N square matrix, B, is the collection of entries **B{i, j}** such that **i + j = N + 1** for all **1 <= i, j <= N**. That is, it runs from the top right corner to the bottom left corner.

    1.3: In order to 记忆这个主对角线与副对角线的规律，我们知道主对角线一定是从左上角划到右下角，可以理解为男左（男的作为主）。然后副对角线，一定是从右上划到左下的，可以理解为女右（女的作为副）。Another **`important note`** is that: antidiagonal is only used on square matrix, but main diagonal is used on any matrix.

2. ??? I found a sentence from [this website](http://pi.math.cornell.edu/~mec/Winter2009/RalucaRemus/Lecture1/lecture1.html), and I feel like it is wrong: Fact 1: For any matrices A, B, C of the same size: (A+B)·C = A·C+B·C, and C·(A+B) = C·A+C·B.

3. [Transpose of a matrix](https://en.wikipedia.org/wiki/Transpose): In linear algebra, the transpose of a matrix is an operator which flips a matrix over its diagonal, that is it switches the row and column indices of the matrix by producing another matrix denoted as A(T).

    3.1: Formally, the i-th row, j-th column element of A(T) is the j-th row, i-th column element of A: [A(T)]{i, j} = [A]{j, i}. **If A is an m × n matrix, then AT is an n × m matrix.**

    3.2： some properties: assuming that r, s are scalars and the sizes of the matrices A, B, C are chosen so that each operation is well defined

    3.2.1: (A·B)(T) = B(T)·A(T), and (A+B)(T) = A(T) + B(T). Proof of (A·B)(T) = B(T)·A(T) is: ![](https://i.imgur.com/NcLLfFT.jpg). 

    3.2.2: (A+B)·C = A·C+B·C, and C·(A+B) = C·A+C·B.





    