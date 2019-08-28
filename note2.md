# note2:

1. **[Diagonal Matrix](https://en.wikipedia.org/wiki/Diagonal_matrix)**: In linear algebra, a diagonal matrix is a matrix in which the entries outside the main diagonal are all zero. Also note that diagonal matrix usually refers to square matrices.

    1.1: then we want to know what a [main diagonal](https://en.wikipedia.org/wiki/Main_diagonal) is: In linear algebra, the main diagonal of a matrix A is the collection of entries **A{i, j}** where **i = j**. Note that this  **main diagonal** definition applies to any matrix based on Wiki. See the three different main diagonals in the link above.

    1.2: Then, based on main diagonal, we have another concept called the **Antidiagonal**, definition here: The antidiagonal of a dimension N square matrix, B, is the collection of entries **B{i, j}** such that **i + j = N + 1** for all **1 <= i, j <= N**. That is, it runs from the top right corner to the bottom left corner.

    1.3: In order to 记忆这个主对角线与副对角线的规律，我们知道主对角线一定是从左上角划到右下角，可以理解为男左（男的作为主）。然后副对角线，一定是从右上划到左下的，可以理解为女右（女的作为副）。Another **`important note`** is that: antidiagonal is only used on square matrix, but main diagonal is used on any matrix.

2. ??? I found a sentence from [this website](http://pi.math.cornell.edu/~mec/Winter2009/RalucaRemus/Lecture1/lecture1.html), and I feel like it is wrong: Fact 1: For any matrices A, B, C of the same size: (A+B)·C = A·C+B·C, and C·(A+B) = C·A+C·B. 
    
    Answer: the restrict on the size of matrix A, B, C shouldn't be any size, but we should assume that A, B, C are chosen so that each operation is well defined. See this [website](http://math.mit.edu/~dyatlov/54summer10/matalg.pdf) for more, which also contains a lot of basic properties of matrix operation.
    

3. [Transpose of a matrix](https://en.wikipedia.org/wiki/Transpose): In linear algebra, the transpose of a matrix is an operator which flips a matrix over its diagonal, that is it switches the row and column indices of the matrix by producing another matrix denoted as A(T).

    3.1: Formally, the i-th row, j-th column element of A(T) is the j-th row, i-th column element of A: [A(T)]{i, j} = [A]{j, i}. **If A is an m × n matrix, then AT is an n × m matrix.**

    3.2： some properties: assuming that r, s are scalars and the sizes of the matrices A, B, C are chosen so that each operation is well defined

    3.2.1: **(A·B)(T) = B(T)·A(T)**, and (A+B)(T) = A(T) + B(T). Proof of (A·B)(T) = B(T)·A(T) is: ![](https://i.imgur.com/NcLLfFT.jpg)

    3.2.2: (A+B)·C = A·C+B·C, and C·(A+B) = C·A+C·B.
    
4. [Rule of Sarrus](https://en.wikipedia.org/wiki/Rule_of_Sarrus): Sarrus' rule or Sarrus' scheme is a method and a memorization scheme to compute the determinant of a 3×3 matrix. (Currently known only applies to 3*3 matrix, larger matrix might not be compatible).

    4.1: Another way of thinking of Sarrus' rule is to imagine that the matrix is wrapped around a cylinder, such that the right and left edges are joined. (this idea of wrapped around cyclinder is great)

    4.2: [Laplace expansion](https://en.wikipedia.org/wiki/Laplace_expansion): In linear algebra, the Laplace expansion，also called cofactor expansion, is an expression for the determinant |B| of an n × n matrix B that is a weighted sum of the determinants of n sub-matrices (or minors) of B, each of size (n−1) × (n−1). One **disadvantage** is that: For large matrices, it quickly becomes inefficient when compared to methods using matrix decomposition.

    4.2.1: try to write Laplace expansion in a Math fomula: we first need to know; (1). The i, j cofactor of the matrix B is the scalar Cij: Cij = (-1) ** (i + j) * Mij, where Mij is the i, j minor of B, that is, the determinant of the (n − 1) × (n − 1) matrix that results from deleting the i-th row and the j-th column of B(B is a n * n matrix). ![](https://i.imgur.com/18hBLSS.png)
    **Important note:** **i** in the above fomula can be **any one of the rows in matrix** **B**(from 1 to n), and **j** in the second line of the above fomula can be **any one of the columns of matrix B**(from 1 to n). A total of n + n = 2n results are the same.
    
    4.2.2: ???[ ]proof of Laplace transform, don't understand now. There are some other things such as minor, and complementary minors. (To be done: it contains group theory)

    4.2.3： The Laplace expansion is computationally inefficient for high dimension matrices, **with a time complexity in big O notation of O(n!)**. This is easy to understand, for example: for a 4 * 4 matrix, say we choose the first row, then we have to four sub 3 * 3 matrix, and for each of the four sub 3 * 3 matrix, we have to again choose say the first row, so that we can get the determinant of the sub 3 * 3 matrix. In short, we need a 4 * 3 times in total, which is O(n!).


5. [Permutation](https://en.wikipedia.org/wiki/Permutation#Two-line_notation): 

    5.1: In Notations: (1): two-line notation; (2): one-line notation； (3): Cycle notation: **the steps** are clear and good to read. One thing to notice is **the inverse of permutation**: A convenient feature of cycle notation is that one can find a permutation's inverse simply by reversing the order of the elements in the permutation's cycles. For example: [(125)(34)]^-1 = (521)(43). (4): Canonical cycle notation: **there are two rules:** in each cycle the largest element is listed first **and** the cycles are sorted in increasing order of their first element. For example: (312)(54)(8)(976). Rule one makes the first element in each ```()``` the largest number among other numbers in the same ```()```, and rule two makes thee whole ```()``` sequence increasing, that is 3 < 5 < 8 < 9.


6. A proof:

    fact: Any matrix A has the same eigenvalues as its transpose At.
    ![](https://i.imgur.com/m92kchu.jpg)






    




    