# CSE-5311-005-Hands-On-4
Faisal Ahmad - 1002239354

Call Stack for fib(5)

fib(5) calls fib(4) and fib(3)

fib(4) calls fib(3) and fib(2)

fib(3) calls fib(2) and fib(1)

fib(2) calls fib(1) and fib(0)

fib(1) returns 1

fib(0) returns 0

fib(1) returns 1

fib(2) calls fib(1) and fib(0)

fib(1) returns 1

fib(0) returns 0

fib(3) calls fib(2) and fib(1)

fib(2) calls fib(1) and fib(0)

fib(1) returns 1

fib(0) returns 0

fib(1) returns 1

# Time Complexity Analysis
The time complexity for the recursive fibonacci function is O(n^2) because the function calls on itself twice on (n-1) and (n-2) and since T(n-1) is almost equal to T(n-2), the recurrance relation would be T(n) = 2 * T(n-1)


# Potential improvements 
We could use iteration instead of recursion which would reduce the time complexity to O(n) and the space complexity to O(1) because no space is used for recursion stack. The implementation is as follows: 

```python
def fib(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    
    return b
