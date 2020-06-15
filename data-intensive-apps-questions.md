# Designing Data-Intensive Applications

## Questions

**1. Why is it hard to find the perfect tools to manage an application database?**

Because nowadays, there are many tools and many types of databases, as well as different hardware and software requirements. When deciding which tools or database type to use, it is necessary to take in consideration the aim, functions and needs of the application.

**2. How is it possible to create a new, special-purpose data system?**

By combining several tools which will be hidden inside the application programming interface (API), in a way that said system will be composed from smaller components working as one.


**3. What are the main 3 concerns of software systems?**

  -The system should always work correctly.
  
  -The system is capable of growing as users demand.
  
  -The system is capable to receive maintance by different people.

**4. When and why is reliability most important?**

Reliability is especially important when we are talking about software systems designed for delicate operations, such as air traffic control, power stations, police departments, hospitals, etc. Bugs with the software on said cases can lead to legal risks (lawsuits) or even human losses.

**5. What's the difference between latency and response time, and which is more important?**

Response time is the time that the client has to wait to obtain the result of a request or query. This time includes the processing time, network and queuing delays. 

Latency is the duration that the request waits to be processed.

Both are important in their own way, but given that response time includes the latency and that ensuring a good user experience should be a priority, response time is the most important.

6.

