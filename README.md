## NAME:jenil pio
## REG NO:212223220040

# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
## client.py
~~~
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'JENIL, 6-3-25, 212223230168')
    print(f'Received: {s.recv(1024)!r}')
~~~
## server.py
~~~
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
~~~


## OUTPUT:
#CLIENT
![image](https://github.com/user-attachments/assets/954f449e-0068-44a7-817f-b7d239a5331e)

#SERVER
![image](https://github.com/user-attachments/assets/1ad333f8-ae37-4d6e-9ac1-bd956e008727)




## RESULT:
The program is executed successfully.
