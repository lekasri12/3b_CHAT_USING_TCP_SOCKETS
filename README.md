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
## CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

## SERVER
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
## CLIENT
![325087986-e274dfa2-62a2-4109-816c-84560374145c](https://github.com/lekasri12/3b_CHAT_USING_TCP_SOCKETS/assets/149037427/68aa3733-26ef-48c4-b363-062bc358ae5d)

## SERVER
![325088033-41fb8813-9c24-469b-a3d2-2f8a2f15e8dd](https://github.com/lekasri12/3b_CHAT_USING_TCP_SOCKETS/assets/149037427/ed12499d-a1c7-49d4-9851-4c87af56c1bb)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
