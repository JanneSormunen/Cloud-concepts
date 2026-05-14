# Cloud concept terms

## Cloud Concepts

- Cloud computing = Delivery model for services like, storage, compute power, networking, analytics and more over the internet.
- Scalability = process of adding or removing virtual resources either manually or automatically.
- Elasticity = Automatically scaling your resources to meet changing demands of resources during a period of time. Scale dynamically.
- Agility = Resources on the cloud are ready to use within minutes or seconds. The ability to react quickly.
- Fault tolerance = Data is stored on multiple discs in case one disc breaks. System remains up and running in case of compotent and service failures.
- Disaster recovery = Ability to recover from an event that has taken down an entire region or availability zone.
- High availability = Ability to keep systems running for extended periods of time with little downtime or none at all.

## Consumption based model

- No upfront cost
- No wasted resources
- Pay only for additional resources you need
- Stop paying at any time
  
- Multiple pricing components per service
- Very granular usage measurement (Granular = In a figurative sense, it means highly detailed, precise, or broken down into the smallest possible component parts.)

## Iaas, SaaS, PaaS

- On premises, you manage Infrastructure, Software and Platform.

- Infrastructure as a service (IaaS).
- Cloud provider manages infrastructure (networking, hardware, virtualization).
- You manage platform and software (OS, middleware runtime) (data and applications).

- Platform as a service (PaaS).
- Cloud provider manages infrastructure and platform (networking, hardware, virtualization) (OS, middleware, runtime).
- You manage software and data applications.

- Software as a service (SaaS)
- Cloud provider manages infrastructure, platform and software.
- You manage nothing.

<img width="1198" height="645" alt="kuva" src="https://github.com/user-attachments/assets/5a9c72d0-9434-44b4-a156-9e9080eff93e" />

## Cloud global infrastructure

- Region = interconnected data center clusters usually in one county. (3 or so data centers in one cluster)
- Availability Zone (AZ) = Data center groups, one or more DCs in one group. Connected by high speed low latency network.
- Global availability = Available everywhere
- Subnet = Each subnet belongs to one AZ, helps organize and secure resources. Public = has internet access. Private = No direct access.
- Edge location = small data center closer to the user for fast content delivery.

- Select a region based on data governance, proximity to users, services available in the region and costs.

- Data centers = elastic, scalable, fault tolerant, highly available.

- Hypervisor = software that creates and runs VMs
- Hyperscaler = company that provides cloud services at a global scale (AWS, Azure)

## Cloud governance management and monitoring.

- Cloud landing zone = How to separate and operate your cloud
- Multi account, governance, management, observability, security.
- Must have one root account, directories and subscriptions

- Policies (guardrails). Management groups set policies for subscriptions.
- Makes it easier to do things right.

- Tags = metadata for resources
- logically organizes resources
- name-value pairs
- useful for billing info

- CLI = Command line interface
- Tools help simplify tasks and enhances tasks without the use of the portal
- SDK/Library = Use to access APIs
- Infra as code = defines resources in plain text

- Dashboard, alerts apps, 3 levels
  
- Control plane - logs
- Operations that are performed via the cloud platform
  
- Data plane - metrics/logs
- Operational logs for your resources
  
- App - metric/logs

## Load balancing

- Elastic load balancing = distributes incoming apps or net traffic to multiple AZ:s or a single AZ
- Scales LB as traffic to your apps

- Application LB = balances HTTP, routes traffic, application layer (L7)

- Network LB = balances TCP, UDP, TLS, routes traffic based on IP data, transport layer (L4)

- Classic LB = Does a bit of both

## IaM and security

- IaM = Identity and access management
- Permissions (CRUD = Create read update delete destroy execute)
- User directory - user record
- Authentications - login
- Authorization - permissions
- RBAC = Role based access control (how perms are defined and allocated)

- Access is defined by who can access, which resources and how.

- Identities can be humans, bots, OS, IoT device, apps, services

- Identity user group/role
- Always deny by default and only give access to a resource a member or a group needs (Least privileges principle)
- Scope = Target area for permissions
- Permissions are documented in json.

- Login authentication
- complex passwords - mfa - access keys - tokens

- Zero trust = assume nobody can be trusted (least permissions)

- Shared responsibility
- Customer responsibility = OS, apps, security group, firewalls network and account management
- CSP = Physical security of data centers, hardware and software infra, network infra, virtualization infra.

## Resources and resource groups

