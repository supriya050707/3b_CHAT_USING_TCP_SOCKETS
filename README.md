# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

client 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

server

```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUPUT

client 

<img width="514" height="284" alt="Screenshot 2025-10-22 101334" src="https://github.com/user-attachments/assets/97633e8d-d08e-4438-b751-cbe12a8f5070" />

server

<img width="595" height="337" alt="Screenshot 2025-10-22 101328" src="https://github.com/user-attachments/assets/922040fa-15a7-40a0-bd30-b76de17d8a36" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
