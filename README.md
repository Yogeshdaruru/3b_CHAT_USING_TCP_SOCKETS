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
client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8500))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8500))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUPUT
client.py

<img width="677" height="178" alt="image" src="https://github.com/user-attachments/assets/77f28060-5c07-4f80-b4e3-0098802133c4" />

server.py

<img width="691" height="144" alt="image" src="https://github.com/user-attachments/assets/d7c5cfe9-b675-4f09-9575-f4ce5c87ccee" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
