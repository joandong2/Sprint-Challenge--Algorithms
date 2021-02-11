#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) O(n) = Its looping once, O(n3), then using operations in N on the next line which is O(n2), thus removing constants results to linear

b) O(n^2) = Its looping n twice, first in for i in range(n): which is O(n), and while j < n: also an O(n),

c) O(n) = If i add N bunnies, it will make N recursive calls until bunnies equal to zero which is the base case

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

I would use binary search for this problem:

1. Find F which is the floor where eggs broken will be minimized when dropped.
2. Anything higher or equal to F will results to higher eggs broken when thrown off, best case to check first in the middle floor.
3. Throw the eggs and check the no. of eggs broken.
4. If results are high, split the floor into halves but the highest floor would become our previous middle floor - 1, then check.
   -If result is high, do step #4 again and check again the middle floor.
   -If result is low, split the floors into halves, and move the starting point to the previous middle + 1 then check.
5. Repeat step #4 until we reach the value of F

I think the time complexity would be O(log n), since we are looping the N, and dividing it into halves in each iteration.
