# Linear Algebra Review

1. **3 dimensional real coordinate space**. V(x)[meaning x is a vector] = ([i, 0, 1])T(transpose meaning that we change it from a row vector to a column vector) is not a real valued 3-tuple(because it has an imaginary number as its first element).
    Any vector in N dimensional space is a tuple of n real numbers.

2. **parametric representation of lines**. for example: in R2(this means two dimensional), we have a V(a) = [1, 2], and V(b) = [2,3], then the line that determined by these two points are: [V(b){you can also use V(a)} + t * (V(b) - V(a){you can also do (V(a) - V(b))} such that t is R(real numbers)] note that V(b) - V(a) is the direction, and the V(b) at the front is the shift. You can also write the above fomula in a parametric notation: x = 1 + (2-3) * t, and y = 2 + (2-3) * t.

    2.1: In R3, the only way for you to define a line is to use paramtrix equations, you CANNOT write **x+y+z = c**, this is not a line, but a plane.

3. **span and linear combination**: 
    3.1: the span of the zero vector is the zero vector
    3.2: definition of [span](https://en.wikipedia.org/wiki/Linear_span) from Wiki: Given a vector space V over a field K, the span of a set S of vectorsthe span of S may be defined as the set of all finite linear combinations of elements (vectors) of S: span(S) = {the summation(i = 1, k) lambda(i) * V(i) such that k is N, V(i) belongs to S, and lambda(i) belongs to K}. from Khan: span(V1, V2, V3, ... Vn) = the set{c1 * V1 + c2 * V2 + ... + cn * Vn such that ci belongs to R for 1 <= i <= n}

4. **linear dependence and linear independence**:
    4.1: a proof by Khan: ![](https://i.imgur.com/RMqGX3i.png)
    4.2: the definition of linear independence: c1 * V1 + c2 * V2 + ... cn * Vn = V(0), all of ci, 1 <= i < =n are 0.

