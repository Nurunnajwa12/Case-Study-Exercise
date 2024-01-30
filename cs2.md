# Case Study 2: Netflix System Design

### Question:
- How does Netflix use Kafka and Cassandra to handle streaming data and ensure availability?
- What are the challenges of scaling Netflix's backend to serve millions of users across the globe?
- How does Netflix use AWS cloud services to optimize its performance and reduce costs?
- What are the trade-offs of using eventual consistency over strong consistency for Netflix's data storage?
- How does Netflix use Hystrix and Zuul to implement fault tolerance and load balancing for its microservices?


1. **Use of Kafka and Cassandra for Streaming Data and Availability:**
   - **Kafka:** Netflix uses Apache Kafka for stream processing. Kafka serves as a distributed streaming platform that can publish, subscribe to, store, and process streams of records in real time. In Netflix's context, it's used for event sourcing where actions by users (like play, pause, stop) are captured as events and processed. Kafka's distributed nature helps in reliably handling high volumes of messages.
   - **Cassandra:** Apache Cassandra is a distributed NoSQL database favored for its scalability and high availability without compromising performance. Netflix utilizes Cassandra for its ability to handle large amounts of data across multiple data centers and cloud regions. This is crucial for Netflix's global user base, ensuring that the system remains operational even in the case of server or data center failures.

2. **Challenges of Scaling Netflix’s Backend:**
   - **Handling High Traffic and Data Volume:** As the user base grows, handling the massive influx of data and maintaining a seamless streaming experience becomes challenging.
   - **Global Distribution:** Ensuring low latency for a global audience requires strategically located data centers and efficient content delivery networks.
   - **Resource Management:** Efficiently allocating resources to handle varying loads and optimizing server capacity to reduce costs without affecting performance.
   - **Data Consistency:** Managing data consistency across distributed systems while maintaining high availability and performance.

3. **Use of AWS Cloud Services:**
   - Netflix heavily relies on Amazon Web Services (AWS) for its infrastructure needs. AWS provides a highly reliable, scalable, and low-latency environment.
   - **EC2 Instances:** For compute capacity to run applications.
   - **S3:** For storage and backup of massive media files and other data.
   - **CloudFront:** As a content delivery network (CDN) to serve content to users from the nearest geographical location.
   - **AWS’s Elastic Load Balancing and Auto Scaling:** To manage the load and automatically scale the resources as per demand, which helps in performance optimization and cost reduction.

4. **Eventual Consistency vs. Strong Consistency Trade-offs:**
   - Netflix opts for eventual consistency in its data storage (like in Cassandra) which means the system will eventually become consistent over time.
   - **Pros:** Higher availability, better tolerance for network partitions, and faster read/write operations, which are crucial for a global service like Netflix.
   - **Cons:** The trade-off is the possibility of reading stale data; users might not see the most current data immediately, which is generally acceptable for Netflix's use case (e.g., viewing history, watch lists).

5. **Use of Hystrix and Zuul:**
   - **Hystrix:** Netflix uses Hystrix for circuit breaking and fault tolerance. In a microservices architecture, if one service fails, Hystrix prevents this failure from cascading to other services. It does this by stopping cascading failures and providing fallback options, ensuring that the system remains robust and resilient.
   - **Zuul:** Zuul is an API gateway that provides dynamic routing, monitoring, resiliency, and security. Netflix uses Zuul for load balancing and to route requests to the appropriate backend systems. It helps in managing incoming traffic and distributing it across multiple resources, thereby balancing the load and ensuring that no single service gets overwhelmed.

