---
layout: post
categories: [Coding, Useful]
tags: coding
image: https://i.ytimg.com/vi/-QylJgiVbhA/maxresdefault.jpg
---

#### List of Possible errors on coding platforms:

A runtime error means that the program was compiled successfully, but it exited with a runtime error or crashed. You will receive an additional error message, which is most commonly one of the following:

**SIGSEGV**
This is the most common error, i.e., a "segmentation fault". This may be caused e.g. by an out-of-scope array index causing a buffer overflow, an incorrectly initialized pointer, etc. This signal is generated when a program tries to read or write outside the memory that is allocated for it, or to write memory that can only be read. For example, you’re accessing a[-1] in a language which does not support negative indices for an array.

**SIGXFSZ** 
"output limit exceeded". Your program has printed too much data to output.

**SIGFPE**
"floating point error". This usually occurs when you’re trying to divide a number by 0, or trying to take the square root of a negative number.

**SIGABRT**
These are raised by the program itself. This happens when the judge aborts your program in the middle of execution. Due to insufficient memory, this can be raised.

**NZEC** 
(non-zero exit code) - this message means that the program exited returning a value different from 0 to the shell. For languages such as C/C++, this probably means you forgot to add "return 0" at the end of the program. It could happen if your program threw an exception which was not caught. Trying to allocate too much memory in a vector.

For interpreted languages like Python, NZEC will usually mean that your program either crashed or raised an uncaught exception. Some of the reasons being in such cases would be: the above mentioned runtime errors. Or, for instance usage of an external library which is causing some error, or not being used by the judge.

**MLE (Memory Limit Exceeded)** 
This error means that your program tried to allocate memory beyond the memory limit indicated. This can occur if you declare a very large array, or if a data structure in your program becomes too large.

**OTHER** 
This type of error is sometimes generated if you use too much memory. Check for arrays that are too large, or other elements that could grow to a size too large to fit in memory. It can also be sometimes be generated for similar reasons to the SIGSEGV error.

> Some ways to avoid runtime errors: - Make sure you aren't using variables that haven't been initialized. These may be set to 0 on your computer, but aren't guaranteed to be on the judge. - Check every single occurrence of accessing an array element and see if it could possibly be out of bounds. - Make sure you aren't declaring too much memory. 64 MB is guaranteed, but having an array of size [100000][100000] will never work. - Make sure you aren't declaring too much stack memory. Any large arrays should be declared globally, outside of any functions - putting an array of 100000 ints inside a function probably won't work.


## Time Limit Exceeded:(TLE)

The most common reason that you would get a Time Limit Exceeded is because your program is too slow. If a problem tells you that N <= 999999, and your program has nested loops each which go up to N, your program will never be fast enough. Read the bounds in the input carefully before writing your program, and try to figure out which inputs will cause your program to run the slowest.

The second most common cause of TLE is that your method of reading input and writing output is too slow. In Java, **do not use a Scanner; use a BufferedReader instead.** In C++, **do not use cin/cout - use scanf and printf instead.** In C++, you can also avoid using STL, which can be a little slow sometimes.

Also note that our judge might be slower than your machine, but the time limit is always achievable. It is common for a program to take 2-3 times as long on the judge as it does on your computer. You need to come up with faster algorithms to achieve the execution with time limit.

Also in case of TLE, it is not guaranteed that whether the solution was correct or not. There is also no way of knowing how many more seconds it could have taken to finish.

TLE IN JAVA 
If you keep receiving time limit in Java, the first thing to check is if your solution is using optimized methods of input and output. As test cases can be large in some of the problems, using Scanner and System.out might result in "Time Limit Exceeded", even though there exists a time limit multiplier (x2) times for JAVA, i.e., JAVA is assigned twice the normal time limit of the question.

> content taken from Hackerearth.


