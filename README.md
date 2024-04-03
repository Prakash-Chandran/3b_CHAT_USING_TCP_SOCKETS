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
````
CLIENT:
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

````
````
SERVER:
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
````
## OUPUT
CLIENT:

![Screenshot 2024-04-03 105457](https://github.com/Prakash-Chandran/3b_CHAT_USING_TCP_SOCKETS/assets/147120899/3462adb1-8d9f-4d4b-b5c3-503e34a707d8)


SERVER:

![Screenshot 2024-04-03 105502](https://github.com/Prakash-Chandran/3b_CHAT_USING_TCP_SOCKETS/assets/147120899/d36332ca-9e13-4165-8719-9c772b42a6a5)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
