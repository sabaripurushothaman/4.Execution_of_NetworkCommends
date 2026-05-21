## 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
```
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer
All commands related to Network configuration which includes how to switch to privilege mode
and normal mode and how to
configure router interface and how to save this configuration to
flash memory or permanent memory.
This commands includes
• Configuring the Router commands
• General Commands to configure network
• Privileged Mode commands of a router
• Router Processes & Statistics
• IP Commands
• Other IP Commands e.g. show ip route etc.
```

## PROGRAM:
## CLIENT:
```
client.py
import socket
from pythonping import ping
s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True: hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```
## SERVER:
```
server.py

import socket s=socket.socket() s.connect(('localhost',8000)) while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```
## OUTPUT:
## NESTAT:
<img width="802" height="374" alt="Screenshot 2026-05-21 131008" src="https://github.com/user-attachments/assets/5f5ec6a2-9307-4f1b-971f-96a32fe4e294" />
## IP CONFIGURATION:
<img width="923" height="695" alt="image" src="https://github.com/user-attachments/assets/b7b28d99-39b4-4f04-a90f-8498f6f95df7" />
## GETMAC:
<img width="807" height="166" alt="Screenshot 2026-05-21 131111" src="https://github.com/user-attachments/assets/dcfc56b0-7870-4f54-84e3-e4db82f22af6" />
## ARP:
<img width="803" height="394" alt="Screenshot 2026-05-21 131138" src="https://github.com/user-attachments/assets/35b8d0d5-2dbf-4e9f-afa7-ec67d584af24" />
## SYSTEM INFO:
<img width="1180" height="907" alt="image" src="https://github.com/user-attachments/assets/4a38c81b-5958-4045-8ee1-a969bb2253d5" />
## NBTSTAT:
<img width="1046" height="520" alt="image" src="https://github.com/user-attachments/assets/a441617c-3f97-4079-be7c-1c10f16b282a" />
## HOST NAME:
<img width="1038" height="358" alt="image" src="https://github.com/user-attachments/assets/17c469a3-5143-4b83-9b1e-8fdb987ac1f8" />
## NS LOOKUP:
<img width="693" height="149" alt="image" src="https://github.com/user-attachments/assets/596655fc-825c-4c2b-bfc7-c7eb59acbe7b" />
## PING:
<img width="807" height="581" alt="image" src="https://github.com/user-attachments/assets/5c03be71-7733-48ae-9bab-8b776e0db2b1" />
## TRACET:
<img width="814" height="109" alt="image" src="https://github.com/user-attachments/assets/47b163b6-99d9-4e4c-b2fd-bc8a45439796" />

## RESULT:
Thus Execution of Network commands Performed












