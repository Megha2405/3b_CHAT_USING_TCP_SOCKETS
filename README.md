# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
server:
```
import socket


    client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    client_socket.connect(("localhost", 12345))  # Connect to the server
    print("Connected to the server. Type 'exit' to quit.")

    while True:
        message = input("Client: ")
        client_socket.send(message.encode())

        if message.lower() == "exit":
            break

        response = client_socket.recv(1024).decode()
        print(f"Server: {response}")

    client_socket.close()
```
client
```
import socket


    client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    client_socket.connect(("localhost", 12345))  # Connect to the server
    print("Connected to the server. Type 'exit' to quit.")

    while True:
        message = input("Client: ")
        client_socket.send(message.encode())

        if message.lower() == "exit":
            break

        response = client_socket.recv(1024).decode()
        print(f"Server: {response}")

    client_socket.close()


```


## OUPUT
![output](<Screenshot 2025-09-21 222051.png>)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
