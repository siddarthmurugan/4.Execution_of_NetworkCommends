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
import socket
import subprocess

# Create socket
s = socket.socket()

# Bind host and port
s.bind(("localhost", 5000))

# Listen for client
s.listen(1)

print("Server waiting for connection...")

# Accept connection
c, addr = s.accept()

print("Connected with:", addr)

# Receive website/IP from client
host = c.recv(1024).decode()

# Execute ping command
result = subprocess.getoutput("ping " + host)

# Send result to client
c.send(result.encode())

# Close connections
c.close()
s.close()
##program
server.py
```
import socket
import subprocess

# Create socket
s = socket.socket()

# Bind host and port
s.bind(("localhost", 5000))

# Listen for client
s.listen(1)

print("Server waiting for connection...")

# Accept connection
c, addr = s.accept()

print("Connected with:", addr)

# Receive website/IP from client
host = c.recv(1024).decode()

# Execute ping command
result = subprocess.getoutput("ping " + host)

# Send result to client
c.send(result.encode())

# Close connections
c.close()
s.close()
```
client.pt
```
import socket

# Create socket
c = socket.socket()

# Connect to server
c.connect(("localhost", 5000))

# Get website/IP from user
host = input("Enter website/IP: ")

# Send to server
c.send(host.encode())

# Receive and print result
print(c.recv(4096).decode())

# Close connection
c.close()
```
route.py
```
import subprocess

target = input("Enter website or IP: ")

subprocess.run(["tracert", target])
```
## Output
server.py




<img width="467" height="261" alt="image" src="https://github.com/user-attachments/assets/54214d45-169b-4b07-8f04-a37d6e19c576" />




client.py




<img width="484" height="355" alt="image" src="https://github.com/user-attachments/assets/d74660ab-106d-463c-81db-4515851f7332" />



route.html




<img width="734" height="492" alt="image" src="https://github.com/user-attachments/assets/c5851692-f208-436e-8b82-f95acf2bab4a" />

## Result
Thus Execution of Network commands Performed 
