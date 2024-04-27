ntroducing our group project, "distributed-system-replication-RabbitMQ". This project utilizes RabbitMQ to facilitate communication between clients and servers within a distributed system.

Here's how it works:

A client writes messages to a text file, with each line representing a distinct message.
These messages are then sent to the servers (replicas) that are currently active.
Each server records the messages it receives from the client in its own text file.
A client reader can request to read these messages using either the "Read Last" or "Read All" commands.
The "Read Last" command returns the last message read by any replica, ensuring consistency even if some servers were offline when the message was initially sent.
The "Read All" command instructs the replicas to send their entire file contents to the client reader. The client then compares the results and displays the majority of the lines in the order they were written by the client writer.
This project provides a robust solution for distributed message replication, ensuring reliable communication and data consistency across multiple servers.
