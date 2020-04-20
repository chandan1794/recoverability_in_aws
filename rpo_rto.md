# Estimate availability of this configuration

### 1. Minimum RTO for a single AZ outage
	It will be in minutes. Because a parallel secondary is maintained synchronously. And if the primary fails, secondary will take over.

#### 2. Minimum RTO for a single region outage
	This value depends on how fast we react to the disaster and also the size of the read-replica. In the case of disaster, we can promote a read-replica. When we do so, it reboots the instance and it can take upto several minutes.
	

#### 3. Minimum RPO for a single AZ outage
	It will be zero, because if one data center for some reason goes down, the location of other datacenter is different and system can switch to it directly. Also since we maintain a parallel synchronous copy of the database, no data loss occurs.

### 4. Minimum RPO for a single region outage
	 If an Availability Zone failure occurs, the availability impact is limited to the time automatic failover takes to complete: typically one to two minutes.
	 DB Instance failover is fully automatic and requires no administrative intervention. Amazon RDS monitors the health of your primary and standbys, and initiates a failover automatically in response to a variety of failure conditions.


## Conditions that triggers Failover
- Loss of availability in primary Availability Zone
- Loss of network connectivity to primary
- Compute unit failure on primary
- Storage failure on primary
