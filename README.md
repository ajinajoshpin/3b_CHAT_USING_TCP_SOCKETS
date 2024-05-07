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
DEVELOPED BY:AJINA JOSHPIN.A
REGISTER NUMBER:212223230008
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
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
## OUPUT:
## CLIENT:
![image](https://github.com/ajinajoshpin/3b_CHAT_USING_TCP_SOCKETS/assets/148514578/f211a320-30cf-4629-8424-ea3f4bb419c7)

## SERVER:
![image](https://github.com/ajinajoshpin/3b_CHAT_USING_TCP_SOCKETS/assets/148514578/be704c62-e63e-4a34-a146-dcc83c44d789)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
