18 Setembro 2023 - #ASCN

## Why distributed systems?
- Modularity, decoupling different concerns.
- Performance.
- Dependability


## How to distribute?
### 1. Monolythic system
- Architecture: [[Monolithic system.excalidraw]]
- Multiple services for multiple targets in the same server
## 2. Distributed system
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
- 