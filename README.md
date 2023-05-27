## EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER
```
DATE : 27-04-2023
```
### AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.
### ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the 
  Socket module in server.
4.Send and receive the message using the send function in socket.
```
### PROGRAM :
```
Developed by: G Venkata Pavan Kumar
Register No: 212221240013
```
#### Client_Side:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
#### Server_Side:
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
### OUTPUT :
#### Client_Side:
![image](https://github.com/Pavan-Gv/EX-8/assets/94827772/10472420-5845-4185-8f77-c9d7f20826ef)
#### Server_Side:
![image](https://github.com/Pavan-Gv/EX-8/assets/94827772/3b7ee27d-c191-43c4-8fd8-30f135c88c06)
### RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
