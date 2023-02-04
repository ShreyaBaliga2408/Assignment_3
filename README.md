ASSIGNMENT-3
# PROBLEM DESCRIPTION:
You are to implement three (3) methods (repeat, getClock, and toMillisecs) of a class
called Timer. Please see the skeleton class that I created in the repository. Timer is
invoked from a class called Benchmark_Timer which implements the Benchmark
interface. The APIs of these class are as follows:
public interface Benchmark<T> {
default double run(T t, int m) {
return runFromSupplier(() -> t, m);
}
double runFromSupplier(Supplier<T> supplier, int m);
}
[Supplier is a Java function type which supplies values of type T using the method:
get().]
public class Benchmark_Timer<T> implements Benchmark<T>
public Benchmark_Timer(String description, UnaryOperator<T> fPre, Consumer<T>
fRun, Consumer<T> fPost)
[Consumer is a Java function type which consumes a type T with the method: accept(t).
UnaryOperator is essentially an alias of Function<T, T> which defines apply(t) which
takes a T and returns a T.]
public Benchmark_Timer(String description, UnaryOperator<T> fPre, Consumer<T>
fRun)
public Benchmark_Timer(String description, Consumer<T> fRun, Consumer<T> fPost)
public Benchmark_Timer(String description, Consumer<T> f)
public class Timer {
... // see below for methods to be implemented...
}
public <T, U> double repeat(int n, Supplier<T> supplier, Function<T, U> function,
UnaryOperator<T> preFunction, Consumer<U> postFunction) {
// TO BE IMPLEMENTED
}
[Function<T, U> defines a method U apply(t: T), which takes a value of T and returns a
value of U.]
private static long getClock() {
// TO BE IMPLEMENTED
}
private static double toMillisecs(long ticks) {
// TO BE IMPLEMENTED
}
The function to be timed, hereinafter the "target" function, is the Consumer function
fRun (or just f) passed in to one or other of the constructors. For example, you might
create a function which sorts an array with n elements.
The generic type T is that of the input to the target function.
The first parameter to the first run method signature is the parameter that will, in turn, be
passed to target function. In the second signature, supplier will be invoked each time to
get a t which is passed to the other run method.
The second parameter to the run function (m) is the number of times the target function
will be called.
The return value from run is the average number of milliseconds taken for each run of
the target function.
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
#Relationship Conclusion:
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
#Evidence:
An array that is sorted in reverse order, will take the most amount of time since all the
numbers are to be swapped. This can be related to the observations table below. As
seen from the benchmarking output in the observation table, the array sorted in reverse
takes the most amount of time to run the insertion sort algorithm, the randomly sorted
array runs faster than the reverse sorted array, the partially sorted array runs even
faster than the randomly sorted array, and the sorted array runs the fastest with
insertion sort.
Therefore,Ordered < Partially Ordered < Randomly Ordered < Reverse Ordered

