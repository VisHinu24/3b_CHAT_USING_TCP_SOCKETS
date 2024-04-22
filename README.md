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
Client : 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
Server :
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
Client : 
![Screenshot 2024-04-22 201709](https://github.com/VisHinu24/3b_CHAT_USING_TCP_SOCKETS/assets/144244396/371e485e-2437-4fab-ab38-4b04809157d7)

Server :
![Screenshot 2024-04-22 201705](https://github.com/VisHinu24/3b_CHAT_USING_TCP_SOCKETS/assets/144244396/28bb4db0-8898-4d03-b271-6e8e5533e064)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
