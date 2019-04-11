# MIT-6.002-Project-1

#Overview
This is the first project of the MIT-6.002 class: Introduction to Computational Thinking and Data Science

In this problem set, I will create two algorithms: Greedy algorithm and Brute Force algorithm. Both algorithm takes in a dictionary containing the cows' names and their corresponding weights. Both algorithms will return the highest sum weight, depending on different methods.

Greedy Cow Transport( Greedy algorithm):

This algorithm will prioritize the heaviest cow.

Example:

Suppose the spaceship has a weight limit of 10 tons and the set of cows to transport is {"Jesse": 6, "Maybel": 3, "Callie": 2, "Maggie": 5}.

The greedy algorithm will first pick Jesse as the heaviest cow for the first trip. There is still space for 4 tons on the trip. Since Maggie will not fit on this trip, the greedy algorithm picks Maybel, the heaviest cow that will still fit. Now there is only 1 ton of space left, and none of the cows can fit in that space, so the first trip is [Jesse, Maybel].

For the second trip, the greedy algorithm first picks Maggie as the heaviest remaining cow, and then picks Callie as the last cow. Since they will both fit, this makes the second trip [[Maggie], [Callie]].

The final result then is [["Jesse", "Maybel"], ["Maggie", "Callie"]].


Brute Force Cow Transport( Brute Force algoritm):

This algorithm will look at every possible combination of trips and pick the best one.

Example:

Suppose the spaceship has a cargo weight limit of 10 tons and the set of cows to transport is {"Jesse": 6, "Maybel": 3, "Callie": 2, "Maggie": 5}.

The brute force algorithm will first try to fit them on only one trip, ["Jesse", "Maybel", "Callie", "Maggie"]. Since this trip contains 16 tons of cows, it is over the weight limit and does not work. Then the algorithm will try fitting them on all combinations of two trips. Suppose it first tries [["Jesse", "Maggie"], ["Maybel", "Callie"]]. This solution will be rejected because Jesse and Maggie together are over the weight limit and cannot be on the same trip. The algorithm will continue trying two trip partitions until it finds one that works, such as [["Jesse", "Callie"], ["Maybel", "Maggie"]].

The final result is then [["Jesse", "Callie"], ["Maybel", "Maggie"]]. Note that depending on which cow it tries first, the algorithm may find a different, optimal solution. Another optimal result could be [["Jesse", "Maybel"],["Callie", "Maggie"]].
