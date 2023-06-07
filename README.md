# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL
# DATE:16-03-2023
# AIM :
To write a python program to perform stop and wait protocol

# ALGORITHM :
Start the program. Get the frame size from the user To create the frame based on the user request. To send frames to server from the client side. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client. Stop the program

# SERVER PROGRAM :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
CLIENT PROGRAM:
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
 ```
# SERVER OUTPUT :
![image](https://github.com/gracia55/EX-2/assets/129026838/b0aeae81-b09f-46eb-8337-c0e2f7627997)


# CLIENT OUTPUT:
![image](https://github.com/gracia55/EX-2/assets/129026838/8305c399-d1c1-4dc2-a82b-0fa9f765ac11)



# RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



