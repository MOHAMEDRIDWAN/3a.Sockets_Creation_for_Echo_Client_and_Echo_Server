# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# NAME : MOHAMED RIDWAN A
# REG NO : 212223110030
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

### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',3000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```

### Server:
```
import socket
s=socket.socket()
s.bind(('localhost',3000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())

```
## OUTPUT

![Screenshot 2024-04-29 133039](https://github.com/Anas536/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139841834/8eeecdfc-0d8e-4041-88a3-9b9a23548bb9)

![Screenshot 2024-04-29 133050](https://github.com/Anas536/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139841834/086e315b-8ff4-420e-a870-d0a3c8ec8ab2)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
