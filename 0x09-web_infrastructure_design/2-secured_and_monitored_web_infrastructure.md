Specifics about this infrastructure:
	For every additional element, why you are adding it?

	What are firewalls for?
The firewalls are for protecting the network (web servers, anyway) from unwanted and unauthorized users by acting as an intermediary between the internal network and the external network and blocking the incoming traffic matching the aforementioned criteria.
Why is the traffic served over HTTPS?
	What monitoring is used for?
The monitoring clients are for monitoring the servers and the external network. They analyse the performance and operations of the servers, measure the overall health, and alert the administrators if the servers are not performing as expected. The monitoring tool observes the servers and provides key metrics about the servers' operations to the administrators. It automatically tests the accessibility of the servers, measures response time, and alerts for errors such as corrupt/missing files, security vulnerabilities/violations, and many other issues.
	How the monitoring tool is collecting data?
monitoring tools collect data by using various methods and protocols to gather information about the performance, status, and behavior of network devices and services.
Explain what to do if you want to monitor your web server QPS


Issues with this infrastructure:
	Why terminating SSL at the load balancer level is an issue?
Terminating SSL at the load balancer level would leave the traffic between the load balancer and the web servers unencrypted.
	Why having only one MySQL server capable of accepting writes is an issue?
Having one MySQL server is an issue because it is not scalable and can act as a single point of failure for the web infrastructure.
	Why having servers with all the same components (database, web server and application server) might be a problem?
Having servers with all the same components would make the components contend for resources on the server like CPU, Memory, I/O, etc., which can lead to poor performance and also make it difficult to locate the source of the problem. A setup such as this is not easily scalable.

