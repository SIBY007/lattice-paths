# lattice-paths
Starting in the top left corner of a  grid, and only being able to move to the right and down, there are exactly  routes to the bottom right corner.



How many such routes are there through a  grid? As number of ways can be very large, print it modulo .

Input Format

The first line contains an integer  , i.e., number of test cases.
Next  lines will contain integers  and .

Constraints

Output Format

Print the values corresponding to each test case.

Sample Input

2
2 2
3 2
Sample Output

6
10
Explanation

For  as shown in statement above.
-------------------------------------------------------------------------------------------------------------------------------------
# Enter your code here. Read input from STDIN. Print output to STDOUT
# ProjectEuler+ > Project Euler #15: Lattice paths
# Walking on grids. And not slipping.
#
# https://www.hackerrank.com/contests/projecteuler/challenges/euler015
# challenge id: 2641
#

import math




def C(n, k):
   
    return math.factorial(n) // math.factorial(k) // math.factorial(n - k)


for _ in range(int(input())):
    m, n = map(int, input().split())
    print(C(m + n, n) % 1000000007)
