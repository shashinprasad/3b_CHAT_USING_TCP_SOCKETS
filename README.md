# 3b.CREATION FOR CHAT USING TCP SOCKETS
# Date: 
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM 
## CLIENT: 
```
Developed by: RIYA P L
Reg no: 212223240141
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
## OUPUT
![Screenshot 2024-09-11 155120](https://github.com/user-attachments/assets/b792ffb6-a857-4e67-958e-3e7f324a7ef1)
![Screenshot 2024-09-11 155128](https://github.com/user-attachments/assets/a707076d-8dcd-4105-9f46-78c3ae6999ae)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
