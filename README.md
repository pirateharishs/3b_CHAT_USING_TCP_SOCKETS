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

### DEVELOPED BY:HARISH S
### REG NO:212223230071

## client
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## server
```
import socket 
s=socket.socket() 
s.connect(('localhost',9000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT

## client

![Screenshot 2024-04-20 130208](https://github.com/Danica-christa/3b_CHAT_USING_TCP_SOCKETS/assets/151514009/55862165-6434-43ff-a530-3ca9130bd7f5)
## server

![Screenshot 2024-04-20 130221](https://github.com/Danica-christa/3b_CHAT_USING_TCP_SOCKETS/assets/151514009/691a3539-6566-4991-8016-b7d579f3ddaf)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
