## EECS126

1. The first approach is to **define probability** in terms of frequency of occurrence, as a percentage of successes in a moderately large number of similar situations. However, this might be **wrong**, What if this was an experimental drug that was administered for the very first time in this hospital or in the nurse's experience? (如果是**第一次**的话有可能并不知道之前的实验的结果/概率，所以没办法判断)

    1.1 another interpretation of probability is an expression of a subjective belief.

2. ??? find the definition of countably infinite.

    2.1: Similarly, the set of all scalars x in the interval [0, 1] can be writeen as {x | 0 <= x <=1 } Note that the elements x of the latter set take a **continuous range of values**, and **cannot be written down in a list**; such a set is said to be **uncountable**.

3. Two sets are said to be **disjoint** if their intersection is empty. 
   More generally, several sets are said to be **disjoint** if no two of them have a common element. (for example: if there are n sets, them these n sets are disjoint if for 1 <= i,j <= n, i != j, Seti intersect Setj = 0)
   A collection of sets is said to be a **partition** of a set S if the sets in the collection are disjoint and their union is S.
   
4. set operations: 
    S^(T u U) = (S^T) u (S^U)
    Su(T ^ U) = (SuT) ^ (SuU)
    De Morgan's laws:
    ![](https://i.imgur.com/wEEfdjC.png)
    To **prove that SetA = SetB**, you can try to do: for any x that belongs to A, x belongs to B, then A is a subset of B. next for any x in B, x is in A, then B is a subset of A. Then A = B.
    
5. an experiment will produce exactly **one** of several possible outcomes.(每个experiment只能产生**一个**结果). The set of all possible outcomes are called the **sample space** of the experiment. An **event** is a subset of the sample space. 
    This is important: **There is no restriction on what constitutes an experiment. For example, it could be a single toss of a coin, or three tosses, or an infinite sequence of tosses. However, it is important to note that in our formulation of a probabilistic modeL there is only one experiment. So, three tosses of a coin constitute a single experiment. rather than three experiments.**
    
6. Discrete Probability Law; Discrete Uniform Probability Law; Multiplication Rule; 

7. Continuous Model:
    What is the probability of event consisting of a single element? It cannot be possible, because then events with a sufficiently large number of elements would have probability larger than 1. Therefore, the probability of any event that consists of a single element must be 0. 
    



