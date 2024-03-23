Distributed Web Infrastructure Summary
Overview
This infrastructure is designed to manage web traffic more effectively by spreading the load between a main server and a replica server, with a load balancer directing traffic to optimize server use.

Key Details
Load Balancing Algorithm: Utilizes HAProxy with a Round Robin algorithm, cycling through servers based on their assigned weights to evenly distribute processing time. This dynamic method allows for real-time adjustment of server weights.

Load Balancer Setup: Implements an Active-Passive configuration through HAProxy, where not all nodes serve workloads simultaneously. This setup ensures one node is always on standby to take over if the active node fails, enhancing reliability but not maximizing throughput as an Active-Active setup would.

Primary-Replica Database Configuration: Features a Primary server for read/write operations and a Replica server primarily for read operations to minimize read traffic to the Primary. Data synchronization occurs after each write operation in the Primary server.

Application Node Differences: The Primary node handles all write operations required by the website, while the Replica node assists by managing read requests, lightening the load on the Primary node.

Infrastructure Challenges
Single Points of Failure (SPOF): Several vulnerabilities exist; for instance, if the Primary database server fails, the site can't process changes. The load balancer and the application server linked to the primary database also represent single points of failure.

Security Concerns: The absence of SSL certificates means data isn't encrypted, posing a risk of interception. Additionally, the lack of firewalls means there's no mechanism to block potentially harmful or unauthorized IP addresses.

Lack of Monitoring: Without a monitoring system, it's difficult to assess the health or status of each server, hindering proactive management and response to issues.

This infrastructure aims to balance efficiency with reliability by distributing loads between servers and using a load balancer to manage traffic. However, it also faces significant challenges related to security, resilience against failures, and the need for comprehensive monitoring to maintain optimal operation.







