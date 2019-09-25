# EECS127 livebook

1.1 **injective function**:
    ![](https://i.imgur.com/DvCZkH6.png)
    

1.2 **surjective function:
    ![](https://i.imgur.com/fatsMvS.png)

2. homomorphism:

    ![](https://i.imgur.com/o8J4SZ3.png)
    
    |2.1>: **arity** In logic, mathematics, and computer science, the arity of a function or operation is **the number of arguments** or operands that the function takes.

    f(ga(a1, a2, ..., ak)) = gb(f(a1), f(a2), ... ,f(ak))
    
    ![](https://i.imgur.com/Lkuh43L.png)
    note that **source operation ga()** does not need to be the same as **the target operation gb()**: such as in the example below:
    
    1. **source:** e ^ (x + y): f(x) = e ^ x, in this case **ga = addition** operation
    2. **target:** e^x * e^y, in this case **gb = multiplication**.

    3. **source:** ln(xy): f(x) = ln(x), in this case **ga = multiplication** operation
    4. **target:** ln(x) + ln(y), in this case **gb = addition** operation

    |2.2> an imformal defition about **Isomorphism**, if a function satisfy this equation: **f(ga(a1, a2, ..., ak)) = gb(f(a1), f(a2), ... ,f(ak))**, and its inverse function also satisfy it, then it is called **isomorphism**.
    
3. multiplicity:
    In mathematics, the multiplicity of a member of a multiset is **the number of times it appears** in the multiset.
    |3.1> good example: the number of times a given polynomial equation has a root at a given point is **the multiplicity of that root**.

4. **Gramian matrix**:

    |4.1> definition: In linear algebra, the Gram matrix of a set of vectors **{v1, v2, ..., vn}** in an inner product space is the Hermitian matrix of inner products, whose entries are given by Gij = <vi, vj>
    |4.2> an important theorem: An important application is to compute linear independence: a set of vectors are linearly independent if and only if the Gram determinant (the determinant of the Gram matrix) is non-zero.
    ![](https://i.imgur.com/B405atY.png)
    
    ![](https://i.imgur.com/Fhahawr.png)
    from the above picture, we know that **dot_product(a, cross_product(b, c))** is equal to the **volume** of the parallelepiped.
    ![](https://i.imgur.com/27iQiXl.png)
    from above, we know that **dot_product(a, cross_product(b, c))** also equals to the det(**a**, **b**, **c**), we can expand the determinant to see that det(**a**, **b**, **c**) = a1(b2c3 - b3c2) + a2(b3c1 - b1c3) + a3(b1c2 - b2c1), which is a **dot product** of **vector a** and **vector (b * c)**. 
    ![](https://i.imgur.com/NN6XWWA.png)
    the above picture shows that the square of the **scalar triple product** of **(a*b) c** is actually the determinant of a Gram matrix, so if the n vectors **v1, v2, ..., vn** are linearly independent, which means that the **volume** is not zero, which will imply that the **det(Gram Matrix)** will also not be zero.
    ![](https://i.imgur.com/gXESzQl.png)
    **|||>>>** above picture shows a way to calculate cross product
    ![](https://i.imgur.com/zGAkFXa.png)
    **|||>>>** above picture shows an easy way using matrix to calculate cross product



    

