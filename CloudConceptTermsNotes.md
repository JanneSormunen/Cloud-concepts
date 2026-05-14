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

- Network LB = balances TCP, UDP, TLS, routes traffic based on IP data, transport layer (L3)

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

- 

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

- 
