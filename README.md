# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## program
client

```
import socket
s = socket.socket()
host = socket.gethostname()
port = 60000
s.connect((host, port))
s.send("Hello server!".encode())
with open('mytext.txt', 'wb') as f:
 while True:
    print('receiving data...')
    data = s.recv(1024)
    print('data=%s', (data))
    if not data:
        break
    f.write(data)
f.close()
print('Successfully get the file')
s.close()
print('connection closed')
```
server

```
import socket
port = 60000
s = socket.socket()
host = socket.gethostname()
s.bind((host, port))
s.listen(5)
while True:
    conn, addr = s.accept()
    data = conn.recv(1024)
    print('Server received', repr(data))
    filename='mytext.txt'
    f = open(filename,'rb')
    l = f.read(1024)
    while (l):
        conn.send(l)
        print('Sent ',repr(l))
        l = f.read(1024)
    f.close()
    print('Done sending')
    conn.send('Thank you for connecting'.encode())
    conn.close()
```
## Output

client

<img width="717" height="311" alt="image" src="https://github.com/user-attachments/assets/b1e77cc8-bbd1-4c80-8133-2d1262f3ac7e" />

server

<img width="697" height="191" alt="image" src="https://github.com/user-attachments/assets/4e14265b-a4ed-44fe-a187-d20c4e290810" />

netstat

<img width="1142" height="771" alt="image" src="https://github.com/user-attachments/assets/7ca0f6e9-ef4d-4d7b-aa88-201c3ddb90d1" />

ipconfig

<img width="1073" height="927" alt="image" src="https://github.com/user-attachments/assets/cacc9548-0ade-4564-b7fe-e7db68118dc8" />

ping

<img width="957" height="291" alt="image" src="https://github.com/user-attachments/assets/a26f9d29-4585-4593-9e43-9cdd3aeaf503" />

tracert

<img width="1148" height="465" alt="image" src="https://github.com/user-attachments/assets/ab36cb96-e47e-4ce3-a375-9d84c2958e11" />

nslookup

<img width="872" height="567" alt="image" src="https://github.com/user-attachments/assets/637d0cf4-b0c7-4c46-850f-67f87d7f79ba" />

getmac

<img width="993" height="207" alt="image" src="https://github.com/user-attachments/assets/dfa881fd-07f0-449c-8acd-cf0ef8995252" />

hoatname

<img width="1012" height="1042" alt="image" src="https://github.com/user-attachments/assets/bed36386-c8bd-41fb-85d9-fcbdf78b04af" />

nbtstat

<img width="1196" height="601" alt="image" src="https://github.com/user-attachments/assets/96a1493c-a5b1-4fe5-98c3-da57486b588a" />

arp

<img width="922" height="577" alt="image" src="https://github.com/user-attachments/assets/ebc5971b-1afb-4668-88ef-a9a8e7564661" />


systeminfo

<img width="1192" height="1007" alt="image" src="https://github.com/user-attachments/assets/5d7c089e-e465-4c2c-b51d-ebe798a42da7" />



## Result
Thus Execution of Network commands Performed 
