Video 1 review: What is a distributed system
-----------------------------------

In the video he explains that what is a distributed system, in which he recommends not doing centralized systems, these have their advantages and disadvantages

The centralized systems are low cost, easy to understand and fast for a simple user.

The disadvantages are that if the connection to the system is lost, you will no longer be able to access the information inside.

Distributed systems are fault tolerant, if the connection with one is lost, you have access to the information.
They are scales, that is, it can support more than one user.

Explain distributed system part two
-----------------------------------
In the video he explains that a more complex system does not make it a disadvantage, since that helps to make it more secure and reliable.
Mention that Facebook and Google use distributed systems since you have to be mass scalable,they have to be fast and very safe.
If we send an email and it reaches a server that is failing, it will not be sent. But this will not happen to everyone who sends an email, but the other emails that are sent are sent to other servers.


//////////////////////////////////////////////////


Video 2: It explains why we should create a distributed system.
-----------------------------------

10- You should know the reasons why you should create a distributed system.
9- Because it's fun and it's because it's your job to create better solutions.
8- You will need a force server to solve problems that you cannot do simply with a simple computer. Explain that if you handle an application or chat and require information sharing, the server will also be necessary.
7- You need policies in the distributed system (rules).
6- You must create a system proportional to the users who use it, you should not make a system too expensive if you will not take advantage.


Continuing with the video 2 summary.
-----------------------------------

5- You must create a trust-based system and have a good design implemented.

4- PERFORMANCE: You must have a distributed system established in a place where customers do not suffer from weak coverage. The closer it is the better.

3- You must depend on a cloud service, it is not necessary to have a system distributed with 2 carriers.

2- You must have a distributed system with good support, not only on a single computer, but more so that it is safer and thus avoid problems

1- You must create a scalable distributed system, to avoid problems in the future and thus improve your performance and reduce costs. It only applies if you really know what it will take in the future

You should always know why you are going to create a distributed system, but you will only do a job for nothing.

Thats all.

/////////////////////////////////////////////////////

Video 3: How to learn distributed system?
-----------------------------------
In the video he explains how to learn about distributed systems, which is a study in systems and not in theory.

It shows that systems, even if they fail, can continue to function.

There are different types of architectures of distributed systems, this makes them safer for their different implementations


Continuing with the video 3 summary.
-----------------------------------

We need to know exactly what type of distributed system we are going to implement so that it has a better performance when using it.

We need to have established names to our processes so that they can be easily found by the other computers connected to the system.

When working with distributed systems we must take into account the time, since in the systems events or situations will occur and both users and the server must be correctly synchronized.

/////////////////////////////////////////////////////

video 4: What could go wrong?
-----------------------------------

The video title is: What could go wrong?

In the video he explains that if we make a fault-tolerant system, we must know the failures that are going to occur and identify the errors that we could not solve in case they happen.

He asks us a question saying what would be the problems that we would present in our distributed systems.

1- The server stops working
2- That it fails constantly
3- That the information be lost
4- Denial of service attacks


///////////////////////////////////////////////////////

Video 5: The many types of failures
------------------------------------


When we make distributed systems, we have to have classified the types of failures that will present us to have better solutions.

There is a great different between the failure of a network to the failure of a node.

When the network fails, you can lose packets, information, data.

If we have a network, the information can be set to be in 1 node or several, so the information is more secure and simple to use. This prevents congestion and corruption of information.

If we use a network of nodes and a node has to send information to another node, and this fails, the node will look for another route to be able to send the information that was requested. All this is done thanks to the network partition.

If we are connected to a network and a node fails, the nodes will be divided into 2 subnets to continue interacting with each other. They will always be divided by 2 to have the same number of nodes.


Continuing with the video 5 summary: The many types of failures
------------------------------------


The main node failures can be caused by power outages, hardware failures or running out of memory or filling your storage disk. A fail stop is simple as any engineer can take certain strategies. when it stops and is still on one can restart it and restore the data to the last point, this is called checkpoint point, the restart time of the computer can generate high latency
Another option is to switch another node, for this the status is saved periodically on other computers

Another fault that has to be dealt with is the Byzantine failure
Bit flip in memory or on disk corrupts data, you may also receive previous versions of messages or some of the nodes may run a malicious software version
