## Index
- [Video 1 What is a distributed system](#video-1-what-is-a-distributed-system)
- [Video 2 Why build a distributed system](#video-2-why-build-a-distributed-system)
- [Video 3 How to learn distributed system?](#video-3-how-to-learn-distributed-system)
- [Video 4 What could go wrong?](#video-4-what-could-go-wrong)
- [Video 5 The many types of fail](#Video-5-the-many-types-of-fail)
- [Video 6 Byzantine fault tolerance](#video-6-byzantine-fault-tolerance)
- [Video 7 SLIs SLOs and SLAs](#video-7-slis-slos-and-slas)
- [Video 8 Class Project](#video-8-lass-roject)
- [Video 9 Paxos Simplified](#video-9-paxos-simplified)
- [Video 11 Introduction to Blockshain Consensus](#video-11-introduction-to-blockshain-consensus)
- [Video 12 What is a Blockshain](#Video-12-what-is-a-blockshain)
- [Video 13 Bitcoin Blockshain Consensus](#video-13-bitcoin-blockshain-consensus)
- [Video 14 Should you use Bitcoin consensus](#video-14-should-you-use-bitcoin-consensus)
- [Video 15 Distributed System Design Example](#video-15-distributed-system-design-example)
- [Video 16 The CAP Theorem](#video-16-the-cap-theorem)

## Video 1 What is a distributed system

*In the video he explains that what is a distributed system, in which he recommends not doing centralized systems, these have their advantages and disadvantages

The centralized systems are low cost, easy to understand and fast for a simple user.

The disadvantages are that if the connection to the system is lost, you will no longer be able to access the information inside.

Distributed systems are fault tolerant, if the connection with one is lost, you have access to the information.
They are scales, that is, it can support more than one user.

Explain distributed system part two
-----------------------------------
In the video he explains that a more complex system does not make it a disadvantage, since that helps to make it more secure and reliable.
Mention that Facebook and Google use distributed systems since you have to be mass scalable,they have to be fast and very safe.
If we send an email and it reaches a server that is failing, it will not be sent. But this will not happen to everyone who sends an email, but the other emails that are sent are sent to other servers.*


## Video 2 Why build a distributed system

*10- You should know the reasons why you should create a distributed system.
9- Because it's fun and it's because it's your job to create better solutions.
8- You will need a force server to solve problems that you cannot do simply with a simple computer. Explain that if you handle an application or chat and require information sharing, the server will also be necessary.
7- You need policies in the distributed system (rules).
6- You must create a system proportional to the users who use it, you should not make a system too expensive if you will not take advantage.*


***Continuing with the video 2 summary.***

*5- You must create a trust-based system and have a good design implemented.

4- PERFORMANCE: You must have a distributed system established in a place where customers do not suffer from weak coverage. The closer it is the better.

3- You must depend on a cloud service, it is not necessary to have a system distributed with 2 carriers.

2- You must have a distributed system with good support, not only on a single computer, but more so that it is safer and thus avoid problems

1- You must create a scalable distributed system, to avoid problems in the future and thus improve your performance and reduce costs. It only applies if you really know what it will take in the future

You should always know why you are going to create a distributed system, but you will only do a job for nothing.

Thats all.*



## Video 3 How to learn distributed system?

*In the video he explains how to learn about distributed systems, which is a study in systems and not in theory.

It shows that systems, even if they fail, can continue to function.

There are different types of architectures of distributed systems, this makes them safer for their different implementations*


***Continuing with the video 3 summary.***
-----------------------------------

*We need to know exactly what type of distributed system we are going to implement so that it has a better performance when using it.

We need to have established names to our processes so that they can be easily found by the other computers connected to the system.

When working with distributed systems we must take into account the time, since in the systems events or situations will occur and both users and the server must be correctly synchronized.*


## Video 4 What could go wrong

*The video title is: What could go wrong?

In the video he explains that if we make a fault-tolerant system, we must know the failures that are going to occur and identify the errors that we could not solve in case they happen.

He asks us a question saying what would be the problems that we would present in our distributed systems.

1- The server stops working
2- That it fails constantly
3- That the information be lost
4- Denial of service attacks*

## Video 5 The many types of fail

*When we make distributed systems, we have to have classified the types of failures that will present us to have better solutions.

There is a great different between the failure of a network to the failure of a node.

When the network fails, you can lose packets, information, data.

If we have a network, the information can be set to be in 1 node or several, so the information is more secure and simple to use. This prevents congestion and corruption of information.

If we use a network of nodes and a node has to send information to another node, and this fails, the node will look for another route to be able to send the information that was requested. All this is done thanks to the network partition.

If we are connected to a network and a node fails, the nodes will be divided into 2 subnets to continue interacting with each other. They will always be divided by 2 to have the same number of nodes.*


***Continuing with the video 5 summary: The many types of failures***

*The main node failures can be caused by power outages, hardware failures or running out of memory or filling your storage disk. A fail stop is simple as any engineer can take certain strategies. when it stops and is still on one can restart it and restore the data to the last point, this is called checkpoint point, the restart time of the computer can generate high latency
Another option is to switch another node, for this the status is saved periodically on other computers

Another fault that has to be dealt with is the Byzantine failure
Bit flip in memory or on disk corrupts data, you may also receive previous versions of messages or some of the nodes may run a malicious software version*

## Video 6 Byzantine fault tolerance

*Byzantine failures can be nodes that send conflict messages to other nodes, this can cause the results to be incorrect,
squamous nodes can be one of the things that proves that failure, just like a malicious node that could be affected by a hacker.

There are 2 general problems, the consensus problem is when two nodes*

## Video 7: SLIs SLOs and SLAs

*Review of video 7: SLI SLO and SLA

SLI: Service level indicator (Service level indicator): What are you measuring: Indicates the response time to the request that the user is requesting from the system.

SLO: Service level Objective: How good it should be: We want all users or at least 99% to obtain the requested results in set times (for example, 500 milliseconds)

SLA: Service level agreement: SLO + consequences: It is the same as the SLO, only that it integrates a system in which you assure the client that his system will work, otherwise, you pay the consequences of what was promised .

Studying these 3 terms helps us learn what really matters, we don't waste time on things that don't matter.

A reliable 90% system is inactive for 3 days a month.
A reliable 99% system is inactive for 7 hours per month.
A reliable 99.9% system is idle for 43 minutes per month.
A reliable 99.99% system is inactive for 4 minutes per month.

To reach the reliability of 99.999% per month, it is almost impossible since they are 25 inactive seconds per month and for a system to be repaired in such a short time it is difficult.

Microsoft, Azure, Mazon and Google promise 99.95% uptime, which is 22 minutes a month that is not active. This is checked every minute.*

## Video 8 Class Project

*A multi-user char will be built in the project class
an appspot.com chat was created, upon entering you are asked if it is okay to share your email address with this application.
Once accessing, it retrieves the last message sent on the server and displays it on the screen.
When you send a new message in the chat, everyone who is connected to the server can see the message, and it is saved in the app engine data store.

AppEngine Pros:
Scaling done, authentication done, reliable storage, multicast done, SRE as a service, simple code.

App Engine Cons:
Cost money, only uses google login, channel deprocated, needs loadtesting, needs application-level monitoring.*

## Video 9 Paxos Simplified

*Paxos is a family of protocols for solving consensus in a network of unreliable processors (that is, processors that may fail). Consensus is the process of agreeing on one result among a group of participants. This problem becomes difficult when the participants or their communication medium may experience failures.

Suppose the decision is to take the largest number. Therefore a proposal in a round is considered valid if it is greater than the rest of the proposals in that round. All those proposals for that round with smaller numbers are considered invalid.

It also explains the problem of the Byzantine generals. How to find a traitor if there are generals or lieutenants.*

## Video 11 Introduction to Blockshain Consensus

*This video gives us a brief summary of what the following videos will be about.
in the first video he will explain the bitcoin dlockshain, in the second video it will be seen how to replicate a blockshain to another computer forming a consensus.
in the third video the bitcoin blockshain consensus algorithm will be shown to compare it with the paxos algorithm.*

## Video 12 What is a Blockshain

*Blockshain is a data structure
Suppose we have a quantity of data, we store that data in a block and place an empty header. When more data arrives we create a second block in which and the hash of the first block will be placed to calculate that the first block is fine. It also serves to realize that an attacker tries to enter our block.
In the case of blockshain bitcoins, the data is not stored in block but uses a data structure called Merkel's tree.
A Merkel tree is a binary tree, so each node contains the ash of the nodes below it.*

## Video 13 Bitcoin Blockshain Consensus

*A bitcoin consensus cannot be created with basic algorithms like the raft of paxos and pbft since you may not reach a consensus because you don't have many votes available to complete the algorithm.
Another problem is that if many bad computers are connected they can balance the votes, they can stop the system of creating consensus.
Bitcoin needs an algorithm that is resistant to attackers who have accessed.
To generate a bitcoin consensus you need to create a new block, that new block needs to be replicated to all the good nodes of the system.
Our systems have livelock because we can add new blocks faster than learn them.
The solution to this problem is to slow down our system, so every time you want to add a block you sleep a random period of time and after that time the block is added.
When a network partition is created between the computers that were connected, the new blocks that are added will no longer get them from the other part of the network.
to make a timer you can use cryptography and reliable computer modules.*

## Video 14 Should you use Bitcoin consensus

*In bitcoin it is necessary to maintain an algorithm that is resistant to attacks, and is safe for users. Blockshain compared to other algorithms, is slower and has a high consumption of resources, but it is quite safe.

A disadvantage of bitcoin is that it takes a long time to save the information of a block, since each block carries a duplicate of the previous one, but still bitcoin maintains a lower consumption of resources.
Paxos or bullets can become even safer than the Blockshain algorithm*

## Video 15 Distributed System Design Example

*The acronym in English G U I D stands for Globally Unique ID, it is a unique identifier for each transaction made, that is, it will never generate an identical number on the same computer or on a system. Like the GetDate function, you are creating a different identifier every millisecond even if the function is corrupted, but in this use it is necessary for the same computer.

For this you can use the identity, which consists of:
IP address
Ethernet HW Address
CPU serial number

To create an identifier that does not exist in the past we will use something called Monotonically increasing unique ID*

## Video 16 The CAP Theorem

*The computer scientists ask: how reliable can we build a system
Consistency
Availability
Partition Tolerance

We have seen distributed systems a lot in banks. The bank has our money balance and at the ATM it synchronizes and has access to the movements that the user can make, such as withdrawing money.

But there are also failures in these distributed systems, using an example of a customer goes to withdraw money from an ATM:

The first is if the customer goes to an ATM and is not working, he will have to find another to make his request.

The second is that the client goes to the other ATM and is not working either


For these types of problems, it is necessary to use “The Cap Theorem”
Formalizes the trade-off between consistency and availability in the presence of partitions*


**Authors**
*Martinez Iribe David Ernesto
Quintero Renteria Omar Israel*
