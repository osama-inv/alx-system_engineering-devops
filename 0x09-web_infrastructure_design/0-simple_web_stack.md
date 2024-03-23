Simplified Web Stack Overview
Overview
This setup is a basic web system hosting a site accessible at www.foobar.com, lacking firewalls and SSL certificates for security. The server’s resources—CPU, RAM, SSD—are shared among its components, like the database and app server.

Key Components Explained
Server: A piece of computer hardware or software that offers services to other computers, known as clients.

Domain Name: Acts as an easy-to-remember address for a website, like www.foobar.com, instead of using a numeric IP address. The Domain Name System (DNS) links the domain name to the IP address.

DNS Record for www: www.foobar.com is linked to an IP address through an A record, found by using tools like dig.

Web Server: The technology that processes requests via HTTP/HTTPS and sends back either the requested webpage or an error.

Application Server: Hosts and manages web applications and services for users and organizations, ensuring the delivery of content.

Database: Organizes and stores data in a way that makes it easy to retrieve, manage, and update.

Communication: The server and client communicate over the internet using the TCP/IP protocol suite.

Infrastructure Challenges
Single Points of Failure (SPOF): The setup has several vulnerabilities. For example, if the database fails, the entire site goes down.

Maintenance Downtime: Performing maintenance on any part requires shutting it down, leading to site unavailability due to the single-server setup.

Difficulty Scaling: Handling increased traffic is a challenge with this structure since all components reside on one server, which can quickly become overwhelmed.
