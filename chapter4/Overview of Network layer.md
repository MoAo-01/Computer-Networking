# Overview of Network layer

![image](https://user-images.githubusercontent.com/83717535/140716799-684f2d2d-1800-44f5-973f-47517f87e658.png)

## Network Layer
- transport segment from sending to receiving host
- on sending side encapsulates segments into datagrams
- on receiving side, delivers segments into datagrams
- network layer protocols in **every** host, rounter
- rounter examines header fields in all IP datagrams passing through it

## Two key network-layer functions
- forwarding:
  - move packets from router’s input to appropriate router output
- rounting:
  - determine route taken by packets from source to destination
  - **rounting algorithms** 
 
 ![image](https://user-images.githubusercontent.com/83717535/140719244-61c574f5-5dde-416c-bff3-48890e81904f.png)

 
## Data Plane and Control Plane
- Data Plane
  - local, pre-rounter function
  - determines how datagram arriving on rounter input port is forwarded to rounter output port
  - forwarding function
- Control Plane
  - networking-wide logic
  - determines how datagram is rounted among rounters along end-end path from source host to destination host
  - two control-plane approaches:
    - traditional rounting algorithms: implemented in rounters
    - software-defineded networking (SDN): implemented in (remote) servers


![image](https://user-images.githubusercontent.com/83717535/140885493-bd26ea16-2693-48ac-bdf0-e78cd09c3c28.png)


## Pre-router Control Plane

Individual routing algorithm components _in each and every router_ interact in the control plane 


![Uploading image.png…]()


## Logically Centralized Control Plane

A distinct (typically remote) controller interacts with local control agents (CAs)





