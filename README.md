# Inter Process Communication using sockets
Inter process communication (IPC) is a mechanism which allows processes to communicate with each other and synchronize their actions. The communication between these processes can be seen as a method of co-operation between them. Processes can communicate with each other through both:
### 1) Shared Memory 
Communication between processes using shared memory requires processes to share some variable and it completely depends on how programmer will implement it. {Ex: Producer-Consumer problem -> i) unbounded buffer problem, ii) bounded buffer problem}
### 2) Message passing 
In this method, processes communicate with each other without using any kind of shared memory. In message passing you have a sender and a receiver–they usually run in separate threads.

## IPC methods 
1. Pipes (Same Process) – This allows flow of data in one direction only.
2. Names Pipes (Different Processes) – It can be used in processes that don’t have a shared common process origin.
3. Message Queuing – This is managed by system kernel these messages are coordinated using an API. (queue)
4. Semaphores – This is used in solving problems associated with synchronization and to avoid race condition. (value are int >= 0)
5. Shared memory – This allows the interchange of data through a defined area of memory.
6. Sockets – This method is mostly used to communicate over a network between a client and a server. It allows for a standard connection which is computer and OS independent.

## Socket Programming in Python 
A socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to. An endpoint is a combination of an IP address and a port number.

## Executing the files in python IDLE
### 1. local_server.py and local_client.py
As soon as you run local_server.py and then local_client.py, you can talk between the terminals. You can stop the process by writing bye and hit enter.

### 2. chat_server.py and chat_client.py
a) Localhost - Open both the files in IDLE and run first chat_server.py and then chat_client.py. Now, it will ask for Host value as 127.0.0.1 and PORT as 33000 (as defined in code).
Tkinter GUI will apperar where you can first enter your name and then type the message. Since it is locally, therfore there is no one else to communicate. You can quit by typing "quit" (without double quotes) and hit the send button.

b) With muliple machines - Firstly make all machines connected via a single network (hotspot). Now run chat_server.py in one machine and all chat_client.py in other machines. Enter the ip address of the network (hotspot) as Host value and PORT value as 33000. Now, Tkinter GUI will appear and people with their machines can communicate.

### 3. psutil_server.py and psutil_client.py
It runs same as above code, here the server machine can see all the cpu related statistics of other connected machines.

## References
1. https://www.geeksforgeeks.org/inter-process-communication-ipc/
2. https://www.geeksforgeeks.org/methods-in-interprocess-communication/
3. https://medium.com/swlh/lets-write-a-chat-app-in-python-f6783a9ac170
