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
## client:
import socket
s = socket.socket()
s.connect(('localhost', 8080))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    server_reply = s.recv(1024).decode()
    if not server_reply:
        break
    print("Server >", server_reply)
s.close()

## server:

import socket
s = socket.socket()
s.bind(('localhost', 8080))
s.listen(5)
print("Waiting for connection...")
c, addr = s.accept()
print("Connected to:", addr)
while True:
    client_message = c.recv(1024).decode()
    if not client_message:
        break
    print("Client >", client_message)
    msg = input("Server > ")
    c.send(msg.encode())
c.close()
s.close()
## OUTPUT
<img width="1918" height="1021" alt="Screenshot 2026-05-21 141030" src="https://github.com/user-attachments/assets/1dce0ee5-42a8-46dd-b1e0-a2ca0f1dcc70" />
<img width="1918" height="1017" alt="Screenshot 2026-05-21 141040" src="https://github.com/user-attachments/assets/d8c1bcc6-eceb-4cd7-896e-440bb125755e" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
.


















.














.




















.
