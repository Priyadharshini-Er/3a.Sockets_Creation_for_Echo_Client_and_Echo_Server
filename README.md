# Ex No:3a Creation For Echo Client And Echo Server Using TCP Sockets
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
### Server Side
```python
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
### Client Side
```python
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUTPUT
![324262488-f4e589ec-f630-44a7-8392-cfeb331f28e3](https://github.com/Priyadharshini-Er/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/119558093/0895a4bf-c117-4d2f-b284-5e6645911215)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
