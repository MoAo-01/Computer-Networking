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
- longest prefix matching: often performed using ternary content addressable memories (TCAMs)
  - content addressable: present address to TCAM: retrieve address iin one clock cycle, regardless of table size
  - Cisco Catalyst: can up ~ 1M rounting table entries in TCAM
![image](https://user-images.githubusercontent.com/83717535/141428653-e978435c-cb54-48f8-a08c-267a8b1015b4.png)
