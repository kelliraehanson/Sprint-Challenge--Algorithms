Add your answers to the Algorithms exercises here.

# Analysis of Algorithms

## Exercise I

a)  a = 0
    while (a < n * n * n):
      a = a + n * n

```
Answer: 0(n^2)

I would describe this as being 0(n^2) because the while is the largest
and will make "n" larger as it is run.
```

b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1

```
Answer: 0(n^3)

For this code I would say it is 0(n^3) because there are three nested for loops in the code. So, each time the outer loop runs the inner loop also runs.
```

c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```
Answer: 0(n)
I would describe this as the "bunnyEars" is being called called "bunnies" times 
until "bunnies" is == 0 (equal to zero true). "bunnies" decrements by one each time. Linear. 
```
### What is Time Complexity?

```
Extra explanation:

Above are all examples of Time Complexity. Which is something in Computer Science that describes the amount of time it takes to run a specific algorithm. 

To describe what it does one would say that the time an algorithm takes to run is estimated by counting the number of operations in the algorithm. There are three cases of this: best-case, average-case, and worst-case. Usually we are finding the worst-case for example the value of the last element in a list ([1, 2, 3, 4, 5]). 

To find these we use something called a Linear Search. A Linear Search is a method for finding an element within a list. It check each element in the list until a match is found or the whole list has been sesarched. 

To describe the Time Complexity of an algorithm we use something called Big-O Notation. This is used to describe algorithms according to how their running time or space requirements grow as the input size (n) grows.
```

### Table of Common Time Complexities

|          Name        |  Time Complexity  |
|----------------------|-------------------|
|      Constant Time   |         0(1)      |
|   Logarithmic Time   |       0(log n)    |
|     Linear Time      |       0(n)        |
|   Quasilinear Time   |     0(n log n)    |
|    Quadratic Time    |       0(n^2)      |
|   Exponential Time   |       0(2^n)      |
|    Factorial Time    |        0(n!)      |

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

```
Answer: O(log n)

To describe this I would say to use binary serach method to find what floor "f" is. This means you will have to drop an egg off of floor to find the one floor the egg doesn't break when it is dropped off of. 

So, the first thing I would do is drop an egg off of the middle floor of the building. If the egg breaks I would go to a floor between the middle floor and the ground level floor until I find the floor the egg doesn't break on.

If the egg didn't break on the middle floor of the building I would then go to a floor between the middle floor I am currently on and the top floor of the building. If the egg doesn't break on that floor I would move to a floor between the middle floor of the building and the ground level and drop an egg from that floor and drop an egg from that floor. If the egg doesn't break I would keep doing that process on different floors until I find the floor the egg breaks on.

```