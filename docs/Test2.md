# CodingSortedSwap
Calculate the amount of money to pay based on logs of phone calls.

A non-empty zero-indexed array A consisting of N integers is given.

You can perform a single swap operation in array A. This operation takestwo indices I and J, such that 0 ≤ I ≤ J < N, and exchanges the values ofA[I] and A[J].

The goal is to check whether array A can be sorted into non-decreasingorder by performing at most one swap operation.

For example, consider array A such that:
```
A[0] = 1
A[1] = 5
A[2] = 3
A[3] = 3
A[4] = 7
```
After exchanging the values A[1] and A[3] we obtain an array [1, 3, 3, 5, 7],which is sorted in non-decreasing order.

Write a function:
```
class Solution { public boolean solution(int[] A);}
```

that, given a non-empty zero-indexed array A consisting of N integers,returns true if the array can be sorted into non-decreasing order byperforming at most one swap operation or false otherwise

For example, given:
```
A[0] = 1
A[1] = 5
A[2] = 3
A[3] = 3
A[4] = 7
```
the function should return true, as explained above.

On the other hand, for the following array:
```
A[0] = 1
A[1] = 3
A[2] = 5
A[3] = 3
A[4] = 4
```
the function should return false, as there is no single swap operationthat sorts the array.
For the following array:
```
A[0] = 1
A[1] = 3
A[2] = 5
```

the function should return true, as the given array is already sorted.
Assume that:
- N is an integer within the range [1..100];
- each element of array A is an integer within the range[1..1,000,000,000];

In your solution, focus on correctness. The performance of your solutionwill not be the focus of the assessment

