# Chapter 5

1. What is the "read-after-write consistency" and what is its main limitation? It is a guarantee that the page will show all the updates made if it is reloaded, if the update was submitted by the user reloading. Its main limitation is that this guarantee is not valid when talking about updates made by other users.

2. What is "replication"?
Replication is a strategy for distributing data processes across multiple nodes, it keeps multiple copies of the data in several different places.

3. Can replication lag be mitigated?
Some specific types of lag can be mitigated (at the cost of performance and complexity), if doing so is desirable for the application.

4. What is the main problem with multi-leader replication and how can it be solved?
The principal problem with this class of replication is that concurrent authoritative writes may occur on multiple leaders.
To prevent it, we must include some kind of conflict resolution in our architecture.


# Chapter 6

1. What is a skewed partition and how does it affect partitioning? 
A partition is called skewed when some partitions have more data or queries than other (are unfair).
A skewed partition is less effective than no-skewed ones. 

2. 


3. 


4. 


# Chapter 7

1. Why are concurrency bugs hard to reason about and to find by testing? 
Because this kind of bug, when it occurs in large applications, makes difficult to find  which codes are accessing the database at any given time. 
They are find to test because they only occurs in certain situations regarding timing,  which makes them difficult to reproduce when testing.

2. 


3. 


4. 