- Resources = objects used to manage service, represents a service lifecyclem, usually a .json file.
  
- Resource groups = grouping of resources, holds logically related resources.
- Organize by type, lifecycle (app, environment), department, and billing, location or both.
- Each resource can only be in one resource group.
- Resource groups must have their location assigned
- Resources in the resource groups can reside in different locations
- Resources can be moved between groups
- Organize based on your organization needs

- Resource manager = management layer for all resources and resource groups.
- Controls access and resources.

## Compute services

- Docker = Able to create virtualized OS, repeatable, self contained, software runs in different environments
- Kubernetes (container orchestration)
- Virtual machine
- Lambda/Serverless code = code only runs when triggered, pay only when triggered, timeout in 15 minutes.
- Virtual machine scale set = simplifies creating and managing a group of load balanced VMs

## Intermediate cloud concepts

- Autoscaling = Adding or removing virtual resources either manually or automatically.
- Elastic load balancing = distributes incoming apps or net traffic to multiple AZ:s or a single AZ

## Storage

- Each VM has detachable and swappable storage discs.
- Can attach new discs.
- Snapshots (backup)
- Block and object storage
- Block storage = change one block (piece of file) that contains the character that is being changed (partial updates)
- Object storage = entire file must be updated.

## Networking

- IPv4 = 32 bit address (192.0.2.0)
- IPv6 = 128 bit address
- Subnets are discrete sections used for effective address allocation and network filtering.
- CIDR block (Classless inner domain routing) = Way to define a range of IP addresses using a compact notation.
- 5 out of 256 addresses get reserved in a virtual network (10.0.0.0 network address - 10.0.0.1 internal communication - 10.0.0.2 DNS resolution - 10.0.0.3 future use - 10.0.0.255 network broadcast address)
- First feasible size on cloud is /29 or /28
- Largst size is /16 (IPv6 also supported)
- Public network = internet, public IPv4
- LAN = private IPv4, AWS VPC, Azure VNet

- VPC = Virtual private cloud (private isolated network inside a public cloud) only you control access
- Belongs to only one region and multiple AZs
- Subnets = range of IP addresses that divide a VPC, belongs to one AZ, classified public or private.

- Internet gateway = accessible from the internet as long as your NIC is associated with a public IPv4
- NIC = Network interface card
- Elastic network interface (VNIC)
- Detach and attach to another instance to redirect network traffic (attributes follow)

- Public = Internet gateway, local
- Private NAT gateway, local
- Route table = set of rules to configure to direct network traffic to subnet

- VPC peering = allows two VPCs to communicate with eachother as if they were the same network
- Can only have one peering resource between the same two VPCs
- Can connect VPCs in your own account between other accounts or regions
- Open internet (cheapest, simple, HTTP, Firewall, site to VPN (more encryption), direct from OnPrem to cloud outside internet (fastest, most secure and most expensive)

- VPC security = TLS, Network segmentation, L4 Firewall, NAT Gateway
- Network segmentation = Split network into multiple smaller segments to improve security, performance and management

- L4 Firewall, works through firewall rules - packet filtering
- Action: allow/deny packets to pass
- Protocol: TCP, UDP, ICMP
- Source: IP address range, TCP ports
- Destination: IP address range, TCP ports

- CDN = Global content delivery
- NSG = Security rules
- DNS = Domain name service

## Databases

- Structured data - table like (excel)
- Semi-structured data - data with slightly differing properties (json file)
- SQL = Relational database (has structured data)
- No-SQL = Non-relational database (has semi-structured data)
- SQL queries - tables, columns rows, records
- NoSQL - tables, .json objects
- NoSQL is easily compatible with HTTP
- ACID principle (Atomicity = A transaction happens fully or it doesn't. Consistency = data must follow rules/constraints before and after a transaction. Isolation = concurrent transactions do not interfere with eachother. Durability = Once committed, data survives crashes or power loss)
- Fast when DB is fully loaded with RAM
- Why DBs are so resource consuming
- Dependent on transaction log
- DB file discs need to be fast and never run out of space

- DBs are single node systems, only way to boost performance is cache, optimization, replicas
- redundancy features are often causing extra license costs
- High availability with multt-AZ deployment
- Can synchronize DB content to another DB
- Semi-passive

- Read replica, asynchronous replication, can be promoted to primary if needed, use for read heavy database workloads
- Split the load of the single node system by reading from the replica and write from the original

- DB characteristics = Engine, Size, Memory class
- Pay for storage and backups and transfers of data
