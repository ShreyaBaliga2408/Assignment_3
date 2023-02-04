ASSIGNMENT-3
# PROBLEM DESCRIPTION:
You are to implement three (3) methods (repeat, getClock, and toMillisecs) of a class
called Timer. Please see the skeleton class that I created in the repository. Timer is
invoked from a class called Benchmark_Timer which implements the Benchmark
interface. 
Implement InsertionSort (in the InsertionSort class) by simply looking up the insertion
code used by Arrays.sort. If you have the instrument = true setting in
test/resources/config.ini, then you will need to use the helper methods for comparing
and swapping (so that they properly count the number of swaps/compares).
Implement a main program (or you could do it via your own unit tests) to actually run the
following benchmarks: measure the running times of this sort, using four different initial
array ordering situations: random, ordered, partially-ordered and reverse-ordered. I
suggest that your arrays to be sorted are of type Integer. Use the doubling method for
choosing n and test for at least five values of n. Draw any conclusions from your
observations regarding the order of growth.
# Relationship Conclusion:
The insertion sort algorithm is both stable and adaptive. The average number of
comparisons required are ¼ *( N*(N-1) ) and the average number of swaps required
are ¼ * (N*(N-1)) as well. So as the number of swaps is none for the sorted array, it
takes the least amount of time to run the insertion sort algorithm on it. In contrast, an
array that is sorted in reverse order, will take the most amount of time since all the
numbers are to be swapped. The array sorted in reverse takes the most amount of time
to run the insertion sort algorithm, the randomly sorted array runs faster than the
reverse sorted array, the partially sorted array runs even faster than the randomly sorted
array, and the sorted array runs the fastest with insertion sort.
Therefore,Ordered < Partially Ordered < Randomly Ordered < Reverse Ordered.
# Evidence:
An array that is sorted in reverse order, will take the most amount of time since all the
numbers are to be swapped. This can be related to the observations table below. As
seen from the benchmarking output in the observation table, the array sorted in reverse
takes the most amount of time to run the insertion sort algorithm, the randomly sorted
array runs faster than the reverse sorted array, the partially sorted array runs even
faster than the randomly sorted array, and the sorted array runs the fastest with
insertion sort.
Therefore,Ordered < Partially Ordered < Randomly Ordered < Reverse Ordered

