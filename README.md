# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Developed By:Mirtyunjay .S
## Register Number:212224040190
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
### Client
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
msg=input("Client > ") 
s.send(msg.encode()) 
print("Server > ",s.recv(1024).decode())
```
### Server
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
### Client
<img width="1055" height="365" alt="Screenshot 2025-10-22 091544" src="https://github.com/user-attachments/assets/dbbb1163-48f4-42ea-be1d-9b8b25fb5d26" />

### Server

<img width="872" height="325" alt="Screenshot 2025-10-22 091551" src="https://github.com/user-attachments/assets/3fa2c229-32c3-472c-a962-ae35129cb4f9" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
