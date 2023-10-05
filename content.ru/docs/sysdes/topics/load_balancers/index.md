---
---

# Load Balancers

## Plan

### Use cases of LB (HA, monitoring, roling updates)

### L4, L7 Proxies

### Virtual IP

### Fixed IP, Floating IP

### Octavia failover HAProxy scheme

### The Power of Two Choices.

### BGP Anycast


Load Balancers

Load balancers are a crucial component in any distributed system. They help distribute network or application traffic across many servers, enhancing both the performance and reliability of applications.
Use cases of Load Balancers
High Availability (HA)

Load balancers play a critical role in maintaining high availability. By distributing traffic across multiple servers, they ensure that if one server goes down, the load can be quickly shifted to another, preventing service disruption.
Monitoring

Load balancers can also provide valuable monitoring capabilities. They can track the performance of the servers they distribute traffic to, allowing for early detection of issues and preventing potential outages.
Rolling Updates

In a rolling update, a new version of an application is gradually deployed across all servers. Load balancers can help manage this process by gradually shifting traffic from servers running the old version to those running the new one.
L4, L7 Proxies

Load balancers can operate at different layers of the network protocol stack. Layer 4 (L4) load balancers operate at the transport layer, where they balance traffic based on transport layer information such as the TCP or UDP port number. Layer 7 (L7) load balancers operate at the application layer, where they can balance traffic based on application-specific data such as HTTP headers.
Virtual IP

A Virtual IP (VIP) is an IP address that is not tied to a specific device. In the context of load balancing, a VIP is often used as the address that client devices connect to. The load balancer then distributes traffic from the VIP to the actual servers.
Fixed IP, Floating IP

In some systems, each server has a fixed IP address. However, in others, servers may have a "floating" IP address that can be quickly reassigned to another server if the original server fails. This can help maintain high availability.
Octavia failover HAProxy scheme

Octavia is an open-source load balancing solution for OpenStack. It can use HAProxy, a popular open-source load balancer, to provide failover capabilities. In this scheme, if a primary HAProxy instance fails, a secondary instance takes over, ensuring that service is not disrupted.


A Virtual IP (VIP) is an IP address that is not tied to a specific physical network interface or server. Instead, it's an address that can be dynamically assigned or reassigned to one or more servers in a network.

In the context of load balancing, a VIP is typically assigned to the load balancer itself. Client devices connect to this VIP, and the load balancer then distributes the incoming traffic to the actual servers based on its load balancing algorithm.

Here's a simplified flow:

1. The client sends a request to the VIP.
2. The load balancer, which owns the VIP, receives the request.
3. The load balancer selects a server based on its load balancing algorithm (like Round Robin, Least Connections, etc.).
4. The load balancer forwards the client's request to the selected server.
5. The server processes the request and sends a response back to the load balancer.
6. The load balancer forwards the server's response back to the client.

So, at any given time, a VIP can be used to route traffic to many servers. The specific server that a particular client's request is routed to depends on the load balancer's algorithm. This allows the load balancer to distribute the load evenly across all servers, improving the system's overall performance and reliability.


Load balancers are a crucial component in any distributed system. They help distribute network or application traffic across many servers, enhancing both the performance and reliability of applications.
Use cases of Load Balancers
High Availability (HA)

Load balancers play a critical role in maintaining high availability. By distributing traffic across multiple servers, they ensure that if one server goes down, the load can be quickly shifted to another, preventing service disruption. This is particularly important in cloud environments like OpenStack, where load balancers can be used to manage traffic across multiple virtual machines1.
BGP for High Availability

Border Gateway Protocol (BGP) is a protocol used to exchange routing information across autonomous systems on the internet. In the context of load balancing, BGP can be used to achieve high availability by advertising the same IP prefix from multiple locations. If one location fails, traffic can be automatically rerouted to another location that is advertising the same prefix.
Monitoring

Load balancers can also provide valuable monitoring capabilities. They can track the performance of the servers they distribute traffic to, allowing for early detection of issues and preventing potential outages.
Rolling Updates

In a rolling update, a new version of an application is gradually deployed across all servers. Load balancers can help manage this process by gradually shifting traffic from servers running the old version to those running the new one.
L4, L7 Proxies

Load balancers can operate at different layers of the network protocol stack. Layer 4 (L4) load balancers operate at the transport layer, where they balance traffic based on transport layer information such as the TCP or UDP port number. Layer 7 (L7) load balancers operate at the application layer, where they can balance traffic based on application-specific data such as HTTP headers.
Virtual IP

A Virtual IP (VIP) is an IP address that is not tied to a specific device. In the context of load balancing, a VIP is often used as the address that client devices connect to. The load balancer then distributes traffic from the VIP to the actual servers. In OpenStack, a VIP can be associated with a floating IP address, allowing it to be accessible from outside the private network2.
Fixed IP, Floating IP

In some systems, each server has a fixed IP address. However, in others, servers may have a "floating" IP address that can be quickly reassigned to another server if the original server fails. This can help maintain high availability.
Octavia failover HAProxy scheme

Octavia is an open-source load balancing solution for OpenStack. It can use HAProxy, a popular open-source load balancer, to provide failover capabilities. In this scheme, if a primary HAProxy instance fails, a secondary instance takes over, ensuring that service is not disrupted1.



---

DNS Load Balancing is a technique used to distribute network or application traffic across multiple servers using the Domain Name System (DNS). This method improves service availability and response times by spreading the load across multiple servers, reducing the risk of overloading a single server.

Here's how it works:

1. When a client makes a request to a service, it first resolves the service's domain name to an IP address by querying a DNS server.
2. The DNS server is configured with multiple IP addresses for the same domain name, each corresponding to a different server that hosts the service.
3. The DNS server selects one of these IP addresses to return to the client, using a variety of algorithms (like round-robin or least connections).
4. The client then sends its request to the IP address provided by the DNS server.

This method of load balancing is simple and doesn't require any special software or hardware on the client's side. However, it doesn't account for server health or capacity, and it can't distribute load based on more complex criteria like application-specific data or real-time server load.

For High Availability (HA) scenarios, DNS Load Balancing can be combined with health checks and failover mechanisms. If a server becomes unhealthy, it can be automatically removed from the DNS server's pool of IP addresses, preventing clients from being directed to it. If all servers in a particular location fail, traffic can be rerouted to servers in a different location, ensuring the service remains available.

However, DNS Load Balancing has some limitations in HA scenarios. DNS caching by clients or intermediate DNS servers can delay the propagation of changes in server health or availability. Also, DNS doesn't provide session persistence, which can be important for certain types of applications.

For these reasons, DNS Load Balancing is often used in combination with other load balancing techniques, like hardware or software load balancers, to provide more robust load distribution and high availability1.