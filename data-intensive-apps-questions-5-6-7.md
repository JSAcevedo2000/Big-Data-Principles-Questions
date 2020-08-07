# Chapter 5

**1. What is the "read-after-write consistency" and what is its main limitation?**

It is a guarantee that the page will show all the updates made if it is reloaded, if the update was submitted by the user reloading. Its main limitation is that this guarantee is not valid when talking about updates made by other users.

**2. What is "replication"?**

Replication is a strategy for distributing data processes across multiple nodes, it keeps multiple copies of the data in several different places.

**3. Can replication lag be mitigated?**

Some specific types of lag can be mitigated (at the cost of performance and complexity), if doing so is desirable for the application.

**4. What is the main problem with multi-leader replication and how can it be solved?**

The principal problem with this class of replication is that concurrent authoritative writes may occur on multiple leaders.
To prevent it, we must include some kind of conflict resolution in our architecture.


# Chapter 6

**1. What is a skewed partition and how does it affect partitioning?**

A partition is called skewed when some partitions have more data or queries than other (are unfair).
A skewed partition is less effective than no-skewed ones. 

**2. What is partitioning and when is it useful?**

Partitioning is the splitting of data across multiple nodes. It should not be confused with replication, as partitioning occurs in the same place instead of in accross different places. It is especially useful for scaling to particularly large datasets and, usually, it is used along replication.

**3. What is one of the main problems oof partitions?**

The main problem when working with partitions is the creation of hotspots: they happen when data is not accessed or written to equally. This can result in a degraded architecture performance.

**4. Is there a way to partition without creating hotspots? How?**

Partitioning by key hash means no hot spots. It is based in having a good hashing function, which will uniformally distribute skewed data, avoiding hotspots at the cost of range query performace.


# Chapter 7

**1. Why are concurrency bugs hard to reason about and to find by testing?**

Because this kind of bug, when it occurs in large applications, makes difficult to find  which codes are accessing the database at any given time. 
They are find to test because they only occurs in certain situations regarding timing,  which makes them difficult to reproduce when testing.

**2. What is a transaction in a Data Management context?**

A transaction is basically any action in our data that is guaranteed, in other words, any action that has been registered to happen.
Transactions do not exist in all architecture or applications, and some architecture or applications are not designed to work with them.

**3. Mention the 4 concepts of the ACID-type transactions and describe them**

Atomic - all the transactions should have a boolean result, either their are completed or not.

Consistency - all the transactions are valid, that they can exist in our data.

Isolated - each transaction is independent of any other, and a transaction cannot affect in any way a different one.

Durable - a transaction must be completed without data loss.

**4. When can we call an operation to be "single-object"?**

An operation can be classified as single-object if it only touches one record in the database (depending on the database we are working it, said record could also be a row, a document, a value, etc.). All single-object operations include the Isolation and Atomicity features naturally, so it is important to focus on the other 2 ACID concepts when working with them.
