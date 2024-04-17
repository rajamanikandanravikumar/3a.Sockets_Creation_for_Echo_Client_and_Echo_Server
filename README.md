# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### NAME:RAJAMANIKANDAN R
### REG NO:212223220082
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
# PROGRAM
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
    c.send(ClientMessage.encode())
```
## OUTPUT
# CLIENT:
![321079218-0613a19d-ab5f-495a-9a14-79d021e4d318](https://github.com/rajamanikandanravikumar/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742839/6ac49f4d-c4ff-4365-ac82-f161866b8866)

# SERVER:
![321079257-094d8ba2-3c67-4feb-aa54-a6a666bfb42b](https://github.com/rajamanikandanravikumar/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742839/d18a70ae-2808-46ee-9df2-79c398795d6c)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
