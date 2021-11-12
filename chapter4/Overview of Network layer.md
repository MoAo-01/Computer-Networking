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
  - 转发是指将分组从一个输入链路接口转移到适当的输出链路接口的路由器本地动作。
- rounting:
  - determine route taken by packets from source to destination
  - **rounting algorithms** 
  - 路由选择是指确定分组从源到目的地所采用的端到端路径的网络范围处理过程。
 
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
  - ### Pre-router Control Plane
    - Individual routing algorithm components _in each and every router_ interact in the control plane 

![image](https://user-images.githubusercontent.com/83717535/141412512-76634d1e-8569-4cb2-a63d-2854a7a4c9a7.png)
  - ### Logically Centralized Control Plane
    - A distinct (typically remote) controller interacts with local control agents (CAs)


## Network Service Model
- guaranteed delivery
- guaranteed delivery with less than 100 msec delay (for example)
- in-order datagram delivery
- guaranteed minimum bandwidth to flow
- security




