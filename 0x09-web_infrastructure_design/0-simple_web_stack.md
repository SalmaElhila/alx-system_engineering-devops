Specifics about this infrastructure:
-	What is a server?
A server is a computer hardware or software that provides services to other computers, which are usually referred to as clients.
-	What is the role of the domain name?
It provides a human-friendly alias for an IP Address. For example, the domain name www.foobar.com is easier to recognize and remember than 8.8.8.8
-	What type of DNS record www is in www.foobar.com?
www.foobar.com uses an A record. This can be checked by running dig www.foobar.com.
Note: the results might be different but for the infrastructure in this design, an A record is used.
Address Mapping record (A Record)—also known as a DNS host record, stores a hostname and its corresponding IPv4 address.
-	What is the role of the web server?
The web server is a software/hardware that accepts requests via HTTP or secure HTTP (HTTPS) and responds with the content of the requested resource or an error message.
-	What is the role of the application server?
It serves as an intermediary between a client application (such as a web browser or a mobile app) and the database server.
-	What is the role of the database?
It helps organizing information so it could be easily accessed, managed and updated.
-	What is the server using to communicate with the computer of the user requesting the website?
Communication between the client and the server occurs over the internet network through the TCP/IP protocol suite.


Issues with this infrastructure:
-	SPOF
There are multiple SPOF (Single Point Of Failure) in this infrastructure. For example, if the MySQL database server is down, the entire site would be down.
-	Downtime when maintenance needed (like deploying new code web server needs to be restarted)
When we need to run some maintenance checks on any component, they have to be put down or the server has to be turned off. Since there's only one server, the website would be experiencing a downtime.
-	Cannot scale if too much incoming traffic
Only one server contains the required components in this infrastructure. It can easily run out of resources or face a downtime. 

