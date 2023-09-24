18 Setembro 2023 - #ASCN

## Why distributed systems?
- Modularity, decoupling different concerns.
- Performance.
- Dependability


## How to distribute?
### 1. Monolythic system
- Architecture: [[Monolithic system.excalidraw]]
- Multiple services for multiple targets in the same server
## 2. Distributed systems
- Main distribution concerns:
	1. Replication
	2. Partitioning
	3. Service-orientation
- All of these address scaling out a service/application.
- Not mutually exclusive, can be combined.

### 2.1 Replication
- Architecture: [[Replication.excalidraw]]
- Multiple copies  of the same data and functionality
- Addresses resilience and scale-out
### 2.2 Partitioning
- Architecture: [[Partitioning.excalidraw]]
- A server is split horizontally (Sharding).
- Addresses scale-out.
- Can be applied to computation, data, ...
### 2.3 SOA - Service-Oriented Architecture
- Architecture: [[SOA.excalidraw]]
- Addresses scale-out and modularity.
- Example: micro-services.
#### 2.3.1 Microservices
- Each service implements specific functionality.
- Services can scale independently.
- Decomposition may be troublesome: how micro is micro?
- Consistency.
- Complex deployment and testing 



## Distributed architectures
### 1. Client-server
- Architecture: [[client-server.excalidraw]]
- Functionality and data are in the server.
- A stub runs embedded in the client.
- The stub is part of the server software package
	- E.g., the Web (“protocol” is HTTP)

### 2. Proxy Server
- Architecture: [[proxy.excalidraw]]
- Multiple servers can be used transparently.
- The proxy is a performance and availability bottleneck.
	- E.g. MongoDB

### 3. Master Server
- Architecture: [[master.excalidraw]]
- Scale out!
	- E.g. HDFS

### 4. Server Group
- Architecture: [[server-group.excalidraw]]
- All servers can process requests.
- Coordination may be necessary.
- Resiliency!
	- E.g. ZooKeeper

### 5. Bus
- Architecture: [[bus.excalidraw]]
- The bus routes messages.
- Participants publish and consume messages to/from the bus.
- Decouples producers from consumers.
- **Flexibility!**
	- E.g. Kafka

### 6. Multi-tier
- Architecture: [[multi-tier.excalidraw]]
- Each server acts as a client of the next tier.
- Allows independent deployment and scaling of different functionality.
- E.g. AS + DBMS:
	- “protocol A” == Web (e.g.)
	- “Stub B” == Database Driver!
	- “protocol B” uses SQL
#### 6.1 State in multi-tier
- 
