Overview
This project implements a secure multi-tier web application infrastructure that separates concerns between different layers of the application. The architecture includes a Load Balancer, Web Server, and Database Server, each running on separate servers to enhance security and scalability. This project focuses on implementing best practices for security, including SSL encryption, firewall configurations, and database access controls.

Table of Contents
Features
Architecture
Technologies Used
Prerequisites
Installation Guide
Configuration
Testing the Application
Security Measures
Contributing
License
Features
Multi-tier architecture for enhanced security and scalability.
Load balancing using HAProxy.
Web server running Nginx to serve static content.
Database server using MySQL with strict access controls.
SSL encryption for secure data transmission.
Firewall rules to restrict access based on predefined policies.
Architecture
The architecture consists of three main components:

Load Balancer (HAProxy): Distributes incoming traffic across multiple web servers for improved performance and reliability.
Web Server (Nginx): Serves static content and forwards requests to the application layer.
Database Server (MySQL): Stores application data and is secured with strict access controls.
lua
Copy code
          +----------------+
          | Load Balancer  |
          |     (HAProxy)  |
          +-------+--------+
                  |
       +----------+----------+
       |                     |
+------+-----+      +-------+-----+
|  Web Server 1|      |  Web Server 2|
|     (Nginx)  |      |     (Nginx)  |
+------+-----+      +-------+-----+
       |                     |
       +----------+----------+
                  |
          +-------+--------+
          |   Database      |
          |    (MySQL)      |
          +-----------------+
Technologies Used
Linux (Ubuntu/CentOS)
HAProxy for load balancing
Nginx as the web server
MySQL as the database server
UFW for firewall management
Certbot for SSL certificate management (Let’s Encrypt)
Prerequisites
A minimum of three servers (Load Balancer, Web Server 1, Web Server 2, and Database Server).
SSH access to all servers.
Basic knowledge of Linux commands and server administration.
