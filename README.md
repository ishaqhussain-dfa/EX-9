# APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
# EXP: 9
# DATE:03-05-2023
# AIM:
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM:
# Client:
Import the necessary modules in python
Create a socket connection to using the socket module.
Send message to the client and receive the message from the client using the Socket module in server
Send and receive the message using the send function in socket.
# PROGRAM:

## Developed : ISHAQ HUSSAIN A
## Reg no : 212221040059

# CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
# SERVER:
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
# CLIENT OUTPUT :
![image](https://github.com/DhanushPalani/EX-NO-9/assets/121594640/7a1ae7c2-85c3-48f3-99ef-8e0cd8891521)

# SERVER OUTPUT :
![image](https://github.com/DhanushPalani/EX-NO-9/assets/121594640/18d54810-4593-4b1a-ade7-889aae7943cb)

# RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
