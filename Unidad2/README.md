Asynchronous programming in Python

In the document explains the differences that characterize asynchronous programming in Python, it can perform different processes even if it does not completely end each thread.

They make us understand and explain why asynchronous programming is better than traditional linear style programming.

The way we use asynchronous programming in Python is through the multiple processes that the GPU will be responsible for sharing resources. There are already multiprocessing libraries in Python, which would save us many tasks.

If we go deeper into Python asynchronous programming, we are going to go into multiple threads, multiple threads to multiple processes are not the same. A thread is an execution line, more or less as a process, but it can have several threads in the context of a process and everyone shares access to common resources.

Corutinas with performance: They are used for cooperative multitasking.
Corroutines are similar to generators but with few additional methods and a slight change in the way we use the declaration of performance. Generators produce data for iteration, while corroutines can also consume data.



Asynchronous programming

asyncio is the new concurrency module introduced in Python 3.4. It is designed to use corroutines and futures to simplify the asynchronous code and make it almost as readable as the synchronous code since there are no callbacks.
Asyncio uses different constructions: loops of events, corutins and futures.
An event loop manages and distributes the execution of different tasks. Registers them and is responsible for distributing the flow of control among them.
Routines (previously covered) are special functions that work similar to Python generators, waiting to release the control flow back to the event loop. A routine must be scheduled to run in the event loop, once the scheduled routines are wrapped in Tasks, which is a type of Future.
Futures represent the result of a task that may or may not have been executed. This result may be an exception.
 
With Asyncio, it allows you to structure your code so that subtasks are defined as corroutines and allows you to program them as you wish, even simultaneously. Routines contain performance points where we define possible points where a context change can occur if there are other pending tasks, but it will not do so if there is no other pending task.


Async IO in Python: A Complete Walkthrough
In order to use Python Asynchronous IO (async IO), it is necessary to upgrade to version 3.7.

The parallelism consists in performing multiple operations at the same time. Multiprocessing is a means to achieve parallelism and involves the distribution of tasks over the central processing units (CPUs or cores) of a computer. Multiprocessing is very suitable for CPU-related tasks: tightly linked forbucles and mathematical calculations generally fall into this category.

Concurrence is a slightly broader term than parallelism. It suggests that multiple tasks have the ability to execute in an overlapping manner.

Threading is a concurrent execution model in which several threads take turns executing tasks. A process can contain multiple threads.

In fact, async IO is a single process and single thread design: it uses cooperative multitasking, a term that will be developed at the end of this tutorial. In other words, it has been said that asynchronous IO gives a sense of concurrence despite using a single thread in a single process. Routines (a central feature of asynchronous IO) can be programmed simultaneously, but they are not inherently concurrent.

As we saw earlier, an asynchronous routine can pause your results, allowing other routines to run.
An asynchronous code, using the previous mechanism facilitates concurrent execution.


El código asincrónico, a través del mecanismo anterior, facilita la ejecución concurrente. Para decirlo de otra manera, el código asincrónico da la apariencia de concurrencia.

Async IO toma largos períodos de espera en los cuales las funciones de otra forma estarían bloqueadas y permite que otras funciones se ejecuten durante ese tiempo de inactividad.

Cabe mencionar que la programación asíncrona en Python no es sencilla, ya que nos han mostrado diferentes temas a abordar como los multiprocesos, los hilos y la concurrencia en los procesos. Y a lo que hemos investigado es cierto, la programación asíncrona es difícil y hacer un código de multiproceso también, pero gracias la librería de Python llamada Async IO nos brinda las herramientas para hacerlo posible.

Encadenando Corutinas
Una característica clave de las corutinas es que se pueden encadenar juntas. Esto le permite dividir los programas en pequeñas, manejables y reciclables.

Usando una cola
El asyncio paquete proporciona clases de cola que están diseñadas para ser similares a las clases del módulo queue.
Existe una estructura alternativa que también puede funcionar con IO asíncrona: varios productores, que no están asociados entre sí, agregan elementos a una cola. Cada productor puede agregar varios elementos a la cola en momentos escalonados, aleatorios y sin previo aviso. Un grupo de consumidores saca artículos de la cola a medida que aparecen, con avidez y sin esperar ninguna otra señal.

Procesamiento Paralelo
El procesamiento paralelo es un modo de operación donde la tarea se ejecuta simultáneamente en múltiples procesadores en la misma computadora. Está destinado a reducir el tiempo total de procesamiento.
La cantidad máxima de procesos que puede ejecutar a la vez está limitada por la cantidad de procesadores en su computadora. Si no sabe cuántos procesadores hay en la máquina, la función lo mostrará.cpu_count()multiprocessing

Una ejecución síncrona es aquella en la que los procesos se completan en el mismo orden en que se inició. Esto se logra bloqueando el programa principal hasta que finalicen los procesos respectivos.

Asíncrono, por otro lado, no implica bloqueo. Como resultado, el orden de los resultados puede confundirse, pero generalmente se hace más rápido.

Paralelización usando Pool.apply ()
Se paraleliza la función usando .howmany_within_range()multiprocessing.Pool()



Paralelización usando Pool.map ()
Pool.map()acepta solo un iterable como argumento. 

Paralelización usando Pool.starmap ()
Acepta solo un iterable como argumento, pero en , cada elemento en ese iterable también es iterable. Puede proporcionar los argumentos a la 'función a ser paralelizada' en el mismo orden en este elemento iterable interno, a su vez se desempaquetará durante la ejecución.Pool.map()Pool.starmap()starmap()

Procesamiento paralelo asincrónico
Los equivalentes asíncronos , y le permiten ejecutar los procesos en paralelo de forma asíncrona, es decir, el siguiente proceso puede comenzar tan pronto como se complete el anterior sin tener en cuenta el orden de inicio. Como resultado, no hay garantía de que el resultado esté en el mismo orden que la entrada.apply_async()map_async()starmap_async()

Paralelización con Pool.apply_async ()
apply_async() debe proporcionar una función de devolución de llamada que le indique cómo se deben almacenar los resultados calculados.apply()

Cuando se trata de paralelizar a DataFrame, puede hacer que la función sea paralelizada para tomar como parámetro de entrada una fila del marco de datos, una columna del marco de datos, todo el marco de datos en sí.
