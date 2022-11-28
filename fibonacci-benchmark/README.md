# Fibonacci
I will compare the time and space complexity based on the algorithm results for this assignment utilizing the iterative and recursive approach to the sequence of fibonacci.
### Iterative Approach
```
int fibonacciIterative(int N){
    int num1 = 0, num2 = 1, numN;
    if (N==0){
        return num1;
    } else if(N==1){
        return num2;
    } else{
        for (int i = 2; i <= N; i++){
            numN = num1 + num2;
            num1 = num2;
            num2 = numN; 
        }
        return numN;
    }
}
```
### Recursive Approach
```
int fibonacciRecursive(int N){
    if (N==0){
        return 0;
    } else if (N==1){
        return 1;
    } else{
        return fibonacciRecursive(N-1) + fibonacciRecursive(N-2);
    }
}
```
# Testing
We must run a test to see if all 

### How To Run
The following command can be entered into your terminal:
```
make; ./main_test.out
```
# Benchmark
This benchmarking procedure's main goal is to evaluate the performance of my implementation code by contrasting the time and space complexity of each approach.
## Time Complexity
This also contains the benchmark implementation, which displays the time required to complete my iterative and recursive 
### How To Run
The following command can be entered into your terminal:
```
make time
```
## Space Complexity
This benchmark implementation can be used to check how much memory my iterative and recursive technique uses.
### How To Run
In your terminal you can use these commands below:
```
make space
./main_b_space_iterative.out
```
```
make space
./main_b_space_recursive.out
```
I use the same N = 1000 and N = 10000 for my iterative and recursive routines, and I run them in an infinite loop. I could easily see on my activity monitor how much RAM each function used thanks to this comparatively huge N.

# Closing
Recursive is more time-consuming than iterative, yet iterative is quicker and more effective (time complexity). To find the nth Fibonacci number using an iterative strategy, I loop or iterate n times, linearizing the time complexity. On the other hand, the time complexity of the recursive approach is exponential since, for each recursion, I must call two further recursive functions in order to reach the nth Fibonacci number. As we already know, constantly calling and returning a function requires more time than running a loop.
The iterative technique is consistently constant in terms of space complexity. Iterative approach is the opposite of recursive technique in that it occupies less space but moves more slowly. As a result, iterative approach has a greater space complexity but a lower time complexity.