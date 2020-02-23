#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) O(n)

b) O(nlogn)

c) O(n)

## Exercise II

### Constraints and Parameters

Height of story building => n
Number of Eggs => Plenty
Floor at which eggs begin to break => f

### Goal

Determine f with the least amount of broken + dropped eggs

### First Pass Solution

Starting from the ground floor, throw an egg from each floor, increasing the current floor count by 1 after each throw. Floor k is the first floor an egg breaks.

Time Complexity => O(n)
In the worst case scenario where the top floor == k, we have to drop n eggs.

### Second Pass Solution

The number of dropped + broken eggs can be drastically reduced by using a binary search where we halve the input at each iteration.
We drop the first egg at n/2

- If it breaks, then the input for the next pass is constrained to maximum for n/2.

- If it doesn't break, then the input for the next pass is constrained to a minimum of n/2 + 1.

This is repeated till we find the floor where the egg first breaks.

Time Complexity => O(logn)
