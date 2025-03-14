What Is Load Balancing? / 什么是负载均衡？

Load balancing is a technique for distributing workloads across multiple machines or clusters. The purpose of load balancing is to:

负载均衡是一种用于在多台服务器或集群之间分配工作负载的技术。负载均衡的目的包括：

Optimize resource usage (avoid overload and under-load of any machines) / 优化资源利用率（避免服务器过载或空闲）

Achieve Maximum Throughput / 提高最大吞吐量

Minimize response time / 减少响应时间

Load Balancing Techniques for Stateless Services / 针对无状态服务的负载均衡技术

For stateless services, the load balancing process is simpler since requests do not depend on previous interactions. Common algorithms include:

对于无状态服务，负载均衡流程相对简单，因为请求之间没有依赖关系。常见的负载均衡算法包括：

Round Robin (RR, 轮询算法)

Requests are distributed sequentially across all available nodes in a circular order.

简单高效，适用于负载均衡均匀的情况。

Weighted Round Robin (WRR, 加权轮询算法)

Assigns different weights to each node based on their capacity.

节点权重越高，分配到的请求越多，适用于不同性能的服务器。

Smooth Weighted Round Robin (SWRR, 平滑加权轮询算法)

Ensures a smoother distribution of requests over time.

避免请求突发式分配，确保请求均匀平滑地分布在各个服务器上。

Load Balancing in Web-Based Applications / Web 应用中的负载均衡

Session Affinity (Sticky Session) / 会话亲和性: Ensures requests from the same user are directed to the same backend node.
确保同一用户的请求始终发送到同一台后端服务器。

IP Address Affinity / IP 地址亲和性: Uses IP hashing to consistently assign clients to specific backend nodes.
通过 IP 哈希算法保证相同 IP 地址的请求分配到同一台服务器。
