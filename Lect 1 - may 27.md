# 1) NETWORK:
A computer network is a group of 2/more devices connected together for sharing resouses.

### TYPES:
| PAN |  Very small personal range|
|-|-|
| LAN | small area |
| MAN | City-level |
| WAN | Large/gloabl |

### BASIC COMPONENETS:
1. Node -> Any device in a network
2. IP Address -> Logical address of a device in a network
3. Protocol -> Rules of communication
4. Switch -> Connects different devices within the network(LAN)
5. Router -> Connects differnt Networks

### HUB vs SWITCH
|HUB(DUFFER DEVICE)|SWITCH|
|-|-|
|Works in the Physical Layer.|Works in the Data Link Layer.|
|Broadcast the message ti all the device within the network.|Forward the message to only the Destination Device by checking the MAC address.|
|Hight bandwwidth utilization ,looping and conession due to broadcasting.|Less congesion, bandwidth usage and fewer collision.|
|No Use of MAC address.|Uses MAC address table (CAM Table).|

### SWITCH - CAM TABLE:
CAM table stores 2 value, MAC adress of the device and the port of the switch where those particular devices are connected.Using theois table the switch can send messages efficiently to the destination device. The switch can automatically learn by observing incoming frames andstores the MAC address in the table. This process is called as MAC LEARNING.
|MAC Address|	Port|
|-|-|
|MAC of PC1|	1|
|MAC of PC2|	2|
|MAC of PC3|	3|

### MAC ADDRESS:
It is the Physical address of a device. For a device there can be only one MAC address and it cannot be changes.

### ROUTER:
- Works in the Network Layer.
- Works with different network.
- Uses IP adress for communication.
- Find the best path for routing data packets from source to destination.

<br><br>
# 2) OSI MODEL
- OSI model was intoduced to deal with the problem of communication between 2 different networks(companies) beacuase they had different venders.
- OSI model helps to communicatebtw different venders.
- Layer Architectur(7 Layers)

|Application Layer|User services|
|-----------|---|
|Presentation Layer|Translation/Encryption|
|Session Layer|Connection Management|
|Transport Layer| Reliable Delivery|
|Network Layer|Routing|
|Data Link Lyaer|MAC+Frames|
|Physical Layer|Bits/signals|

<br><br>
# 3) TRANSPORT LAYER
- Responible for end to end delivery of data.
- PDU - segment(TCP) / Datagram(UDP)
- Ensures reliable delivery by
- Performs
  - Error Checking
  - 3 way handshake (communication establishing)
  - Windoeing (Flow control)
  - Data Sequening
  - Data retransfer in case of data lose

### TCP VS UDC
|TCP|UDC|
|-|-|
|Connection oriented| connectionless|
|PDU- segment| PDU- Datagram|
|Reliable communication|Unreliable|
|3 Way handshake| No handshake|
|Data flow control| No data flow control|
|Data arrive in sequence| Data may not arrive in sequence|
|Error checking and Retransmission on datalose| No retransmission|
|Slower|Faster|
|Higher overhead| Lower Overhead|
  
### 3 WAY HANDSHAKE:
It is used to establish a realable communication between the sender and the reciever befor the actual data transfer.

S -----SYN-----> R <br>
S <---SYN-ACK--- R <br>
S -----ACK-----> R

<br><br>
# ABBRIVIATION
|PAN| Personal Arean Network|
|-|-|
|LAN| Local AreaNetwork|
|MAN|Metropolitan Network|
|WAN|Wide Area Network|
|IP|Internat Protocol|
|MAC|Media Aseses Protocol|
|OSI|Open System Interconnectiom|
|PDU| Protocol Data Unit|
|TCP|Transfer Communication Protocol|
|UDC|User Datagram Protocol|
|SYN|Syncronize|
|ACK|Acknolegement|
