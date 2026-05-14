# Cloud concept terms

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
