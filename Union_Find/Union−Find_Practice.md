## Week 1 Questions (optional)
*Social network connectivity.*
Given a social network containing n members and a log file containing m timestamps at which times pairs of members formed friendships, design an algorithm to determine the earliest time at which all members are connected (i.e., every member is a friend of a friend of a friend ... of a friend). Assume that the log file is sorted by timestamp and that friendship is an equivalence relation. The running time of your algorithm should be mlogn or better and use extra space proportional to n.

> set up a counter to record maximum disjoint size so far,
> if it exceeds the total member, then we will return the  timestamps associated with last pair unioned




*Union-find with specific canonical element.*
Add a method 𝚏𝚒𝚗𝚍() to the union-find data type so that 𝚏𝚒𝚗𝚍(𝚒) returns the largest element in the connected component containing i. The operations, 𝚞𝚗𝚒𝚘𝚗(), 𝚌𝚘𝚗𝚗𝚎𝚌𝚝𝚎𝚍(), and 𝚏𝚒𝚗𝚍() should all take logarithmic time or better.

For example, if one of the connected components is {1,2,6,9}, then the 𝚏𝚒𝚗𝚍() method should return 9 for each of the four elements in the connected components.

> always choose the larger element as root in the union method.
> find can just return root of the element.

>Hint: maintain an extra array to the weighted quick-union data structure that stores for each root >𝚒 the large element in the connected component containing 𝚒.

*Successor with delete.*
Given a set of N integers S={0,1,...,N−1} and a sequence of requests of the following form:
- Remove x from S
- Find the successor of x: the smallest y in S such that y≥x.
design a data type so that all operations (except construction) should take logarithmic time or better.

>Hint: use the modification of the union−find data discussed in the previous question.
