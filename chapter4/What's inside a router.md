# What's inside a router


## Router architecture overview
- high-level view of generic router architecture
![image](https://user-images.githubusercontent.com/83717535/141427566-b8547828-8bfa-4409-aa9a-cd32419eeb46.png)


## Input port functions
![image](https://user-images.githubusercontent.com/83717535/141427743-045535f5-1f80-4142-83d3-f05f45a25cdb.png)
![image](https://user-images.githubusercontent.com/83717535/141428279-e205b6d8-f18b-4d77-ba7b-2f6aa2f20855.png)


## Destination-based forwarding
![image](https://user-images.githubusercontent.com/83717535/141428522-49486cbd-0cec-4657-99da-2878ed99da8c.png)


## Longest prefix matching
![image](https://user-images.githubusercontent.com/83717535/141428653-e978435c-cb54-48f8-a08c-267a8b1015b4.png)
- longest prefix matching: often performed using ternary content addressable memories (TCAMs)
  - content addressable: present address to TCAM: retrieve address iin one clock cycle, regardless of table size
  - Cisco Catalyst: can up ~ 1M rounting table entries in TCAM


## Switching fabrics
- transfer packet from input buffer to appropriate output buffer
- swithcing rate: rate at which packets can be transfer from inputs to outputs
   - often measured as multiple of input/output line rate
   - N input: switching rate N times line rate desirable
- three types of switching fabrics
![image](https://user-images.githubusercontent.com/83717535/141430045-3c1f8cf6-a969-4b4b-a2a7-5775bafee86f.png)



## Switching via memory
![image](https://user-images.githubusercontent.com/83717535/141430438-ef97b125-1aaf-4c3b-8cbb-810851d46885.png)
- first generation routers:
  - traditional computers with switching under direct control of CPU
  - packet cpied to system's memory
  - speed limited by memory bandwidth (2 bus crossing per datagram)




## Switcing via a bus
![image](https://user-images.githubusercontent.com/83717535/141430983-04eedb04-d700-4ee5-971a-3f15b55573e6.png)
- datagram from input port memory to output port memory via a shared bus
- _bus contention:_ switching speed limited by bus bandwidth
- 32 Gbps bus, Cisco 5600: sufficient speed for access and enterprise routers


## Switching via interconnection network
![image](https://user-images.githubusercontent.com/83717535/141431687-090316d7-76ef-47de-9eff-2b041e23ef63.png)
- overcome bus bandwidth limitations
- banyan networks, crossbar, other interconnection nets initially developed to connect processors in multiprocessor
- advanced desgin: fragmenting datagram into fiixed length cells, switch cell through the fabri
- Cisco 12000: switches 60 Gbps through the interconnection network


## Input port queuing
![image](https://user-images.githubusercontent.com/83717535/141432260-988512dd-e1d0-4964-8363-749a16b9b8d4.png)
- fabric slower than input ports combined → queueing may occur at input queues
  - queueing delay and loss due to input buffer overflow
- Head-of-the-Line (HOL) blocking: queued datagram at front of queue prevents others in queue from moving forward


## Output port _(Hugely important!)_
![image](https://user-images.githubusercontent.com/83717535/141434564-31076f3e-8124-4a35-8d20-368a234a5540.png)
- **buffering** required when datagrams arrive from fabric faster than the transmission rate
  - Datagram (packets) can be lost due to congestion, lack of buffers
- **scheduling discipline** chooses among queued datagrams for transmission
  - Priority schduling - who gets best performance, network neutrality


## Output port queueing
![image](https://user-images.githubusercontent.com/83717535/141435188-b3973a1f-717e-41b7-a0dc-d09b21f20c27.png)
- buffering when arrival rate via switch exceeds output line speed
- **queueing (delay) and loss due to output port buffer overflow!**







