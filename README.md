# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS:
## REG NO:212223230121
## NAME:MANIKUMAR.DK
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.

## PROGRAM:
## CLIENT:
```
import socket
s = socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr = s.accept()
while True:
    clientMessage=c.recv(1024).decode()
    c.send((clientMessage.encode()))
```
## SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT:
## CLIENT:
![image](https://github.com/MANIKUMARDK/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147215581/92ba1f26-b86c-4296-b50a-af8f022c10e8)
## SERVER:
![image](https://github.com/MANIKUMARDK/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147215581/523bff8d-e494-461a-9bf1-4e4b60a40a30)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
