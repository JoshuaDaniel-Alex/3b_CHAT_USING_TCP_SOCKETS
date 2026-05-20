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
Client:
```
# Developed by:Joshua Daniel A
# Register Number:212225040161
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
Server:
```
# Developed by:Joshua Daniel A
# Register Number:212225040161
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
Client:
<img width="1274" height="352" alt="Screenshot 2026-05-20 085636" src="https://github.com/user-attachments/assets/8e8938a8-caae-4531-97ec-a68f8abf9665" />

Server:
<img width="1206" height="333" alt="Screenshot 2026-05-20 085653" src="https://github.com/user-attachments/assets/439f70d3-a7bb-40a3-95ff-6f68f6c62f1a" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
