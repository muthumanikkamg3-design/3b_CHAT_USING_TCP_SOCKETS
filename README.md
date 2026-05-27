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

Developed by :MUTHU MANIKKAM.G

Reg no :21222251000229

Client Code:

client.py

~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~

Server Code:

server.py

~~~
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
~~~


## OUPUT:
<img width="1426" height="417" alt="image" src="https://github.com/user-attachments/assets/f46b542a-8b2e-48f5-b2d3-bc475656172e" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
