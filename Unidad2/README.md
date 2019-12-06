***Asynchronous programming in Python***

In the document explains the differences that characterize asynchronous programming in Python, it can perform different processes even if it does not completely end each thread.

They make us understand and explain why asynchronous programming is better than traditional linear style programming.

The way we use asynchronous programming in Python is through the multiple processes that the GPU will be responsible for sharing resources. There are already multiprocessing libraries in Python, which would save us many tasks.

If we go deeper into Python asynchronous programming, we are going to go into multiple threads, multiple threads to multiple processes are not the same. A thread is an execution line, more or less as a process, but it can have several threads in the context of a process and everyone shares access to common resources.

Corutinas with performance: They are used for cooperative multitasking.
Corroutines are similar to generators but with few additional methods and a slight change in the way we use the declaration of performance. Generators produce data for iteration, while corroutines can also consume data.



***Asynchronous programming***

asyncio is the new concurrency module introduced in Python 3.4. It is designed to use corroutines and futures to simplify the asynchronous code and make it almost as readable as the synchronous code since there are no callbacks.
Asyncio uses different constructions: loops of events, corutins and futures.
An event loop manages and distributes the execution of different tasks. Registers them and is responsible for distributing the flow of control among them.
Routines (previously covered) are special functions that work similar to Python generators, waiting to release the control flow back to the event loop. A routine must be scheduled to run in the event loop, once the scheduled routines are wrapped in Tasks, which is a type of Future.
Futures represent the result of a task that may or may not have been executed. This result may be an exception.
 
With Asyncio, it allows you to structure your code so that subtasks are defined as corroutines and allows you to program them as you wish, even simultaneously. Routines contain performance points where we define possible points where a context change can occur if there are other pending tasks, but it will not do so if there is no other pending task.


***Async IO in Python: A Complete Walkthrough***

In order to use Python Asynchronous IO (async IO), it is necessary to upgrade to version 3.7.

The parallelism consists in performing multiple operations at the same time. Multiprocessing is a means to achieve parallelism and involves the distribution of tasks over the central processing units (CPUs or cores) of a computer. Multiprocessing is very suitable for CPU-related tasks: tightly linked forbucles and mathematical calculations generally fall into this category.

Concurrence is a slightly broader term than parallelism. It suggests that multiple tasks have the ability to execute in an overlapping manner.

Threading is a concurrent execution model in which several threads take turns executing tasks. A process can contain multiple threads.

In fact, async IO is a single process and single thread design: it uses cooperative multitasking, a term that will be developed at the end of this tutorial. In other words, it has been said that asynchronous IO gives a sense of concurrence despite using a single thread in a single process. Routines (a central feature of asynchronous IO) can be programmed simultaneously, but they are not inherently concurrent.

As we saw earlier, an asynchronous routine can pause your results, allowing other routines to run.
An asynchronous code, using the previous mechanism facilitates concurrent execution.

The asynchronous code, through the previous mechanism, facilitates concurrent execution. To put it another way, the asynchronous code gives the appearance of concurrency.

Async IO takes long waiting periods in which functions would otherwise be locked and allows other functions to be executed during that downtime

It is worth mentioning that asynchronous programming in Python is not simple, since we have been shown different topics to address such as multiprocesses, threads and concurrence in processes. And what we have investigated is true, asynchronous programming is difficult and make a multithreaded code as well, but thanks to the Python library called Async IO it gives us the tools to make it possible.

***Chaining Corutinas***

A key feature of corutins is that they can be chained together. This allows you to divide the programs into small, manageable and recyclable.

***Using a tail***

The asyncio package provides queue classes that are designed to be similar to the queue module classes.
There is an alternative structure that can also work with asynchronous IO: several producers, who are not associated with each other, add elements to a queue. Each producer can add several elements to the queue at staggered, random moments and without prior notice. A group of consumers pull items out of the queue as they appear, greedily and without waiting for any other signal.

***Parallel Processing***

Parallel processing is a mode of operation where the task runs simultaneously on multiple processors on the same computer. It is intended to reduce the total processing time.
The maximum number of processes you can run at once is limited by the number of processors on your computer. If you don't know how manyprocessors are in the machine, the function will show it.cpu_count () multiprocessing

A synchronous execution is one in which the processes are completed in the same order in which they started. This is achieved by blocking the main program until the respective processes are finished.

Asynchronous, on the other hand, does not imply blocking. As a result, the order of the results can be confused, but generally it becomes faster.

***Parallelization using Pool.apply ()***

The function is parallelized using .howmany_within_range () multiprocessing.Pool ()

***Parallelization using Pool.map ()***

Pool.map () accepts only one iterable argument.

***Parallelization using Pool.starmap ()***

Accept only one iterable as an argument, but in, each element in that iterable is also iterable. You can provide the arguments to the 'function to be parallelized' in the same order in this internal iterable element, in turn it will be unpacked during execution.Pool.map () Pool.starmap () starmap ()

***Asynchronous Parallel Processing***

Asynchronous equivalents, and allow you to execute processes in parallel asynchronously, that is, the next process can begin as soon as the previous one is completed without taking into account the starting order. As a result, there is no guarantee that the result will be in the same order as the entry.apply_async () map_async () starmap_async ()

***Parallelization with Pool.apply_async ()***

apply_async () must provide a callback function that tells you how the calculated results should be stored.
When it comes to parallelizing DataFrame, you can make the function parallel to take as input parameter a row of the data frame, a column of the data frame, the entire data frame itself.
