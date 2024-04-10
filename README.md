# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name:Ashwin Kumar A
## REG NO:212223040021
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### client:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server:
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
``` 
## OUPUT
### client:
![image](https://github.com/AshwinKumar-Saveetha/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/155129814/0613a19d-ab5f-495a-9a14-79d021e4d318)

### server:
![image](https://github.com/AshwinKumar-Saveetha/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/155129814/094d8ba2-3c67-4feb-aa54-a6a666bfb42b)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
